# econ3916-lab03-visualization
ECON3916 LAB 03 - EDA &amp; Visualization
**Objective:** Demonstrate how visualization choices (axis truncation, window
selection, scale transformation, and nominal-versus-real measurement) can make
the same economic data support contradictory conclusions, and apply a
systematic EDA workflow to detect these distortions before they reach an
analysis.

## Methodology

- **Anscombe's Quartet:** Reproduced four datasets with nearly identical summary
  statistics (mean x = 9.0, mean y ≈ 7.50, r ≈ 0.816, identical OLS fit) and
  plotted them side by side to show that summary statistics alone cannot
  identify outliers, nonlinearity, or high-leverage points.
- **Lie Factor analysis:** Quantified distortion in a truncated-axis revenue
  chart using Tufte's Lie Factor (size of effect shown ÷ size of effect in data),
  then redesigned the chart with a zero baseline.
- **Wage series framing:** Retrieved FRED average hourly earnings for production
  and nonsupervisory workers (AHETPI), deflated them to 2020 dollars with
  CPI-U (CPIAUCSL), and plotted the series four ways: full range with a zero
  baseline, truncated y-axis, a cherry-picked recent window, and a log scale.
- **Exploratory data analysis:** Applied a four-step checklist (structure,
  distributions, relationships, anomalies) to World Bank WDI GDP including a log10 transformation of
  heavily right-skewed GDP levels and a missingness heatmap.
- **Interactive tool:** Built an ipywidgets dashboard that lets users switch
  between nominal and real wages, adjust the y-axis floor, select the time
  window, and toggle linear or log scale, with a live Lie Factor readout.

## Key Findings

- **Summary statistics can conceal structure.** In Anscombe's Dataset IV, a
  single high-leverage observation produces the entire regression slope;
  without it, x has no variance and no relationship can be estimated.
- **Axis truncation produced a Lie Factor of 49.0.** A 4.1% revenue increase
  was drawn as a 200% increase in visual height.
- **Framing determines the wage narrative.** Real hourly earnings fell from a
  1973 peak of about $24.12 to a 1995 trough of about $19.71 and have since
  recovered, a gain of roughly 20% over six decades. Nominal earnings rose more
  than twelvefold over the same period, mostly reflecting inflation. Truncated
  axes, selective windows, and nominal dollars can each turn the same data into
  a story of collapse, boom, or steady growth.
- **GDP requires a log transformation for meaningful analysis.** Raw GDP levels
  span several orders of magnitude, and the log10 transform produces a roughly
  symmetric distribution suitable for cross-country comparison.
- **Missing data is not random.** Gaps cluster at the start of the sample (newly
  independent states and limited statistical capacity) and at the end
  (publication lags). The missingness is largely MAR, with a likely MNAR
  component in early years, which rules out naive listwise deletion for
  comparisons across decades.
- **AI-generated code required verification.** The initial AI-generated
  dashboard computed the Lie Factor as a ratio of ratios rather than a ratio of
  changes, and it pulled a different wage series. Testing it against the
  hand-calculated value of 49.0 exposed the error.

# econ3916-lab03-visualization
ECON3916 LAB 03 - EDA &amp; Visualization
Objective:
To critically evaluate and demonstrate the ethical implications of data visualization choices, ensuring that graphical representations accurately reflect underlying data without distortion.

Methodology:
Anscombe's Quartet Recreation: Reproduced four distinct datasets that possess identical summary statistics (mean, variance, correlation) but exhibit profoundly different graphical forms, underscoring the necessity of visual data inspection.
Lie Factor Analysis and Honest Redesign: Calculated a Lie Factor of 49.0 for a revenue chart with a truncated y-axis. Subsequently, the chart was honestly redesigned to provide an accurate visual representation of the data's true effect.
Multi-Perspective Data Storytelling: Generated four distinct visualizations of real average hourly earnings (FRED AHETPI, deflated to 2020 dollars), each crafted to convey a different narrative from the same underlying economic data.
Systematic Exploratory Data Analysis (EDA): Applied a four-step EDA checklist (structure, distributions, relationships, anomalies) to World Bank GDP data, analyzing 262 countries over 64 years to uncover patterns, anomalies, and data characteristics.
Interactive Honesty Toggler Development: Engineered an interactive chart toggler featuring live Lie Factor calculation, allowing users to dynamically manipulate visualization parameters (e.g., y-axis floor, scale, time window) and observe the impact on data representation and perceived honesty.
Key Findings:
This project demonstrates that summary statistics alone are insufficient for robust data analysis; visual inspection is paramount to prevent misinterpretation. Truncated axes and selective data presentation can drastically inflate perceived effects, leading to misleading conclusions. The interactive tool reinforces that even subtle changes in visualization parameters can significantly alter a chart's integrity, necessitating careful and ethically conscious design in economic and data science communication. Real average hourly earnings reveal varied narratives depending on the chosen visualization technique, highlighting the rhetorical power of charting. Furthermore, a systematic EDA workflow is crucial for understanding data structure, distributions, relationships, and anomalies, especially with complex datasets like World Bank GDP figures, where transformations (e.g., log scale) are often essential for meaningful analysis.

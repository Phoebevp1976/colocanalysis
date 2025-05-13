Colocalization Analysis

This project analyzes colocalization data for three groups: SPINGFP, CHMP2B, and VAPB33, under two conditions: Sedentary and Sprint. The data is processed, analyzed, and visualized to determine significant differences in colocalization across groups and conditions.


Project Description

This project utilizes R to analyze colocalization data from an Excel file. The main objective is to perform statistical tests (Wilcoxon tests) to compare colocalization levels across three groups (SPINGFP, CHMP2B, and VAPB33) and two conditions (Sedentary and Sprint). The analysis also includes visualizations, such as boxplots with significance annotations.

Installation
To run this analysis, you'll need to have R installed along with the following packages:

ggplot2

dplyr

readxl

tidyr

You can install the necessary packages by running the following code in R:

r

Copy

Edit

install.packages(c("ggplot2", "dplyr", "readxl", "tidyr"))

Usage

Clone this repository to your local machine.

Update the file path in the code to the location of your colocresults.xlsx file.

r
Copy

Edit

file_path <- "path/to/your/colocresults.xlsx"


Run the R script to perform the data analysis and visualize the results.

The script will:

Load and tidy the data.

Perform Wilcoxon tests for between-group and within-group comparisons.

Output a summary table of the test results.

Generate boxplots comparing colocalization levels between groups with significance bars.


Analysis Overview
Data Processing
Tidy Data: The data is transformed from a wide format to a long format using pivot_longer. This helps in easier comparison across groups and conditions.

Group and Condition Classification: The groups are labeled as SPINGFP, CHMP2B, and VAPB33, while conditions are classified as Sedentary and Sprint.

Statistical Analysis
Wilcoxon Test: The Wilcoxon rank-sum test is used for non-parametric comparisons to assess significant differences between groups for each condition.

Significance Labels: Results are labeled as *, **, or *** depending on the p-value thresholds of 0.05, 0.01, and 0.001, respectively.

Visualization
Boxplot: Colocalization levels are visualized using boxplots with different colors for each condition (Sedentary = white, Sprint = black).

Significance Bars: Statistical significance between groups is represented using lines and asterisks above the boxplots.

Results
The script will output the Wilcoxon test results as a summary table in the R console, including the comparison, p-value, and significance level.


Example of the output:

python-repl

Copy

Edit

=== Wilcoxon Test Summary ===

Comparison                       P_Value   Significance

SPINGFP Sprint vs VAPB33 Sprint   0.0012     ***

SPINGFP Sedentary vs VAPB33 Sedentary  0.0324 *

CHMP2B Sprint vs VAPB33 Sprint    0.0004    ***
...


Example Boxplots


Colocalization by Condition (Sedentary vs Sprint)

The first boxplot shows colocalization for each group, with the comparison between the Sedentary and Sprint conditions. Significance bars are included where significant differences were observed.

Colocalization Across Groups

The second boxplot compares colocalization levels between groups (SPINGFP, CHMP2B, and VAPB33) for both Sedentary and Sprint conditions, with significance bars showing statistically significant differences.

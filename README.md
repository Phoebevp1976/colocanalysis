# POSH-GFP Colocalisation Analysis

This project analyzes the colocalisation of POSH with GFP across three groups (SPINGFP, CHMP2B, and VAPB33) under two conditions (Sedentary and Sprint). The data is processed and analyzed using statistical tests to identify significant differences in colocalisation levels across groups and conditions.

## Project Description

This project utilizes R to analyze data from an Excel file containing colocalisation of POSH with GFP in three groups (SPINGFP, CHMP2B, and VAPB33) under two conditions (Sedentary and Sprint). The main objective is to compare the colocalisation levels across groups using Wilcoxon tests and visualize the results with boxplots that include significance annotations.

## Installation

To run this analysis, you'll need to have R installed along with the following packages:

- `ggplot2`
- `dplyr`
- `readxl`
- `tidyr`

You can install the necessary packages by running the following code in R:

```r
install.packages(c("ggplot2", "dplyr", "readxl", "tidyr"))
Usage
Clone this repository to your local machine or download the R script.

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

Generate boxplots comparing POSH-GFP colocalisation levels between groups with significance bars.

Analysis Overview
Data Processing
Tidy Data: The data is transformed from a wide format to a long format using pivot_longer. This makes it easier to analyze across groups and conditions.

Group and Condition Classification: The groups are labeled as SPINGFP, CHMP2B, and VAPB33, while conditions are classified as Sedentary and Sprint.

Statistical Analysis
Wilcoxon Test: Non-parametric comparisons are made using the Wilcoxon rank-sum test to assess significant differences between groups for each condition.

Significance Labels: Results are labeled as *, **, or *** depending on the p-value thresholds of 0.05, 0.01, and 0.001, respectively.

Visualization
Boxplot: POSH-GFP colocalisation levels are visualized using boxplots with different colors for each condition (Sedentary = white, Sprint = black).

Significance Bars: Statistical significance between groups is represented using lines and asterisks above the boxplots.

Results
The script will output the Wilcoxon test results as a summary table in the R console, including the comparison, p-value, and significance level.

Example of the output:
python-repl
Copy
Edit
=== Wilcoxon Test Summary ===
Comparison                    P_Value  Significance
SPINGFP Sprint vs VAPB33 Sprint  0.0023    **
SPINGFP Sedentary vs VAPB33 Sedentary  0.0431    *
CHMP2B Sprint vs VAPB33 Sprint  0.0008    ***
...
Example Boxplots
POSH-GFP Colocalisation by Condition (Sedentary vs Sprint)
The first boxplot shows the POSH-GFP colocalisation for each group, with the comparison between the Sedentary and Sprint conditions. Significance bars are included for comparisons where significant differences were found.

POSH-GFP Colocalisation Across Groups
The second boxplot compares POSH-GFP colocalisation levels between groups (SPINGFP, CHMP2B, and VAPB33) for both Sedentary and Sprint conditions, with significance bars indicating where differences are statistically significant.


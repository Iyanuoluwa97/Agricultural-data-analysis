# Python Exam Walkthrough: Agricultural Data Analysis

This folder contains a Jupyter Notebook documenting step-by-step solutions to a comprehensive Python coding exam focusing on agricultural data analysis. The notebook details calculations and visualizations using a dataset representing farmer field records.

---

## Overview

The walk-through implements advanced data manipulation and statistical workflows on the `MD_agric_exam-4313.csv` dataset:
* **Exploratory Data Analysis**: Inspecting counts, unique entries, filtering values, and rounding data metrics.
* **Custom Calculations**: Functions computing field temperature ranges ($T_{\text{max}} - T_{\text{min}}$) and filtering operations on combinations of climate and soil variables (e.g., pH, rainfall).
* **Statistical Testing**: Conducting independent two-sample t-tests to evaluate crop yield differentials.
* **Recursive Computations**: Building recursive algorithms to calculate string metadata sums.
* **Data Visualization**: Categorizing continuous elevation metrics and displaying distributions via Seaborn violin plots.

---

## Folder Contents

| File Name | Format | Description |
| :--- | :--- | :--- |
| [`Python Exam Walkthrough.ipynb`](file:///c:/Users/HP/OneDrive/Desktop/Projectssssss/Python%20Exam%20Walkthrough/Python%20Exam%20Walkthrough.ipynb) | Jupyter Notebook | Solution workbook implementing the Pandas, NumPy, SciPy, and Seaborn exam answers. |

---

## Detailed Breakdown of Exam Solutions

The walkthrough contains solutions to 12 distinct questions:

1. **Unique Crop Count**: Counting distinct categories in `Crop_type` using `.nunique()`.
2. **Filtered Maximums**: Identifying the maximum value of `Annual_yield` for the crop `"wheat"`.
3. **Aggregated Conditions**: Grouping pollution rates and computing total `Rainfall` for crops matching specific criteria.
4. **Range Function**: Building `calculate_temperature_range(ID)` to extract custom spans for specific fields.
5. **Averaging Minimums**: Finding the crop type with the lowest average minimum temperature.
6. **Conditional Summation**: Finding total `Plot_size` for soil profiles where $\text{pH} < 5.5$.
7. **Multi-Condition Filters**: Counting fields satisfying $(T_{\text{min}} < -5^\circ\text{C}) \land (T_{\text{max}} > 30^\circ\text{C})$.
8. **Median & Standard Deviation**: Using NumPy to calculate standard deviation of rainfall for plots larger than the median plot size.
9. **String Concatenation**: Merging string representations of mode temperatures and least-common crop types.
10. **Violin Plot Visualization**: Mapping annual yields across three categorized elevation bands (`Low` $<300\text{m}$, `Medium` $300\text{m}-600\text{m}$, `High` $>600\text{m}$) using Seaborn.
11. **Recursion**: Building recursive functions to sum the string lengths of unique crop types.
12. **Hypothesis Testing**: Performing an independent two-sample t-test comparing the yield distributions of `coffee` and `banana` crops:
    ```python
    t_stat, p_val = stats.ttest_ind(coffee_yield, banana_yield)
    ```

---

## Setup & Execution

1. Ensure the dataset `MD_agric_exam-4313.csv` is placed in the local documents path referenced in the script.
2. Install the necessary Python packages:
   ```bash
   pip install pandas numpy scipy seaborn matplotlib jupyter
   ```
3. Run the notebook to review the step-by-step logic:
   ```bash
   jupyter notebook "Python Exam Walkthrough.ipynb"
   ```

## Dependencies
* **Python 3.8+**
* **Pandas** & **NumPy**
* **SciPy** (for scientific statistical calculations)
* **Seaborn** & **Matplotlib** (for plotting)

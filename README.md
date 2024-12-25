Exploratory Data Analysis (EDA) on Student Scores Dataset

Overview
This document describes the steps and insights derived from performing Exploratory Data Analysis (EDA) on the `Student_scores.csv` dataset. 
The goal of this analysis was to uncover patterns, relationships, and trends within the data to better understand student performance.

Steps and Observations

 1. Data Loading and Initial Inspection
- The dataset was loaded using 'pandas'.
- Initial steps included:
- Displaying the first and last few rows using 'data.head()' and 'data.tail()'.
- Checking data types, null values, and basic statistics using 'data.info()' and 'data.describe()'.
- Listing column names using 'data.columns.to_list()'.

 2. Data Cleaning
- Null Values:
  - Null values were identified and removed using 'data.dropna(inplace=True)'.
- Duplicates:
  - Checked for duplicates with 'data.duplicated().sum()'.
  - No significant duplicates were found.
- Irrelevant Columns:
  - Dropped the 'Unnamed: 0' column as it was irrelevant.

3. Gender Distribution
- A bar plot was created using 'sns.countplot' to visualize the distribution of gender against weekly study hours.
- Observation: The number of females in the dataset is higher than the number of males.
- ![image](https://github.com/user-attachments/assets/c1c77ae7-2328-4841-b55a-836eec4ffd44)



 4. Histograms
- Histograms were plotted for numerical columns to observe their distributions.
- ![image](https://github.com/user-attachments/assets/c99b905f-28bd-4691-8d73-818b5b37fc3d)
- ![image](https://github.com/user-attachments/assets/b7c20f0e-41be-42ab-b6db-11dee0e5e4f6)
- ![image](https://github.com/user-attachments/assets/655e9fed-faa3-466f-8cdc-727e77e39f28)
- ![image](https://github.com/user-attachments/assets/37d6ea12-9ad0-4c47-9db0-b550f1142b9f)

- Key Observations:
  1. Many students have one sibling.
  2. Math scores are concentrated between 60-65.
  3. Reading scores are prominent in the ranges 65-70 and 75-80.
  4. Writing scores peak around 70.

5. PairPlot
- A pair plot was generated to visualize pairwise relationships among numerical variables.
- ![image](https://github.com/user-attachments/assets/80746547-2796-4ab8-a04d-c82e2d89e972)
- Observation:Reading, Writing, and Math scores are linearly related.


 6. Scatter Plot
- A scatter plot was created for the first two numerical columns.
- ![image](https://github.com/user-attachments/assets/c233ca84-94be-442f-98e5-0b366fc235cb)
- Observation:Clear trends were observed, showing relationships between variables.

7. Parental Education Impact
- Grouped data by `ParentEduc` to calculate the mean of `MathScore`, `ReadingScore`, and `WritingScore`.
- A heatmap was plotted to visualize the impact.
- ![image](https://github.com/user-attachments/assets/3a382a5b-7edc-41cc-b4b6-b6a68c16b1f1)
- Observation: Parental education significantly influences student scores.

8. Parental Marital Status Impact
- Grouped data by `ParentMaritalStatus` and calculated the mean of scores.
- A heatmap was plotted.
- ![image](https://github.com/user-attachments/assets/85731401-b496-4bde-9d92-e14d13a39090)
- Observation: Parental marital status has no significant impact on student scores.

9. Box Plots
- Box plots were created for `MathScore`, `WritingScore`, and `ReadingScore` against weekly study hours.
- ![image](https://github.com/user-attachments/assets/d5925da5-584c-4fbb-be3c-ad7059e7883d)
- ![image](https://github.com/user-attachments/assets/038e89d7-bcd0-499d-9032-6954910f67ca)
- ![image](https://github.com/user-attachments/assets/488ca674-d772-4451-a966-8aa63d660ee6)



- **Observation:** Weekly study hours significantly affect score distributions.

10. Distribution of Ethnic Groups
- A pie chart was plotted to show the percentage distribution of ethnic groups.
- ![image](https://github.com/user-attachments/assets/276d9aba-0c96-448a-b5b4-fe8217cfa010)

- Observation: Group C has the highest number of students, while Group A has the lowest.


11. Correlation Heatmap
- A correlation matrix was computed for numerical columns and visualized using a heatmap.
- ![image](https://github.com/user-attachments/assets/661fe1c7-cfc7-4254-ad8f-c9d6dbb6f5cc)
- Observation: Reading, Writing, and Math scores are strongly correlated and could be used for future predictions.

12. Additional Scatter Plot
- A scatter plot for `ReadingScore` vs `WritingScore` was created.
- ![image](https://github.com/user-attachments/assets/aff32304-60bb-40bf-91eb-765f84507c1a)
- Observation: A strong linear relationship exists between Reading and Writing scores.


Conclusions
1. Gender Distribution: Female students outnumber male students in this dataset.
2. Score Relationships: Reading, Writing, and Math scores are linearly correlated.
3. Parental Influence:Parental education positively affects student performance, whereas marital status does not.
4. Ethnic Group Distribution: Group C has the largest representation, and Group A the least.
5. Study Hours Impact: Weekly study hours influence scores significantly.



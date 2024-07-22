PyCity Schools Analysis
    Overall, students perform better in Reading than in Math across all schools in the district. This trend is consistent when analyzing both average scores and passing rates. Charter schools consistently outperform District schools in both average scores and passing rates. Despite having lower total budgets, Charter schools achieve higher academic outcomes compared to District schools. Larger schools (2000-5000 students) tend to have higher overall passing rates compared to smaller schools. This could indicate potential benefits of scale in educational resources and opportunities. While there appears to be a trend that higher spending per student correlates with lower overall passing rates, this relationship is nuanced. District schools, which generally have higher per student budgets, also face larger student populations and diverse resource allocation needs. 


Two correct conclusions or comparisons from the calculations 
  1) School Size Analysis: Schools with larger student populations (2000-5000) demonstrate higher overall passing rates compared to smaller schools. This suggests that larger schools may benefit from economies of scale in educational resources and opportunities for diverse student needs.
  2) School Type Comparison: Charter schools consistently outshine District schools across all metrics including Average Math Score, Average Reading Score, % Passing Math, % Passing Reading, and % Overall Passing. This performance disparity highlights potential differences in educational philosophy, governance, and resource allocation between Charter and District school types.
---



# pandas-challenge
![education](https://github.com/user-attachments/assets/b40c46bf-2df6-4561-b20f-a63dd711f1a7)

In this assignment, you’ll create and manipulate Pandas DataFrames to analyze school and standardized test data.

Background

You are the new Chief Data Scientist for your city's school district. In this capacity, you'll be helping the school board and mayor make strategic decisions regarding future school budgets and priorities.

As a first task, you've been asked to analyze the district-wide standardized test results. You'll be given access to every student's math and reading scores, as well as various information on the schools they attend. Your task is to aggregate the data to showcase obvious trends in school performance.

Instructions

Using Pandas and Jupyter Notebook, create a report that includes the following data. Your report must include a written description of at least two observable trends based on the data.

District Summary

Perform the necessary calculations and then create a high-level snapshot of the district's key metrics in a DataFrame.

Include the following:

Total number of unique schools

Total students

Total budget

Average math score

Average reading score

% passing math (the percentage of students who passed math)

% passing reading (the percentage of students who passed reading)

% overall passing (the percentage of students who passed math AND reading)

School Summary

Perform the necessary calculations and then create a DataFrame that summarizes key metrics about each school.

Include the following:

School name

School type

Total students

Total school budget

Per student budget

Average math score

Average reading score

% passing math (the percentage of students who passed math)

% passing reading (the percentage of students who passed reading)

% overall passing (the percentage of students who passed math AND reading)


Highest-Performing Schools (by % Overall Passing)

Sort the schools by % Overall Passing in descending order and display the top 5 rows.

Save the results in a DataFrame called "top_schools".

Lowest-Performing Schools (by % Overall Passing)

Sort the schools by % Overall Passing in ascending order and display the top 5 rows.

Save the results in a DataFrame called "bottom_schools".

Math Scores by Grade

Perform the necessary calculations to create a DataFrame that lists the average math score for students of each grade level (9th, 10th, 11th, 12th) at each school.

Reading Scores by Grade

Create a DataFrame that lists the average reading score for students of each grade level (9th, 10th, 11th, 12th) at each school.

Scores by School Spending

Create a table that breaks down school performance based on average spending ranges (per student).

Use the code provided below to create four bins with reasonable cutoff values to group school spending.

spending_bins = [0, 585, 630, 645, 680]
labels = ["<$585", "$585-630", "$630-645", "$645-680"]
Use pd.cut to categorize spending based on the bins.

Use the following code to then calculate mean scores per spending range.

spending_math_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Math Score"].mean()
spending_reading_scores = school_spending_df.groupby(["Spending Ranges (Per Student)"])["Average Reading Score"].mean()
spending_passing_math = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Math"].mean()
spending_passing_reading = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Passing Reading"].mean()
overall_passing_spending = school_spending_df.groupby(["Spending Ranges (Per Student)"])["% Overall Passing"].mean()
Use the scores above to create a DataFrame called spending_summary.

Include the following metrics in the table:

Average math score

Average reading score

% passing math (the percentage of students who passed math)

% passing reading (the percentage of students who passed reading)

% overall passing (the percentage of students who passed math AND reading)

Scores by School Size

Use the following code to bin the per_school_summary.

size_bins = [0, 1000, 2000, 5000]
labels = ["Small (<1000)", "Medium (1000-2000)", "Large (2000-5000)"]
Use pd.cut on the "Total Students" column of the per_school_summary DataFrame.

Create a DataFrame called size_summary that breaks down school performance based on school size (small, medium, or large).

Scores by School Type

Use the per_school_summary DataFrame from the previous step to create a new DataFrame called type_summary.

This new DataFrame should show school performance based on the "School Type".

********************************************************************************************************************    
## References

- **ChatGPT Model**: OpenAI. (2023). ChatGPT (version 3.5). Retrieved July 19, 2024, from https://openai.com


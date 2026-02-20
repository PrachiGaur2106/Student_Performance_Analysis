Student Performance Analysis using Pandas
Project Overview

This project demonstrates how to analyze a student dataset using Python’s Pandas library.
The dataset contains students’ names, hours studied, and scores, and the analysis includes data exploration, cleaning, aggregation, and filtering.

Objective

Explore datasets using Pandas functions like head(), describe(), and isnull().

Create new columns for categorization (Pass/Fail).

Perform aggregation and sorting to find trends.

Filter data to identify top-performing or hardworking students.

Dataset
Student	Hours_Studied	Scores
A	2	21
B	3	25
C	4	30
D	5	34
E	6	40
F	7	45
G	8	50
H	9	55
I	10	60
J	11	65
Key Steps

Load dataset using Pandas DataFrame.

Basic exploration: head(), describe(), isnull().

Data transformation: Add a Pass/Fail column based on scores.

Aggregation & analysis:

Average, max, min scores

Count of Pass/Fail

Filtering & sorting:

Top students

Students studying more than a certain number of hours

Code Snippets
import pandas as pd

# Create DataFrame
df = pd.DataFrame({
    'Student': ['A','B','C','D','E','F','G','H','I','J'],
    'Hours_Studied': [2,3,4,5,6,7,8,9,10,11],
    'Scores': [21,25,30,34,40,45,50,55,60,65]
})

# Add Pass/Fail column
df['Result'] = df['Scores'].apply(lambda x: 'Pass' if x >= 40 else 'Fail')

# Aggregation example
avg_score = df['Scores'].mean()
result_counts = df['Result'].value_counts()

# Sorting & filtering
top_students = df.sort_values(by='Scores', ascending=False).head(3)
hardworking_students = df[df['Hours_Studied'] > 6]
Skills Learned

Python Pandas for data analysis

Data exploration, aggregation, and filtering

Categorization and basic data transformation

Sorting, value counts, and indexing

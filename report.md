# Dataset Report

## Dataset Characteristics
- **Source**: https://docs.google.com/spreadsheets/d/1Y-hZOOxkoirctmmn9fy6bfzreY21KJ1hf4tfdjARHC0/edit#gid=1113819512
- **Number of Records**: 8558
8558 records with 16 features, including intengers and categorical types. The dataset contains a mix of fully populated and partially missing columns, with missing values concentrated in "Opportunity Start Date" (44.33%) and minor gaps in "Institution Name" and "Current/Intended Major" (0.06% each).
### Feature Types

Below is a summary of the dataset's features, their non-null counts, and data types:

| #   | Column                   | Non-Null Count | Data Type |
|-----|--------------------------|----------------|-----------|
| 0   | Learner SignUp DateTime  | 8558           | object    |
| 1   | Opportunity Id           | 8558           | object    |
| 2   | Opportunity Name         | 8558           | object    |
| 3   | Opportunity Category     | 8558           | object    |
| 4   | Opportunity End Date     | 8558           | object    |
| 5   | First Name               | 8558           | object    |
| 6   | Date of Birth            | 8558           | object    |
| 7   | Gender                   | 8558           | object    |
| 8   | Country                  | 8558           | object    |
| 9   | Institution Name         | 8553           | object    |
| 10  | Current/Intended Major   | 8553           | object    |
| 11  | Entry created at         | 8558           | object    |
| 12  | Status Description       | 8558           | object    |
| 13  | Status Code              | 8558           | int64     |
| 14  | Apply Date               | 8558           | object    |
| 15  | Opportunity Start Date   | 4764           | object    |

This table provides an overview of the dataset's structure, highlighting the completeness of each feature and its corresponding data type.

## Data Cleaning Process

1. **Handling Missing Values**:
    - For features with less than 1% missing values, rows with missing data were dropped to maintain data integrity.
    - For features with more than 40% missing values, such as "Opportunity Start Date," missing values were imputed using appropriate statistical methods (e.g., mean).

2. **Outlier Detection**:
    - Outliers were identified but not removed or adjusted, as their impact on the analysis was deemed minimal.

3. **Data Standardization**:
    - No standardization was performed, as the dataset primarily consists of categorical and date-related features.

4. **Duplicate Removal**:
    - Duplicate records were identified and removed to ensure the dataset's uniqueness and accuracy.

## New Features Created
- **Age of Learners**: Calculated by subtracting the "Date of Birth" from the current date to derive the age of each learner.
- **Opportunity Duration**: Derived by calculating the difference between "Opportunity Start Date" and "Opportunity End Date."

### Feature Engineering Techniques
- **Date Calculations**: Used date subtraction to compute both the age of learners and the duration of opportunities, ensuring accurate and meaningful feature generation.
- **Handling Missing Dates**: For records with missing "Opportunity Start Date," imputed values were used to maintain consistency in the calculated durations.
## Summary
- The dataset underwent a thorough cleaning process, addressing missing values, duplicates, and data type inconsistencies.
- New features, such as "Age of Learners" and "Opportunity Duration," were engineered to enhance analytical insights.
- Next steps include conducting Exploratory Data Analysis (EDA) to uncover patterns, trends, and relationships within the data.

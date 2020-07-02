# School District

## Challenge Overview
School district data (math and reading standardized test scores) was analyzed for trends. Test scores for 9th graders at Thomas High school (THS) were removed (set to "NaN", which is equivalent to a zero value) while keeping these students in all student counts. The impact on trends was assessed with these questions:

1. How is the district summary affected?
2. How is the school summary affected?
3. How does removing the 9th graders' math and reading scores affect THS' performance, relative to the other schools?
4. How does removing the 9th grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type 

## Resources
- Data sources: schools_complete.csv and students_complete.csv
- Software: pandas 1.0.3, Jupyter Notebook 6.0.3, conda 4.8.2, and Python 3.8.2

## Summary
- See PyCitySchools.ipynb <[PyCitySchools.ipynb](PyCitySchools.ipynb)>.
and PyCitySchools_Challenge.ipynb <[PyCitySchools_Challenge.ipynb](PyCitySchools_Challenge.ipynb)>.
for the data analysis.

- For the district summary:
  - Average Math Score (AMS) decreased by 0.1% whereas Average Reading Score (ARS) stayed the same.
  - % Passing Math (%PM), % Passing Reading (%PR), and % Overall Passing (%OP) all decreased by 1%. This was expected since 9th graders at THS made up 1% of students in the district (461 of 39,170).
 
- For the school summary:
  - Total Students, Total School Budget, and Per Student Budget were unchanged.
  - AMS and ARS changed by insignificant amounts (<0.1%). 
  - %PM, %PR, and %OP decreased by 26%, 28%, and 26%, respectively. This was expected since 9th graders at THS made up 28% of total students at THS. 

- When comparing %OP, THS' ranking fell from being the 2nd-highest-performing school to 8th place (out of 15 schools in the district).

- Test scores for all 9th graders (in the district) fell from 80.4% to 80.1% (AMS), and from 82.5% to 82.4% (ARS). Test scores for grades 10 to 12 were unchanged.
- Scores by school spending were only affected in the $630-644 range, which contains THS ($638 budget/student). AMS and ARS were unchanged in this spending range. However, the %PM, $PR, and %OP decreased by 6%, 7%, and 7%, respectively. 
- Scores by school size were only affected in the Medium (1,000-2,000) range, which contains THS (1,635 students). AMS and ARS were unchanged in the Medium size range. However, the %PM, %PR, and %OP all decreased by 6%. 
- Since THS is a charter school, only the scores of charter-type schools were affected. AMS and ARS were unchanged. However, %PM, %PR, and %OP decreased by 4%, 4%, and 3%, respectively. 
- After removal of THS 9th graders' scores, AMS and ARS showed mostly insignificant changes in the subanalyses. This is likely because THS 9th graders were a small subpopulation in most subanalyses and because their mean test scores were similar to the overall mean test scores of the subanalyses. 

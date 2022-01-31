# School_District_Analysis_Challenge
School district analysis of math and reading test scores in the event of academic dishonesty.

---

# Overview of the School District Analysis

There are two instances of this anaylysis. The first iteration of this script analyzes test score data from thousands of students accross 15 different school districts. The purpose of this analysis is to perform cross-comparison metrics of each school with their respect to their math and reading scores. Beyond this, further analysis will be made based on other criteria including the school size, the type of school, and the monetary value spent by the school. This information will be useful for being able to assess and make strategic decisions for how each school can improve.

In the second iteration of this code, the school board was notified the data contained evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. In order to the uphold state-testing standards, this math and reading score data was replaced for Thomas High School with NaNs while keeping the rest of the data intact. The same analysis of the school district was then repeated. This document is intended to describe how these changes affected the overall analysis.

---

# Results: 

## District Summary Analysis 
- Original Code

After aggregating all the data, the averages of the scores was calculated for all students across the 15 districts. The calculated average was based on the total student count for both math and reading. The results are shown in the figure below. The dataframe indicates that approxitmately 75% and 86% of the students passed math and reading respectively. This results in an overall pass rate of 65%. 

![District Summary Original](Resources\Original\district_summary_df.PNG)

- Modified Code

After resulting the math and reading scores for Thomas High School to a not-a-number, NaN, the same analysis was performed for the student averages. It would be expected that by reducing the numbers for the 9th grade test scores that the test score average would drop slightly. However, based on the figure below, it can be observed that there is minimal to no affect to the overall average, assuming one significant figure. This is perhaps due to the fact that not only were the test scores removed by the sutdent count was also dropped, which wouldn't really affect the average. The average also has thousands of numbers to account for, so dropped a certain grade of one school may have a less likely chance to make a big difference.

![District Summary Modified](Resources\district_summary_df.PNG)

## School Summary Analysis
- Original Code

In this anaylsis, each of the averages was performed and then grouped by their respective schools. The score averages for both math, reading, and overall pass rates are shown below.

![School Summary Original](Resources\Original\per_school_summary_df.PNG)

- Modified Code

After modifying the data to remove the dishonest scoring from Thomas High School, there is a drop in it's respective score averages. However, from a meta anaylsis standpoint this drop is only different by one significant figure. While the scores are of substantiated importance to the district, the overall pass rate remains the about the same with no major drop. It makes sense that the other school districts were not affected as this code was ran to modify Thomas High School only.

![School Summary Modified](Resources\per_school_summary_df_THS_correct.PNG)

## Scores Relative to Other Schools
How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

- Original Code

Based on the summary provided above, the data frame was filtered to find the top five schools across all the districts. Reference the figure below for the top five schools. 

![Top Five Schools Original](Resources\Original\top_schools_df.PNG)

This shows that Thomas High School is quite a disinguished school with an overall pass rate at 90.94%. This puts the school in second place relative to Cabrera High School which boasts an overall passing score of 91.33%. This is a marginal difference of less than 0.5%. Compared to the third school, Griffin High School, with an overall passing rate of 90.6%, which is also very marginal. 

- Modified Code

Based on the summary provided above, the data frame was filtered to find the top five schools across all the districts. This also takes place after the correction for Thomas High School's 9th grade class scores. Reference the figure below for the modified top five schools. 

![Top Five Schools Modified](Resources\top_schools_df.PNG)

Thomas High School continues to be a highly ranked school as shown above. The overall pass rate has dropped to 90.63% in comparison with it's original scoring evaluation; however, it is expected that dropping the scores would result in lower averages and percentages. It is somewhat surprising to see that Thomas High School only dropped marginally, and still continues to ran below Cabrera and above Griffin.

## Scores Based on Other Metrics
### Math and Reading Scores by Grade

In order to parse the anaysis even further, it was best to move from aggregated school data to a grouped aggregation by grade level. This would help better identify the metrics for students that are at differing levels in their curriculum.

- Original Code

![Math Scores By Grade Original](Resources\Original\math_scores_by_grade_df.PNG)
![Reading Scores By Grade Original](Resources\Original\reading_scores_by_grade_df.PNG)

:--:

<b>Math (left) and Reading (right) Scores Using Original Data </b>

  - Modified Code

![Math Scores By Grade Modified](Resources\math_scores_by_grade_df.PNG)
![Reading Scores By Grade Modified](Resources\reading_scores_by_grade_df.PNG)

:--:

<b>Math (left) and Reading (right) Scores Using Modified Data </b>

This table allows a direct comparison of each school to each other and each grade level to each other. The data suggests that Thomas High School, with and without the modification, scores well across each of the grades displaying an average just slighly above 80%. Comparing to other schools, Thomas High School continues perform at a level that would be expected from a top academic institution.

### Scores by School Spending

Upon further research, the analysis below is intended to show the summary scores of the schools relative to their spending. The spending was calculated based on the student count and the school budget. The schools were then placed in equalized bins to the appropriate spending per capita of student.

  - Original Code

  ![Scores By School Spending Original](Resources\Original\scores_by_spending_df.PNG)

  - Modified Code

  ![Scores By School Spending Modified](Resources\scores_by_spending_df.PNG)

  Thomas High School spends $638 per student. This places them in the third bin of a range of $630 to $644 per student. In reviewing the medium sized school data between the original and the modified code, there is no visible difference to the overall calculations.

### Scores by School Size

Even further, the analysis below is intended to show the summary scores of the schools relative to their size. The size was also calculated based on the student count. The schools were then placed in equalized bins to appropriate the range of number of students.

  - Original Code

![Scores By School Size Original](Resources\Original\scores_by_size_df.PNG)

  - Modified Code

![Scores By School Size Original](Resources\scores_by_size_df.PNG)

  Thomas High School is considered a medium sized school at a count of 1635 students. In reviewing the medium sized school data between the original and the modified code, and after accounting for the significant figures, there appears to be no visible difference in the score averages.

### Scores by School Type
Lastly, the analysis below is intended to show the summary scores of the schools relative to their type, district or charter. The data was extracted from the school's information data. The schools were then grouped by their appropriate type to observe which type of school performs better.

  - Original Code

![Scores By School Type Original](Resources\Original\scores_by_type_df.PNG)

  - Modified Code

![Scores By School Type Original](Resources\scores_by_type_df.PNG)

  Thomas High School is considered a charter school. In reviewing the averages, it would appear that the charter type schools perform relatively better than the district-type schools. This is not to suggest that charter schools are superior; however, based on the numerical data for math and reading the scores are at or above 80%. After dropping the scores from Thomas High School, there is no visible difference in the overall averages.

# Summary 
After a thorough analysis of the data, there are four distinct changes in the updated school district analysis after the reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.
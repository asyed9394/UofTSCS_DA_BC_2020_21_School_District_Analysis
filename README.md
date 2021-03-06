# School District Analysis

## Project Overview
The School board has received the analyiss of all schoool in the district and their student's performance in a recent academinc evaluation.

Later the school board has found out that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, it was deemed necessary to repeat the school district analysis by replacing all grade 9 scores at Thomas High School with null values and evaluate the impact.
The analysis requested are:
-The district summary
-The school summary
-The top 5 and bottom 5 performing schools, based on the overall passing rate
-The average math score for each grade level from each school
-The average reading score for each grade level from each school
-The scores by school spending per student, by school size, and by school type

## Resources
- Data source: 
    - School Data "schools_complete.csv" [Link to schools raw data](Resources/schools_complete.csv)
    - Students Data "students_complete.csv" [Link to students raw data](Resources/students_complete.csv)
    
- Software: Anaconda Jupyter notebook Python 3.7 and panda
- Link to the Jupyter notebook which performs analysis for challenge is : [PyCitySchools_Challenge.ipynb](PyCitySchools_Challenge.ipynb)
- Data sources format : see the below screenshot to see the expected file format for data source.

  ![datasource file format](Resources/School_format.png)
  
  ![datasource file format](Resources/Student_format.png)


## Analysis Results
- After removing grade 9th math and reading score at Thomas High School, no major variance was noticed in all metrics reporting at the district level.
     ![District analysis before vs after](Resources/District_Summary_Before_Vs_After.png)
- As school summary is by school, the reported metrics affected Thomas High School reporting only. No other school reported metrics were impacted.

- When the analysis run with null math and reading score for grade 9, the % Passing metrics were impacted significantly as the denominator included grade 9 student. After adjusting the analysis to calculate % metrics excluding grade 9 students counts, we noticed there was not a big variance in any reported metrics for the School analysis.
    ![Thomas High School reporting before vs after](Resources/Compare_Thomas_High_school_before_vs_after.png)
    
- Based on the above the Thomas High School performance was not impacted when grade 9 were scores were from the analysis as long as we removed student counts from the % Passing metric calculations.
 
- Below is the breakdown of analysis by other aggregation levels:
    - Math and reading scores by grade:
        -The average Math and Reading score by grade was affected only for Thomas High School grade 9.It was not calculated (NaN)
        
        ![Thomas High School Grade Scores after](Resources/Thomas_High_School_Grade_score.png)
    
    - Scores by school spending: No significant variance found by spend grouping.
        
        ![By Spend analysis before vs after](Resources/By_Spend_analysis_before_vs_after.png)       
     - By School Size: No signficant change noticed.     
        ![By Size analysis before vs after](Resources/By_Size_analysis_before_vs_after.png)
        
     - By type: Again no signifance variance were notices.
      ![By Type analysis before vs after](Resources/By_Type_analysis_before_vs_after.png)
## Summary
Below are some changes noticed in the updated school district analysis after reading and math scores for the ninth grade at Thomas High School have been replaced with NaNs.

- % Passing Reading is down by 1% for Charter schools type. (Most likely due to rounding)
- % Passing Reading is down by 1% for scchools with spending range from $630 to $644 (most likely due to rounding)
- Average grading score for math and reading can't not be evaluated for Grade 9's students at the Thomas High School
- Overall Passing %age for Thomas High School was slighly donw by .3% 

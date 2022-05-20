# School_District_Analysis 

## Overview
The chief data scientist from the state school board has requested that an analysis be conducted on the school districts standardized test results for high school students in both math and reading.  The initial school district analysis included a snapshot of the district's key metrics.  The analyis then went on to show key metrics for each school including: top 5 and bottom 5 performing schools based on overall passing rate, average math and reading scores received by students in each grade level, school performance based on the budget per student, performance based on school size, and performance based on school type. 

It was later discolvered that there may have been occurrences of academic dishonesty in one of the district's schools, Thomas High School, at the ninth grade level.  The analysis was performed again, but with this particular school's ninth grade math and reading test scores nullified. The results from the analysis excluding the Thomas High School ninth grade test results are explained below.  

## Results 
To isolate and replace the math and reading test scores with a null value of 'NaN' the following code was used on the student_data data frame: 


![Replace_Scores_NaN](https://user-images.githubusercontent.com/103215123/169561814-5d083ae2-c115-40d9-84e6-e30b4bedf5cf.png)

The loc method allows access to a group of rows and columns, conditionals are used to get only data for Thomas High School ninth graders and the math and reading scores are replaced with NaN. 

The new student data frame that sets Thomas High School (THS) ninth grader scores to NaN is merged with the school_data data frame to create a new school_data_complete data frame that is used to get the updated results. 

- The new student count is 38,709 students, 461 less students than the initial analysis 
- The per school summary shows the following changes for Thomas High School:
  - Initial Analysis Avg Math Score = 83.42, the Updated Analysis Avg Math Score = 83.35, 
  - Initial Analysis Avg Reading Score = 83.85, the Updated Analysis Avg Reading Score = 83.90
  - Initial Analysis Overall Percent Passing = 90.95%, the Updated Analysis Overall Percent Passing = 90.63%

![THS_per_school_summary](https://user-images.githubusercontent.com/103215123/169577287-fcc37bf4-7957-448b-b077-77e3dfce00fe.png)


- Thomas High School remained in the Top 5 Performing schools:

![THS_Top_Five](https://user-images.githubusercontent.com/103215123/169577756-75314977-f18a-40e3-8b63-92aa51ee4712.png)

- Additional Analysis shows: 
  - Overall Passing Percentage went down as spending per student went up
    
    ![Spending_Scores](https://user-images.githubusercontent.com/103215123/169579035-e6a6baa2-2191-426c-95af-243e6e0410e1.png)

  - Scores by school size show that small and medium schools had higher overall passing percentages:
  
    ![Spending_Scores](https://user-images.githubusercontent.com/103215123/169579520-4f830bc0-2bac-4085-b741-eec7bf0f1ffc.png)
    
  - Scores by school type show that Charter School types had higher overall passing rates than District School types    
  
    
    ![School_Type_Scores](https://user-images.githubusercontent.com/103215123/169580065-362c74a6-961f-43d7-ad40-03792fb64ae2.png)

    
## Summary
The analysis shows that there was not a large difference in the Thomas High School math and reading test scores after taking out the 9th grade test results.  There is a notable relationship between the overall passing percentage and the schools spending per student, school size, and school type. The school board may want to further investigate and consider these results in their future planning. 
The code and full analysis can be found in the PyCitySchools_Challenge.ipynb file.  

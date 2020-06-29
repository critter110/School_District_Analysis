# School_District_Analysis
Analysis of school district standardized testing

## Overview
In this module we were tasked with analyzing data from 15 schools including: test scores, budget data, school size data, and school type in order to help write a report for the district. All analysis was done in Jupyter Notebooks using python 3.7 and Pandas.

## Summary
All analysis and figures can be seen in the PyCitySchools.ipynb file. In general, Charter schools performed better than district schools. Smaller schools performed better than larger schools. Surprisingly, the per student budget did not seem to have an effect on test scores, and the lower budgeted schools even performed marginally better than those with a bigger per student budget. 

### Challenge
In this weekly challenge we found out that the scores of all 9th graders at Thomas High School were voided. We were tasked with replacing every ninth grader's math and reading scores with Not A Number values and recalculating the other statistics that the district was interested in with the new cleaned data. 

### Challenge Summary
First we made a copy of the PyCitySchools file and renamed it PyCitySchools_Challenge.ipynb. All the analysis and figures for this challenge can be found in that file. We created a new file to start cleaning the student data before we performed the actual changes in PyCityScools_Challenge file. We used the pandas loc method and the numpy NaN method to select all the ninth grade reading and math scores in the student data file and change them to not a number values. Then we competed the same calculations as in the module to get the requested figures. 

After cleaning the Thomas High School data, the district summary was marginally changed. The average reading and math scores went down by about 0.1 points and the percentage of studnets who passed math, percentage of students who passed reading, and percentage who passed both went down by about 1%. This is reasonable since 9th graders and Thomas High school made up a relatively small percentage of the total district population. 

The school summary was also changed marginally. Every other school was uneffected, but Thomas high school average reading and math scores went down by about 0.1 points. The percentage of students who passed reading and math, and the percentage of students who passed both went down by about 25%-28%. The large discrepency between change of average scores and change of percentage of passing students is due to the fact that when calculating averages, NaN values are not used in the calculation, leading to small changes in average scores. When calculating percentages however, the value of total students (including the 9th graders) is used which causes a large change in the final percentage value. 

The top performing and bottom performing schools were uneffected by cleaning Thomas High School's data. 

The scores by grade figure was uneffected for every other school except for Thomas High school, and Thomas 10th, 11th, and 12th grade statistics were uneffected.

In the spending ranges per student figure, Thomas High School fell into the $630-$644 bin. The changes to the average scores in this bin were negligable, but the % passing math, %passing reading, and overall % all fell about 7% due to the data cleaning. The other bins were uneffected. 

In the school size figure Thomas High School fell into the Medium bin. Changes to average scores in this bin were negligable, but % passing math, % passing reading, and overall % all fell about 5% due to data cleaning. All other bins were uneffected.

In the school type figure, Thomas High School fell into the Charter bin. Again, changes in average scores were negligable, but % passing math, % passing reading, and overall % all fell about 3%. All other bins were uneffected.

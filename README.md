# Pewlett-Hackard-Analysis.

## Overview of the analysis: 
The company Pewlett Hackard is conducting an HR analysis to examine the number of employees eligible for retirement. By identifying the employees likely to retire in the next couple years as well as their positions within the company, HR can better forecast how many new employees to recruit and what types of positions will need to be filled. Preparing for these workforce trends will ensure that the company's staffing remains stable during this period of transition.

## Results: 
The analysis revealed a few main trends:
 - The most common titles for retirement-eligible employees are Senior Engineer and Senior Staff. This pattern makes sense, since employees who have been in the workforce the longest typically have the most senior levels of experience.   
<img width="181" alt="image" src="https://user-images.githubusercontent.com/114873837/209033645-c1be4769-395a-4512-a7cf-d29465f3a236.png">

 - Many of these employees who are retirement eligible have held several roles in the company. When filtering the data to retiring titles, there were approximately 133,374 employee records listed. When we further filtered the data to recognize only unique employee ID values in the unique titles table, this number was reduced to 72,458, which is a more accurate description of the true number of employees eligible. This means that many of these employees held at least two (or more) positions, suggesting that they moved up the ranks during their tenure. The code below helped isolate the distinct values:
<img width="419" alt="image" src="https://user-images.githubusercontent.com/114873837/209240418-8ba2c57a-08e0-492b-a97f-f0c9c88399b5.png">

 - Because the company will be losing so many senior-level employees, it is wise to create a mentorship program that connects workers who are about to retire with the next cohort of potential leaders. To examine this, we filtered the employee data to just those employees born in 1965 (ten years younger than the retirement-elgible employees born between 1952 and 1955). There are about 1550 employees born in the year 1965. While it will be helpful to provide mentorship and professional development opportunities to this cohort, this will not replace the 72,458 employees eligible for retirement. 

 - The success of the mentorship program will likely be impacted by the similarities of the work performed by the mentor and mentee. It would be beneficial to match current employees with mentors from similar departments. More research is needed to add the "dept no" to the data frame for mentorship eligibility so trends in department data can be examined.

## Summary: 

- How many roles will need to be filled as the "silver tsunami" begins to make an impact?
There are 72,458 employees listed in our table of unique values for retirement-eligible employees. That is a significant number of roles to fill over a period of a few years, so Pewlett Hackard must begin to recruit immediately.

- Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
There are only 1550 employees eligible for the mentorship program. Since the number of retirement-eligible employees greatly exceeds this number, the company should have no issues finding a sufficient number of retirement-ready mentors available to teach the next generation. However, the number of employees in the mentorship program is nowhere near sufficient to replace the number of senior-level staff who are about to retire.

- Provide two additional queries or tables that may provide more insight into the upcoming "silver tsunami."
It would be helpful to calculate the percentage of the workforce that is eligible for retirement. While we have created a table that contains data for the unique number of employees of retirement age, the table that contains data for the total base of employees may contain duplicate values or non-current employees. In order to achieve an accurate calculation of the percentage of workforce belonging to each category, we need to compare unique, non-duplicate values to unique, non-duplicate values. To achieve this, I would recreate the process used to create the "unique titles" file with the employees csv file - run a distinct on function specifying the employee IDs and filter them to current employees. 

I would also be curious to know the department breakdown of the retiring employees and their younger counterparts. While we know what roles need to be filled, we don't have a clear picture whether these roles are evenly distributed over Sales, HR, Development, etc. To include this piece of data in the overall story for analysis, I would edit the mentor eligibility table to include a column for department data. To do this, I would edit the code as pictured below.

<img width="934" alt="image" src="https://user-images.githubusercontent.com/114873837/209255918-6275d5cb-ad3c-4f4d-88d9-3eafe6677c1a.png">


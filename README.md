# HR Analytics Report of XYZ Company

## HR Analytics Report Preview

![HR Analytics Report](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/c8b9899d-6a58-431f-8903-066af54ddbfd)

#### Overview
This HR Analytics Report provides a comprehensive analysis of employee attrition within the company, focusing on various demographic and role-based factors. The report is divided into two main sections: an overall dataset analysis and a detailed examination of the Research & Development department.

#### Data Source
The HR_Analytics.csv file typically contains various attributes related to employees and their employment details, which are crucial for performing HR analytics.
EmployeeID, Age, Attrition, Department, JobRole, Gender, MaritalStatus, EducationField, MonthlyIncome, YearsAtCompany, YearsInCurrentRole, TotalWorkingYears, YearsSinceLastPromotion, DistanceFromHome, JobSatisfaction, WorkLifeBalance, OverTime, PerformanceRating, Education, EnvironmentSatisfaction, TrainingTimesLastYear

#### Data Processing and Transformation
1. Import the CSV File into Excel
2. Clean and Prepare the Data: Check Data Quality, Remove Duplicates\
   Fix Data Types: Ensure all columns have the correct data types (e.g., Age as Number, Attrition as Text).\
   Replace Values: Use the Find and Replace feature to replace any incorrect or placeholder values.
3. Create a Pivot Table
4. Configure the Pivot Table
Field List:\
Drag and drop fields into the appropriate areas (Filters, Columns, Rows, Values).\
Common Configurations:
Total Attrition Count: Drag EmployeeID to the Values area and set it to Count.\
Attrition by Department: Drag Department to the Rows area and Attrition to the Values area (set to Count).\
Attrition by Job Role: Drag JobRole to the Rows area and Attrition to the Values area (set to Count).\
Attrition by Age: Drag Age to the Rows area and Attrition to the Values area (set to Count).\
Attrition by Salary: Drag MonthlyIncome to the Rows area and Attrition to the Values area (set to Count).\
Attrition by Gender: Drag Gender to the Rows area and Attrition to the Values area (set to Count).\
Attrition by Education Field: Drag EducationField to the Rows area and Attrition to the Values area (set to Count).
5. Analyze the Data
Use the PivotTable to analyze different dimensions of the attrition data.\
Apply filters to drill down into specific departments, job roles, or other categories.\
Create additional calculated fields or conditional formatting as needed to highlight key insights.\

#### Import Data in Power Query Editor - Add Conditional Column - AttritionCount
Attrition count is used to quantify the number of employees who have left an organization within a specified period, providing a direct measure of turnover and helping assess workforce stability and management effectiveness.

![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/b73f22f6-161f-4aa4-b3c4-8674913fdac5)

#### New Measure in the HR_Analytics Table - AttritionRate
Attrition rates are used to gauge employee turnover, assess retention strategies' effectiveness, and understand organizational health and financial impacts. They inform strategic planning and benchmarking against industry standards for workforce stability and management effectiveness.
```
AttritionRate = SUM(HR_Analytics[AttritionCount])/SUM(HR_Analytics[EmployeeCount])
```

#### Overall Dataset Analysis - 

![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/1a507797-86d7-4260-b9ef-daf7cd70b576)

#### Total Employee Count
Value: 1470
Insight: This KPI represents the total number of employees in the company.

#### Total Attrition Count
Value: 237
Insight: This is the number of employees who have left the company.

#### Attrition Rate
Value: 16%
This KPI is calculated as (Total Attrition Count / Total Employee Count) * 100.
Insight: A 16% attrition rate indicates a relatively high turnover rate.

#### Average Age
Value: 37
Insight: The average age of employees in the company.

#### Average Salary
Value: 6.5K
Insight: The average monthly salary of employees.

#### Average Years at Company
Value: 7
Insight: The average tenure of employees in the company.


![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/3a829585-d0dc-4d74-ae79-c4d15d5ac976)

#### Attrition by Years
Value:
Year 0: 59 employees left.
Year 1: 16 employees left.
Year 2: 19 employees left.
Year 3: 21 employees left.
Year 4: 9 employees left.
Year 5: 8 employees left.
Year 6: 18 employees left.
Business Insight: This chart shows the number of employees who left the company categorized by their years of service. High attrition in the early years indicates potential onboarding or early engagement issues, necessitating a review of onboarding processes and early career support.


![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/797b1268-34e6-42cf-90a7-912cb4fe25be)

#### Attrition by Education
Value:
Life Sciences: 38%
Medical: 27%
Marketing: 15%
Technical Degree: 14%
Human Resources: 6%
Business Insight: Depicts the distribution of attrition among employees with different educational backgrounds. Higher attrition in certain education fields can suggest that specific roles may not meet the expectations or career aspirations of employees with those backgrounds, prompting a need for targeted training and career path development.


![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/0335fe25-0539-46ce-bb85-be19d1035086)

#### Attrition by Job Role
Value:
Laboratory Technician: 62
Sales Executive: 57
Research Scientist: 47
Sales Representative: 33
Human Resources: 12
Manufacturing Director: 10
Business Insight: Displays the number of employees who have left the company categorized by their job roles. High turnover in specific roles suggests these positions may have particular challenges or unmet employee needs, warranting a deeper analysis and targeted interventions.


![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/055b2594-0534-4ec0-9efc-748c102988eb)

#### Attrition by Salary
Value:
Upto 5k: 163
5k-10k: 49
10k-15k: 20
15k+: 5
Business Insight: Illustrates the distribution of attrition across different salary ranges. Higher attrition in lower salary brackets might indicate dissatisfaction with compensation, suggesting a need for reviewing salary structures and benefits for lower-paid employees.


![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/84badb02-36ce-482b-87a1-ba29a169943b)

#### Attrition by Age
Value:
26-35: 116
18-25: 44
36-45: 36
46-55: 25
55+: 8
Business Insight: Shows the number of employees who have left the company grouped by their age brackets. Higher attrition among younger employees may point to career development issues or a lack of engagement, while attrition among older employees could indicate retirement or role satisfaction factors.


![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/a737ef02-4d5e-4427-a86c-0ed7e992c965)

#### Attrition by Gender
Value:
Male: 150
Female: 87
Business Insight: Compares the number of male and female employees who have left the company. Gender-based differences in attrition rates can highlight potential issues in the work environment, benefits, or career progression opportunities for different genders.


![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/45e6dd3d-47f4-42cb-9031-411ab882f009)

#### JobRole with Job Satisfaction


#### Summary
Employee Tenure: Attrition is highest in the first year of employment, indicating potential onboarding or early engagement issues.

Job Role Impact: Roles like Laboratory Technician, Sales Executive, and Research Scientist exhibit the highest turnover, suggesting specific challenges or unmet needs in these positions.

Salary Influence: Lower salary brackets experience the highest attrition, pointing to possible dissatisfaction with compensation.

Demographic Factors: Younger employees (ages 26-35) and male employees show higher attrition rates, highlighting the need for targeted retention strategies for these groups.

Educational Background: Employees with education in Life Sciences and Medical fields have higher attrition rates, suggesting a mismatch between job expectations and job reality for these backgrounds.

![image](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/8bc81f48-cd1b-431a-ab99-713a55e8acff)

##### This report will be filtered on the basis on Departments

# HR Analytics Report of XYZ (Research & Development)

![Research   Development](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/fa1ef236-83b7-407a-9bd1-e9ef43edc46b)

1. Count of Employees:
Value: 63
The total number of employees in the Research & Development department, indicating the size of this critical function.

2. Total Attrition Count:
Value: 12
The number of employees who have left the Research & Development department, highlighting turnover in this specific area.

3. Attrition Rate:
Value: 19%
The percentage of employees who have left the Research & Development department compared to the total number of employees, showing retention performance within the department.

4. Average Age:
Value: 38
The average age of employees in the Research & Development department, useful for workforce planning and understanding demographic impacts on innovation and development.

5. Average Salary:
Value: 6.7K
The average monthly income of employees in the Research & Development department, reflecting the company's investment in R&D talent.

6. Average Years at Company:
Value: 7
The average tenure of employees in the Research & Development department, indicating loyalty and stability within this critical function.

7. Attrition by Years
Value: 
Year 0: 4
Year 1: 2
Year 2: 1
Year 3: 1
Year 9: 1
Business Insight: This chart shows the attrition trend in the Research & Development department by years of service. High attrition in the early years could indicate onboarding or role fit issues within the R&D department, necessitating improvements in these areas.

8. Attrition by Job Role
Value: 
Human Resources: 12
Manager: 0
Business Insight: Displays the number of employees who left the Research & Development department by job role. High turnover in specific R&D roles may suggest role-specific challenges or unmet needs, which require targeted interventions and support mechanisms.

9. Attrition by Salary
Value: 
Upto 5k: 10
5k-10k: 1
10k-15k: 1
15k+: 0
Business Insight: Illustrates attrition in the Research & Development department across different salary ranges. Higher attrition in lower salary brackets within R&D might indicate dissatisfaction with compensation, suggesting a need for reviewing salary structures and additional incentives for R&D employees.

10. Attrition by Age
Value: 
26-35: 8
18-25: 2
36-45: 2
46-55: 0
55+: 0
Business Insight: Shows the number of employees who have left the Research & Development department grouped by their age brackets. Higher attrition among younger employees in R&D may point to career development issues or lack of engagement in this function.

11. Attrition by Gender
Value: 
Male: 6
Female: 6
Business Insight: Compares the number of male and female employees who have left the Research & Development department. Any significant gender-based differences in attrition rates can highlight potential issues in the work environment, benefits, or career progression opportunities for different genders within R&D.

12. Attrition by Education
Value: 
Human Resources: 58%
Technical Degree: 17%
Medical: 17%
Business Insight: Depicts the distribution of attrition in the Research & Development department among employees with different educational backgrounds. Higher attrition in specific education fields can suggest that certain roles within R&D may not meet the expectations or career aspirations of employees with those backgrounds, prompting a need for targeted training and career path development.

13. JobRole with Job Satisfaction
    

#### Research & Development Report Summary
Higher Attrition Rate: The R&D department has a slightly higher attrition rate compared to the overall company, indicating potential issues specific to this function.

Role-Specific Turnover: All attrition in the R&D department is from the Human Resources role, highlighting a need for role-specific interventions.

Salary and Tenure: Similar to the overall trend, lower salary brackets within R&D see higher attrition, and the highest attrition occurs within the first year.

Demographic Factors: Attrition is equally split between males and females, with the majority occurring in the 26-35 age group, similar to the overall company trends.

Educational Background: The highest attrition rate is among employees with Human Resources education, suggesting a need for better alignment of job roles with employee expectations and career aspirations.

# HR Analytics Report of XYZ (Human Resource)

![Human Resource](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/818ffc76-722d-47c3-8631-f25bee55eced)


# HR Analytics Report of XYZ (Sales)

![Sales](https://github.com/dishadey-github/hr-analytics-report/assets/60807918/c01bc534-9966-47ea-aab7-ec20a8dc63a1)


#### Conclusion
The HR Analytics Report provides a detailed examination of employee attrition within the company, highlighting key trends and areas of concern. Through a comprehensive analysis of overall employee data and a focused look at the Research & Development department, several important insights emerge:

High Early Attrition: The highest attrition occurs within the first year of employment, indicating potential issues with onboarding and early engagement. Addressing these areas can improve retention rates and reduce turnover costs.

Role-Specific Challenges: Certain roles, such as Laboratory Technicians, Sales Executives, and Research Scientists, exhibit higher turnover rates. These positions may have specific challenges or unmet needs that require targeted interventions and support.

Salary Dissatisfaction: Employees in lower salary brackets experience the highest attrition, suggesting dissatisfaction with compensation. Reviewing and potentially adjusting salary structures and benefits for lower-paid employees can help mitigate this issue.

Demographic Factors: Younger employees (ages 26-35) and male employees have higher attrition rates. Developing targeted retention strategies for these groups, including career development opportunities and engagement initiatives, can enhance retention.

Educational Background Impact: Employees with education in Life Sciences, Medical fields, and Human Resources show higher attrition rates. Ensuring that job roles align with the expectations and career aspirations of these employees is crucial for reducing turnover.

Department-Specific Insights: The Research & Development department has a slightly higher attrition rate compared to the overall company. The attrition is concentrated in the Human Resources role within R&D, highlighting a need for role-specific interventions and support.

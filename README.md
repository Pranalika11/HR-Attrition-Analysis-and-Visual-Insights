# HR-Attrition-Analysis-and-Visual-Insights
## Project Background
This project was developed in collaboration with the People Analytics and HR Operations teams to support strategic efforts around employee retention. The company operates within the Information Technology & Services sector and has experienced fast-paced growth across functions like Engineering, Sales, and R&D.

The analysis focused on identifying patterns in employee attrition using internal HR datasets containing information on job roles, compensation, tenure, promotion timelines, and work-life balance ratings. The aim was to provide visibility into workforce trends and help leadership teams understand which areas required targeted attention.

As the analyst on the project, I worked closely with stakeholders to scope key questions, clean and structure the data, and design a series of dashboards and SQL-driven summaries that could inform both immediate decisions and longer-term planning.
 
##  Data Structure & Initial Checks
The dataset used for this analysis includes multiple HR-related dimensions, covering employee demographics, compensation, engagement, and tenure-related attributes. Below is a structured view of the data schema:

###  Employee_Info Table

| Column               | Data Type |    
|----------------------|-----------|
| Age                  | int64     |
| Attrition            | String    |
| BusinessTravel       | String    |
| DailyRate            | int64     |
| Department           | String    |
| DistanceFromHome     | int64     |
| Education            | int64     |
| EducationField       | String    |
| EnvironmentSatisfaction | int64  |
| Gender               | String    |
| HourlyRate           | int64     |
| JobInvolvement       | int64     |
| JobLevel             | int64     |
| JobRole              | String    |
| JobSatisfaction      | int64     |
| MaritalStatus        | String    |


###  Employee_Tenure Table

| Column                   | Data Type |
|--------------------------|-----------|
| Employee ID              | int64     |
| MonthlyIncome            | int64     |
| MonthlyRate              | int64     |
| NumCompaniesWorked       | int64     |
| Over18                   | String    |
| OverTime                 | String    |
| PercentSalaryHike        | int64     |
| PerformanceRating        | int64     |
| RelationshipSatisfaction | int64     |
| StandardHours            | int64     |
| StockOptionLevel         | int64     |
| TotalWorkingYears        | int64     |
| TrainingTimesLastYear    | int64     |
| WorkLifeBalance          | int64     |
| YearsAtCompany           | int64     |
| YearsInCurrentRole       | int64     |
| YearsSinceLastPromotion  | int64     |
| YearsWithCurrManager     | int64     |



###  Initial Checks Performed

- Verified column data types and consistency across tables  
- Checked for missing values and duplicate `Employee ID` entries  
- Confirmed expected cardinality of key fields (e.g., one row per employee)  
- Standardized string fields for case-sensitivity (e.g., Attrition: “Yes/No”)  
- Created calculated fields like `Attrition Rate` and `Tenure Bands` using DAX  

These checks ensured the data was clean, consistent, and reliable for downstream visualizations and analysis.


## Executive Summary
This dashboard presents key workforce insights derived from 50,000 employee records across departments including Research & Development, Sales, Support, Software, and Human Resources. The primary goal was to uncover patterns in attrition and identify drivers behind employee turnover using workforce metrics such as department-level attrition, income distribution, tenure patterns, and engagement indicators.

At an organizational level, the active-to-inactive employee ratio is nearly 1:1, underscoring a critical challenge in employee retention. Attrition rates across most job roles remained around 50%, with Research Scientist roles showing slightly better retention (48.9%). Among departments, R&D had the highest attrition rate at 51.21%, followed by Software (50.54%) and Support (50.19%).

Compensation levels (~₹26K/month on average) remained consistent across job roles and did not strongly correlate with attrition, suggesting that pay alone may not be the primary reason for exits. The gender pay distribution was also nearly equal, with average hourly rates split almost evenly between male (49.92%) and female (50.08%) employees indicating parity in base compensation.

Finally, patterns in promotion and role tenure highlighted areas of concern departments with longer gaps since last promotion tended to show higher attrition. The dashboard is interactive, allowing further exploration by department and role for more actionable insight.


![Screenshot (635)](https://github.com/user-attachments/assets/b0dc21f0-3eca-4119-a675-3c7057f17085)


## Insights Deep Dive
### Impact of Promotion Delay:
- The longer an employee goes without a promotion, the more likely they are to leave.
-	The line chart tracking attrition rate by years since last promotion showed a clear upward trend.
-	Attrition starts around 49–51% within the first 10 years but gradually climbs with time, peaking significantly after 30+ years without a promotion, even touching over 75% at some points.
-	While there are some fluctuations due to smaller population sizes in extreme ranges, the general pattern is clear: lack of career progression is strongly correlated with attrition.
-	 This underscores how attrition risk escalates when internal mobility slows, especially in mid-to-late career phases suggesting that the organization’s current promotion timelines may not align with employee expectations for growth.

![Screenshot (668)](https://github.com/user-attachments/assets/052ac984-f65e-4415-a0ae-d1805b1924fc)


### Attrition Trends by Tenure:
 - Attrition rate remains consistently high across all tenure bands, with even experienced employees leaving.
- Analysis of attrition by tenure band revealed a striking insight, attrition was not concentrated among new hires but was uniformly high across all experience levels.
-	Specifically, employees in the 3–5 year range showed the highest attrition rate at 50.72%, followed closely by 5+ years at 50.20% and 1–3 years at 49.91%.
-	The narrow range between these values suggests that employee experience or tenure is not a protective factor against attrition in this organization. This may indicate underlying systemic issues such as lack of career progression, disengagement, or unaddressed dissatisfaction.
-	This implies that tenure without recognition is likely a more demotivating factor than just tenure alone.	This reinforces the need for a performance-linked promotion cycle that rewards merit early and consistently.
-	From a business lens, losing mid- to senior-tenure talent can be costly, both in terms of domain knowledge and rehiring expenses. 

![Screenshot (667)](https://github.com/user-attachments/assets/be52fbc8-b070-4ee8-b949-d6c3321d0b28)

## Recommendations
**Re-engage experienced employees with new growth paths.**
Attrition remains above 50% even after 3–5 years of tenure, indicating retention issues beyond onboarding. Offering lateral moves, mentorship roles, and refreshed career paths could reduce disengagement.

**Implement a clear promotion cadence.**
Employees not promoted within 2–3 years showed rising attrition, with spikes above 75% after long stagnation. Setting up structured career check-ins and transparent criteria may help reverse this.

**Prioritize departmental deep dives.**
R&D, Software, and Support teams show the highest attrition. Launching targeted diagnostics like stay interviews and culture assessments can uncover root causes and guide action plans.

**Focus on non-monetary retention levers.**
Since attrition trends are similar across job roles and salaries, retention strategies should emphasize recognition, learning programs, and career development rather than compensation.

**Monitor promotion equity across gender.**
While attrition is gender-balanced (~50%), continuous tracking of promotion frequency, leadership visibility, and growth access is key to maintaining inclusion and fairness.







# HIRING TRENDS FOR DATA ANALYST POSITIONS

## Overview

Data analysts have become indispensable across industries as organizations increasingly adopt data-driven strategies. The growing reliance on data as a core asset has driven a significant surge in demand for skilled professionals. However, the available talent pool has not kept pace, leaving many companies struggling to fill roles and fully leverage data for competitive advantage.

The objective of this analysis is to provide an overview of job postings for Data Analyst roles across all 50 US states in 2019, using data sourced from the popular job platform Glassdoor.
The purpose of the study is also to answer the following questions:
+ What are the hiring rates by job titles?
+ What is the geographical distribution of data jobs?
+ What are the hiring success rates across job titles?

The analysis was conducted using Looker Studio (formerly Google Data Studio) and is based on a dataset that can be downloaded [here](2019_data_analyst_job.csv).
The Looker Studio dashboard can be downloaded in pdf format [here](Hiring_trends_for_data_analyst_positions_Dashboard.pdf).

The report offers a detailed visualization of job applications and hiring trends for Data Analyst roles in 2019. It highlights key metrics such as hiring rates, applicant distribution by job title and location, and temporal trends. By providing a comprehensive breakdown of these insights, the project is a valuable resource for understanding recruitment patterns, identifying high-demand roles, and informing workforce planning strategies.

This project leverages Looker Studio’s capabilities to create an interactive dashboard that visualizes key trends and delivers actionable insights for optimizing recruitment strategies and addressing talent shortages in the data analytics field.


## **Table of Contents** <br>
- [Dataset](#dataset) <br>
- [Methodology](#methodology)
- [Executive Summary](#executive-summary)



## Dataset


The dataset for this analysis was obtained from Kaggle and focuses on job applications for Data Analyst positions in the year 2019. It comprises over 32,000 entries.

The dataset was obtain from Kaggle. 
The year is 2019

The dataset, containing more than 32k entries, is made up of six columns:

ID:	Unique identifier for the applicants	
Date	The date when the application was received
Job Title:	The data analytics position applied for	
Job Location	The city where the job is located	
Hired	A binary variable indicating whether the applicant was hired (TRUE) or not (FALSE).
Easy Apply	A binary variable showing whether the application was submitted directly on the agency's website (TRUE) or through other methods such as email (FALSE).


## Methodology

The Google Sheet was imported directly to Looker Studio, without modifying the spreadsheet.

Dynamic filters were added to the dashboard, allowing users to filter data by job title, location, or time range for more targeted analysis. An optional metrics feature was implemented, enabling users to select and analyze single metrics or combine multiple metrics for deeper insights. Drill-down functionality was also incorporated, giving users the ability to explore specific job titles, locations, or time periods in greater detail.

The dashboard features three main types of charts to visualize the data effectively.
Bar charts and line graphs highlight comparisons, such as applications versus hires over time. Pie charts display percentage distributions of applications and hires across different job titles and locations. For the “job title breakdown” and “job location breakdow” sections, users can sort values to customize their view. Summary metrics are displayed at the top of the dashboard, providing a quick overview of key data points, including total applicants (32,596), total hires (7,002), and the overall hiring rate (21.48%).

Three key calculations were carried out using calculated fields.

```
Hired Count:
case
when hired ="TRUE" then 1
else 0
End
```

```
Hiring Rate:
	SUM(hired) / COUNT_DISTINCT(ID) * 100
```

```
Number of Applicants:
	COUNT_DISTINCT(ID)
```


## Executive Summary

The analysis of hiring trends for Data Analyst roles reveals several important patterns across job titles, locations, and time periods. 

+ The Digital Marketing Data Analyst role stands out with the highest hiring success rate of 99.95%, highlighting a strong alignment between candidate profiles and job requirements. Similarly, Manufacturing Data Analyst (22.91%) and Data Quality Analyst (20.77%) roles demonstrate high demand for specialized skills. In contrast, roles such as QA Data Analyst (4.68%) and Clinical Data Analyst (5.1%) have lower hiring rates, likely due to intense competition or stricter qualification standards.
+ The data also shows seasonal fluctuations in application volumes, with a peak in July when 3,138 applications were submitted. However, the number of hires remains relatively stable throughout the year, suggesting that hiring decisions are not heavily influenced by application surges.
+ Geographical trends reveal that New York, NY, attracted the highest number of applications (4,650), followed by Chicago, IL, and San Francisco, CA, reaffirming their importance as major data-driven job markets. Interestingly, Austin, TX, and Charlotte, NC, rank disproportionately high in job applications compared to their population sizes, reflecting their rapid growth as metropolitan areas. Conversely, Washington, DC, despite being the 7th most populous city, shows lower application volumes, likely due to its government-focused economy.
Los Angeles, CA, and San Diego, CA, show notably higher hiring rates at 22.67% and 22.81%, respectively, indicating strong demand for Data Analyst roles in these regions. The top 10 cities collectively account for nearly half of all job applications, emphasizing the concentration of opportunities in major metropolitan areas. 
+ Business Data Analyst and Data Quality Analyst roles dominate in terms of application volume, with 23.7% and 19%, respectively, demonstrating their popularity among candidates. Emerging roles like Digital Marketing Data Analyst and Ecommerce Data Analyst reflect evolving industry demands for specialized skills.

![Screenshot (3)](https://github.com/user-attachments/assets/fe15d863-eb11-4d4d-81d3-853392b55295)


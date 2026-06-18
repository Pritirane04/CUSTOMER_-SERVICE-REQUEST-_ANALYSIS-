# CUSTOMER_SERVICE_REQUEST_ANALYSIS
This project performs end-to-end analysis of NYC 311 customer service requests using Data Wrangling and Exploratory Data Analysis (EDA). Here's what it covers:
NYC 311 Customer Service Request Analysis
Exploratory Data Analysis & Statistical Testing on NYC Open Data

Project Overview
This project performs end-to-end analysis of NYC 311 Service Requests using Data Wrangling and Exploratory Data Analysis (EDA). It cleans real-world open data, engineers a key efficiency metric, produces advanced visualizations, and applies statistical hypothesis testing to uncover meaningful patterns in how the city responds to resident complaints.

Dataset
Source	NYC Open Data – 311 Service Requests from 2010 to Present
File	311_Service_Requests_from_2010_to_Present.csv
Records	364,558 rows × 53 columns
Period	2010 – Present
Coverage	All 5 NYC Boroughs (Manhattan, Brooklyn, Queens, Bronx, Staten Island)

Unique Points & Key Highlights
1. Engineered Efficiency Metric
A custom Request_Closing_Time feature is calculated as the difference between Closed Date and Created Date (in seconds), enabling precise measurement of how long each city agency takes to resolve complaints — a metric not present in the raw dataset.
2. Missing Value Analysis
A dedicated missing value bar chart across all 53 columns reveals that school-related and transport-specific fields (Bridge, Ferry, Vehicle) are nearly entirely null, while core fields like Unique Key and Complaint Type are fully populated — guiding smart data cleaning decisions.
3. Geographic Complaint Mapping
Scatter and hexbin plots of Brooklyn complaints using latitude and longitude coordinates visualize spatial concentration of service requests — identifying hotspot neighborhoods within the borough.
4. City-Level Complaint Profiling
Cross-tabulation and stacked bar charts compare the top 5 complaint types across the top 6 cities, revealing distinct urban patterns:
•	Brooklyn & Bronx: dominated by Blocked Driveway and Illegal Parking
•	Manhattan (New York): leads in Noise - Commercial and Noise - Street/Sidewalk
•	Staten Island: disproportionately high Derelict Vehicle complaints
5. Statistical Hypothesis Testing
Two statistical tests are applied to go beyond visual analysis:
•	Chi-Square Test: confirms whether complaint type and city are significantly related (p < 0.05)
•	Kruskal-Wallis Test: a non-parametric test to determine if response times vary significantly across complaint types — robust to non-normal distributions

Project Workflow
•	Data Import & Exploration — load CSV, inspect shape, data types, sample rows

•	Data Cleaning — remove null Closed Date rows, parse datetimes, fill missing City values

•	Feature Engineering — compute Request_Closing_Time in seconds

•	EDA & Visualizations — bar charts, hexbin maps, stacked charts, cross-tabulations

•	Statistical Testing — Chi-Square and Kruskal-Wallis tests

Tech Stack
•	Python 3
•	pandas       — data manipulation and aggregation
•	numpy         — numerical operations
•	matplotlib & seaborn   — visualizations
•	scipy — statistical testing (chi2_contingency, kruskal)

Key Findings
•	Blocked Driveway (100,881) and Illegal Parking (92,679) account for over 53% of all complaints
•	Manhattan has the highest noise complaint density relative to its size
•	Complaint type and city are statistically significantly related (p < 0.05)
•	Response times vary significantly across complaint categories, suggesting uneven departmental workload
•	School-related columns are largely irrelevant for this dataset and can be safely dropped

NYC 311 Customer Service Request Analysis  |  EDA Project

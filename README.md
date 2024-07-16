# Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities
Delve into the nexus of drug abuse and crime with a data-centric exploration, revealing how substance misuse fuels various criminal activities.

## Business Overview/Problem
Insight Analytics Solutions has been approached by a Non-Governmental Organization eager to address a critical issue: the escalating criminal activities ostensibly linked to substance abuse. This organization has noted a marked escalation in crimes such as theft, assault, and vandalism, presumed to be connected to drug addiction within their jurisdiction. However, they find themselves without the requisite tools and insights to fully comprehend the dynamics and nuances of this alarming issue. The specific challenges they are encountering include:

### A. Lack of Data Integration:
The agency collects data from various sources, but there is no centralized system for data integration and analysis.

### B. Ineffective Resource Allocation:
Limited resources are currently allocated to address drug-related crime, but without accurate insights, resource allocation is suboptimal.

### C. Inefficient Reporting:
Current reporting methods are time-consuming and not data-driven, making it challenging to identify trends and patterns.

### D. Lack of Predictive Capability:
The agency lacks the capability to predict and prevent drug-related crimes proactively.

## Aim of the Project
### A. Data Integration and Validation:
Establish robust data integration processes to compile and validate diverse datasets related to substance abuse and criminal activities, ensuring data consistency and accuracy.

### B. Descriptive Analysis:
Perform descriptive data analysis to summarize key statistics and metrics related to drug-related crimes.

### C. Frequencies, Location Trends, and Drug Types Involved.

### D. Trend Identification:
Identify and document temporal trends in drug-related crimes, such as seasonal variations or long-term increases or decreases, using time-series analysis.

### E. Location Analysis:
Conduct location-based analysis to pinpoint geographical hotspots of drug-related criminal activities, supporting focused law enforcement efforts.

### F. Data Visualization:
Develop clear and intuitive data visualizations, such as charts and graphs, using Excel to present analytical findings for easy interpretation by stakeholders.

## Data Description
- **Incident_ID:** A unique identifier for each incident.
- **Crime_Type:** The type of crime committed in the incident (e.g., Theft, Vandalism, Assault).
- **Crime_Location:** The location where the crime took place (e.g., Urban, Downtown, Rural).
- **Crime_DateTime:** The date and time when the crime occurred.
- **Crime_Details:** A brief description of the specific details of the crime in each incident.
- **Drug_Type:** The type of drugs involved or related to the incident (e.g., Heroin, Cocaine, Methamphetamine, Marijuana).
- **Abuser_Age:** The age of the individual involved in the incident.
- **Abuser_Gender:** The gender of the individual involved in the incident.
- **Treatment_History:** Indicates whether the individual involved in the incident has a history of drug addiction treatment (e.g., "Yes" or "No").
- **Demographic_Data:** Information about the demographic background of the individual involved, such as their living area and income level.
- **Arrest_Record:** Indicates whether the individual was arrested in connection with the incident (e.g., "Arrested" or "Not Arrested").
- **Conviction_Record:** Indicates whether the individual has a prior conviction related to the incident (e.g., "Convicted" or "Not Convicted").
- **Police_Activity:** Describes the police activity related to the incident (e.g., "Investigating," "Patrolling," "Responding").
- **Hospital_Admission:** Indicates whether the individual was admitted to a hospital as a result of the incident (e.g., "Yes" or "No").
- **Overdose_Incident:** Indicates whether the incident involved an overdose (e.g., "Yes" or "No").

## Data Exploration
Once the data was downloaded and imported into Excel, it was cleaned and prepared for analysis. A copy of the original data was stored in Google Drive to allow for easy access. Firstly, a new version of the data was created in case there was a need to drop some columns or make other changes. In the newly created worksheet, the following steps were taken:

- **Missing Values:** A thorough check for blanks in all the columns was carried out. Conviction_Record and Addiction_Treatment columns had some missing values which were replaced with ‘No Conviction’ and ‘No Treatment’ respectively.
- **Data Types:** The Crime_DateTime column was in the whole number format which was changed to the datetime format retaining only the dates. The other columns were in the desired datatypes.
- **Column Split:** The Demographic_Data column contained information about the location type and income class however there was already a column containing the location type and only the income class was needed for analysis from that column. The text to columns feature on Excel was used to split this column on the delimiter (comma) and the column with the income class only was retained.
- **New Column:** For better analysis, a new column was created to classify the Abuser_Age into ranges. This was done using the nested if formula: `=IF([@[Abuser_Age]] <= 27, "18-27 Adolescent", IF([@[Abuser_Age]] <= 38, "28-38 Middle Aged", IF([@[Abuser_Age]] <= 59, "39-59 Senior", "60+ Old")))`
- **Data Extraction:** For clearer analysis, the days of the week were extracted from the Crime_DateTime column using `=TEXT([@[Crime_DateTime]], "dddd")`.
- **Duplicate Checks:** The dataset was checked to confirm all the rows in the dataset were unique. The Incident ID column had some duplicates which were removed using the remove duplicates tool on Excel.

To make the dashboard dynamic and get even more specific information, 7 slicers were created:
- **Crime_Details:** To filter the findings for specific crimes.
- **Income:** To have a deeper look at the findings based on income class.
- **Drug_Type:** To take a look into the impact of the different drugs identified.
- **Addiction_Treatment, Arrest_Record, Treatment_History, and Police_Activity** slicers were also created.

## Insights
- **Trend of Crime Incidence in 2022:** There was a peak of crime incidents in December at 874, while the lowest number of crimes was recorded in February at 793 incidents.

![Trend of Crime Incidence](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Trend%20of%20Crime%20Incidence.png?raw=true)

- **Crime Type:** The most common crime type recorded was theft, followed closely by burglary and assault. Vandalism was the least common.

![Incident by Crime](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Crime.png?raw=true)

- **Crime Location:** Urban areas recorded the most crime incidents, followed by downtown areas and suburbs. Rural areas recorded the least incidence of crime.

![Incident by Location](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Location.png?raw=true)

- **Incident by Drugs:** Marijuana was associated with the most crime incidents, closely followed by cocaine and methamphetamine. Heroin recorded the least incidence.

![Incident by Drugs](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Drugs.png?raw=true)

- **Gender Statistics:** Males were associated with more crime incidents, accounting for 70% of all incidents, while females accounted for 30%.

![Incident by Gender](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Gender.png?raw=true)

- **Demographics:** Individuals within the age ranges of 28-38 and 39-59 were involved in the most crime incidents.

![Demographics](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Demographics.png?raw=true)

- **Police Activity:** Most crimes were committed when the police were responding to calls, and the least when they were on patrol.

![Incident by Police Activity](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Police%20activity.png?raw=true)

- **Incident by Income Class:** Individuals belonging to the low-income class were responsible for the most crimes compared to the middle and high-income classes.

![Incident by Income Class](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Income%20Class.png?raw=true)

- **Incident by Location and Police Activity:** Urban areas had the highest total police activity across all categories (responding, investigating, and patrolling), with responding being the highest.

![Incident by Location and Police Activity](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Location%20and%20Police%20Activity.png?raw=true)

- **Incident by Day of the Week:** The highest number of crime incidents occurred on Sundays and Tuesdays, while the least incidence occurred on Thursdays.

![Incident by Location and Day of Week](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Location%20and%20Day%20of%20the%20Week.png?raw=true)

- **Conviction and Drug Type:** For most drug types, most crimes were seen where there was no prior conviction history.

![Incident by Drug and Conviction Record](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Incident%20by%20Drug%20and%20Conviction%20Record.png?raw=true)

## Dashboard
![Dashboard](https://github.com/Ayanfeoluwadamilola/Drug-Abuse-Exploring-the-Nexus-between-substance-Abuse-and-diverse-criminal-Activities/blob/main/Dashboard.png?raw=true)

## Recommendations
- **Location:** More focus should be placed on urban areas due to the high number of incidents.
- **Empowerment and Engagement Programs:** Implement programs targeted to empower and engage youths and middle-aged adults. These programs could include educational programs on drug use and workshops that can help improve income as people belonging to the low-income class were also associated with high crime rates.
- **Police Patrol:** Re-evaluate police patrol strategies since the least number of incidents occur while on patrol. Increase patrols on Sundays and Tuesdays, as they are associated with the most crime incidents.
- **Crime Prevention:** Since theft is the most common crime, launch awareness campaigns to educate the public on measures to avoid being a victim.
- **Gender-Specific Programs:** Since males were seen as the perpetrators of most crimes, consider intervention programs targeting males.
- **Rehabilitation Programs:** Introduce and expand rehabilitation programs targeting Marijuana and cocaine users, as these drugs were associated with the most crimes.
- **Continued Data Collection:** Continue data collection and monitoring to ensure trends are tracked and any new observations are addressed promptly.





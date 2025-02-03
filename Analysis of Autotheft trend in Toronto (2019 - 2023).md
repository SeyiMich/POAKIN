# Analysis of Auto Theft Cases in Toronto (From 2019 - 2023)

This case study delves into the trends and patterns of auto theft in Toronto from 2019 to 2023 using open data from [Kaggle](https://www.kaggle.com/datasets/syedabdulshameer/auto-theft).

### Problem Statement

A casual conversation about Toronto sparked a curiosity about the city's auto theft rates. While initially skeptical about the claim of a vehicle being stolen every 40 minutes, 
a quick online search confirmed the startling reality. This investigation aims to understand the magnitude and dynamics of auto theft in Toronto, with the goal of providing insights and 
recommendations for mitigating the problem, with exploration of 
year-on-year changes, spatial and temporal distribution, and insights into the factors driving the alarming rise in vehicle theft in the city.

### Data Processing Steps 

- Step 1 : Searched public datasets; BigQuery & Kaggle, for most relevant dataset. Decided to go with Kaggle as it had the updated info as provided by the Toronto Police Service. The PowerBI dataset can be downloaded [here](https://1drv.ms/u/c/9283b4fb94f10f25/EeS8W0K0KmJIh5p_QG8g2-cBxFyoWXxWawGzdX3Jhcp7wQ?e=qHnws4)
- Step 2 : Loaded data into Power BI Desktop using appropriate connector, dataset is a csv file. Then opened it in Power Query window for the neccesary transformation.
- Step 3 : Also by default, column profiling is based only on first 1000 rows, I changed the status bar option to "column profiling based on entire dataset" as I knew the dataset had over 50,000 rows.
- Step 4 : In the power query editor & in view tab under Data preview section, I checked the "column distribution", "column quality" & "column profile" options in order to review the quality of the entries. 
This helped me identify and eliminate duplicate rows.
- Step 5 : After removing duplicate data, I moved on to handling empty and null rows to ensure data integrity and completeness for further analyses.
- Step 6 : A new custom column was created from the [Theft] column using the below expression:

            if [Theft] = "Theft Of Motor Vehicle" then 1 else 0
                    
           This column was named 'Theft count', before this step the table had no empty or null value 
              therefore this new column will have the value 1 in all its rows. 
           This step is critical to make an explicit measure for easy aggregation later on.

- Step 7 : Then I used the "choose columns" option to select only the required fields and I limited the data to the past 5 years to ensure smotther running of the model and also ensure any 
recommendation made is relevant to the current trends. 
- Step 8 : After selecting the right data type for each column. This was then loaded to Power BI Desktop for further analyses, a Date table was also created and the appropriate data category was selected 
for the main table's geographical data; longitude, latitiude, city, etc. 
- Step 9 : Under the Location column there were more than 20 different unique values, so I grouped similar entries into a common heading as below:

![1](https://github.com/user-attachments/assets/3cafccfd-084b-4ea6-a4ac-a9638d94c556)
 

### Analysis 
A couple of visuals were made to represent the various data:

#### (a) 5-year summary 

  ![2](https://github.com/user-attachments/assets/08dd378f-4ba7-4f26-a135-5db4eb27fc9a)

#### The year 2023 witnessed the highest number of vehicle theft cases in recent years in Toronto, with a staggering 12,067 cases. 
This represents a significant increase of 124.34% compared to 2019, highlighting the alarming growth in auto theft incidents. 
These trends suggest a critical need to understand the contributing factors and implement effective countermeasures.


#### (b) Day & Time Analysis
  ![3](https://github.com/user-attachments/assets/dba9c496-28fe-4ddb-b490-1830aafccf47)

        The analysis revealed a clear pattern in the timing of auto thefts. Over 30% of incidents occurred between 8pm and 11pm, 
highlighting a specific window of vulnerability. Additionally, Tuesday, Wednesday, and Thursday consistently saw higher rates of auto theft 
compared to other days of the week, suggesting potential connections to routine patterns 
and possible vulnerabilities.
 
  
#### (c) Auto-Theft trends
![4](https://github.com/user-attachments/assets/d33c7cbe-6e96-4cc6-b55d-e156af3b1d78)

        Based on a 95% confidence level, projections suggest that the number of auto theft cases in Toronto will continue to rise, 
reaching approximately 15,311 in 2025. This represents a significant increase from current levels, necessitating proactive measures to address the problem.


#### (d) Auto-Theft trends by Location groups

![5](https://github.com/user-attachments/assets/a3e27992-aa4a-44e4-a0fd-0bfc74091701)
  
#### (e) Auto-theft cases by Location groups

![6](https://github.com/user-attachments/assets/7b706001-a609-46c4-9743-36dd61ff2334)

        Residential places emerged as the most common locations for auto theft, 
            underscoring the vulnerability of homes and private properties.
        Parking lots followed closely behind residential areas, 
            suggesting the need for enhanced security measures in these spaces.


#### (f) Auto-theft cases by Location groups

![7](https://github.com/user-attachments/assets/9b14cfdd-40ed-4470-ab2c-fb3ed63fec8f)
  


### Insights
The following inferences can be drawn from the report;

#### [a] Total number of Autotheft cases in the past 5 years
        a) Autotheft cases in 2019 = 5379
        b) Autotheft cases in 2020 = 5794
        c) Autotheft cases in 2021 = 6615
        d) Autotheft cases in 2022 = 9791
        e) Autotheft cases in 2023 = 12067 
        
        There's an alarming increase in auto theft incidents. These trends 
            suggests a critical need to understand the contributing factors 
and implement effective countermeasures.

#### [b] Daily Analysis 
  
         3 out of 10 Autotheft cases happened between 20:00 hr and 23:00hr; 8pm and 11pm.

#### [c] Trend Forecast
  
        Car theft in 2025 is projected to be more than 2023 by over 25% 

#### [d] Some other insights
        Residential areas and parking lots had the most car thefts incidents, 
            50% more than all other location groups combined.


### Action Plans
Based on the insights the following action plans are recommended

#### [a] Community engagement
Homeowners' Associations should prioritize security initiatives, including establishing communication channels for reporting suspicious activity 
and promoting awareness among residents.

#### [b] Police Deployment
The Toronto Police Service should increase manpower deployment between 8pm and 12 midnight, focusing on areas with higher concentrations of auto theft cases.

#### [c] Parking Lot Security
Parking lot owners and operators should invest in security measures such as kill switches, alarms, security cameras, and on-site personnel to deter vehicle theft.

#### [d] Stricter Penalties
Given the projected increase in auto theft, the authorities should enforce stricter punishments for individuals convicted of vehicle theft.


### Conclusion
This analysis underscores the critical need for a multi-faceted approach to address the growing problem of auto theft in Toronto. 
Recommendations focus on community engagement, law enforcement, security measures, and stronger deterrents to effectively mitigate the issue. 
Collaboration among residents, law enforcement agencies, and businesses is essential in creating a safer environment for all.


### Analysis of Auto Theft Cases in Toronto From 2019 - 2023
This analysis provides valuable insights into the challenges and potential solutions for addressing auto theft in Toronto. 
Further research and data-driven strategies can help guide future efforts in combating this crime and creating a safer environment for residents.



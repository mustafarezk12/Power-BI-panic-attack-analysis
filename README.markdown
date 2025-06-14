# Panic Attack Analysis Project

## Use Case
This project analyzes data from a dataset of 1200 patients experiencing panic attacks, aiming to uncover insights into the frequency, severity, and key factors influencing these episodes. Panic attacks are sudden episodes of intense fear or anxiety, often accompanied by symptoms such as elevated heart rate, chest pain, sweating, and shortness of breath. Key factors explored include demographic details (age, gender), triggers (caffeine, phobia, PTSD, social anxiety, stress), symptoms (heart rate, chest pain, sweating, shortness of breath), and lifestyle/treatment factors (sleep hours, therapy, medication). The goal is to provide actionable insights for healthcare providers and patients to better manage and mitigate panic attack occurrences.

## Data Source
The dataset is sourced from Snowflake, a cloud-based data platform, and connected to Power BI for analysis and visualization. The connection leverages Snowflake's warehouse to store and manage the data, with Power BI importing or querying the data directly for real-time insights.

### Diagram: Snowflake to Power BI Connection
```
[Snowflake Data Warehouse]
       |
       | (Data Connection: Import or DirectQuery via Snowflake Connector)
       v
[Power BI Desktop]
       |
       | (Visualization and Reporting)
       v
[Power BI Service (Optional for Sharing)]
```
- **Description**: The diagram illustrates the data flow from the Snowflake Data Warehouse to Power BI. The Snowflake connector in Power BI establishes the link, allowing data to be imported into the Power BI model or queried in real-time using DirectQuery mode. The processed data is then visualized in Power BI Desktop, with the option to publish to the Power BI Service for broader access.
![](Images/pipline.png)
## Dataset Overview
The dataset contains records for 1200 patients, with fields including:
- **Demographics**: Age, Gender.
- **Panic Attack Details**: Trigger Reason, Panic Attack Frequency, Panic Score, Duration Minutes.
- **Symptoms**: Heart Rate, Chest Pain, Sweating, Shortness of Breath.
- **Lifestyle and Treatment Factors**: Caffeine Intake, Sleep Hours, Therapy, Medication, Smoking.

## Visualizations and Insights
The report addresses the following key questions, with corresponding visualizations exported as images in the `Images` folder:

1. **What are the most common triggers for panic attacks?**
     
   - **Description**: A column chart displays the count of triggers (Caffeine, Phobia, PTSD, Social Anxiety, Stress) based on the dataset, with Caffeine and Phobia appearing frequently among the 1200 patients.

![](Images/q1_triggers.png)

2. **How do demographic factors like Age and Gender correlate with Panic Attack Frequency or Panic Score?**
   
   - **Description**: A scatter plot with `Age` on the X-axis and average `Panic Score` on the Y-axis, color-coded by `Gender` (Female, Male, Non-binary), shows trends across the 1200 patients.
  
![](Images/q2_triggers.png)


3. **How do symptoms (Heart Rate, Chest Pain, Sweating, Shortness of Breath) vary across different triggers or demographic groups?**
   - **Description**: A table visualizes the count of patients with symptoms (e.g., 500 with Chest Pain True, 500 with Sweating True) across triggers, highlighting variations.

![](Images/q3_triggers.png)

4. **Does Therapy or Medication impact Panic Attack Frequency or Panic Score?**
   
   - **Description**: A pie chart shows the proportion of average `Panic Score` for `Therapy` (49.54% False, 50.46% True), indicating a near-even split among the 1200 patients.

   ![](Images/q4_triggers.png)

## Detailed Report Pages
- **Page 2: Number of Patients by Symptoms**
  - **Content**: Displays the count of patients experiencing specific symptoms, including Chest Pain (500 True, 500 False), Sweating (500 True, 500 False), and Shortness of Breath (500 True, 500 False) across the 1200 patients.
  - **Insight**: Highlights symptom prevalence, equal distribution of `Chest Pain` , `Sweating`, `Dizzinnes` and  `Trembling`
![](Images/p2.png)
- **Page 3: Number of Patients by `Sleep Hours`, `Panic Attack Duration`, and `Drinks per Week`**
  - **Content**: Presents the distribution of patients based on `Sleep Hours`, `Panic Attack Duration (min)`, and `Drinks per Week`, filtered by `Gender`, `Trigger Reason`, `Medical History`, and `Panic Score`. This allows for a detailed breakdown of lifestyle impacts across demographic and clinical factors.


  - **Insight**: Reveals potential correlations, lower sleep hours linked to higher `Panic Score`, or longer durations with specific triggers like PTSD.
  - 
![](Images/p3.png)

- **Page 4: Average of Sleep Hours, Panic Score, and Smoking by Age Group**
  - **Content**: Shows the average `Sleep Hours`, `Panic Score`, and count of `Smoking` (Yes/No) across age groups  for the 1200 patients. 
 
  - **Insight**: Suggests trends,  higher `Panic Score` in older age groups or smoking prevalence affecting sleep, warranting further investigation.
 
  
  ![](Images/p4.png)

![](Images/p4_1.png)

## Thank You 🖤🖥️

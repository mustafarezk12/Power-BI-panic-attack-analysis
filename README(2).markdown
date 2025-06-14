# Panic Attack Analysis Project

## Use Case
This project analyzes data from a dataset of 1200 patients experiencing panic attacks, aiming to uncover insights into the frequency, severity, and key factors influencing these episodes. Panic attacks are sudden episodes of intense fear or anxiety that can include symptoms such as increased heart rate, sweating, and shortness of breath. Key factors explored include demographic details (age, gender), lifestyle habits (caffeine intake, exercise frequency, sleep hours, alcohol consumption, smoking), medical history (anxiety, depression, PTSD), and treatment factors (therapy, medication). The goal is to provide actionable insights for healthcare providers and patients to better manage and mitigate panic attack occurrences.

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

## Dataset Overview
The dataset contains records for 1200 patients, with fields including:
- **Demographics**: Age, Gender.
- **Panic Attack Details**: Panic Attack Frequency, Duration Minutes, Trigger, Panic Score.
- **Symptoms**: Heart Rate, Sweating, Shortness of Breath, Dizziness, Chest Pain, Trembling.
- **Medical and Lifestyle Factors**: Medical History, Medication, Caffeine Intake, Exercise Frequency, Sleep Hours, Alcohol Consumption, Smoking, Therapy.

## Visualizations and Insights
The report addresses the following key questions, with corresponding visualizations exported as images in the `images` folder:

1. **What are the most common triggers for panic attacks?**
   - **Image**: `images/q1_triggers.png`
   - **Description**: A column chart displays the count of each trigger (e.g., Caffeine, Stress, PTSD), highlighting Caffeine as the most frequent in the sample.

2. **How do demographic factors like Age and Gender correlate with Panic Attack Frequency or Panic Score?**
   - **Image**: `images/q2_demographics.png`
   - **Description**: A scatter plot with `Age` on the X-axis, average `Panic_Score` on the Y-axis, and `Gender` as a legend shows trends across demographic groups.

3. **Are there relationships between lifestyle factors (Caffeine Intake, Exercise Frequency, Sleep Hours, Alcohol Consumption, Smoking) and panic attack severity?**
   - **Image**: `images/q3_lifestyle.png`
   - **Description**: A column chart compares average `Panic_Score` across ranges of `Caffeine_Intake`, suggesting potential correlations with higher intake.

4. **How do symptoms (Heart Rate, Sweating, Shortness of Breath, etc.) vary across different triggers or demographic groups?**
   - **Image**: `images/q4_symptoms.png`
   - **Description**: A table visualizes raw data of `Heart_Rate` and `Sweating` (Yes/No as 1/0) by `Trigger`, revealing patterns like higher sweating with Caffeine.

5. **Does Therapy or Medication impact Panic Attack Frequency or Panic Score?**
   - **Image**: `images/q5_therapy_medication.png`
   - **Description**: A pie chart shows the proportion of average `Panic_Score` for `Therapy` (all Yes) and `Medication` (Yes vs. No), indicating limited data impact.

## How to Use This Repository
- **Clone the Repository**: Use `git clone <repository-URL>` to download the project.
- **Open the Project**: Load the `.pbip` file in Power BI Desktop to explore the report.
- **View Visuals**: Check the `images` folder for exported visualizations corresponding to the questions above.
- **Data Connection**: Update the Snowflake credentials in Power BI (`File > Options and Settings > Data Source Settings`) to match your environment.

## Future Improvements
- Expand the dataset with more patient records for robust trends.
- Add interactive filters in Power BI for real-time analysis.
- Incorporate predictive models to forecast panic attack risks.

## License
[Add your preferred license, e.g., MIT, here or state "No license specified" if none.]
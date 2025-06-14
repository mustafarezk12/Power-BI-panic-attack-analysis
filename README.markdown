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

## Dataset Overview
The dataset contains records for 1200 patients, with fields including:
- **Demographics**: Age, Gender.
- **Panic Attack Details**: Trigger Reason, Panic Attack Frequency, Panic Score, Duration Minutes.
- **Symptoms**: Heart Rate, Chest Pain, Sweating, Shortness of Breath.
- **Lifestyle and Treatment Factors**: Caffeine Intake, Sleep Hours, Therapy, Medication, Smoking.

## Visualizations and Insights
The report addresses the following key questions, with corresponding visualizations exported as images in the `images` folder:

1. **What are the most common triggers for panic attacks?**
   - **Image**: `images/q1_triggers.png`
   - **Description**: A column chart displays the count of triggers (Caffeine, Phobia, PTSD, Social Anxiety, Stress) based on the dataset, with Caffeine and Phobia appearing frequently among the 1200 patients.

2. **How do demographic factors like Age and Gender correlate with Panic Attack Frequency or Panic Score?**
   - **Image**: `images/q2_demographics.png`
   - **Description**: A scatter plot with `Age` on the X-axis and average `Panic Score` on the Y-axis, color-coded by `Gender` (Female, Male, Non-binary), shows trends across the 1200 patients.

3. **Are there relationships between lifestyle factors (Caffeine Intake, Sleep Hours) and panic attack severity?**
   - **Image**: `images/q3_lifestyle.png`
   - **Description**: A column chart compares average `Panic Score` across ranges of `Caffeine Intake` and `Sleep Hours`, suggesting potential correlations with severity among the 1200 patients.

4. **How do symptoms (Heart Rate, Chest Pain, Sweating, Shortness of Breath) vary across different triggers or demographic groups?**
   - **Image**: `images/q4_symptoms.png`
   - **Description**: A table visualizes the count of patients with symptoms (e.g., 500 with Chest Pain True, 500 with Sweating True) across triggers, highlighting variations.

5. **Does Therapy or Medication impact Panic Attack Frequency or Panic Score?**
   - **Image**: `images/q5_therapy_medication.png`
   - **Description**: A pie chart shows the proportion of average `Panic Score` for `Therapy` (49.54% False, 50.46% True), indicating a near-even split among the 1200 patients.

## How to Use This Repository
- **Clone the Repository**: Use `git clone <repository-URL>` to download the project.
- **Open the Project**: Load the `.pbip` file in Power BI Desktop to explore the report.
- **View Visuals**: Check the `images` folder for exported visualizations corresponding to the questions above.
- **Data Connection**: Update the Snowflake credentials in Power BI (`File > Options and Settings > Data Source Settings`) to match your environment.

## Future Improvements
- Expand analysis with additional lifestyle factors (e.g., Alcohol Consumption, Smoking).
- Refine visualizations with interactive filters for deeper exploration.
- Incorporate predictive analytics to forecast panic attack risks.

## License
[Add your preferred license, e.g., MIT, here or state "No license specified" if none.]
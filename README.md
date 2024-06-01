# Appointment No-Show Analysis and Prediction

## Project Overview

This project aims to analyze and predict patient no-shows for medical appointments. The dataset includes various patient details and appointment attributes, allowing us to identify patterns and factors influencing no-show behavior. We use several machine learning models to predict whether a patient will show up for their appointment.

## Data Description

The dataset contains the following features:

- **AppointmentID**: Unique identifier for each appointment.
- **Gender**: Patient's gender (Male or Female).
- **ScheduledDay**: The date the patient booked the appointment.
- **AppointmentDay**: The date the appointment is scheduled for.
- **Age**: Patient's age.
- **Neighbourhood**: Location of the appointment.
- **Scholarship**: Indicates if the patient is enrolled in the Bolsa Família program (True/False).
- **Hypertension**: Indicates if the patient has hypertension (True/False).
- **Diabetes**: Indicates if the patient has diabetes (True/False).
- **Alcoholism**: Indicates if the patient is an alcoholic (True/False).
- **Handicap**: Number of disabilities (0-4).
- **SMS_received**: Number of SMS reminders sent to the patient.
- **No-show**: Indicates whether the patient showed up for their appointment (True/False).

## Project Structure

1. **Data Loading and Initial Inspection**
    - Loaded the dataset 
2. **Data Wrangling**
    - Renamed columns for better readability.
    - Checked for and handled null values.
    - Applied one-hot encoding to categorical variables.
    - Extracted and transformed date-related features.
    - Calculated the number of days between the scheduled date and appointment date.
    - Removed outliers and inconsistencies in the data.

3. **Exploratory Data Analysis (EDA)**
    - Visualized the distribution of `AwaitingDays`.
    - Inspected its shape and basic statistics
    - Checked for class imbalance in the target variable (`No-show`).
    - Analyzed the proportion of patients showing up based on various conditions (e.g., Hypertension, Diabetes, etc.).
    - Explored the relationship between gender and show-up rates.
    - Investigated the distribution of appointments by day of the week.
    - Analyzed the number of patients showing up across different neighborhoods.
    - Examined the impact of SMS reminders on show-up rates.
    - Analyzed age distribution and its correlation with no-shows.
    - Investigated the distribution of age among patients with different conditions (Hypertension, Diabetes, Alcoholism, Handicap).

4. **Model Training and Evaluation**
    - **Decision Tree Classifier**
        - Trained a decision tree model and evaluated its performance.
        - Visualized the decision tree.
    - **Random Forest Classifier**
        - Trained a random forest model and evaluated its performance.
        - Addressed class imbalance and feature importance.
    - **Gradient Boosting Machine (GBM)**
        - Trained a gradient boosting model and evaluated its performance.

5. **Power BI Dashboard**
    - Created an interactive dashboard to visualize key insights from the analysis.
    - Dashboard components include:
        - Summary of patient demographics.
        - Analysis of appointment scheduling and no-show patterns.
        - Impact of medical conditions on show-up rates.
        - Visualization of no-show distribution across neighborhoods.
        - Effect of SMS reminders on appointment attendance.
        - Age distribution and its correlation with no-shows.

## Key Findings

- Approximately 20% of patients do not show up for their appointments.
- Patients with certain conditions (Hypertension, Diabetes, Handicap) are more likely to show up.
- Women, particularly in the age range of 50-60, visit the doctor more frequently than men.
- The majority of appointments are scheduled on weekdays, with Tuesday having the highest number of show-ups.
- Patients receiving SMS reminders do not necessarily show up more often compared to those who don't receive reminders.
- Age distribution shows a high number of patients in the 0-10 and 50-60 age groups.

## Model Performance

- **Decision Tree**: Achieved an overall accuracy of 72%, with limitations in predicting no-shows.
- **Random Forest**: Improved performance with better precision and recall for predicting show-ups.
- **Gradient Boosting**: Further improvement in prediction accuracy and balanced performance for both classes.

## Conclusion

The analysis and modeling provide insights into the factors affecting patient no-shows. The models developed can help in predicting no-shows and potentially improving appointment management in healthcare settings. The Power BI dashboard offers an intuitive way to explore the data and insights interactively.



This project provides a comprehensive analysis and prediction approach to understand and manage patient no-shows in healthcare appointments. The Power BI dashboard enhances the analysis by offering interactive visualizations for deeper insights.

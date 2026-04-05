# Cyclistic Bike Share 
# ![a_generate_a_a_group_o](https://github.com/user-attachments/assets/a1f3b886-1b43-4cb3-a6b0-e801e1035c36)
## Project Overview
This project analyzes bike-share usage patterns for Cyclistic, a Chicago-based bike-share company, with the goal of supporting marketing strategies that drive the conversion of casual riders into annual members.
### Business Statement 

The goal of this project is to support Citi Bike’s growth by increasing annual memberships, which generate more consistent and higher revenue than casual riders.
This analysis focuses on identifying behavioral differences between casual riders and annual members using historical ride data, in order to uncover opportunities for targeted marketing and conversion strategies.

### Data Source 
This analysis uses publicly available bike-share trip data provided by Motivate International Inc., the operator of a real-world bike-share program. “Citi Bike” is used in this project as a fictional company name for analysis purposes, while the underlying dataset reflects actual rider behavior.
The dataset includes key variables such as:
Ride start and end times 
Trip duration 
Station locations 
Rider type (casual vs annual member) 
To ensure privacy and ethical data use, personally identifiable information (PII) is not included. Therefore, the analysis focuses on aggregated trends and usage patterns rather than individual riders.
This data is well-suited for identifying behavioral differences, seasonal trends, and usage patterns, which support the objective of converting casual riders into annual members.

### Data Cleaning 
* Data Quality Checks\
    Identified and removed null, missing, and incomplete records 
* Column Filtering\
    Excluded unreliable fields (IDs, demographics, coordinates, tripduration)\
    Retained only relevant columns for analysis  
* Standardization\
    Unified column names across datasets\
    Standardized usertype labels
     *  Subscriber → Member
     *  Customer → Casual 
* Feature Engineering\
   Created:
   *  ride_length= ABS(end_time – start_time)
   *  weekday = TEXT(start_time, “ddd”) </sub>
* Outlier & Missing Data Handling\
    Removed extreme ride durations (invalid outliers)\
    Filtered remaining null/empty rows 
* Data Consolidation\
    Merged datasets using Python (Pandas) 
* Final Transformation\
    Adjusted data types using Power Query




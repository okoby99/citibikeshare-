# Cyclistic Bike Share 
# ![a_generate_a_a_group_o](https://github.com/user-attachments/assets/a1f3b886-1b43-4cb3-a6b0-e801e1035c36)
## Project Overview
This project analyzes bike-share usage patterns for Cyclistic, a Chicago-based bike-share company, with the goal of supporting marketing strategies that drive the conversion of casual riders into annual members.
### Business Statement 

The goal of this project is to support Citi Bike’s growth by increasing annual memberships, which generate more consistent and higher revenue than casual riders.
This analysis focuses on identifying behavioral differences between casual riders and annual members using historical ride data, in order to uncover opportunities for targeted marketing and conversion strategies.

### Data Source 
This analysis uses publicly available bike-share trip data provided by Motivate International Inc.,the operator of a real-world bike-share program.“Citi Bike” is used in this project as a fictional company name for analysis purposes, while the underlying dataset reflects actual rider behavior.
The dataset includes key variables such as:
Ride start and end times 
Trip duration 
Station locations 
Rider type (casual vs annual member) 
To ensure privacy and ethical data use, personally identifiable information (PII) is not included. Therefore, the analysis focuses on aggregated trends and usage patterns rather than individual riders.
This data is well-suited for identifying behavioral differences, seasonal trends, and usage patterns, which support the objective of converting casual riders into annual members.
[Data Source](https://divvy-tripdata.s3.amazonaws.com/index.html)           [License](https://divvybikes.com/data-license-agreement)


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

### 🛠 Tools Used
*    Excel
*    Power Query
*    Power BI
*    Python(Pandas)

### Analysis Summary
 #### 📊 Dual Demand Model
  *    Members (≈82%) → Stable, commuter-driven usage 
  *    Casual (≈18%) → Seasonal, leisure-driven usage 👉 Subscription-led model with seasonal upside

 #### 📅 Seasonality & Usage Trends
  *    Peak: June–July (~400K rides) 
  *    Low: Winter (Dec–Feb)
  *    Summer → longer rides (leisure) 
  *    Winter → shorter rides (commuting)

 #### 👥 Customer Behavior Segmentation
  *    Members: Weekday + peak-hour commuters 
  *    Casual: Weekends + summer leisure users 👉 Distinct segments require targeted strategies

 #### 🕒 Demand Patterns
  *    8 AM: Morning commute peak 
  *    5 PM: Highest demand (evening return + errands) 
  *    Midday: Leisure/flexible usage 👉 Strong commuter core with leisure overlay

 #### 📍 Location Insights
  *    High demand: Business districts & transit hubs
  *    Leisure demand: Tourist & waterfront areas 👉 Demand concentrated in key stations

 #### ⚖️ Business Implications
  *    Members → Recurring, stable revenue
  *    Casual → High-margin growth opportunity
  *    weekdays = Work mobility | Weekends = Leisure mobility

### Visualizations & Findings
👉
[Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNjI3YmQ2N2MtZDNkYi00Yjc0LTkzZGMtYWY1Nzc5MTU3MjMwIiwidCI6IjY3ZjdhOGVkLTdiNTEtNGQ4Mi05MzM2LWQwN2U1NTI4NTI0YiJ9)

<img width="837" height="606" alt="Screenshot (1610)" src="https://github.com/user-attachments/assets/7d51772b-f76b-42f2-8c47-cb51f1a1b412" />



 #### 📊 Rider Type Distribution
  *    👥 Members: 81.6%→ Majority of users are regular riders (commuters) 
  *    🚴 Casual: 18.4%→ Smaller group, mostly occasional or leisure users



  <img width="1148" height="642" alt="Screenshot (1616)" src="https://github.com/user-attachments/assets/7ab9843f-7e07-4c16-9a19-e75c218a9608" /><br/>

 #### 📊 Total Rides by Hour — Key Insights
  *    🌙 Low Activity (12 AM – 5 AM)→ Minimal usage (lowest demand overnight)
  *    🌅 Morning Peak (7 AM – 9 AM)→ Sharp increase (~257K)→ Work commute begins 
  *    ☀ Midday Stable (10 AM – 3 PM)→ Steady rides (~110K–157K)→ Mix of errands & leisure
  *    🌆 Evening Peak (4 PM – 6 PM)→ Highest demand (~368K at 5 PM)→ Return commute + activities 
  *   🌙 Evening Drop (After 6 PM)→ Rapid decline in usage



  <img width="1109" height="624" alt="Screenshot (1617)" src="https://github.com/user-attachments/assets/a17d3c03-b45d-4259-bfb2-133a056386c2" /><br/>


 #### 📊 Weekly Ride Volume by Rider Type
  *    👥 Members dominate weekdays→ Highest rides (Tue–Fri ~364K–428K)→ Driven by daily commuting 
  *    🚴‍Casual riders peak on weekends→ Sharp increase on Sat & Sun (~113K–116K)→ Driven by leisure & tourism 
  *    📉 Member usage drops on weekends→ Significant decline (~213K–208K)  Weekly Ride Volume by Rider Type
  *    👥 Members dominate weekdays→ Highest rides (Tue–Fri ~364K–428K)→ Driven by daily commuting
  *    🚴‍Casual riders peak on weekends→ Sharp increase on Sat & Sun (~113K–116K)→ Driven by leisure & tourism 
  *    📉 Member usage drops on weekends→ Significant decline (~213K–208K)


<img width="1026" height="614" alt="Screenshot (1619)" src="https://github.com/user-attachments/assets/18dbe538-35fb-49e7-9f2f-0cf3b5d71ecd" /><br/>

 #### 📊 Ride Volume by Start Station
  *    📍 Top Stations (High Demand)→ Canal St & Adams St (~44K)→ Clinton St locations (~39K)👉 Major commuter hubs 
  *    👥 Member-Dominated Areas→ Business districts show higher member usage👉 Driven by daily work commute 
  *    🚴‍ Casual Hotspots→ Streeter Dr & Grand Ave (~29K casual)→ Tourist/waterfront locations👉 Driven by leisure & tourism 
  *    📉 Low-Volume Stations→ Parks & attractions (~7K–12K)👉 Seasonal or occasional use

###    Recommendations

 #### Top 3 Recommendations
  1. Target Casual Riders During Peak Seasons Focus marketing campaigns in summer months, when casual riders take longer, leisure trips and are more likely to convert.<br/>
  2. Promote Membership for Daily Commuters Offer incentives (e.g., discounts, free trials) during peak commute hours to encourage frequent riders to switch to annual plans.<br/>
  3. Personalize Marketing by Usage Behavior Segment users based on ride duration and time of use to deliver tailored messages (leisure vs commute) that drive higher conversion rates.








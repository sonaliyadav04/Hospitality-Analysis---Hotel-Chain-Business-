# Hospitality-Analysis---Hotel-Chain-Business-
**Hotel Chain Business [Power BI | Excel]**

Synopsis
AtliQ Grands is a well-established hospitality company that owns multiple five-star hotels across India. The company has been in the industry for the past 20 years and is known for its luxury and business hotels.

**PROBLEM STATEMENT**

AtliQ Grands owns multiple five-star hotels across India. They have been in the hospitality industry for the past 20 years. Due to strategic moves from other competitors and ineffective decision-making in management, AtliQ Grands is losing its market share revenue in the luxury/business hotels category.

Objective: To provide AtliQ Grands with insights from their historical data to regain their market share and revenue.

**SKILLS DEMONSTRATED**

This project exposed me to learn a lot using Microsoft Power BI.

· Multiple complex DAX formulas and Functions.

· Calculated columns

· Data Extraction, Cleaning, and Transformation (ETL)

· Data Modelling

· Data Visualization

**MOCKUP- To build this kind of dashboard. mock up dashboard_atliq grands**

![Screenshot 2025-05-15 183935](https://github.com/user-attachments/assets/11616a0c-0b1f-42e4-94e4-8749a78b24d5)


**DATA SOURCING**

The dataset used for this analysis was collected from Code Basics’ website, I have uploaded the CSV files.

dim_date
dim_hotels
dim_rooms
fact_aggregated_bookings
fact_bookings
DATA TRANSFORMATION

**Data Loading and Power Query Documentation**

Create a folder in Desktop and store all the CSV files related to the hospitality challenge.

Open a Power BI file, and in "Get Data", select the option as folder and browse through the folder containing CSV files.

Then go to Transform data to expand each and every dataset.

Now, duplicate the data source 4 times and in each one, expand one dataset by clicking on the "Binary" option. Also, rename the tables accordingly.

Power Query steps for tables:

dim_date:

Remove the column 'day_type', we are deleting this because we got feedback from the mock dashboard review that Friday and Saturday are considered as weekends in the industry and not sunday. But In our datasets, Saturday and Sunday are considered as weekends. So we delete this column and re-create day_type using calculated columns. dim_rooms

The column names are not captured here. We need to select the "Use First Row as Headers" option.

**DATA MODELLING Data_model_Hotel**

![Screenshot 2025-05-18 145901](https://github.com/user-attachments/assets/3b6181a2-efc9-460a-b4a0-e852472d9972)



**BUILDING DAX**

**Calculated Column**

Our first Calculated column is to get number from week_no column of dim_date into week_number and the formula is : week_number = WEEKNUM(dim_date[date])

Our Second Calculated column to get day_type from dim_date table. So, as we know in hospitality domain weekdays are Sunday to Thursday and weekends are Friday and Saturday. So, the formula to get day_type is : day_type = var wkd = WEEKDAY(dim_date[date]) return if(wkd>5,"Weekend","Weekday")

**MEASURES**

Revenue : To get the total revenue_realized : formula : Revenue = SUM(fact_bookings[revenue_realized]) : and the table is fact_bookings.

Total Bookings : To get the total number of bookings happened: Formula : Total Bookings = COUNT(fact_bookings[booking_id]): and the table is fact_bookings.

As, there are 26 measures. To check the detail of all measures visit [Metric List](https://1drv.ms/x/c/a51016d50e3ba61c/ET46WrjQ2q9AkDH9TlHhhdQByJm7tm2c-5kznvU5KcrMFA?e=nYxcju)


**
**INSIGHTS****

Mumbai generates the highest revenue (669 M) followed by Bangalore, Hyderabad and Delhi.
AtliQ Exotica performs better compared to all 7 type of properties with 320 Million revenue, rating 3.62, occupancy percentage 57 and cancellation rate as 24.4%.
AtliQ Bay has the highest occupancy of 66%.
Week 24 recorded the highest revenue among all, which is 139.6 Million.
Delhi tops both in occupancy and rating followed by Hyderabad, Mumbai, Bangalore.
AtliQ lost around 298 Million in cancellation.
Elite type rooms has the most booking and as well higher cancellation rate.

**Linkedin Profile-**[LINKEDIN PROFILE](https://www.linkedin.com/in/sonali-yadav-a50823171/)

**Portfolio-**

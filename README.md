# Call-Centre-Analysis
# Problem Statement
With the help of this dashboard we would know about total number of calls received by our call centre over a specific period of time for specific state also 
understand the total amount of time our call centre staff spends on calls in hours as well as in minutes for more granular view of call duration.
also it shows response time for customer satisfaction.

# KPI's Requirement
1. Total Number of Calls
2. Total Call Duration in Hours
3. Total Call Duration in Minutes
4. Avearge Call Duration in Minute 
5. Response Time Percentage

# Chart's Requirment
1. Total Call by Day
2. Total Call by State
3. Top Reason for Calls
4. Total Calls by Channel
5. Total Calls by Sentiment
6. Total Calls by Call Centre
7. Grid View Dashboard

# DAX Query Used
1. Date Table = CALENDER (MIN('Call Centre_Call Centre'[Call Timestamp]), MAX('Call Centre_Call Centre'[Call Timestamp]))
2. Day = FORMAT ('Date Table'[Date], "ddd")
3. Total Number Of Calls = COUNT('Call Centre_Call Centre'[Id])
4. Total Call Duration in Minutes = SUM('Call Centre_Call Centre'[Call Duration In Minutes])
5. Total Call Duration in Hours = Total Call Duration in Minutes / 60
6. Average Call Duration in Minutes = AVEARGE('Call Centre_Call Centre'[Call Duration In Minutes])
7. Response Time Percentage = CALCULATE ([Total Calls],'Call Centre_Call Centre'[Response Time] = "Within SLA"|| 'Call Centre_Call Centre'[Response Time] ="Above SLA")/ [Total Calls]
   
 




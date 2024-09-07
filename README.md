
# 🏨 AtliQ Hospitality Analysis - PowerBI

As part of the Codebasics Monthly Resume Challenges, I worked on this Hospitality Analysis project.

📌 [Challenge Link](https://codebasics.io/challenge/codebasics-resume-project-challenge)  
📊 [Interactive Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNjJlYzBjMjEtNWRiZS00ODZkLTllMGQtNWRjYTBmMDg3MWM2IiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)  
🔗 [LinkedIn Post](https://www.linkedin.com/posts/arindam430_hospitality-analysis-activity-7208358776813285377-47cg?utm_source=share&utm_medium=member_desktop)

## 📝 Problem Statement

AtliQ Grands owns multiple five-star hotels across India and has been in the hospitality industry for 20 years. Due to strategic moves by competitors and ineffective decision-making, AtliQ Grands is losing market share and revenue in the luxury/business hotel category. To counter this, the managing director aims to incorporate “Business and Data Intelligence” to regain their market share and revenue. However, they lack an in-house data analytics team.

Their revenue management team decided to hire a third-party service provider to gain insights from their historical data.

### 📋 Task List

As a data analyst, I was provided with sample data and a mock-up dashboard to complete the following tasks:

- Develop metrics according to the provided list.
- Create a dashboard based on the stakeholder mock-up.
- Generate additional insights beyond the provided metrics/mock-up.

### 🗄️ Dataset Understanding

Understanding the available data is crucial before analysis. Here's a breakdown:

- **Dimension Table**: Static data such as customer and product details.
- **Fact Table**: Transaction data.

#### dim_date

- 🌍 `date`: Dates in May, June, and July.
- 👥 `mmm yy`: Date in the format of mmm yy (month year).
- 📅 `week no`: Unique week number for each date.
- 🗓️ `day_type`: Indicates if the day is a Weekend or Weekday.

#### dim_hotels

- 🏨 7 distinct hotels.
- 🏷️ 2 categories: Business and Luxury.
- 🌆 4 cities: Bangalore, Delhi, Hyderabad, Mumbai.

#### dim_rooms

- 🆔 `room_id`: Type of room (RT1, RT2, RT3, RT4).
- 🛏️ `room_class`: Room class (Standard, Elite, Premium, Presidential).

#### fact_aggregated_bookings

- 🏢 `property_id`: Unique ID for each hotel.
- 🗓️ `check_in_date`: Customer check-in dates.
- 🏨 `room_category`: Type of room.
- ✔️ `successful_bookings`: Successful room bookings for a specific date.
- 🛏️ `capacity`: Maximum room count available on a specific date.

#### fact_bookings

- 🆔 `booking_id`: Unique Booking ID for each customer.
- 🏢 `property_id`: Unique ID for each hotel.
- 📅 `booking_date`: Date the customer booked their room.
- 🗓️ `check_in_date`: Customer check-in date.
- 📆 `check_out_date`: Customer check-out date.
- 👥 `no_guests`: Number of guests in the room.
- 🏨 `room_category`: Type of room.
- 🌐 `booking_platform`: Booking method.
- ⭐ `ratings_given`: Customer ratings for hotel services.
- 📊 `booking_status`: Booking status (Cancelled, Checked Out, No Show).
- 💵 `revenue_generated`: Amount generated from the booking.
- 💰 `revenue_realized`: Final revenue based on booking status (deductions for cancellations).

## 📥 Importing Data into PowerBI

Imported five CSV files from SharePoint directly into PowerBI using the required account credentials.

## 📊 Provided Mock-up Dashboard

<p align="center">
    <img src="https://github.com/Arindam430/Hospitality_Analysis_PowerBI/blob/main/Resources/mock%20up%20dashboard_atliq%20grands.png" width="600">
</p>

## 🗂️ Data Model

<p align="center">
    <img src='https://github.com/Arindam430/Hospitality_Analysis_PowerBI/blob/main/Resources/Data%20Model.png' height="400">
</p>

## 📊 Overview Page

<p align="center">
    <img src='https://github.com/Arindam430/Hospitality_Analysis_PowerBI/blob/main/Resources/Overview%20Page.gif' width="600">
</p>

## 💵 Revenue Analysis Page

<p align="center">
    <img src='https://github.com/Arindam430/Hospitality_Analysis_PowerBI/blob/main/Resources/Revenue%20Analysis%20Page.gif' width="600">
</p>

## 🎓 Learnings from this Project 

- Created a new type of bar chart visual (stacked percentage bar chart) using a 100% stacked column chart, useful for various analysis purposes.
- Built dynamic tooltips on card visuals, unlocking different use cases during data analysis.
- Understood how price and demand dynamics, as well as price elasticity, differ significantly between the travel and tourism industry and product industries.
- Hotels often sell through multiple channels, including their own websites. To avoid high platform commissions, they aim to offer the lowest prices on their own sites. However, they can't significantly differ prices across channels, as bots scrape prices and lower their rankings on comparison sites. Offering unique promotions like discount coupons, free items, or extra complimentary night stays helps maintain consistent base prices while providing better deals for direct bookings.
- Discovered that RevPAR is affected by both rate and occupancy. Higher rates typically lead to lower occupancy and RevPAR, and vice versa.
- Explored various cancellation policies followed by different hotels and learned that most hotels charge zero fees if the booking is canceled three months prior. Post that period, charges range from 60% to 90% of the booking cost.
- Utilized bookmarks and selection for various purposes, such as page navigation and filter clearing on the dashboard. [YouTube tutorial](https://www.youtube.com/watch?v=xCSYLrcLW00).
- Adopted a color palette for consistency throughout the dashboard ([Color palette link](https://coolors.co/fbc481-a3d9a5-5ca878-4a7c59)).

## 🔍 Key Insights from the Dashboard

- Occupancy rates fluctuate across hotels, which is normal, but room rates have remained constant. Implementing dynamic pricing could significantly boost revenue.
- Mumbai generates the highest revenue (669M), followed by Bangalore, Hyderabad, and Delhi.
- Mumbai shows both the highest and lowest occupancy rates among hotels.
- AtliQ Exotica outperforms other properties with 316 million revenue, 3.62 rating, 57% occupancy, and 24.4% cancellation rate.
- Ratings greatly impact online channel performance. For instance, across all the cities, AtliQ Seasons has the lowest occupancy% at 44.57% due to its poor average rating (2.3).
- AtliQ Blu boasts the highest occupancy in Mumbai at 66.19%.
- Week 24 recorded the highest revenue at 139.6 million.
- Delhi leads in both occupancy and ratings, followed by Hyderabad, Mumbai, and Bangalore.
- AtliQ lost approximately 298 million due to cancellations.
- Elite rooms have the most bookings but also the highest cancellation rate.
- When customers find the hotel doesn't meet their expectations due to outdated photos, inaccurate online content, or poor pre-check-in service they often cancel upon arrival. Regularly updating content across all channels can help prevent cancellations and improve ratings.

---

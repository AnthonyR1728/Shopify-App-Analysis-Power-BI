# Shopify App Analysis: Power BI Project

## Project Overview
  - This project focuses on analyzing the landscape of Shopify apps using data scraped from publicly available sources on the Shopify App Store. The goal is to identify the key factors contributing to the success of apps on the platform, using Power BI for visualization and analysis.
  - This project involves exploring the app landscape, reviewing user feedback, and evaluating developer responsiveness based on various metrics. Each part of the project is represented in a separate Power BI report page.

## Dataset
  - The analysis uses the shopify.xlsx dataset, which includes the following four tables:

    - apps: Contains details of the apps listed in the Shopify App Store.
    - apps_categories: A join table that connects apps with their respective categories.
    - categories: Contains categories to which each app belongs (one app can have multiple categories).
    - reviews: Contains reviews of the apps, including user ratings, comments, and developer responses (if available).

## Project Breakdown

## Part 1: App Landscape
  - In this section, we analyze the overall app ecosystem, looking at statistics like the total number of apps and trends in user engagement over time.

  Steps:

  1. KPI Card - Unique App Count:
![Proj6  1 1](https://github.com/user-attachments/assets/50fef342-07c3-417d-88af-e1dbaf5de867)

     - Created a KPI card that counts the unique number of apps in the Shopify App Store.

     - Visualization: KPI Card showing the total number of unique apps.

  2. Line Chart - Reviews Over Time:
![Proj6 1 2](https://github.com/user-attachments/assets/97b4f7d3-6070-4925-9caf-c65e5c38a726)

     - Created a line chart showing the sum of review counts over time, with the lastmod date on the X-axis (set to continuous format) and review count on the Y-axis.

     - Visualization: Line chart showing trends in the number of reviews over time.

  3. Scatterplot - Reviews vs. Average Rating:
![Proj6 1 3](https://github.com/user-attachments/assets/e7294f74-d043-46f5-8297-ada31f8937ab)

     - Created a scatterplot comparing the number of reviews (X-axis) with the average rating (Y-axis).
   
     - Added a Text Box for interpretation of insights derived from the scatterplot.
    
     - Visualization: Scatterplot with reviews and ratings, along with an explanatory text box.

## Part 2: Reviews Analysis
  - This section dives deeper into the app reviews, exploring the impact of helpfulness and developer responsiveness on app success.

  Steps:

  1. Helpful Reviews Calculation:
![Proj6 2 1](https://github.com/user-attachments/assets/ffdd1ed8-7244-4c5b-88eb-8edbb67157c4)

     - Created a new column in the Reviews table called helpful_reviews using a DAX formula: rating * (1 + helpful_count).

     - Created a card visual that shows the average value of this new column.

     - Visualization: Card showing the average helpful review score.

  2. Developer Answered Reviews:
![Proj6 2 2](https://github.com/user-attachments/assets/4b4daef8-617f-47a3-be0f-0766d1d106b2)

     - Created a new DAX column called developer_answered, which returns 1 if a developer responded to a review and 0 if they did not.

     - Created a scatterplot comparing the average rating (Y-axis) with the developer_answered status (X-axis) to assess the impact of developer responses on ratings.

     - Visualization: Scatterplot showing the correlation between developer responses and app ratings.

## Part 3: App Reviews and Developer Responsiveness
  - In this section, we explore the relationship between apps and their reviews, as well as the responsiveness of developers.

Steps:

  1. Create Relationship Between Reviews and Apps:
![Proj6 3 1](https://github.com/user-attachments/assets/b79fe6b9-9eae-4351-b617-4d5d0d0d5bc8)

     - Established a many-to-one relationship between the Reviews table and the Apps table using the app_id from the Reviews table and the id from the Apps table.

     - Visualization: A bar chart with developers (X-axis) and the sum of ratings (Y-axis) based on this new relationship.

  2. Bar Chart - Correcting Misleading Insights:
![Proj6 3 2](https://github.com/user-attachments/assets/2056c431-eae8-4119-aaca-18671461beb7)

     - The first bar chart may give misleading insights since a high sum of ratings doesn’t necessarily mean high quality. Created a second bar chart using the helpful_reviews average to correct for this.

     - Visualization: A bar chart showing developers and the average helpful review score, providing a clearer picture of app quality.

  3. Developer Responsiveness:
![Proj6 3 3](https://github.com/user-attachments/assets/4b756b5a-043c-42a7-ad98-3b8174d06c16)

     - Created a bar chart showing the developers (X-axis) and the developer_answered rate (Y-axis) to identify the most responsive developers.

     - Added a filter to display only developers with more than 500 reviews for better accuracy.

     - Visualization: Bar chart showing developer responsiveness filtered by apps with 500+ reviews.

## Power BI Report Pages
  - Each section of the project is represented as a separate page within the Power BI report, with corresponding visualizations for each question.

    - App Landscape: Includes the KPI card, line chart, and scatterplot.

    - Reviews: Contains the average helpful reviews card and developer response scatterplot.

    - App Reviews: Features the bar charts displaying developer ratings and responsiveness, as well as the corrected chart using helpful reviews.



## Project Files

  - shopify-app-analysis.pbix: The Power BI report containing all visualizations and analysis.
  
  - shopify.xlsx: The dataset used for the analysis.
  
  - screenshots/: Screenshots of each question and subquestion, as required for the project.


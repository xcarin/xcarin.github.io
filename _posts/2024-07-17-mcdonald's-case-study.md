---
layout: post
---
![mg dashboard](https://github.com/user-attachments/assets/5ea75658-7356-4a6e-9b43-12df3b58b584)

Click [here](https://public.tableau.com/app/profile/xcarin) to view it interactively in Tableau Public.

> Problem

- McDonald's wanted to enhance the customer experience and better serve customers with good food and service.

> Solution

- To understand customer needs through basic visualise and anlyse mock data using python and tableau.

> Python

- Basic exploratory data analysis and sentiment analysis

> Tableau

- Chart
- Star rating
- Filters

<br/>
<br/>

# UIUX Feedback & Basic Sentiment Analysis

### User Feedback Flow

![m preview](https://github.com/user-attachments/assets/b2131a2d-3d3e-4ae2-b9fd-12b1d727e9a3)

1. Open M app
2. Navigate to bottom navigation bar to select more… options
3. Select My Feedback
4. Click Start Survey
5. Redirect to M Feedback Form
6. Complete Q1 and Q2
7. Click Submit
8. M will receive customers feedback

### User Feedback Insights

The dataset consists of 33000+ records (I have edited and added new columns.) mock data from kaggle anonymized reviews of McDonald’s stores in the United States. The columns include reviewer_id, name, store_name, category, store_address, latitude, longitude, rating_count, review_time, review, rating, rating_x and sentiment.

<b>Objective:</b> To conduct a quick in-depth understanding of large customers reviews, so that M can improve customer experience.

1. An administrator would download the feedback form and collect the data.
2. Conduct data analysis using common data tools such as excel etc. Excel (PivotTable and PivotCharts) will be able to display simple feedback charts ratings.
3. In this case study, python will be used to conduct exploratory data analysis and basic natural language processing sentiment analysis.

<br/>

## Quick & Basic — Exploratory Data Analysis & Sentiment Analysis

### Python — Basic Exploratory Data Analysis (EDA): Ratings

![m pchart](https://github.com/user-attachments/assets/459f8d3b-4e9a-45ef-8cfd-5e4ab88dea77)

It can be observed that most of the customers are satisfied and rated 5 stars, while a slightly higher number of the customers are dissatisfied and rated 1 star only. However, it would be tedious work to read through the large dataset. By leveraging sentiment analysis, not only could compare with the ratings and gain valuable insights of customers reviews but also streamline work processes.

### Python — Basic Natural Language Processing (NLP) & Sentimental Analysis: Reviews

Sentimental analysis uses natural language processing to identify and classify users feedback into sentiments: negative, neutral & positive.

![ms](https://github.com/user-attachments/assets/389f08d4-dfc7-4266-8599-58d457a5f8d3)

After calculating the sentiments, the different sentiment categories are combined into the original dataset and create a dashboard.

![mergems](https://github.com/user-attachments/assets/6476ab1a-b145-4919-9668-52d01e3170a2)

<br/>

> References

- https://en.wikipedia.org/wiki/Golden_Arches
- https://www.mcdonalds.com.sg
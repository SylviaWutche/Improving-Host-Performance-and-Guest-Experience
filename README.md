# Improving-Host-Performance-and-Guest-Experience

I conducted a sentiment analysis on review comments to and examine it's impact on host performance. Here’s the process I followed and the insights I gathered:

### Data Preparation
To begin the analysis, I utilized two main tables from the Madrid AirBnB dataset:

reviews_detailed: This dataset included review comments and details for each review.

listings_detailed: This dataset provided information about listings and their associated hosts.

### Sentiment Classification
I performed sentiment analysis on the review comments to classify them into three categories:

Positive Sentiment: Identified reviews containing keywords such as "Good," "Great," "Excellent," etc.

Negative Sentiment: Detected reviews with keywords like "Bad," "Poor," "Dirty," etc.

Neutral Sentiment: Classified reviews as neutral when no positive or negative keywords were found.

I implemented this classification using a SQL CASE statement to automatically assign sentiment categories based on the presence of these keywords.

### Mapping reviews to hosts
To understand how these sentiments relate to host performance, I mapped each review to its corresponding host by joining the review data with the listing data using the listing_id and host_id,
this enabled me to group the sentiment analysis results at the host level.

### Counting sentiments for each host
I aggregated the data to count the number of positive, negative, and neutral reviews for each host. 

This provided an overview of the sentiment distribution across different hosts, which is key to understanding guest satisfaction levels.

### Calculating host performance metrics
In addition to sentiment analysis, I computed an average review score for each host based on ratings for various aspects, such as cleanliness, communication, and location, 
this helped quantify host performance in a structured way.

### Aggregating results to analyze impact
I combined the sentiment data and the calculated review scores to analyze how review sentiment correlates with host performance. I specifically focused on hosts with the highest number of positive reviews to derive key insights.

## Results and Analysis
Top Hosts by Positive Reviews: I identified the top hosts ranked by the number of positive reviews. For example, the leading host had over 143,842 positive reviews, while others had similar high counts.
Average Review Score: The average review score across the top hosts was 22.86, indicating generally favorable ratings.
Sentiment Distribution Summary:

Positive Reviews: 501,410

Negative Reviews: 8,984

Neutral Reviews: 620,504

## Insights and Recommendations
Despite having a high number of positive reviews, top hosts still had significant neutral review counts. This suggests room for improvement, particularly in converting neutral experiences to positive ones by addressing common concerns highlighted in neutral feedback.
Focusing on areas where neutral sentiments are prevalent could help hosts enhance the guest experience and potentially increase their overall ratings.

This analysis highlights the relationship between sentiment in guest reviews and host performance, offering actionable insights to improve customer satisfaction.

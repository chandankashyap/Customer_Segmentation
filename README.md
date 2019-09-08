# Customer_Segmentation

Customer Segmentation
The topic is divided into 3 significant components:
1.	Calculation of Retention Rate through Cohort Analysis
2.	Customer Segmentation – Approach 1
3.	Customer Segmentation – Approach 2

Calculation of Retention Rate through Cohort Analysis
Cohort Analysis is a Descriptive analytics tool.
In the exercise here we are grouping the customers in Mutually Exclusive Cohorts, which are then measured over time.
Cohort Analysis helps with understanding the high level trends by providing insights on metrics across both the product and the customer life cycle.
Essentially, there are 3 major types of cohorts:
•	Time Cohorts - 
Customers who signed up for a product or service during a particular time frame. The time can be monthly, quarterly or even daily.
•	Behaviour Cohorts - 
Behaviour Cohorts are customer who purchased or subscribed to a service that can be categorized on the scale of basic level to advanced level.
Understanding the needs of various cohorts can help a company design custom made services or products for particular segments.
•	Size Cohorts – 
This categorization can be based on the amount of spending in some period of time after acquisition, or the product type that the customer spent most of their order in some period of time.
Cohort Analysis representation
The Cohort Analysis data is typically formatted as a pivot table.
The row values represent the cohort, in the exercise it represents the month of acquisition and the customers are pooled into these groups based on first ever purchase.
The column values represent months since acquisition. It can be measured in other time periods like months, days, even hours or minutes.
All of this depends on the scope of the analysis.
The first column with Cohort Index 1 represents the total number of customers in that cohort. This is the month of their 1st transaction.
This data is used to calculate the retention rate and other metrics.

Creating Customer Segments based on Recency Frequency & Monetary (RFM) values
RFM stands for Recency, Frequency, and Monetary value, each corresponding to some key customer trait. These RFM metrics are important indicators of a customer’s behavior because frequency and monetary value affects a customer’s lifetime value, and recency affects retention, a measure of engagement.
Businesses that lack the monetary aspect, like viewership, readership, or surfing-oriented products, could use Engagement parameters instead of Monetary factors.
Furthermore, this Engagement parameter could be defined as a composite value based on metrics such as bounce rate, visit duration, number of pages visited, time spent per page, etc.
•	Recency – The freshness of customer activity
•	Frequency – The frequency of customer’s transactions in the last 12 months
•	Monetary – The amount spent by customer in the last 12 months.
RFM factors illustrate these facts:
•	the more recent the purchase, the more responsive the customer is to promotions
•	the more frequently the customer buys, the more engaged and satisfied they are
•	monetary value differentiates heavy spenders from low-value purchasers

In the example we have sorted customers by recency, with the most recent purchasers at the top. Since customers are assigned scores from 1-4, the top 25% of customers receive a recency score of 4, the next 25% a score of 3, and so on.
Similarly, we can then sort customers by frequency from most to least frequent, assigning the top 25% a frequency score of 4, etc. For the monetary factor, the top 25% of customers (big spenders) will be assigned a score of 4 and the lowest 25% a score of 1. 

There are 2 approaches considered to create segments:

Approach 1 – 
Here, the R, F and M values are used to RFM_Score and RFM_Segment.
RFM_Score is calculated by simply adding the R, F and M values. Therefore, the highest score being (4+4+4 = ) 12 and the lowest scores being (1+1+1 = ) 3.
RFM_Segment is calculated by concatenating the R, F and M values generating values like (‘4’+’3’+’4’ = ) 434, 232, 444 etc, based on the R, F and M values a particular customer possesses.
Finally, based on the RFM scores we divide the customer set into 3 quantile, to provide “Gold”, “Silver” and “Bronze” segments.

Approach 2 – 
A more robust and logical approach is to create customer segments with the use of K-means cluster algorithm.
The R, F and M scores were processed using:
•	Standard Scalar – to bring the values to a same scale
•	Log function – to normalize the data and remove skewness

The k-means algorithm is applied and the appropriate value of “k” is determines using the “Elbow Graph” method.

Finally, the Segments are demonstrated by: 
•	The “Snake Plot” which provides an understanding of attributes, i.e., Recency, Frequency and Monetary value that belongs to each segment (with the attributes on the same scale, which was the result of Standard Scalar module).
•	Heat map for relative importance.

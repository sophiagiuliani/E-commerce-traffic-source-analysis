# E-commerce-traffic-source-analysis

The e-commerce company under analysis engaged a marketing agency to create and publish ads on Instagram and Facebook. Since its establishment in April 2023, the business has been most active on Instagram, conducting sales directly through Instagram's chat. However, it aims to expand its business and attract more customers to its website. To achieve this, a marketing agency was hired to promote ads. The agency suggested a 50% budget allocation to Facebook and 50% to Instagram.

This project aims to determine if allocating half of the budget to each platform is the optimal strategy and if it is yielding returns. It also aims to analyze the performance of TikTok for future investments in ads using the platform.  It is essential to note that a high number of sessions from a specific traffic source may not necessarily indicate meaningful engagement. For this reason, the analysis includes session attribution, bounce rate, conversion rate, median session time, and number of sessions through time per traffic source to evaluate the quality of those sessions. 

Calculating other important metrics such as ROI (return on investment) was challenging due to most sales occurring directly through Instagram chat. This complicates accurately assessing whether customers were influenced by the ads on each platform and for this reason this metric was not included in this analysis. 

Data for this analysis was gathered using Google Analytics and processed using SQL in BigQuery. The period analyzed corresponds to November 11th, 2023 to January 9th, 2024. After cleaning and manipulating the data, visualizations were created to display the number of sessions attributed to each traffic source and the quality of these sessions, which includes the bounce rate, conversion rate, number of sessions over time, and median session time per traffic source.

The analysis showed that Facebook had the lowest performance in terms of engaged sessions, bounce rate, and conversion rate. Instagram had the highest performance. TikTok’s performance was very good considering that no paid ad was run on the platform. This shows that reallocating the marketing budget to TikTok could bring more returns than Facebook. Therefore, the results support the conclusion that reallocating the marketing budget is necessary to achieve better results. In this sense, it is suggested to redistribute the marketing budget to TikTok and Instagram for three months, and then compare the results of the period with the results of this analysis.


# Project background

E-commerce is a rapidly growing and competitive industry relies on marketing campaigns and strategies to make the business known. Small and new businesses are often owned and managed by individuals with limited business experience. It is common for such businesses to hire marketing agencies to handle their marketing needs instead of doing it themselves. The marketing team will always face the challenge of demonstrating value and relevance to the business they work for. Therefore, they rely on data analytics to understand customer behavior, optimize business performance, and demonstrate results with evidence. Data analysis provides information that can be used to create a marketing strategy and to evaluate prior marketing efforts. These insights are crucial to understanding if the goals were reached or if changes need to be made. 

However, some marketing agencies do not have a data analytics team and fail to inform the business about the results of the marketing efforts. Of course, the ads are bringing return in terms of the number of sessions, but the question is, how much? For this reason, this project aims to provide insights into the performance of different traffic sources on this e-commerce website by calculating the bounce rate, median session time, number of sessions, and conversion rate. The project will address the following questions:

How many engaged and converted sessions come from each traffic source?
How can the marketing strategy change to improve customer engagement and conversion?
Should the business redistribute the marketing budget? What would be the optimal distribution?


# Approach

The data for this project was obtained from the Google Analytics account of an e-commerce website that sells accessories. The data contains information about the sessions, such as the day and time; events, such as the name of the page visited; and purchases. The analysis covers a period of 2 months, from November 11th of 2023 to January 09th of 2024. The data was imported into BigQuery for data preparation and analysis. The following steps were taken:

Deciding which attribution model would be used in Google Analytics 4.
Connecting Google Analytics to BigQuery to be able to write SQL and manipulate the data to make calculations.
Writing queries to find the number of sessions, bounced sessions, number of engaged sessions, the duration of each session, revenue and conversion rate, all separated by each traffic source. 
Transforming this data into visualizations and creating dashboards using Looker Studio.
Interpreting the data to find insights regarding the performance of each traffic source.
Using the insights to give suggestions to the marketing team for future campaigns.

The data was filtered to exclude information that was not going to be used in this analysis, such as product category, mobile brand, country, etc. The data was aggregated to create new variables such as session time, conversion rate, bounce rate, and number of sessions. The data was then joined to create a single table containing all the relevant variables for the analysis. The results of the conversion analysis were validated using the A/B test, as well as by checking for errors and inconsistencies in the data, such as missing values, duplicates, outliers, and anomalies. 

It is important to note that this approach has some limitations. The Google Analytics data on BigQuery can only be accessed from the last 3 months, and all data before 3 months counted from the date of the analysis cannot be accessed, which limits the amount of data analyzed. Additionally, some important metrics such as Return on Investment from Facebook and Instagram could not be performed, since a big part of the sales are made directly through Instagram chat and therefore cannot be tracked, making it impossible to know if the person was attracted by the campaign or not.

In this context, some adaptations were necessary, such as considering a view of a product on the website as a conversion instead of a purchase. This is because the website has a very high bounce rate, therefore considering the view of a product as a conversion can be useful. However, it is important to note that this approach could be ineffective depending on the particularities of the business, especially if the volume of sales is high on the website, which is not the case here.


# Analysis

Customer engagement is crucial for new e-commerce businesses because it increases the likeability of forming bonds with them. Moreover, consistent engagement leads to stronger and healthier customer relationships, since it can develop customer loyalty and help collect valuable customer information. Fortunately, engagement can be measured and this information can help make decisions that lead to actions that can increase the customer’s engagement.

Although the number of sessions from each traffic source is an important metric to gauge the reach of the marketing campaign, it does not provide any information about the quality of these sessions. Quality in this context means whether those sessions are from people who are engaging with the website. A website could have thousands of sessions in one day, but if those sessions only involve looking at the main page for 3 seconds, they have little to no value for the business, and part of the marketing budget is not bringing any return.

When analyzing the number of sessions per traffic source, we found that Facebook had the most number of sessions (522), followed by Instagram (499) and TikTok (360). However, Facebook had a bounce rate of 67.6%, which means that only 169 sessions were engaged with the website. The table above shows the difference between the total number of sessions compared to the number of sessions that were engaged with the website.

These numbers show that even though Facebook has the highest number of sessions, it has the least number of engaged sessions, losing even to TikTok, where there is no paid ad. Instagram has the better performance, considering that it has the lowest bounce rate and the highest number of engaged sessions. There could be some reasons for that:

Facebook ads are not being well-targeted: the ads are not reaching the audience that could be interested in buying the products.
The brand is not very present on Facebook: the page has more posts, followers, and content on Instagram compared to Facebook. 
There is a missing call to action on the website, which attracts people to stay when they first see the page 

Moreover, when analyzing the number of sessions over time, the chart shows that Facebook  sessions are high only while the ad is running, while Instagram stays linear for all three months of the analysis. This indicates that the Instagram audience, in general, is more engaged with the brand, while the Facebook one accesses the website only after seeing the ad. The TikTok  number of sessions seem to increase when a video is published; they were almost as numerous as Instagram sessions in November. It is important to mention that in this period, many videos were posted on the platform about the store. The numbers show that posting videos on TikTok can be a good strategy, especially because the sessions did not come from paid ads.

The last metric about engagement, but also a very important one, is the median session time. The data shows that the highest median session time comes from Instagram (39 seconds), followed by TikTok (34 seconds) and Facebook (16 seconds). The median session time does not include the bounced sessions because it would drag the median down. These results are coherent with the number of engaged sessions, showing that usually sessions that came through Instagram and TikTok are more engaged compared to Facebook.

Another important metric is the conversion rate. Usually, a conversion rate is calculated based on the number of purchases and the total number of sessions. However, as explained before, most of the sales are made directly through Instagram chat, which means that using the purchase as a conversion action would lead to inaccurate numbers. Also, the business is relatively new and in the phase of expanding its brand visibility. The more the customers interact with the products on the website, the more they tend to remember the brand. This is why for this analysis, a session was considered a conversion when the user looked at a product on the website. Facebook conversion rate was 4.37% which means that from the 522 sessions, only 23 of those sessions viewed a product. TikTok, however, has a conversion rate of 51.12%, and Instagram 75.85%. 

A crucial step in the process of conversion analysis is to perform an A/B test. This statistical method is used to compare the traffic sources to determine which one performs better in terms of achieving the desired outcome which in this case is the results of the conversion analysis. By doing the test we can be confident that the performance of these traffic sources will remain consistent over time. This is very important to make an informed decision about how to allocate marketing resources. The results of the test assure that Facebook will, with a 95% confidence, perform worse than TikTok and Instagram over time and that Instagram will perform better than TikTok. In summary, the ranking of traffic sources in terms of conversion performance is: 

1. Instagram; 
2. TikTok and; 
3. Facebook. 


# Results

From calculating the total number of sessions and the engaged number of sessions from each traffic source it was clear that overall instagram had the better performance. Facebook, however, had the highest total number of total sessions, and the lowest number of engaged sessions. Tiktok had the least amount of total sessions, but the second highest number of engaged sessions, as seen below: 

By analyzing the number of sessions per traffic source over time it was possible to notice that the sessions from Facebook last just as long as the marketing campaign is running (November 30th), while from TikTok and Instagram, they seem to keep more constant. It is still possible to see that the number of sessions dropped in general after December 15th, but it could be due to the holidays. 

The conversion rate was calculated by dividing the number of converted sessions and the total sessions. The result is coherent with the results of the analysis of the engaged sessions, showing that Facebook has the lowest conversion rate, which means that only 4.37% of customers visualize a product on the website.

# Conclusion 

The results of the analysis put in evidence the low performance of Facebook as a traffic source since it has a very high bounce rate, a low number of engaged sessions, a low median session time, and a low conversion rate. The data also shows that Facebook users are not engaged with the brand, since they usually visit the website when reached by an ad, while sessions that originated from Instagram were constant even after the end of the campaign. TikTok showed good results considering that there are no paid ads running on the app, with a relatively low bounce rate and conversion rate. The results show that reallocating and redistributing the marketing budget is necessary to improve engagement and conversion.  


# Recommendations

The analysis suggests the necessity of a change in the marketing strategy, especially regarding the ads run on Facebook. It is very hard, if not impossible, to calculate how much percent of the marketing budget should go to each platform, if any. However, it is possible to implement a strategy and then test it. In this sense, based on the results of the analysis, two different plans are suggested:

1. Invest 50% of the budget on Instagram, 25% on Facebook and 25% on TikTok
The analysis showed that even though there is a high number of sessions from Facebook, most of them are not engaging with the website, which means that it is not increasing sales and/or customer loyalty. The analysis also showed that most of those sessions only happen while the ads are running on the platform, meaning that the presence of the brand on this social media is not as expressive as it is on Instagram, for example. TikTok, however, shows organically a lower bounce rate and a significant amount of engaged sessions, this is an indicator that brand awareness in this social media has potential. The 50% of the budget on Instagram is justified by the analysis results, and also by the fact that most of the sales are already made on the platform. 

In addition, it is suggested to change the target audience on Facebook ads. It is not known in this analysis what the type of Facebook audience created for the previous ads, but it is recommended to focus on: interests that are related to high-end fashion, jewelry, and art; behaviors that indicate a high purchasing power or tendency to spend more than average like online shoppers and frequent travelers; and demographics attributes that are correlated with higher income such as education level. This is because the products sold on the website have a high quality and relatively high price, so if the targeted audience is not expecting high prices, it can lead to a low conversion rate, since they rapidly lose interest. It is also suggested a higher amount of posts on Facebook since the brand activity is not as high as on Instagram.

2. Invest 75% of the budget on Instagram and 25% on TikTok
Considering that increasing the brand activity on Facebook may not be a viable option because it demands work and time, this second option excludes the investments in Facebook ads and includes the investment in TikTok ads. Considering the analysis results, the brand presence on TikTok is promising. As mentioned before, the sessions that originated from TikTok are organic, and have a low bounce rate and a high number of engaged sessions. Moreover, the account already has almost ten thousand followers and five hundred thousand likes. 

The business owner is a fashion student and posts videos on TikTok about her thoughts, life, and her brand. Talking about the products she sells and the reality of being a business owner approximates people with the brand, leading to higher customer loyalty and engagement. Running ads on TikTok could invite new possible customers to the website, but it could also invite them to follow her page, increasing the reachability of her posts and therefore the business. The platform also allows the target audience to use various criteria such as demographics, location, interests, and behavior. In this sense, it is suggested to target women who could identify with the business owner, as well as people who have an interest in fashion, jewelry, and art. 

# Further Analysis

After deciding how to reallocate the budget, it is recommended to perform another analysis to compare the results in three months. In this analysis, the following questions should be answered, analyzing separately each traffic source:

Did the bounce rate decrease or increase? By how much? 
Did the number of engaged sessions increase or decrease? By how much?
Did the conversion rate increase or decrease? By how much?

It is also suggested for further analysis, tracking social media advertisement data, such as reach, impressions, frequency, cost per result, and return on ad spend. This will help to understand the performance of the ads themselves, which is limited when using only data from Google Analytics since it is only related to the website. This information will allow calculations such as return on investment and cost per click, which is very important to check if the investment is bringing the expected results.



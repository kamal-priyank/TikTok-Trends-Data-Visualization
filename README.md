**DATA VIZUALIZATION TikTok Trending Content**

**Data Cleaning**

The TikTok trending videos data is loaded using json.load and the empty lists are initiated for the columns needed in the data Frame, initiating a for loop to iterate through the data and appending data corresponding to the right columns using append function, the columns with only two unique values such as verified and musicOriginal are turned into binary values, the number of hashtags and mentions are also counted through iteration and separating "dayoftheweek" along with the "hour" in which the video was uploaded.  

Then a data Frame is created using pandas which are saved as a file “tiktok.csv” using the function. 

Grouping the data Frame obtained concerning “playCount” and adding a column “count\_mean” which returns the mean value of views, resetting the index to ensure it is enumerating correctly. 

As we came across some outliers while plotting the scatterplot which makes the graphical representation skewed have been removed by calculating the Z-score of the “playCount” and then conditioning it with less than or equal to 3, which removes all the rows having a Z-score above 3.

**Statistical Charts**

**Boxplot:** 

The boxplot shows the differences in the number of views and distinguishes between two categorical factors established from the TikTok dataset. The aim is to look at varying views for when a video is verified vs non-verified, and between videos that use original music or music already available within the application. 

The design of the chart has simplistic features with two colors separating the variables from each other. This is done to make it as easy for the readers to understand this distinction when looking at the chart. With a total number of views on the y-axis, and the variables plotted into boxplots along the x-axis. Moreover, we have assigned values to the boxplot of verified videos, to provide more information regarding the trends for differing views in both cases. There are outliers in both cases, which signify extreme cases in which some videos have gained more views than what is considered average. 

As expected, views tend to be significantly higher for verified videos than for non-verified accounts. Already having a verified account on Tiktok is likely to gain the users more popularity faster than to non-certified accounts. Also, the view of non-original music is slightly higher on average than for original. This indicates that using Tiktok viral songs is likely to gain a user more views. The Y-axis is populated as log form of the playCount and the x-axis is binary in which the boxplots are grouped with respect to binary values. 

We can interpret from the boxplot that the median value (middle quartile) of playcount for videos uploaded from a verified account is greater and music being original or not is insignificant.

<p align="center">
<img width="667" alt="Screenshot 2022-10-02 at 22 01 24" src="https://user-images.githubusercontent.com/66077662/193476104-35d9a901-fd2e-4a66-b003-8c798da4c152.png">
</p>

**Scatterplot**

This is a scatter plot with weekdays along y-axis and hour on the x-axis. The design choice here is again kept as simple as possible with two colors to separate between verified and non-verified videos. We see verified (purple dots) and non-verified (yellow dots) scattered across the chart. The bigger circles indicate a higher concentration of the variable in each weekday/hour. 

The aim was to look at different patterns of popularity as playcount with weekday and hour (time when video is uploaded) as the main influencing factors. At a first glimpse, the reader may not be able to fully understand the impact of these factors. However, a closer look will disclose how certain days have higher views for both verified and non-verified videos. Also, the pattern of the chart shows that videos uploaded after (time) gain a higher playcount. This gives an insight into how the Tiktok logarithm works for videos uploaded during different hours of the day and day of the week.

The Scatterplot shows that the videos uploaded between 18:00 pm and 20:00 pm are the ones with the highest views but also the videos uploaded after noon in general could be expected to gain a considerable number and all the videos uploaded on Tuesdays have gained a sizable number of views over a period when compared to the other days of the week.

<p align="center">
<img width="684" alt="Screenshot 2022-10-02 at 22 02 06" src="https://user-images.githubusercontent.com/66077662/193476125-6c4698f6-ce21-4dd7-9cbd-e1e1a06207e0.png">
</p>

**Histogram**

The grouped histogram along with marginal Boxplots shows that the median duration of videos uploaded from non-verified and verified accounts is 14 sec and 15 sec respectively, most of the videos uploaded with a duration between 5 to 15 sec have a substantial number of views when compared to the ones with higher duration.

The design of the chart has simplistic features with two colors separating the variables from each other. This is done to make it as easy for the readers to understand this distinction when looking at the chart. With a total number of views on the y-axis, and the variables plotted into grouped histogram along the x-axis.

As expected, views tend to be significantly higher for verified videos than for non-verified accounts when uploaded with a duration of 15 sec.

<p align="center">
<img width="674" alt="Screenshot 2022-10-02 at 21 59 52" src="https://user-images.githubusercontent.com/66077662/193476047-5224d513-937e-4325-b83e-be274b7623e0.png">
</p>

## kickstarter-analysis
## Deliverable 3

# 1.	Overview of Project
Louise wants to start a crowd funding campaign to facilitate the funding of her play “Fever”. She has an estimation of budget over 10,000 dollars. However, she is not sure about this project as there are chances of failure and before jumping into it, she wants to gather all the information which might provide her insights and help her to make an informed decision to set her up for success.
The purpose of this project is to help Louise with the analysis of available crowd funding data to determine if there are any specific factors which can make this funding campaign a success.

# 2.	Analysis and Challenges
The first step was to retrieve the available Kickstarter data and made the data more readable and searchable. Before analyzing the data, I familiarized with it, sized it up, changed the format of the dates and tried to get a sense out of it. I organized the data so that it could be easily understood and, could generate insights. I exercised filtering, formatting, freezing specific columns & rows in this phase. 
After the organization of the data, I focused my attention on money raised by various campaigns. Louise estimated her budget of her play to be around $12,000. So, I researched on the data from pledged column to search for the projects which were having similar monetary goals. I sorted the pledges in descending order and did conditional formatting to categorize the outcomes column. The “Successful”, “Failed” and “Canceled” outcomes were color coded to refine the data for visual presentation. It was clearly seen which campaigns were successful for further study, but there were campaigns which were missed their goal by a small margin. So, to include those in the study, I created another column with the percentage funded: (Pledged/goal)x100, and color graded them. 

***Challenge 1:*** The color graded “Percentage Funded” column was almost in single color. It indicated an outlier in the data. Plotted a box plot to find out the outliers and to removed it from the rest of the data.

Then I created a new column for average donation (Pledged money/number of backers). By knowing the average donation that have pledged to campaigns historically, Louise could add incentives for different pledge amounts to encourage backers.

***Challenge 2:*** While creating the column for average donation, there was error “#DIV/0!” and which was removed using “IFERROR(Value, Value_if_error)

Now that the data is clean, filtered, formatted and ready for performing the analysis. We could create several numbers of tables and charts with it to assist us in gaining insights to help Louise in making her decision.

At this stage we had a data of Kickstarters which were successful or nearly missed within similar funding range i.e., 10,000. To further refine the data, we used Pivot table to remove other categories but “Theater”. And then we created another pivot table using subcategories in order to focus on analysis on an area that is more relevant for Louise i.e., "play". With the analysis I came to know that plays subcategory was the most successful in US as well as Great Britain. The ***picture 2.1*** shows a pivot table and a bar chart for the country "Great Britain".

![***Refer Picture 2.1***](Module_1_Challenge/Resources/Picture_2.1.png)
 
Then, I organized the data according to the need of our goals for the project. As Louise is interested in the “plays” which comes in “theater” category. 
I created pivot tables and charts to check the effect of length of campaign on it success. I created another table and chart for plays outcomes based on their monetary goals which are shown and discussed in the following 3.1 and 3.2 sections. 

***Challenge 3:*** It was quite challenging to create the table for the outcome of plays based on goal as there so many COUNTIFS looped in each other. At first it was confusing, and I kept doing mistake. But with practice and meticulous attention I was able to successfully produce the chart. Please chech the following picture for reference. 

**Refer Picture 2.2**
 Module_1_Challenge/Resources/Picture_2.2.png

# 3.	Results
## 3.1	Analysis of Outcomes Based on Launch Date

***Refer picture 3.1*** Module_1_Challenge/Resources/Picture_3.1.png

**Conclusion 1:** The month of May has highest number of successful Theater outcomes.

**Conclusion 2:** There no such peak in failed Theater outcomes with respect to the months as there is for successful theater outcomes. However, in the month of January, March, September, and November, the number of failed Theater outcomes are almost same and lowest. And the highest number of failed outcomes are in the month of May.

## 3.2	Analysis of Outcomes Based on Goals

***Refer picture 3.2*** Module_1_Challenge/Resources/Picture_3.2.png

**Conclusion:** The highest percentage of Successful outcomes in “Plays” subcategory was found to be in goal range of less than $1000. And the highest number of failed outcomes in “Play” subcategory was in the goal range of $45,000 to 49,999. 

## 3.3	Limitations of this data set
The are many factors which can influence the success of a Kickstarter. And there are not quite enough mentioned in the given data. If Louise wants to set, her campaign to mirror other successful ones in the same category than pondering upon the monetary goals and launching date can help her in decision making but is not sufficient to rely on it completely. It would have been nice if there would be more data on the reasons for the success and failure of the Kickstarter projects.  For example, how was the economic growth in that region and country. If there was economic crisis in those year, then people will less likely spend money on leisure. In the decade of COVID-19, Netflix, and super awesome video games people might be interested in other avenues of entertainment which could affect the success of these Kickstarter positively or negatively.

## 3.4	Other possible tables and/or graphs that could be created
There could be multiple number of possible tables and/or graphs that could be created to assist us for making better decision, but due to limited time and efforts I am mentioning only the following:

**a.**	 The outcomes based on launch date chart (picture 3.1) is misleading. The chart in section 3.1 is showing that the month of May has the highest number of successful Theater outcomes, but the month of May also has a highest number of failed outcomes. So, if we plot the successful outcomes in relation to the total outcomes then there is not much significant peak in that month. 

***Refer picture 3.4 (a)***Module_1_Challenge/Resources/Picture_3.4_a.png


**b.** With time, place, and generations the choice of entertainment changes. It would be helpful if we can see if there is a increase or decrease in the popularity of the theater over each year. Or if people in the given country is seeking out to other sources of entertainment over watching plays. So, a graph for year versus successful and failed theater would tell the how the trend is going.  The following pictures of pivot table and chart shows the trend of outcomes over the years, and it clearly shows that there was an increasing trend from 2010 till 2015 but then there is a decrease in 2016 and 2017 from previous years. 
So, we should investigate further to identify what has influenced such trend. 
 

 
***Refer picture 3.4 (b)***Module_1_Challenge/Resources/Picture_3.4_b.png



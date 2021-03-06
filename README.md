# Kickstarting with Excel

## Overview of Project

The purpose of this analysis was to uncover trends in [Kickstarter data](https://github.com/fobordo/kickstarter-analysis/blob/cb1ee7c131f969fe81963381501d0e881acdfcc7/Kickstarter_Challenge%20copy.xlsx.zip) from 2014 to 2016 to determine the best practices to follow for success in launching a theatre or play Kickstarter campaign in countries such as the US and Great Britain.

## Analysis and Challenges

Initially, before the analysis could be performed, the Kickstarter data was cleaned in order to make it more readable and searchable. This involved ensuring all the data was in the proper format, and separated into individual columns as necessary. Once the data was cleaned up and in more readable and searchable formats, a deep-dive analysis was performed on the following two metrics: Outcomes Based on Launch Date and Outcomes Based on Goals.

### Analysis of Outcomes Based on Launch Date

In the analysis of Outcomes Based on Launch Date, focus was given to the launch dates of theatre Kickstarters, specifically, to determine if this metric had any impact on the outcomes of those campaigns. A pivot table was created to include the count of successful, failed, cancelled, and total number of campaigns by launch date month, filtered to calculate results for only theatre campaigns, as seen below.

#### Theatre Outcomes Based on Launch Date Pivot Table

![Theatre Outcomes Based on Launch Date Pivot Table](/Resources/Theater_Outcomes_vs_Launch_PivotTable.png)

Digging into the data, the pivot table showed that some Kickstarters were more successful than others depending on the launch date month. Using the data from the pivot table, a line graph was created to reveal these trends.

#### Theatre Outcomes Based on Launch Date Graph

![Theatre Outcomes Based on Launch Date Graph](/Resources/Theater_Outcomes_vs_Launch.png)

The "Theatre Outcomes Based on Launch Date" graph above shows that from 2014 to 2016, the most successful theatre Kickstarters were launched in May. Ironically, the most failed were also launched in May. Diving further into these metrics, 111 out of 166, or 66.9% of theatre campaigns launched in May were successful, while 52 out of 166, or 31.3% failed. Although the largest number of failures occurred in May, the data shows that the rate of success for theatre campaigns launched in May was still significantly higher than the rate of failure.

The graph reveals another interesting metric for the month of December. Theatre campaigns that were launched in December had an almost equal success and failure rate, with a success rate of 49.3% (37 out of 75) and failure rate of 46.7% (35 out of 75). The data suggests that if a theatre campaign is launched in December, it has an almost 50/50 chance of success.

### Analysis of Outcomes Based on Goals

In the analysis of Outcomes Based on Goals, focus was given to the monetary goals of play Kickstarters to determine if this metric had any impact on the outcomes of those campaigns. In order to reveal any trends in the data, a new table was created, which extracted the goal ranges, number of successful, failed, and canceled campaigns, total projects, and percentage of successful, failed, and canceled campaigns of play Kickstarters from the Kickstarter data. 

#### Outcomes Based on Goal Table
![Outcomes Based on Goal Table](/Resources/Outcomes_vs_Goals_Table.png)

Using the data from the new table, a line graph was created to visualize the data, which uncovered a trend that showed the correlation between goal range and percentage of successful, failed, and canceled play campaigns.

#### Outcomes Based on Goal Graph

![Outcomes Based on Goal Graph](/Resources/Outcomes_vs_Goals.png)

The "Outcomes Based on Goal" graph above shows that from 2014 to 2016, the highest percentage of successful play Kickstarter campaigns had goals of less than $1,000, or $1,000 to $4,999. The play campaigns with goals of less than $1,000 had the highest success rate of 76%, while those with goals within the range of $1,000 to $4,999 had a success rate of 73%. Interestingly, most other data points for the success rates of other goal ranges fell below 60%, except for two goal ranges. The play campaigns with goals of $35,000 to $39,999 and $40,000 to $44,999 each had a success rate of 67%, indicating that the goal range does not necessarily need to stay below $4,999 to be successful.

On the other hand, the graph shows that the two highest percentage of failed play Kickstarter campaigns had goals of $45,000 to $49,999, or greater than $50,000, respectively. The play campaigns with goals of $45,000 to $49,999 had the highest failure rate of 100%. The runner-up was play campaigns with goals greater than $50,000, which had a failure rate of 88%.

### Challenges and Difficulties Encountered

The first challenge was interpreting the data in columns "deadline" and "launched_at." The data in these columns was not in a readable format, and contained long, random numbers that didn't add any value to the data story. In order to make this data more readable, a [Unix Timestamp Converter](https://www.epochconverter.com/) was used to confirm that the numbers weren't just random, and were, in fact, Unix Timestamps. After confirming that the numbers represented Unix Timestamps, two new columns were created in Excel containing formulas to convert the numbers to a more readable format. The two new columns, "Date Created Conversion" and "Date Ended Conversion" converted the "launched_at" and "deadline" numbers to "DD/MM/YYYY" date formats, allowing a better observation of the metrics for trends and patterns. 

In addition to the challenge of interpreting the data for launch dates and deadlines, another challenge was having to separate the data in the "Category and Subcategory" column into two columns for "Parent Category" and "Subcategory" in order to analyze the data for trends based on each metric individually. Other challenges included determining what metrics should be calculated to reveal more trends in the data, such as percentage of goals funded abd average donations pledged.

## Results

### Conclusions on Outcomes Based on Launch Date

Two conclusions that can be drawn about the Outcomes based on Launch Date are as follows:

1. To increase the chances of a successful theatre Kickstarter campaign, the data suggests it should be launched during the month of May.
2. Theatre campaigns launched in December have an almost 50/50 chance of success or failure, suggesting it would be best to avoid launching a campaign during this month.

### Conclusions on Outcomes Based on Goals

Three conclusions that can be made about the analysis of Outcomes Based on Goals are as follows:
1. To optomize the chances of a successful play Kickstarter, the goal should remain below $5,000.
2. If the campaign will be a more costly production, the next optimal goal range would be $35,000 to $44,999.
3. The goal range to absolutely avoid would be anything greater than $45,000 because this range had the highest percentage of failed campaigns.

### Limitations of the Dataset

Some limitations of the dataset are the timeframe this data was pulled from, that being 2014 to 2016. Since seven years have passed since the earliest data from this dataset was collected, it is quite possible that data from more recent years could show very different trends. The data also only ranges the span of two years, limiting the accuracy of the conclusions drawn from this analysis. If data was pulled from, say, the years 2019 to 2021, the data would be heavily skewed by the impact the COVID-19 pandemic had on the world. As such, it would be best to analyze a larger timeframe in order to level out any possible biases in the data.

Another limitation is the breakdown of categories. In the analysis of Outcomes Based on Goals for play Kickstarter campaigns, we saw that play campaigns with goals of $35,000 to $44,999 had the third highest success rate of 67%. This was a very specific goal range, but our conclusions were limited to the broad subcategory of "plays," so we couldn't perform an even deeper analysis of what kind of plays, specifically, succeeeded in this goal range. More in-depth insights could be analyzed if a sub-subcategory for types of plays could be pulled from the Kickstarter data.

### Other Possible Tables/Graphs

An example of another possible table and graph we could create are Outcomes Based on Goals for plays in Great Britain versus the US to find trends from the two countries separately. Similarly, we could create a table and graph for Theatre Outcomes Based on Launch Date for theatre campaigns in Great Britain versus the US to see if there are any differences in trends. Other examples of tables and graphs we could create would be for Outcomes of Parent Categories by country, Outcomes of Subcategories by country, Outcomes Based on Percentage Funded, or Outcomes Based on Average Donation.

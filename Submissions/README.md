# Kickstarting with Excel

## Overview of Project

### Purpose
The goal of this report is to help Louise understand how is the fundraising campaign for Fever performing when compared with other similar Kickstarter campaigns of the past

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

The following chart demonstrates the number of campaigns that were either successful, failed or canceled in the theater category in relation to the month they were launched. In order to conduct this analysis, I split the data in Category & Subcategory into two separate columns: 'Parent Category' and 'Sub-Category'. I used Pivot table in excel to group the data by 'Parent Category - Theater'. I used the line chart functionality in excel to visualize the relationship between outcomes and launch month.

<img src="/Resources/Theater_Outcomes_vs_Launch.png" >

### Analysis of Outcomes Based on Goals

The following chart shows the percentage of campaigns that were either successful, failed or canceled in the theater category in relation to the fundraising goals. To obtain the numbers of Successful, Failed and Canceled campaigns by fundraising goal dollar-amount ranges, I used the COUNTIF function. An example of my code to get number of successful campaigns that has dollar-amount range between 1000 and 4999 is:"=COUNTIFS(Kickstarter!$D:$D,">=1000",Kickstarter!$D:$D,"<5000", Kickstarter!$F:$F,"=successful")". I used the "SUM" function to obtain the total number of campaigns in each dollar-amount range, which I used to calculate percentage of successful, failed and canceled campaigns. I then used the line chart to visualize the relationship between the goal-amount ranges and the percentage of successful, failed, or canceled campaigns.

<img src="/Resources/Outcomes_vs_Goals.png" >

### Challenges and Difficulties Encountered

* When I copied the COUNTIF code for successful campaigns over to get the numbers of failed and canceled campaigns, I did not lock the cells in the formula, which resulted in incorrect data or error. 
* It is also very easy to make a typographical error while establishing dollar-amount ranges in the formula. I made a few such mistakes and as result the number of total projects did not add up to the numbers of projects in the Kickstarter sheet.
* For the Outcome based on Launch Date analysis: some students also encountered difficulties in grouping the "Row Labels" column to show just the months of the year. It took me a few attempts to figure it out as well.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
    1. The number of successful campaigns jump significantly from April to May. While the number of failed campaigns also increase slightly from April to May, the percentage of successful campaigns launched during that month is the highest at 67%. Generally, campaigns launched during early spring to summer months (April to August) have higher chances of succeeding. 
    2. Percentage of successful campaigns drop significantly during the month of December to 49%. Generally, campaigns launched during late Fall and winter months (October to January) have lower chances of being successful.

- What can you conclude about the Outcomes based on Goals?
    1. Campaigns with lower dollar amount goals have higher chances of succeeding. As the goal amount goes up the likelihood of campaign being successful goes down. However, the success rate improves a bit for dollar-amount range between 35,000 and 45,000.
    2. Over one third of the campaigns had dollar-amount range between 1000-4999. They had relatively good success rate.
    3. Projects with higher dollar amount goal get canceled at a higher rate.

- What are some limitations of this dataset?
    1. It only represents online campaigns that too just one website
    2. There is not enough data for some of the parameters e.g. category, country etc.
    3. The subcategories still group the data at a very high level e.g. it would have been nice to be able to analyze data by genre.

- What are some other possible tables and/or graphs that we could create?
    1. We could analyze the relationship between the success rate of campaign and the duration for which the campaign is active
    2. We could analyze the percentage of projects in relation to dollar-amount to understand what is the "sweet spot" for fundraising on Kickstarter
    3. We could visualize the relationship between years and percentage of successful projects to understand any potential trends
    4. We could visualize the data by country to see if one category or subcategory performs better in a specific country
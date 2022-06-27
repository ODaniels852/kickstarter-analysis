# An Analysis of Kickstarter Campaigns

## Overview of Project
An up-and-coming playwright, Louise, recently started a crowdfunding campaign to help fund her US play, Fever. She previously requested my assistance in analyzing crowdfunding data to determine whether there are specific factors that make a project's campaign successful. After receiving my findings and suggestions Louise began her campaign, which has come close to its fundraising goal in a short amount of time. 

### Purpose
Louise has once again sought my assistance in determining how different campaigns fared in relation to their launch dates and their funding goals. Therefore, I have been tasked with visualizing campaign outcomes based on their launch dates and their funding goals. 

## Analysis and Challenges
My analysis involved the review Kickstarter crowdfunding data for 4114 campaigns. Data was originally represented with parent and subcategory classifications combined; I added additional columns and separated these categories to allow for more detailed analysis of data most relevant to Louise’s campaign.
Additionally, within the dataset provided, campaign launch dates were represented in Unix timestamps that were not easy to read making visualizing campaign outcomes based on their launch dates more challenging. Therefore, an additional column was added to convert these timestamps to an easily understood short date format.

### Analysis of Outcomes Based on Launch Date
Data was summarized in a Pivot table to allow for easy review of outcome data. With the use of a filter on the parent category, I was able to isolate review of only theater campaigns. Also, data was organized by month and outcomes were sorted in descending order revealing the following:

- In the theater category, the majority (61%) of campaigns were successful.
- In the theater category, the campaigns launched in the months of May and June experienced the most success. While campaigns in July also performed well, there’s a steady decline for the remainder of the year.
- In the theater category, failed campaigns didn’t appear to be influenced as much by launch date as no months greatly stood out from the rest; the number of failures was relatively steady throughout the year. This indicated that other factors may have been larger influences on campaign failure.
- In the theater category, canceled campaigns also didn’t appear to be influenced much by launch date. Not only did canceled campaigns represent only about 3% of theater campaigns in total, but the number of canceled campaigns was relatively steady throughout the year.

Analysis results have been visualized in the line chart below:

<picture>
 <source media="(prefers-color-scheme: light)" srcset="https://github.com/ODaniels852/kickstarter-analysis/raw/main/Resources/Theater_Outcomes_vs_Launch.png">
 <img alt=" Shows a line chart displaying outcomes for theater campaigns by launch date."/>
</picture> 


### Analysis of Outcomes Based on Goals

A new table was created to summarize the total number of plays by outcome and by goal range. A total of 12 goal ranges were included and only Successful, Failed and Canceled outcomes were included. The percentage of successful, failed, and canceled projects was then calculated for each goal range. Data was summarized in a line chart to allow for easy review of outcomes based on goals. Review of this visualized revealed the following:

- There is an inverse relationship between Successful play campaigns and Failed play campaigns when reviewing outcome percentages by goal amount; except in the goal ranges between $5000 to $25000, in which outcomes were relatively close. 
- Most Successful play campaigns had contribution goals of between $1000 and $4999. However, most Failed play campaigns had contribution goals between $1000 and $4999. This indicated that goal amount alone wasn’t the only driver affecting campaign success
- The goal range that experienced the highest rate of success (76%) were those campaigns with goals of less than $1000. 
- Of the 17 play campaigns with goals over $45000, 15 campaigns failed; indicating that, while it may be possible to achieve success, the likelihood appears much less likely once the campaign goal exceeds $45000.

Analysis results have been visualized in the line chart below:

<picture>
 <source media="(prefers-color-scheme: light)" srcset="https://github.com/ODaniels852/kickstarter-analysis/raw/main/Resources/Outcomes_vs_Goals.png">
 <img alt=" Shows a line chart displaying percentage outcomes for play campaigns by goal range."/>
</picture> 


### Challenges and Difficulties Encountered

Initially, I had trouble while conducting the analysis of outcomes based on goals. Although, I was confident that I had correctly created the table required and accurately generated the associated line chart, I knew I did something wrong because my chart did not match the one depicted in the instructions. After reviewing the Deliverable 2 instructions a second time I realized that I accidentally excluded the ‘plays’ subcategory from my Countifs formulas in the table. Once I updated these formulas to accurately include this requirement and refreshed my chart, it matched the chart depicted in the Challenge instructions.


## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

  1. Campaigns have a higher likelihood of success if launched in the months of May and June.
  2. While launch dates in May and June are preferred, launch date alone isn’t enough to predict or indicate a successful campaign.


* What can you conclude about the Outcomes based on Goals?
    * Of the 694 Successful play campaigns, 529 campaigns had goals under $4999. When purely considering the highest likelihood of success a goal under $4999 is most preferable.
    * Campaigns with goals between $5000 and $24999 also appeared to be somewhat successful, but the chance of failure in this goal range is similarly likely, so this goal range is a bit riskier. 
    * The likelihood of this success drops for goals over $25000, so it may not be advantageous to have goals higher than this unless other factors mitigating failure are put into place.      


* What are some limitations of this dataset?
    * Review of outcomes by both launch dates and goals reveals that there are other factors we don’t have data for that are influencing whether campaigns are successful or not. While I can identify successful trends, failed campaigns have some commonalities with successful campaigns meaning that there are additional factors that may be larger drivers of the failed campaigns.
    * One additional piece of data that I believe would be helpful if obtained is the method advertising for each of the campaigns. This could potentially be a major driver of success or failure and could even help better understand if there are trends within the number of backers or average donation for each of the campaigns based on advertising. For example, campaigns advertised on social media may have had more backers and done better to achieve campaign goals than those campaigns advertised using flyers.


* What are some other possible tables and/or graphs that we could create?
    * Another possible table and graph we can create is one showing Outcomes based on Average Donations. The tab ‘Outcomes Based on Avg Donation’ has been added to the Kickstarter_Challenge workbook and the line chart created is pictured below. Analysis of this data reveals that for 72% of the 694 play campaigns the average donation was between $25.00 and $99.99. Additionally, 47% of the 353 failed play campaigns had average donations of $24.99 or less.
  
 
<picture>
 <source media="(prefers-color-scheme: light)" srcset="https://github.com/ODaniels852/kickstarter-analysis/raw/main/Resources/Outcomes_vs_AverageDonation.png">
 <img alt=" Shows a line chart displaying percentage outcomes for play campaigns by average donations."/>
</picture> 



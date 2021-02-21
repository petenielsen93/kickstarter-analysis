# Kickstarting with Excel

## Overview of Project
    We spent Module 1 working with data in Excel to help Louise, our fictional playwright, figure out the best way to launch her Kickstarter campaign. In this particular project, we are going to look at the analysis of campaign Outcomes based on Launch Date, and the analysis of Outcomes based on the financial goal.  

    ### Purpose
        The purpose of this analysis was to dig deeper on fundraising campaigns and how they fared in relation to their launch dates and funding goals. This project was started after Louise's play Fever came very close to it's fundraising goal, and further insight was desired on how often these goals were completed in relation to their launch dates and goals. 

## Analysis and Challenges
    The analysis was done in Excel, with data on the outcome of the theater production's launch date and on the size of the play's fundraising goal being the two main points of analysis. The first was done by creating a pivot table of the successful, failed, and cancelled theater production, and filtering by months. A line chart was created from this pivot table which led us to conduct our analysis. The latter point of analysis was done by creating our own parameters for the play's fundraising goals. Once they were created, we broke down the campaigns into their groups based on those parameters using the countifs function and filtering by the play's outcome (successful, failed, cancelled), fundraising goal, and subcategory of campaign (our choice being 'plays').
    
    There were not many significant challenges for myself with this analysis, but I did run into a snag with the countifs function when I did not include the "=" in the formula when filtering by fundraising goal (for example '=countifs(Kickstarter!$D:$D,>=4999)). When I created my chart, it did not look like the finished product, so I spent about 5-10 min looking over my data before I realized my error.
    
    
    ### Analysis of Outcomes Based on Launch Date
        After breaking down the successful, failed, and cancelled theater productions by month, and visualizing the data using a line chart, we were able to discover that the timing of the launch date of these campaigns has a significant impact on their success. Campaigns that launched in the month of May were the most successful, with the months June, July, August and April respectively being the next best months.  It appears that when these campaigns begin in the summer, they are more likely to end up successful. As to why this is so, further analysis is needed. As to the failed and cancelled theater productions, there was no significant timing that contributed to its failure or cancelation. See the chart below for more. 

        ![](2021-02-21-16-02-09.png)

    ### Analysis of Outcomes Based on Goals
        In this part, we wanted to gather data on the amount and percentage of Successful, Failed, and Cancelled campaigns and compare them with their financial goals. To analyze the outcomes based on goals, we first broke down the campaign goal amounts into ranges, with the first range being campaigns who's goal was less that $1000. The next range was equal to or greater than $1000 to $4999, equal to or greater than $5000 to $9999, and continued in that pattern until reaching the final range of greater than $50,000. We then developed a COUNTIFS function to find the specific type of outcome we desired: the outcome of the Kickstarter campaign, the amount of the campaign goal, and the subcategory "play". This allowed us to calculate the number of Successful, Failed, and Cancelled campaigns for plays and categorize them into our goal ranges. We could then calculate the percentage of each campaign outcome for the goal range, and we used that info to create the below chart. 

        ![](2021-02-21-16-01-41.png)

        This took a bit more analysis than the launch dates. It makes sense that the smaller the goal amount, the more likely it is to be successful. Around the $15,000 - $19,999 range, is where the failures become more common than the successes. However, from the $35,000 - $39,999 to the $40,000 - $44,999 range, the successes begin to outweigh the failures again. The failures take over for the rest of the ranges. Looking back at the raw data on my Excel sheet, I can see that for the $35,000 - $39,999 range, there was a total of 6 campaigns, with 4 successes. In the $40,000 - $44,999 range, there are three total campaigns with two of them being successful. Due to the small number of plays in these higher ranges, the successful campaigns should be considered outliers. There are a total number of 1047 projects in this data set, with 985 of the campaigns having a goal less than $20,000. Any successful campaign with a goal of more than $20,000 should be considered an outlier.

    ### Challenges and Difficulties Encountered
        Like I mentioned earlier, the only major challenge I had with the project was the syntax when creating the COUNTIFS function. I have previous experience with Excel so my familiarity in the platform was very helpful. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

    The first major conclusion we can draw about the Outcomes based on Launch Date is that May is the most successful month, followed closely by June and the rest of the summer months. I wish I could come to a conclusion about why these months are the most successful for theater campaigns, but the lack of additional data and my lack of knowledge of the theater world does not allow me to draw any more definite conclusions. (Do play's have a season in which they are produced or conducted? Are May/June popular months for all types of Kickstarter campaigns?)

    The second major conclusion we can draw is that there are more successes than failures, no matter the month. If you look at the totals in our raw data, there are 839 successful theater campaigns, while 493 have failed. That means that 61% of theater campaigns are successful. We can safely assume that because these are Kickstarter campaigns, that they are small scale productions. Taking from our Outcomes Based on Goals analysis, we know that the smaller the goal, the more likely to be successful. So we can draw the conclusion that you are likely to be successful when starting a campaign. (Make sure to launch in May for a higher probability of success!)

- What can you conclude about the Outcomes based on Goals?

    The major conclusion we can take from the Outcomes based on Goals section is that the smaller the goal, the more likely it is to succeed. It is common sense that a smaller number is a more attainable number. A campaign that requests funds of $1000 is of course more likely to succeed than a campaign that requests $10,000. From the data, it appears that around the $5000 dollar mark, the gap between successful and failed campaigns decreases, with failures eventually taking over successes at the $15,000 mark. Of course they cross again twice when the outliers are present, but without those, it would be clear that small campaigns tend to be more successful. 

- What are some limitations of this dataset?

    The first limitation of this dataset would be that it does not include data for how the campaigns marketed their goal. What are they using the money for specifically? How much of the total would be broken down into the various parts of production? I would specifically like to know this when it comes to the failures. Were they asking for too much? Did they not describe how the funds would be used? 

    Another limitation is that Kickstarter campaigns are a relatively new phenomenon. There have been fundraising campaigns for decades prior, but the earliest data we have here is only from 2009, and the earliest on plays coming from 2010. If the data set was larger, by including fundraising campaign from the past, or campaigns from a different fundraising source, we would be able to be more certain in our conclusions.

- What are some other possible tables and/or graphs that we could create?

    I think an important factor in these campaigns that we did not discuss is the length of time these campaigns were up. Maybe some failed campaigns could have succeeded with more time. Maybe some successful campaigns would have failed if they had been cut short. This all depends on their financial goals as well, so I would love to see the relationship between financial goal, outcome, and length of the campaign. 

    I would also like to use the backers count part of the data. I can hypothesize that the bigger campaigns probably had more backers, but I would be interested to see if there were any outliers when it came to this data. 
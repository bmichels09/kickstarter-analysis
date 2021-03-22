# Kickstarting with Excel

## Overview of Project

### Purpose
The purpose of this analysis is to find how successful Kickstarter campaigns are based on their launch dates and funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
This analysis was done in a pivot table, using the Outcomes and Date Created Conversion columns in the dataset.  Only campaigns with a parent category of "theater" were used, and live campaigns were filtered out as they don't have a result yet.  The pivot table shows the number of successful, failed, and canceled campaigns started in each month.

When graphed, the results look like this:
![Theater Outcomes by Launch Date](/resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
This analysis was done by grouping the campaigns into 12 different categories based on the funding goal.  For each one, I used the COUNTIFS() function to find the number and percentage of successful, failed, and canceled campaigns within each category.  I only counted campaigns with a subcategory of "plays", to make the analysis more relevant to Louise's campaign.

When graphed, the results look like this:
![Outcomes Based on Goals](/resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
For the Outcomes Based on Launch Date analysis, it was a bit tricky to separate the Date Created Conversion field into months.  I tried removing the Years and Quarters fields from the pivot table's rows, leaving just Date Created Conversion, and that ended up doing what I was looking for.

For the Outcomes Based on Goals analysis, the main challenge was the COUNTIFS() function.  I'm not familiar with the function, and filling out the new data table required a lot of manually editing formulas.  As a check to see if I did everything correctly, I compared the total number of campaigns in the new data table with the number of campaigns in the subcategory "plays" in the original dataset (minus the live ones).  The totals matched, so I feel pretty confident that the new data table is correct.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
  - Campaigns are most likely to be successful when started in May, June, or July.  Campaigns are least likely to be successful when started in December.

- What can you conclude about the Outcomes based on Goals?
  - Campaigns with smaller goals are more likely to be successful.

- What are some limitations of this dataset?
  - None of the campaigns in the "plays" subcategory were canceled, which could mean there are issues with the dataset or could be an expected quirk with how Kickstarter works.  Also, the "plays" subcategory has different kinds of campaigns.  Some are new plays, some are performances of existing plays, and some are for theaters where plays will be performed.  Being able to look at just the new plays might provide better insight.

- What are some other possible tables and/or graphs that we could create?
  - We could create the same graphs, but filtered to include only US campaigns, or we could have a graph of successful/failed/canceled campaigns started in each year.

# Kickstarting with Excel

## Overview of Project

### Purpose

The puropose of this analysis is to show how the different Theater kickstarters compared to each other based on their launch dates and  how the different Plays matched up to each other based on their funding goals.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

To perform the analysis of outcoms based on launch date, I had to first add a new column, "Years", to the Kickstarter worksheeet. This column pulled the years from the "Date Created Conversion" column using the year() function. I then created a pivot table from the Kickstarter worksheet, filtering using the Parent Category, showing only Theater, and Years, showing all years. I set the columns to show outcomes and the rows to show the Months from the "Date Created Conversion field". I also counted the outcomes by moving outcomes to the Values area. Finally, to visualize the data within the pivot table I created a pivot chart titled [Theater Outcomes Based on Launch Date](https://github.com/kellyd7/kickstart-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png).

### Analysis of Outcomes Based on Goals

To perform the analysis of outcomes based on goals, I had to first filter the Kickstarter worksheet to only show plays. I then created a new worksheet titled "Outcomes Based on Goals" with the following columns:

	Goal
	Number Successful
	Number Failed
	Number Canceled
	Total Projects
	Percentage Successful
	Percentage Failed
	Percentage Canceled

And with the following rows listed under the "Goal" column:

	Less than 1000
	1000 to 4999
	5000 to 9999
	10000 to 14999
	15000 to 19999
	20000 to 24999
	25000 to 29999
	30000 to 34999
	35000 to 39999
	40000 to 44999
	45000 to 49999
	Greater than 50000

I then used the countifs() function to populate the "Number Successful," "Number Failed," and "Number Canceled" columns, based on the project "outcome," the "goal" amount using the goal ranges shown above. Next, I used the sum() function to populate the total number of projects in the "Total project" column. Finally, I calculated the "Percentage Successful" by dividing "Number Successful" column by the "Total Projects". I repeated this calculation for the "Percentage Failed" and "Percentage Canceled" columns by using the "Number Failed" and "Number Canceled" columns respectively. To visualize this data, I highlighted the completed table and inserted a line chart titled, [Outcomes based on Goal](https://github.com/kellyd7/kickstart-analysis/blob/main/Resources/Outcomes_vs_Goals.png).


### Challenges and Difficulties Encountered

One possilbe challege to note here is during the analysis of Outcomes Based on Launch Date, it is important to know how to filter the column within the pivot table to only show "Succesful", "failed", and "canceled" outcomes and also sorting them Z to A so that "Successful" outcomes are listed first. If this step is done incorrectly or missed, then our analysis will be misleading.

Another challenge to note is understanding how to use the countifs() function. Using the help option within excel to understand how to use this function was huge in populating the correct information in "Outcomes Based on Goals" worksheet.


## Results

Two conclusion that can be drawn about the Outcomes based on Launch date is that: 

1.	The most success in Theater campaigns was experience between May and June.
2.	No campaigns were cancelled in the month of October for all years reported.

A conclusion that can be made about the Outcomes based on Goals is that the probability of a campaign being successful is higher when the Goal is less than 1000 dollars.

One key limitation to highlight is that the analysis performed doesn't account for the currency used. I say this because some campaigns were funded using Great Britain pounds, US Dollars, Euros and more. So,taking into account the currency exchange may bring about different results in our analysis. 

But, looking at the kickstarter worksheet, we could create a pivot table to show the outcomes by backer count. This will help us understand the effect backer count has on the success of the campaign.

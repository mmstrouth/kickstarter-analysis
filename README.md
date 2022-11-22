# Kickstarting with Excel

## Overview of Project
Louise, an up-and-coming playwright, was initially interested in launching a kickstarter campaign to fund her play, Fever. She was provided with an initial analysis based on Kickstarter data that provided insight into specific factors that could make her campaign more successful. After launching her campaign and coming close to her fundraising goal, she has requested further analysis.

### Purpose
The purpose of this additional analysis is to provide Louise with insight into the success of different theater campaigns, relative to their launch date, as well as the funding goals and outcomes of Kickstarter campaigns for plays. 

## Analysis and Challenges
Using the Kickstarter dataset, two overall analyses were conducted. The first analysis via pivot table and line graph looks at outcomes of theater campaigns by the month they were launched. The second analysis provides insight into the outcomes of Kickstarter campaigns, specifically plays like Louise’s campaign, broken down by ranges of the goal amount and their outcomes, also via pivot table and line graph.  

### Analysis of Outcomes Based on Launch Date
To perform the analysis of Outcomes Based on Launch date, I ensured the following columns were created: Parent Category, Date Created Conversion, and Years. I then inserted a PivotTable, filtering for years and parent category. The columns reflected the possible outcomes, while each row displayed the month of the launch date and the subsequent counts for each outcome in that month. I then chose Theater as the parent category. To create the chart, I used PivotChart under the PivotTable Analyze menu. I selected the appropriate line graph and added labels for the axes. I copied the chart to the Google Drawings application where I cropped it and downloaded it as a png file. 

![This is an image](https://github.com/mmstrouth/kickstarter-analysis/blob/9fd334dcfdba89573f19830110244dddede0632b/Theater_Outcomes_PivotTable.png)

![This is an image](https://github.com/mmstrouth/kickstarter-analysis/blob/eea25568d67e6824a6c234b3de216bcb1f9cb4e3/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
To perform the analysis of Outcomes Based on Goals, I set up a new sheet with the following column headers: goals, number successful, number failed, number canceled, total projects, percentage successful, percentage failed, and percentage canceled. I also typed in all the provided goal ranges in the first column. I began with cell B2 and ensured that the criteria were all correct in order to account for the goal range, type of subcategory of plays, and the outcome. I used absolute reference ($) and dragged the formulas to the right in the row and down the column, updating the relevant criteria. To find the total projects, I used the SUM function and summed the prior three columns. The percentage successful was found by using the IFERROR function to account for possible errors when dividing by zero and then dividing the outcome total by total projects. I changed the cell format to % and then dragged the formula down the column. I repeated this process for percentage failed and percentage canceled. To create the chart, I highlighted the relative columns holding the Ctrl key and inserted a line chart. I added the labels to the axes and stretched it out horizontally so that the goal ranges were easy to read. I copied the chart to the Google Drawings application where I cropped it and downloaded it as a png file. 

![This is an image](https://github.com/mmstrouth/kickstarter-analysis/blob/f8250f06bfd2e8f715e878037499dea9d3ad24a0/Outcomes_Formula_example.png)
 
![This is an image](https://github.com/mmstrouth/kickstarter-analysis/blob/6c8563fd7da360ad71d9fd3756dc15c1a040f9be/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
Outcomes Based on Goal was the most challenging analysis because it involved multiple criteria within the COUNTIFS, due to the ranges themselves, as well as the focus on the outcome and specific subcategory of plays. Due to the nature of the argument, it could not be easily replicated in all the subsequent rows and columns. I began with Cell B2 and dragged it to the right to fill the cells for number failed and number canceled. I had to repeat the process after I realized that the columns I was referencing were changing, so I added the absolute reference with dollar signs to the column names. This allowed me to drag it to the right and just change the outcome, instead of retyping. Similarly, I dragged down the column for number of success and changed the criteria, relative to the goal range. This also saved time. I did mistype some of the criteria in the formula and did not realize until I compared the line chart to the one provided. Of course, I was reminded to use the IFERROR function when I saw the challenge presented with dividing by zeros and quickly corrected the formula to address the error. 


## Results
### Theater Outcomes Based on Launch Date Conclusions
According to the line chart titled Theater Outcomes Based on Launch Date, the month of May saw a peak in successful theater kickstarter campaigns with 111 out of the total of 166 that month (a month-based success rate of 67% which also beats the overall rate of successfully funded campaigns of 61%). While May also has the most number of failing campaigns, the percentage of failing campaigns that month was only 31%, below the overall failure rate of 36%. December appears to have the lowest number of campaigns launched, and importantly, the data reveal a nearly even likelihood of succeeding or failing if a campaign is launched that month. 

### Outcomes Based on Goals Conclusions
According to the line chart titled Outcomes Based on Goal, Kickstarter campaigns to fund plays with goals of less than $1000 were most successful with a success rate of 76%. However, one cannot make the general observation that a smaller goal is always better, as the line chart shows that while the percentage of success decreases as the goal increases, this trend reverses itself when the goal reaches $35,000 to $44,999. Importantly, Louise initially estimated a budget of over $10,000 and the percentage of success for the $10,000 to $14,999 range was only 54%. 

### Limitations
The Kickstarter dataset presents some limitations; primarily, the most recent data is from 2017. Since that year, the COVID-19 pandemic has changed the landscape of many aspects of our lives which may have changed the outlook for funding Kickstarter campaigns for live theater. However, more than ever in history, Kickstarter campaigns can be easily shared and spread electronically, possibly leading to additional funding opportunities from more individual donors. 

### Recommendations for Additional Analysis
With Louise’s goal in mind, further analyses could be pursued. To provide additional insight into theater outcomes by their launch date, a table showing the percentage of each outcome could be calculated and then displayed with a side-by-side bar graph that reflects the percentage of each outcome, in addition to the initial line chart depicting raw counts shown above. 

![This is an image](https://github.com/mmstrouth/kickstarter-analysis/blob/23ce8e0d2d78b989cd30a57e92c5c459528e490d/Theater_Outcomes_Percent.png)

When investigating outcomes based on goal ranges for Kickstarter campaigns for plays, a stacked bar graph could provide an additional visual of the percentage of campaigns that succeeded and failed per goal range. 

![This is an image](https://github.com/mmstrouth/kickstarter-analysis/blob/938854a1cb8dcf5a42c71563691e715f3f05670c/Outcomes_vs_Goals_bar.png)

Since Louise is interested in relative success related to launch date, finding the average length of successful theater, or specifically play, campaigns may be an analysis worth pursuing since she came close to her fundraising goal in a short amount of time. An analysis could provide insight into how her experience compared to other campaigns like hers. 

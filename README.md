# Kickstarting with Excel

## Overview of Project
Louise is an up-and-coming playwright and is eager to produce her play, "Fever". To do so, she needs to raise $10,000 to cover the production expenses. She is interested in launching a crowdfunding campaign to successfully raise the funds and wants to learn from other fundraising campaigns. 

### Purpose
The purpose of this assessment is to determine if there are ways that Louise can optimize her crowdfunding campaign. To inform this project, data on past crowdfunding campaigns was analyzed. Particular focus for this analysis was on theater campaigns as well as data specifically for plays. Campaign outcomes were compared by campaign launch dates as well as crowdfunding financial goal. 

## Analysis and Challenges
Analysis was done using a sample of 4,114 kickstarter campaigns and related data metrics and information. This information was analyzed to provide Louise with insight into what time of year best predicted a successful campaign and at what fundraising level.


### Analysis of Outcomes Based on Launch Date
To determine if time of year influenced the outcome of other theater kickstarter campaigns, the analysis started with converting the Unix timestamp variable [launched_at] to a calendar date using a date conversion formula. This new variable [Date Created Conversion] was further refined to only list the year of the campaign using the Year formula in Excel. 

A pivot table was created to compare campaign outcomes by date. Data was filtered to specifically include theater kickstarter campaigns and then, displayed to show campaign outcomes (count by each outcome category) by date (displayed by calendar months) to visually compare outcomes by month in which the campaign was launched.  

### Analysis of Outcomes Based on Goals
The second analysis compared past kickstarter campaigns and their fundraising goals to their ultimate outcome (i.e., successful, failed, canceled). To do this, dollar-amount ranges were created to group campaigns by their fundraising goals to help simplify interpretation of results. The COUNTIFS function was used to categorize campaigns by outcomes into each fundraising goal range. This resulted in a table displaying the number of campaigns falling into each outcome category by funding goal range. The outcomes were then added together using the SUM function by each funding goal range. For visual interpretation, outcome by funded range categories were displayed in a line chart.

### Challenges and Difficulties Encountered
The challenges presented were relatively simple to overcome. For the 'Outcomes Based on Launch' analysis, it took time to realize that 'Field Buttons' in the Pivot Table toolbar could be modified in order to remove the filters from the graph. It took me some time to figure out how to do this and mirror the graph presented with the Challenge instructions.   

Without the clear instruction to convert a Unix timestamp to date, I would have been greatly challenged to figure out how to do this and that it was even possible to do such a conversion with a random string of numbers.  

Writing the COUNTIF formulas for the 'Outcomes Based on Goal' was challenging for me. I had trouble copying the formula properly from cell to cell. I also thought there must be a trick to quickly add the $ to hold cells for formulas and was frustrated that I was doing it manually. I'd be excited to learn the trick for this - F4 did not work for me!

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
Based on this sample, the majority of successful campaigns were launched in May. The number of successful campaigns launched is lowest in December. 
The number of failed campaigns is fairly consistent across the year. However, as the majority of campaigns (regardless of outcome but by sheer volume of campaigns) are launched in May, May also yields the highest number of failed campaigns. 

- What can you conclude about the Outcomes based on Goals?
The highest percentage of successful kickstarter campaigns for plays is at the lowest funding goal range (<$1000) at 76% followed by the much higher funding goal ranges of $35,000 to $39,999 and $40,000 to $44,999 both with 67% success. It is striking to see that the percentage of successful campaigns decreases significantly as the funding levels increase beyond $45,000. 

Kickstarter campaigns for plays at the funding range of $25,000 to $29,000 as well as >$45,000 resulted in the greatest percentages of failures.

In conclusion, it appears that based on funding goals that your success decreases as your funding goal increases until you reach the $25,000 level at which point, the percentage of successful campaings increases until dropping off again at the $45,000 range.

- What are some limitations of this dataset?

Limitations of this dataset include other factors that might influence outcomes that are not included in this set. These might include things like how (and if) the campaigns were advertised and promoted and comparing the influence of these efforts on campaign success. Another hypothetical impact on a campaign's outcome could be whether the location was well-suited or well-known for the ultimate theater/play event -  perhaps a kickstarter campaign for a play in a remote location would be less successful than a popular theater in an urban center that recently lost federal support for the arts. This dataset doesn't provide this level of granularity.

- What are some other possible tables and/or graphs that we could create?
We could create graphs to compare campaign outcomes by country. It would be interesting to create a table or graph showing what types of campaigns (parent category) are most successful in each country and to see if funding goals varied across categories across the globe.
Once could also assess when the majority of campaigns were launched/created and see if there was a relationship to economic downturns or other similar measures where things like theater or the arts may have received less support.

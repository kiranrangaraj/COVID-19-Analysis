# COVID-19: An Examination of Data Accuracy and the Effectiveness of Local Mandates and Testing on Preventing Transmission
Kiran Rangaraj, Emily Keymon and Reginald Malden

An analysis of the accuracy of three COVID-19 data sources, in addition to how COVID-19 count in six US states changed in regard to the percentage of the population being tested, as well as the state and local government mandates in effect during the reopening phases. Data was initially pulled from health department, county, and state CSV datafiles and filtered into a dataset that contained the six states. 

## Data Comparison of the Following US States:
* Florida
* Georgia
* Texas

* New York
* New Jersey
* Connecticut

## Why Did We Pick These Specific States?
*All state data as of 7/22/20

* We chose New York, New Jersey and Connecticut because the governors of these states took collective measures to contain COVID-19 within their region of the United States. Consequently, their shutdown dates are within a days of each other. They also approached the progressive reopening of their states with similar degrees of restrictions on businesses and the public.
* The other three states we chose were Florida, Georgia and Texas. Though they each had similar shutdown dates as the other three states, the governors imposed significantly less mandates on the public and businesses during the phases of reopening. 
* The comparison of these two groups of states allows an examination into the effectiveness of certain mandates on containing COVID-19 spread.  

## State Statistics:
* Florida was #2 in the total positive cases counts. Florida's cases starting increasing to over 1,000 per day on 6/6/20.  The largest daily spike so far occurred on 7/12/20 at 15,135.  The 7-day average is currently 11,006.  
* Georgia was #8 on the list.  The largest daily spike occurred on 7/18/20 at 4,689 cases per day.  Current 7-day average is 3,495 cases per day.
* Texas was #3 on the list.  Texas started seeing daily cases over 1,000 starting 5/5/20.  The largest daily spike so far occurred on 7/17/20 at 14,916 cases per day.  The 7-day average is currently 9,893.
* New York was #4 on the list.  The largest daily spike occurred on 4/10/20 at 8,593 cases per day.  The current 7-day average is 200 new cases per day.
* New Jersey was #6  on the list.  The largest daily spike occurred on 4/3/20 at 4,305 cases per day.  The current 7-day average is 324 new cases per day.
* Connecticut was #26 in total positive case counts.  Connecticut's largest spike occurred on 4/22/20 at 2,109 cases per day.  The 7-day average is currently 84.

## Analysis Questions and Answers:
### How do the three data sets compare?  Do they reveal either consistencies or inconsistencies?
* To answer this aspect of our analysis, we produced a line plot using each of the three different data sources. The line plots examine date versus total Covid-19 cases in the 6 states. We then compared the plots to see if there were any descrepancies in the data.
* The three data sets selected for this analysis proved to be staistically significantly similar.  The histogram showed the data sets overlayed each other indicating the data sets are similar.  For further analysis, a t-test was performed.  This resulted in t-scores with p-values larger than .05.  Therefore, the difference found is not statistically significanlty different.

### What % of population was tested and how much does testing vary from state to state? Do the testing percentages correlate to COVID-19 count?
* To examine these aspects of the data, we compared the state populations in a histogram and then plotted the percentage of each states population that was tested over time. We then ran a linear regression to see how closely the average testing percentage of each state correlates to the average daily Covid-19 count.
* The correlation coefficient between testing percentages and COVID-19 count was only 0.12, which indicates there is no relationship between the two variables. This is also demonstrated in the scatter plot where the data points are spread all over rather than being clustered in a linear fashion. The r-squared value of 0.0136 indicates that only 1.36% of the movements of daily COVID-19 count (dependent variable) are explained by the movements in the testing percentage (independent variable). Thus, there is no relationship between the two at all.

### Did the state shutdown and reopening timings of these six states impact the daily new COVID-19 cases? Did the reopening of specific businesses in certain states cause COVID-19 transmission to skyrocket?
* To approach this objective, we manipulated the data from source 1 to show new daily Covid-19 cases rather than total cases. We then created line graphs of date versus new daily counts. We then looked at the line graphs to see if there were any trends and considered these trends against state mandates or reopening phases that were being implemented at the time. Each states new daily counts was plotted separately and then examined in relation to the state mandates in effect at the time.
* There appeared to be two different trends in the states data. Florida, Georgia, and Texas have spikes in daily Covid-19 counts from June onwards, whereas New York, New Jersey, and Connecticut have progressively lower daily counts in the same time frame.

Independent T-Test - (statistic = 12.73767146105426, pvalue = 2.9448198049160806e-25)
* Here we examine whether there is a statistically significant difference in average new daily Covid-19 cases of states that reopened bars, nightclubs, recreational venues, and laxed restaurant dine-in restrictions verses states that did not reopen under such parameters during the same time frame.
* Sample 1 includes Florida, Georgia, and Texas. Since these 3 states implemented similar reopening guidelines on June 5th, June 1st, and May 22nd, respectively, we considered daily new Covid-19 cases from June 1st through July 17th.
* Sample 2 includes New York, New Jersey, and Connecticut, all of which did not have such reopening guidelines.
* By running an independent t-test we will compare the means of the 2 independent populations and will be able to see any statistical significant differences between the 2.
* The means generated for the 2 groups are noticeably different from each other. Group 1 had, on average, 4273 daily new cases of Covid-19 versus the 401 of group 2.
* The t-test produced a p-value that is significantly smaller than 0.05, which indicates that the differences between the average COVID-19 daily cases in the two state groups is statistically significant. This indicates that the reopening of bars, nightclubs, recreational venues, and lax restaurant dine-in policies significantly contributed to higher transmissions of COVID-19.

ANOVA - (statistic = 58.26540963214147, pvalue = 3.0112022192395693e-41)
* We then examined whether any of the 6 states was statistically signifcant.
* We were able to establish that the policies in the 2 groups of states had a profound impact on Covid-19 count, however we did not consider if any of 6 the states was significantly different than the others.
* Creating a boxplot helps to visualize how the states compare in terms of daily new Covid-19 case distribution, the central values, and the variability.
* Florida, Georgia and Texas have much higher daily Covid-19 counts than Connecticut, New Jersey, and New York. The daily Covid-19 highest and lowest values of Florida, Georgia and Texas are both higher than Connecticut, New Jersey, and New York in the corresponding values. These 3 states also have a median Covid-19 count that is higher than the other 3 states, and they also have an immensely larger interquartile range.
* These results suggest that Florida, Georgia, and Texas are consistently experiencing higher Covid-19 counts than Connecticut, New Jersey, and New York. The higher variances in these 3 states also suggests that they experienced much larger fluctuations in the daily Covid-19 counts between June 1st and July 17th.
* A significance level of 0.05 indicates a 5% risk of concluding that a difference exists when there is no actual difference. Since the p-value here is drastically lower than the significance level, we have rejected the null hypothesis with no risk and concluded that not all of the 6 states Covid-19 means are equal.


## References:
* https://covidtracking.com/data/download
* https://www.kaggle.com/fireballbyedimyrnmom/us-counties-covid-19-dataset?select=us-counties.csv
* https://raw.githubusercontent.com/nytimes/covid-19-data/master/us-states.csv
* https://www.kaggle.com/headsortails/covid19-us-county-jhu-data-demographics/data?select=us_county.csv
* https://www.washingtonpost.com/graphics/2020/national/states-reopening-coronavirus-map/
* https://www.cdc.gov/covid-data-tracker/#cases

# **Pyber-Analysis**

### Introduction & Background
In this dataset, rideshare data was examined for the impact of city size (urban, suburban, and rural) on trends in total fares, total rides, number of drivers, average fare per number of rides, and average fare per number of drivers (2019). This resembles what a data analyst may encounter in the **Transportation Mobility as a Service** industry. Using Python, Jupyter Notebook, and the Matplotlib and Pandas modules, this analysis was a breeze. As a result I feel prepared to create intuitive dataframes and plots to best express specific trends with real world data.

### Method and Results
Using the Pandas library, I began by importing two .csv files, which I would combine and transform to create the dataframe below (city and ride data). Here I categorized the data into *city type* groups to best show the most important comparisons between city types.


<p align="center">
  <img width=auto height="150" src=analysis/By_Type_df_Summary.png>
  </p>
  
Here we observe that "urban" cities (large cities) have the most rides, the most drivers, and the highest total fares. Naturally, suburban cities follow, and after that is rural cities. One interesting thing to notice is that this trend flips with average fares per ride and average fares per driver.
Next, I reoriented the inital dataframe by grouping values by *date* and *city type*; this was not necessarily for presentation, but rather as a necessary step to plot the data later on. The regrouped, resampled, pivot-table-esque table is shown below:

<p align="center">
  <img width=auto height="500" src=analysis/Resampled_df.png>
  </p>
  
There is little to note here, as the fare values are difficult to compare in this format. But that's okay! It's just a step to creating a beautiful representation more pleasing for human eyes!  

Moreover, a business report would not be complete without a fiscal comparison. Using the previous pivot-table, a line-plot was created to better visualize and compare the impact of city-size over time. To do so, I made use of Pandas dataframes (to organize) and Matplotlib (to plot and format).

<p align="center">
  <img width=auto height="350" src=analysis/Fare_by_Type_Line.png>
  </p>

Here we can again see the vast difference in fares in each type of city. Average urban city fares are roughly 8-10x greater than average rural fares, and average suburban city fares are roughly 4x higher than average rural fares.

### Conclusions
For someone running a ride share business, larger cities will clearly offer the most revenue with the most riders, drivers, and highest fares. Some things not explicitly shown in the data are the relationship between larger cities and higher average incomes. Higher income may allow more financial flexibility to spend money on rides and to possibly not own a car. Also, tourism is one attraction that enables higher numbers of rides in larger cities. Travelers need transportation because city parking is terribly expensive, and flyers will not have cars to use anyway.

From the perspective of a driver, a goldilocks solution may be the play. Distance and travel-time data would be essential to draw any meaningful conclusion on this aspect of the business. However, I would bet that rider turnover takes longer in rural areas due to low-population density and low attraction count. If turnover is shorter, drivers can cram more rides into their evening, and the higher rates may prove to make them more money. But there's one more variable at play -> Higher driver numbers increase competition which reduces the average number of nightly rides per driver. So for drivers, a large suburban or small urban city is probably the sweet spot. I would need to create an optimization to test this with better data.

While that is all theoretical and unfounded, if the company is aware of this they would be wise to write an optimization of their own to determine what cut to take from drivers to maintain "fairness" between employees of all citiy types to increase employee retention, as well as which cities to incentivize driving / riding through discounts and other marketing.

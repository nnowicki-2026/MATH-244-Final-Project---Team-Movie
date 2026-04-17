# #MATH-244-Final-Project---Team-Movie
# Exploratory Data Analysis

Research Question: What factors contribute to a successful movie?
Success will be defined by the profitability and gross of the movie. 

Our outcome variable is going to be Profitability and WorldGross. High profitability will indicate that the movie made a lot of money with a small budget, and gross measures how much money the movie made in total. We are interested in measuring what factors contribute to a successful movie, and because profitability is a measure of (WorldGross/ Budget)*100, it will be able to explain how many times over the budget a movie earned in total revenue. This way, we can evaluate whether the budget of a movie is directly related to how much money it will make, and investigate the features of the highly profitable movies that are low-budget and high-return. When the profitability is above 100, it represents that the movie is making a profit. If not, then the movie suffered losses. From our dataset, we originally expected the movies with very high profitability to be the world-famous movies. However, we discovered that most of the movies with extremely high profitability are less well-known movies with extremely low budgets. For instance, there is a movie named Fireproof with a profitability of 6694.40, but this is due to its low budget of only 0.5 million dollars.

The explanatory variables will be TheatersOpenWeek, OpeningWeekend, BOAvgOpenWeekend, and Budget. TheatersOpenWeek measures how many theaters showed the movie during the open weekend. OpeningWeekend measures the performance of the movie in the first weekend. BOAvgOpenWeekend measures the average revenue per theater during the open weekend. 

# Table of Summary Statistics


| Variable | Minimum | Median | Mean | Maximum |
| :---- | :---- | :---- | :---- | :---- |
| Movie |  |  |  |  |
| LeadStudio |  |  |  |  |
| Rotten Tomatoes | 0 | 48 | 49.55 | 99 |
| AudienceScore | 19 | 61 | 60.68 | 96 |
| Story |  |  |  |  |
| Genre |  |  |  |  |
| Theaters OpenWeek | 2 | 2875 | 2729 | 4468 |
| Opening Weekend | 0.032 | 14.8 | 23.184 | 174.14 |
| BOAvg Weekend | 151 | 5947 | 8134 | 93230 |
| Domestic Gross | 0.36 | 44.67 | 74.91 | 760.5 |
| ForeignGross | 0.01 | 46.93 | 99.96 | 2021 |
| WorldGross | 1.52 | 91.4 | 174.74 | 2781.5 |
| Budget | 0.5 | 39 | 57.57 | 300 |
| Profitability | 15.25 | 254.32 | 371.73 | 6694.4 |
| OpenProfit | 0.34 | 36.9 | 59.65 | 1368 |
| Year | 2007 | 2009 | 2009 | 2013 |
| BOAvg Weekend(M) | 0.0001504 | 0.0059195 | 0.0081153 | 0.0925000 |


# Data Wrangling and Transformation

We performed the beginning of our data wrangling in Excel. First we had to make sure that all the variables that were in units of money were in millions of dollars, BOAvgOpenWeekend was in thousands so we had to create a new column in the data set where it was in millions. After we added that new column we went through the data to delete the observations where one of our exploratory or outcome variables were missing. For the visualization and analysis we wanted to perform we decided we were not going to use the LeadStudio or Story variables, so even though some of our rows are missing values under those columns we did not delete them because they had values for the variables we were testing. The majority of the observations that were excluded from our data were missing a Genre, which we intend to perform clustering on, so we excluded the missing values so that the movies included in our supervised analysis are the same as the ones included in our unsupervised clustering analysis. Other observations that were excluded did not have a value for one of the Gross columns or did not have a profitability amount, and those variables are key to our analysis. 

# Codebook


| Variable | Description | Units |
| :---- | :---- | :---- |
| Movie | Movie name |  |
| LeadStudio | Movie production company name |  |
| RottenTomatoes | The Rotten Tomatoes critics’ website ratings of movies | Percent |
| AudienceScore | Scoring for the movie by the audience | Percent |
| Story | The type of story the movie is about  |  |
| Genre | Movie categories |  |
| TheatersOpenWeek | Count of the number of theaters showing the movie for the open week | Count |
| OpeningWeekend | Total box office revenue earned during the opening weekend | Millions |
| BOAvgWeekend | The average box office revenue per theater during the opening weekend | Dollars |
| DomesticGross | The amount of money the movie gross in the United States | Millions |
| ForeignGross | The amount of money the movie gross outside the United States | Millions |
| WorldGross | The amount of money the movie gross worldwide | Millions |
| Budget | Amount of money spent on movie production | Millions |
| Profitability | How much money the movie made relative to its total cost over its entire run | Millions |
| OpenProfit | Profit earned only during the opening weekend | Millions |
| Year | The year when the movie is produced | 2007 \- 2013 |
| BOAvgWeekend(M) | The modified version for BOAvgWeekend, changing the units from dollars to millions | Millions |



# Data Visualization


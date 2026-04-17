# #MATH-244-Final-Project---Team-Movie
# Exploratory Data Analysis

Research Question: What factors contribute to a successful movie?
Success will be defined by the profitability and gross of the movie. 

Our outcome variable is going to be Profitability and WorldGross. High profitability will indicate that the movie made a lot of money with a small budget, and gross measures how much money the movie made in total. We are interested in measuring what factors contribute to a successful movie, and because profitability is a measure of (WorldGross/ Budget)*100, it will be able to explain how many times over the budget a movie earned in total revenue. This way, we can evaluate whether the budget of a movie is directly related to how much money it will make, and investigate the features of the highly profitable movies that are low-budget and high-return. When the profitability is above 100, it represents that the movie is making a profit. If not, then the movie suffered losses. From our dataset, we originally expected the movies with very high profitability to be the world-famous movies. However, we discovered that most of the movies with extremely high profitability are less well-known movies with extremely low budgets. For instance, there is a movie named Fireproof with a profitability of 6694.40, but this is due to its low budget of only 0.5 million dollars.

 

# Data Wrangling and Transformation

We performed the beginning of our data wrangling in Excel. First we had to make sure that all the variables that were in units of money were in millions of dollars, BOAvgOpenWeekend was in thousands so we had to create a new column in the data set where it was in millions. After we added that new column we went through the data to delete the observations where one of our exploratory or outcome variables were missing. For the visualization and analysis we wanted to perform we decided we were not going to use the LeadStudio or Story variables, so even though some of our rows are missing values under those columns we did not delete them because they had values for the variables we were testing. The majority of the observations that were excluded from our data were missing a Genre, which we intend to perform clustering on, so we excluded the missing values so that the movies included in our supervised analysis are the same as the ones included in our unsupervised clustering analysis. Other observations that were excluded did not have a value for one of the Gross columns or did not have a profitability amount, and those variables are key to our analysis. 

# Codebook
Variable
Description
Units
Movie
Movie name


LeadStudio
Movie production company name


RottenTomatoes
The Rotten Tomatoes website's ratings of movies


AudienceScore
Scoring for the movie by the audience


Story
The type of story the movie is about 


Genre
Movie categories


TheatersOpenWeek
Count of the number of theaters showing the movie for the open week
Counts of the weeks
OpeningWeekend
Total box office revenue earned during the opening weekend
Millions
BOAvgWeekend
The average box office revenue per theater during the opening weekend
Dollars
DomesticGross
Revenues made in domestic regions
Millions
ForeignGross
Revenues made in foreign regions
Millions
WorldGross
The total revenue
Millions
Budget
Amount of money spent on movie production
Millions
Profitability
How much money the movie made relative to its total cost over its entire run
Millions
OpenProfit
Profit earned only during the opening weekend
Millions
Year
The year when the movie is produced
Year ≥ 2007
BOAvgWeekend(M)
The modified version for BOAvgWeekend, changing the units from dollars to millions
Millions




# Data Visualization


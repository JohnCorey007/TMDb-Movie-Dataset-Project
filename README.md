# TMDb The Movie Dataset Project
## Introduction

### Dataset Description 

> This data set contains information about 10,000 movies collected from The Movie Database (TMDb), including user ratings, popularity, directors responsible, runtime, budget, and revenue. The following is a list of all the present variables and a description where necessary:

| Variable | Description |
| --- | --- |
| id | --- |
| imdb_id | --- |
| original_title | Title of the movie |
| popularity | A score between 1 and 0 representing user ratings |
| budget | Production budget for the movie |
| revenue | The box-office revenue after movie release |
| cast | Main actors |
| homepage | --- |
| director | The director responsible for the movie |
| tagline | --- |
| keywords | --- |
| overview | --- |
| runtime | The time the film lasts |
| genres | --- |
| production_companies | The production company responsible |
| release_date | Exact date of release |
| vote_count | --- |
| vote_average | --- |
| release_year | Gaussian |
| budget_adj | Budget adjusted for inflation |
| revenue_adj | Revenue adjusted for inflation |



### Questions for Analysis
1. Who has directed the most movies?
2. Which genres are most popular from year to year? 
3. What kinds of properties are associated with movies that have high revenues?
4. What was the average budget for movies?
5. What was the average box office revenue?

### Data Wrangling
For our data wraging efforts we concerned ourselves with two issues:
1. Getting rid of duplicates in our dataset
2. Changing the data type of release_date to datetime

### Exploratory Data Analysis
#### 1. Most popular genres by year
We used groupby to group the dataset by its release year then called value_counts() to get the most watched genres.
#### 2. Properties Associated With Movies That Have Higher Revenue
To answer this question, scatterplots will be plotted on adjusted revenue versus different properties, beginning with the budget allocated to the movie. Below are all the properties plotted with adjusted revenue:
- adjusted budget
- runtime
- release year

Budget is the variable that influences revenue the most out of the ones tested(budget,
runtime, and year of release). This makes sense as the larger the budget a production
company has at its disposal to create a movie, the higher the chance that the creation
is of the best quality, and will thus attract the most viewers. Marketing expenses also
come in place in this variable.

#### 3. Who has directed most movies?
We can use value_counts() to get the total number of movies each director has been featured in.
Woody Allen has directed the most movies. 
#### 4. What was the average budget for movies?
The average budget spent on a movie is 17,551,039. About 18 million US dollars
#### What was the average revenue for movies?
The average collected revenue after a movie release is about USD 51 million.

### Conclusions
The properties that seems to influence revenue the most is the budget. There is little
to no link between runtime and the adjusted revenue. There is a small amount of
evidence that the latest movies have been scoring higher revenues, although this has
not been scientifically tested.
Woody Allen has directed the most movies with a total of 43 between the years 1960
and 2015. Clint eastwood comes second with 34 while Martin Scorcese and Steve Spielberg come third with 29 movies each. Plotting the directors and the amount of movies
gives the Pareto distribution, a distribution famous for describing social, scientific, and
geophysical phenomena in society. It is most commonly associated with inequality and
the bible verse, "I tell you, that to every one who has will more be given; but from him
who has not, even what he has will be taken away."
It is also quite clear that most movies collect at least 3X their budget in revenue.

### Limitations
In finding the most popular genre by year, the research into this was limited as it did
not provide a summary list of the genres broken down by year, but would instead have
to be run again to get one for a specific year.
Other limitations present in this analysis is a lack of statistical analysis done to answer
any of these questions. For example correlation tests could’ve been conducted as part
of the bivariate analysis in order to find if any correlation exists between revenue with
runtime and budget.



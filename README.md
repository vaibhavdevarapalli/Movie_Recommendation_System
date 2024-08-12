# Movie Recommendation System

## Objective
The primary goal of this project is to gain insights into a movie dataset and develop a content-based recommendation system. The dataset used contains 1000 movies and includes various attributes such as title, genre, rating, and more. Python libraries like Matplotlib, Seaborn, and Pandas are employed for data analysis and visualization.

## Libraries Used
- Pandas
- Matplotlib
- Seaborn
- WordCloud
- Scikit-learn (for TF-IDF Vectorization)

## Dataset
The dataset, in CSV format, is loaded into a Pandas DataFrame. The dataset contains 1000 movies with 12 attributes, including title, genre, director, actors, year, runtime, rating, votes, revenue, and metascore. Data is collected on 12 different attributes of a movie, with rating being in the order of 1 (worst) and 10 (best) and the metascore being in the order from 1 (worst) and 100 (best).

## Workflow
## Data Preparation:
### Loading the Dataset:
The dataset, in CSV format, is loaded into a Pandas DataFrame. The dataset contains 1000 movies with 12 attributes, including title, genre, director, actors, year, runtime, rating, votes, revenue, and metascore.

### Handling Missing Values:
Missing values in the 'Revenue' and 'Metascore' columns were identified and filled with the respective column's mean value.

### Data Cleaning:
Columns not required for analysis and the recommendation engine, such as 'Description', 'Director', and 'Actors', were dropped from the dataset.

## Exploratory Data Analysis (EDA)
### Univariate Analysis:
Rating: The ratings are left-skewed, with most ratings between 6 and 8.
Runtime: The distribution is slightly right-skewed, with most movies having a runtime between 100 and 120 minutes.
Metascore: The Metascore follows a normal distribution, with an average score of 60.

### Bivariate Analysis:
Year vs Rating: A slight decreasing trend in ratings over the years, with a peak in the number of movies in 2016.
Year vs Metascore: A slight decrease in Metascore over the years, similar to the rating trend.
Year vs Runtime: The average runtime of movies has been consistent, around 120 minutes, over the years.

### Multivariate Analysis:
Analyzed the relationship between runtime, rating, and year, revealing that most movies from 2016 have a runtime between 100 and 125 minutes.
WordCloud Analysis:

### Title WordCloud:
Visualized the most common words in movie titles.
#### Genre WordCloud:
Visualized the most common genres in the dataset.

### Content-Based Recommendation System
#### TF-IDF Vectorization:
Implemented TF-IDF (Term Frequency-Inverse Document Frequency) vectorization on the 'Genre' column to convert textual data into numerical format.

### Recommendation Engine:
The recommendation system suggests movies based on the genre, utilizing the cosine similarity between TF-IDF vectors.

## Summary
From the above given dataset we built a content based Recommendation system or Personalized recommendation system.First we had to clean the datset as there were some missing values then we had to drop the columns which didn't seem necessary for out Analysis. After that we did some Exploratory Data Analysis on the movie dataset and found some trends and observations from the plots.

Then we used the concept of TF-IDF vector to convert our texts into a matrix form and find the cosine similarity so that we can predict the similar movies present in the dataset. At last we were sucessfull in building a very small version of a personalized recommendation system.

# Machine Learning Project – Movie Recommendation System in Python 🎦🎬 
# Aim of Project
Have you ever used online streaming platforms like Netflix, Amazon Prime, or Voot? Imagine watching a movie and then noticing how the platform starts recommending movies and TV shows that match your taste. It’s fascinating how these platforms understand your viewing habits and suggest content you’ll likely enjoy. This is the magic of a Recommendation System.
Such systems analyze user behavior to provide personalized suggestions. In this era of rapid technological advancement, where Artificial Intelligence and Machine Learning are reshaping industries, recommendation systems have become an integral part of our daily lives. If you’ve ever wondered how they work, this project is for you.
In this Machine Learning project, we’ll explore the fundamentals of recommendation systems, and I’ll guide you through building one from scratch. Let’s dive into the world of personalized content discovery!

![new](https://github.com/user-attachments/assets/37f4b297-5018-43fe-9f9f-06fd4c7711cd)

# Movie Recommendation System Project using ML
The main goal of this machine learning project is to build a recommendation engine that suggests movies to users. This Python project is designed to provide a practical understanding of how a recommendation system operates. We have developed a recommendation system using User-Based Collaborative Filtering, Item-Based Collaborative Filtering, and Model-Based Filtering. Through this project, I gained hands-on experience in applying Python, Data Science, and Machine Learning techniques to a real-world problem.

# What is a Recommendation System?
A recommendation system is a platform that offers personalized suggestions to users by leveraging a filtering process based on user preferences and browsing history. It takes user-related information as input, often derived from prior interactions, such as browsing data, ratings, or purchase history. This information helps the system understand user preferences and provide tailored content recommendations.
Recommendation systems also identify similarities between products or users. For instance, Netflix's recommendation engine suggests movies similar to the ones you’ve previously watched. Collaborative filtering, on the other hand, suggests movies based on the preferences of other users with similar tastes.

There are two main types of recommendation systems:

1. Content-Based Recommendation Systems: These recommend items similar to those the user has previously interacted with.
2. Collaborative Filtering Recommendation Systems: These rely on user-item interactions to find patterns, either through similarities between users (User-Based Filtering) or between items (Item-Based Filtering).

In this project, I implemented a collaborative filtering recommendation system in Python, combining user-based, item-based, and model-based filtering techniques to deliver personalized and effective recommendations.

![Screenshot 2024-11-29 212452](https://github.com/user-attachments/assets/95b14aa3-f826-4e4c-8178-335fc3bee70d)

# Dataset used
In order to build our recommendation system, we have used the MovieLens Dataset. You can find the movies.csv and ratings.csv file that we have used in our Recommendation System Project [here](https://drive.google.com/file/d/1Dn1BZD3YxgBQJSIjbfNnmCFlDW2jdQGD/view).  This data consists of 105339 ratings applied over 10329 movies.

# Necessary Libraries
To implement the recommendation system, several essential libraries were utilized:

**_Numpy_** and **_Pandas_** for data manipulation.
**_Seaborn_** and **_Matplotlib_** for data visualization.
**_Surprise_** library for building model-based collaborative filtering using SVD.
**_Scikit-learn_** for computing similarity and data normalization.

# Data Loading
The project utilized two datasets:

1. movies.csv: Contains details about movies, such as movieId, title, and genres. 
2. ratings.csv: Includes user ratings of movies with columns userId, movieId, rating, and timestamp.
The first few rows of each dataset were displayed to understand the structure of the data.

# Data Preprocessing
- Handling Missing Values: Checked for missing values in both datasets and confirmed that there were none.
- Timestamp Conversion: The timestamp column in the ratings dataset was converted into a more readable datetime format.
- User-Movie Matrix Creation: A pivot table was created where rows represent users, columns represent movies, and the cells contain ratings. Missing values were filled with 0 to simplify computation.

# Data Exploration
- Basic Statistics: Summary statistics for ratings were computed, including count, mean, and quartiles.
- Unique Counts: The number of unique movies and users was calculated to understand dataset dimensions.
- Visualization: Distribution of movie ratings was plotted using a histogram, showing the frequency of different ratings.

# User-Based Collaborative Filtering
- User Similarity Matrix: Calculated using the cosine similarity function. A similarity matrix was constructed, indicating the similarity between pairs of users.
- Recommendation Logic:
  - For a given user, similar users were identified based on the similarity matrix.
  - Ratings from these similar users were aggregated and averaged to recommend the top movies that the target user had not rated.
- Heatmap: A heatmap of the user similarity matrix was visualized to better understand user relationships.

# Item-Based Collaborative Filtering
- Item Similarity Matrix: Similarity between movies was computed using cosine similarity on the transpose of the user-movie matrix.
- Recommendation Logic:
  - For a given user, ratings for movies were used to find similar items based on the similarity matrix.
  - Weighted scores were calculated for all unrated movies by combining similarity values and existing ratings.
  - Top movies were recommended based on these scores.
- Heatmap: A heatmap of the item similarity matrix was visualized to highlight relationships between movies.

# Model-Based Collaborative Filtering (SVD)
- Algorithm: Singular Value Decomposition (SVD) from the surprise library was used to build a recommendation model.
- Training and Testing:
  - Data was split into 75% training and 25% testing sets.
  - The SVD model was trained on the training set and evaluated on the testing set using the RMSE (Root Mean Square Error) metric.
- Prediction Logic:
  - For a given user, predictions were made for all unrated movies.
  - Top recommendations were generated based on predicted ratings.

# Data Visualization
**Heatmaps were created to visualize:**

- User Similarity Matrix: Relationships between users based on their ratings.
- Movie Similarity Matrix: Relationships between movies based on their ratings.
- Top Movies by Views: A bar chart displayed the total number of views for the top 6 most-watched movies, providing insight into movie popularity.
- Heatmap of Ratings: A heatmap of a subset of the user-movie matrix (20 users × 25 movies) illustrated the distribution of ratings.
- Normalized Ratings Heatmap: The user-movie matrix was normalized, and a heatmap was generated to observe normalized rating patterns.


Finally, I added everything. The project effectively demonstrates the working principles of recommendation systems and provides insights into user preferences and movie popularity.

# 
📣 Feel free to have a look at all the files in this repository !🤗

# 
Languages used : 

![python-logo-only](https://github.com/user-attachments/assets/a78aa447-fe92-4892-aaed-4dd6ea761795)

❎ In case you find issues in any of my Repositories, you can Hit Me Up [here](https://github.com/issues)! 👈






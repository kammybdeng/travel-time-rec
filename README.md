# Travel Time: Travel Destination Recommender
* Please switch to dev branch to clone the repo

In the main folder,
run:
  * 1) src/spark_model.py
  * 2) src/pickle_model.py
  * 3) webapp/server.py

# Overview/ Motivation
Traveling is always fun and relaxing. However, how do you know where would be a best match for you to travel?
TraveTime is a travel desitination recommender that match the user's travel style, age, and other preferences to a selected type of city. Whether, it's a solo trip in a dynamic environment or a fun family vacation, we will always find your best match!


# Recommender System
The Youtube recommendations videos on the left side of the screen, or the next suggested movie in your Netflix account. They are a product of recommender system based on user and item data.

Being able to personalized user's recommendations, recommender system is a powerful data science tool in any industry.

## Hybrid Model

### 1. Collaborative Filtering Recommender
The recommeder system starts with a sparse utility matrix with items listed horizontally and users listed vertically on the matrix. The recommender system will then break the utility matrix into two smaller U, V matrixes. These two small, dense matrixes (often with reduced rank) will then combined to reform a new, dense utility matrix with filled in predicted ratings.

In this project, I used the ALS model from Spark as my recommender model.

###  2. Hybrid Recommender System
In order to improve the accuracy of my model. I decided to add in another user-user similarity matrix. I build up the function to calculate the user similarty with jaccard similarity.

The final predicted rating of my model is a combination of the ALS model and the user-user similarity matrix.

### 3. Clustering
Besides accuracy, I also want to personalize the recommendation. Therefore, I used kMean on the vectorized TFIDF city reviews  to create distinct city clusters.


# Workflow




# Data

Three Tripadvisor data sets from ResearchGate.
1) User's Big 5 personality scores
2)



# Future work
Adding new user info into website


# Tools
## Modeling/Machine Learning/Feature Engineering
* Scikit-learn
* Natural language processing
* TFIDF
* Numpy
* Pandas
## Data visualization:
* Matplotlib
* Seaborn
## Web App:
* Flask
* Bootstrap
* HTML
* CSS
* JavaScript

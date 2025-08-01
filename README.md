# Movie-Recommendation-System

Overview
This project implements a user-based collaborative filtering movie recommendation system using the MovieLens 100K dataset. The system recommends movies to users by computing similarity scores between users based on their movie ratings. The core idea is that users with similar tastes will likely enjoy similar movies.

Dataset
Source: MovieLens 100K Dataset

Contains 100,000 ratings from 943 users on 1,682 movies.

Objectives
Build a user-item interaction matrix from the dataset.

Compute similarity scores between users using cosine similarity.

Generate top-N movie recommendations for each user based on the preferences of similar users.

Evaluate the performance of recommendations using Precision@K metric.

Tools and Libraries
Python

Pandas

NumPy

Scikit-learn

Key Components
User-Item Matrix Construction
Created a pivot table where rows represent users, columns represent movies, and values represent ratings.

Cosine Similarity Computation
Used sklearn.metrics.pairwise.cosine_similarity to measure the similarity between users based on their rating vectors.

Recommendation Generation
For a given user, the system identifies the top-k most similar users, aggregates their rated items, and recommends the highest-rated movies that the target user hasn't seen yet.

Train/Test Split
The dataset was split into training and testing sets to evaluate the model's generalization.

Evaluation: Precision@K
Calculated the precision at K for each user by comparing recommended movies to those actually rated in the test set.

Performance
The system evaluates recommendation quality using Precision@5 averaged over all test users with available data.

This metric provides an indication of how many of the top 5 recommended movies were relevant (i.e., actually watched/rated by the user in the test set).

Future Improvements
Implement item-based collaborative filtering.

Explore model-based approaches (e.g., matrix factorization using SVD).

Add support for content-based filtering using movie metadata.

Enhance evaluation with additional metrics like Recall@K and F1@K.

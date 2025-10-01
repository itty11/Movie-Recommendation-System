# Movie-Recommendation-System
This project builds a Movie Recommendation System using the MovieLens dataset. It implements both Matrix Factorization (NMF) and Collaborative Filtering (cosine similarity) to recommend movies to users. The system is also evaluated using RMSE, Precision@K, and Recall@K.

# Dataset

Ratings: 100,836 ratings

Movies: 9,742 unique movies

Users: 610 users

User–Item Matrix: (610, 9724)

# Methods Implemented

1. Data Preprocessing

- Loaded ratings.csv and movies.csv.

- Created a user-item rating matrix.

- Handled missing values (unrated movies filled with 0).

2. Collaborative Filtering Approaches

- Matrix Factorization (NMF) with 20 latent factors.

- Item-based Collaborative Filtering using cosine similarity.

3. Evaluation

- RMSE (rating prediction error).

- Precision@K & Recall@K (top-N recommendation quality).

- Leave-One-Out cross-validation for realistic evaluation.

# Sample Results

# Model Training

NMF factorization:

W (users × latent) = (610, 20)

H (latent × items) = (20, 9724)

# Movie Similarity Example

Sample movie: Toy Story (1995)

Top-5 similar movies:

| Movie                                      | Similarity |
| ------------------------------------------ | ---------- |
| Home Alone (1990)                          | 0.936      |
| Aladdin (1992)                             | 0.932      |
| The Lion King (1994)                       | 0.923      |
| Mrs. Doubtfire (1993)                      | 0.904      |
| Willy Wonka & the Chocolate Factory (1971) | 0.901      |

# User-Based Recommendations

Top-10 recommendations for User 1 (NMF):

| Movie                                  | Predicted Rating |
| -------------------------------------- | ---------------- |
| Terminator 2: Judgment Day (1991)      | 4.20             |
| Aliens (1986)                          | 4.17             |
| Star Trek II: The Wrath of Khan (1982) | 3.37             |
| Stand by Me (1986)                     | 3.29             |
| The Sixth Sense (1999)                 | 3.23             |
| Die Hard (1988)                        | 3.18             |
| The Breakfast Club (1985)              | 2.99             |
| Star Trek: First Contact (1996)        | 2.97             |
| The Godfather (1972)                   | 2.81             |
| Star Trek IV: The Voyage Home (1986)   | 2.73             |

Top-10 recommendations for User 1 (Item-based CF):

| Movie                                  | Score |
| -------------------------------------- | ----- |
| Kill Bill: Vol. 2 (2004)               | 4.90  |
| The Professional (1981)                | 4.90  |
| Dylan Moran: Monster (2004)            | 4.90  |
| Bill Hicks: Revelations (1993)         | 4.90  |
| The Thing Called Love (1993)           | 4.89  |
| The Sixth Sense (1999)                 | 4.89  |
| The Girl with the Dragon Tattoo (2009) | 4.86  |
| Donnie Darko (2001)                    | 4.86  |
| The Last King of Scotland (2006)       | 4.86  |
| Ashes of Time (1994)                   | 4.85  |

# Evaluation

NMF Leave-One-Out Evaluation Results:

RMSE: 3.1441

Precision@K: 0.0156

Recall@K: 0.1557

Tested Users: 610

# Outputs

sample_recommendations_user_1.csv → saved example recommendations for User 1.

# Next Steps

Try Deep Learning approaches (Autoencoders / Neural CF).

Add content-based filtering using movie genres or tags.

Deploy as a Flask/Streamlit app for interactive recommendations.

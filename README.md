
# Movie Recommendation System

This project implements a movie recommendation system using the MovieLens dataset. It includes implementations of content-based filtering, collaborative filtering, and a hybrid approach, along with a Gradio interface for interactive recommendations.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Setup and Installation](#setup-and-installation)
- [How to Run](#how-to-run)
- [Recommendation Approaches](#recommendation-approaches)
    - [Content-Based Filtering (Genres)](#content-based-filtering-genres)
    - [Collaborative Filtering (Ratings)](#collaborative-filtering-ratings)
    - [Hybrid Approach](#hybrid-approach)
- [Gradio Interface](#gradio-interface)
- [Evaluation](#evaluation)
- [Files](#files)

## Project Overview

The goal of this project is to build a simple movie recommendation system that can suggest movies to users based on different criteria. We explore content-based filtering (using movie genres), collaborative filtering (using user ratings), and a hybrid approach that combines both. A Gradio interface is provided to allow users to interact with the hybrid recommendation system.

## Features

- Implement content-based filtering based on movie genres.
- Implement collaborative filtering based on user ratings.
- Develop a hybrid recommendation function combining content-based and collaborative filtering.
- Provide a Gradio interface for interactive movie recommendations.
- Basic evaluation of the hybrid recommendation system.

## Dataset

The project uses the publicly available [MovieLens 100k Dataset](https://grouplens.org/datasets/movielens/100k/). The following files are used:

- `movies.csv`: Contains movie metadata including `movieId`, `title`, and `genres`.
- `ratings.csv`: Contains user ratings including `userId`, `movieId`, `rating`, and `timestamp`.
- `tags.csv`: Contains user tags for movies including `userId`, `movieId`, `tag`, and `timestamp`.

## Setup and Installation
    pip install pandas scikit-learn gradio
## How to Run

1.  **Download the dataset:** Download the MovieLens 100k dataset and place the `movies.csv`, `ratings.csv`, and `tags.csv` files in the same directory as your notebook or script.
2.  **Run the notebook:** Execute the cells in the provided Jupyter Notebook or Colab notebook sequentially.
3.  **Launch the Gradio interface:** The last code cell in the notebook will launch the Gradio interface. Click on the public URL provided to access the movie recommender.

## Recommendation Approaches

The project explores the following recommendation approaches:

### Content-Based Filtering (Genres)

This approach recommends movies based on their genre similarity. It uses TF-IDF vectorization on movie genres and cosine similarity to find movies with similar genre profiles. The `get_movies_by_genres` function filters movies based on user-provided genres.

### Collaborative Filtering (Ratings)

This approach recommends movies based on user rating patterns. It builds a user-item matrix from the `ratings.csv` and uses cosine similarity to find users with similar rating preferences.

### Hybrid Approach

The hybrid approach combines both content-based and collaborative filtering. The `get_hybrid_recommendations` function takes a user ID and a movie title as input and generates recommendations by considering both genre similarity and user rating patterns.

## Gradio Interface
![image](https://github.com/user-attachments/assets/0b209148-3a36-49e8-99b4-84fcac7ff35f)


A Gradio interface is provided to interact with the hybrid movie recommendation system. The interface allows users to select a user ID and a movie title and get top 5 movie recommendations.

## Evaluation

The project includes a basic evaluation of the hybrid recommendation system using metrics such as Hit Rate, Average Rating of Recommended Movies, and Proportion of Recommended Movies with Matching Tags. The `evaluate_recommendations` function performs this evaluation using the `ratings.csv` and `tags.csv` files.

## Files

- `(your_notebook_name).ipynb`: The main Jupyter Notebook or Colab notebook containing all the code for data loading, preprocessing, recommendation logic, Gradio interface, and evaluation.
- `movies.csv`: Movie metadata.
- `ratings.csv`: User ratings.
- `tags.csv`: User tags.

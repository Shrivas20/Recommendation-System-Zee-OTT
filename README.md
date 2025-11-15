# 🎬 Zee Recommender System: Business Case Study

## 🎯 About The Project

This project is a business case study for **Zee Recommender Systems**, an ambitious venture to enhance user experience by providing personalized movie recommendations.

The primary goal is to leverage a comprehensive dataset of movie ratings, user demographics, and movie details to build a robust recommender system. By accurately predicting user preferences, the system aims to drive user engagement, increase satisfaction, and foster a more intuitive user experience.

---

## 🚀 What We Did: A High-Level Overview

This repository contains the complete workflow for analyzing user data and building several types of movie recommender systems.

### 1. 💾 Data Loading and Preparation
* **Loaded Data:** The project began by loading three core datasets: `zee-users.dat` (user demographics like age, gender, occupation), `zee-movies.dat` (movie details like title and genres), and `zee-ratings.dat` (user ratings for movies).
* **Data Cleaning:** These datasets were parsed, cleaned, and merged into a single master dataframe for analysis.
* **Feature Engineering:** New features were created, such as extracting the release `Year` from the movie `Title` and converting genre strings into a usable list format.

### 2. 📊 Exploratory Data Analysis (EDA)
Before modeling, we performed a deep dive into the data to understand user and movie characteristics:
* Analyzed the distribution of user **Age**, **Gender**, and **Occupation**.
* Visualized the most popular **Movie Genres** and the distribution of movie **Release Years**.
* Examined the overall **Rating Distribution** to understand user rating behavior.

### 3. 🧠 Building the Recommender Systems
Several different recommendation techniques were built and evaluated to find the most effective approach.

* **Collaborative Filtering (Memory-Based):**
    * **User-Based Similarity:** Built a model to find similar users and recommend movies that they liked.
    * **Item-Based Similarity:** Built a model to find similar movies based on user ratings and recommend items similar to those a user has already liked. (e.g., finding movies similar to "Liar Liar (1997)").

* **Model-Based Filtering:**
    * **Matrix Factorization (SVD):** Implemented a powerful SVD (Singular Value Decomposition) model using the `scikit-surprise` library to predict user ratings for movies they haven't seen. This was cross-validated to ensure accuracy.

* **Hybrid Recommender (Ensemble):**
    * To achieve even better performance, we combined the predictions from a Gradient Boosting model with the predictions from the Matrix Factorization (SVD) model. This ensemble approach leverages the strengths of both models and was evaluated using RMSE and MAPE metrics.

---

## 🛠️ Technologies Used

* **Data Analysis & Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Recommender Systems:** Scikit-learn (`cosine_similarity`, `NearestNeighbors`), Scikit-surprise (SVD), CMFrec
* **Model Evaluation:** Scikit-learn (RMSE, MAPE)

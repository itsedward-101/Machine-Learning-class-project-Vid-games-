# Machine-Learning-class-project-Vid-games-
🎮 Video Game Hit vs. Non-Hit Prediction

Machine Learning Classification Project

📌 Project Overview

This project explores whether video games can be classified as “Hit” or “Non-Hit” based on their attributes using supervised machine learning models. By analyzing global video game metadata and review scores, the project aims to uncover patterns that explain what makes a video game successful and to build predictive models that can support data-driven decision-making in the gaming industry.

This project was completed as part of a Machine Learning course in the Master of Science in Business Analytics program and emphasizes both predictive accuracy and business interpretability.

🎯 Business Problem

Video game development is costly and risky, with success often dependent on uncertain market reception. Being able to predict whether a game is likely to become a hit can help developers and publishers:

Allocate marketing budgets more effectively

Optimize product portfolios across genres and platforms

Reduce financial risk before launch

This project formulates the problem as a binary classification task:

Hit (1): Review score ≥ 75

Non-Hit (0): Review score < 75

The classification threshold is based on the Metacritic rating system, a widely used industry benchmark.

📊 Dataset

Name: Discovering Hidden Trends in Global Video Games

Source: Kaggle

Link: https://www.kaggle.com/datasets/thedevastator/discovering-hidden-trends-in-global-video-games

Usability Score: 10 / 10

Published: ~3 years ago

Total Observations: 1,907 video games

Key Features

The dataset contains global video game information including:

Title

Platform

Genre

Publisher

Year of release

Regional and global sales

Review score

The review score is used to construct the target variable for hit vs. non-hit classification.

🔧 Methodology
1. Data Preparation

Cleaned and validated dataset

Handled missing values

Encoded categorical variables (e.g., genre, platform, publisher)

Removed variables that could cause data leakage

Created binary target variable based on review score threshold

Split data into training and testing sets

2. Exploratory Data Analysis (EDA)

Examined distribution of hit vs. non-hit games

Analyzed genre and platform popularity trends

Investigated relationships between game attributes and review scores

Identified patterns that informed feature selection and modeling decisions

3. Modeling Approaches

The following supervised classification models were implemented and compared:

Logistic Regression

Interpretable baseline model

Assessed how individual attributes affect the probability of a game being a hit

Naive Bayes

Probability-based classification

Evaluated model performance under conditional independence assumptions

Decision Tree

Tree-based model for intuitive rule-based interpretation

Visualized how different attributes lead to hit vs. non-hit outcomes

Random Forest

Ensemble method combining multiple decision trees

Improved predictive accuracy and reduced overfitting

📈 Model Evaluation

Models were evaluated using standard classification metrics, including:

Accuracy

Precision

Recall

ROC-AUC

Comparisons focused on both predictive performance and interpretability, with an emphasis on understanding practical business implications.

🔍 Key Findings & Insights

Ensemble models such as Random Forest generally outperformed simpler models

Certain genres and platforms showed higher likelihoods of producing hit games

Model interpretability helped translate technical outputs into actionable insights for developers and publishers

Results highlight the importance of aligning game attributes with audience preferences

🧠 Business Implications

Developers can use predictive insights to prioritize projects with higher success probabilities

Publishers can refine launch strategies based on genre and platform trends

Data-driven modeling can complement creative decision-making in the gaming industry

🛠️ Tools & Technologies

Programming Language: Python

Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn

Modeling Techniques: Logistic Regression, Naive Bayes, Decision Tree, Random Forest
🚀 Future Improvements

Incorporate additional features such as marketing spend or social media metrics

Experiment with advanced models (e.g., Gradient Boosting, XGBoost)

Perform hyperparameter tuning to further optimize model performance

Extend analysis to multi-class success levels instead of binary classification

👤 Author

Edward Dai,
Meghna Prakash,
Alex Huang,
Srinidhi Chevvuri,
Preme Chinpattanakul

---
layout: page
title: Midterm Report
permalink: /midterm-report/
---

[Introduction/Background](#introductionbackground) \
[Problem Definition](#problem-definition) \
[Methods](#methods) \
[Results and Discussions](#potential-results-and-discussions) \
[Peer Reviewed References](#peer-reviewed-references) \
[Proposed Timeline](#proposed-timeline) \
[Contribution Table](#contribution-table)

### **Introduction/Background**

We will be working on a ML project where we are predicting an NBA Player’s Performance. We will mainly focus on predicting their points for specific games. So far, some research and implementation have been performed to predict a player’s performance, however there is no solid evidence if it has actually been implemented by real professionals and NBA Team’s Front Offices. We were inspired by the research conducted by Kevin Wheeler and the documentation he provided. The dataset we currently plan to use will be a combination of the player’s stats (per game), as well as the opponent's team defensive statistics. We had multiple literature reviews on some of the potential methods/ implementation we wanted to work on for this project, and we were also impressed on how the NBA are now transitioning to this AI and ML era and how beneficial it would be not only for NBA Teams and the Players, but also for its fans. The application of machine learning and deep learning in sport: predicting NBA players’ performance and popularity by Nguyen Hoang Nguyen, Duy Thien An Nguyen, Bingkun Ma & Jiang Hu, Predicting the Outcomes of NBA Games by T. Horvat, J. Job, R. Logozar, and Č. Livada, as well as Predicting NBA Players Performance by Kevin Wheeler.

### **Problem Definition**

Basketball Player Evaluation Metrics are essential for analyzing NBA players' performances objectively. They break down a player's contributions into categories like scoring efficiency, individual value, and adjust plus-minus, providing insights for coaches and teams to make informed decisions. These metrics aid in player development and strategic planning. They also facilitate fair player comparisons, crucial in the diverse NBA. Metrics influence contract negotiations, scouting, and the draft, helping identify talent. Moreover, they engage fans by offering insights beyond on-court actions, enriching the overall experience.

### **Data Colletion**

The dataset we used for data collection was gathered from the NBA official website, which contained NBA games from 1996 up until 2023. We used a Python based API web scraper to collect data from around 9 years and various seasons from 2012 to 2021. In addition, the MVP dataset is from the Basketball Performance website which shows all the MVP of the year. To make data more efficient, we selected players in each season to collect data from. The features we are most interested in looking at are the value over replacement players and win shares. An important observation from the outcome that we want to investigate further is that how win shares can greatly impact a single player's morality and potentially their performance within the next games they play. As an additional feature, we will add the player efficiency rating to see its potential influence on its respective current game. We are trying to use correlation matrix to give us a comprehensive view of different variables in the dataset. For data cleaning, first use panda is a method to help us detect if our dataset contains missing values, then we remove the duplicate rows. We also remove non-important features and unuseful columns. Then we change some of the feature or column names to make data understandable. Below shows the final cleaned dataset. The detailed table of data can be found in Github.

![Data Collection](/data-collection.jpeg)
![Clean Data](/clean-data.jpeg)

### **Methods**

**Linear Regression**:
Linear regression is employed to build the predictive model, leveraging libraries like scikit-learn in Python. Model evaluation involves assessing performance using metrics like Mean Squared Error, and coefficients are interpreted to understand the impact of each feature on performance.

**XGBoost**:
Create an XGBoost model, using XGBRegressor for regression or XGBClassifier for classification, and train it on the designated training set. Evaluate the model on the testing set using appropriate metrics, such as Mean Squared Error for regression or Accuracy for classification.

**LightGBM Regressor**
Install LightGBM, set regression parameters, and create LightGBM datasets. Train the model and evaluate its performance using mean squared error on the testing set. Analyze feature importance to understand the factors influencing player performance.

### **Results and Discussions**

For this Midterm report, we are creating a model to predict the MVP winner for each NBA Regular Season. We already have cleaned pre-processed data as mentioned from the Data Cleaning section above for our model. For Data Pre-Processing, we had to do some feature selections on selecting which statistics we wanted to use to train our model to predict the MVP, all of which have been discussed in our Data Collection Section. We decided to use Linear Regression Supervised Learning to create, train and test our model and we and here are the results:

- **Average MAE**: 0.1453
- **Average R Squared**: 0.4717
- **Prediction Accuracy**: 0.6483

![Result 1](/result.png)
![Result 2](/result2.png)

To improve our model for the future iterations, here are some ideas that we think might be good for us to implement. To enhance the performance of our linear regression model, we can also curate the feature set by selecting those with a strong linear relationship to the target variable and eliminating irrelevant or redundant ones that might introduce noise. Some more preprocessing can also be done by handling missing data through imputation or removal and addressing outliers that can significantly impact model accuracy. We should also think about normalizing or standardizing features aids in achieving convergence and stability. Incorporation of polynomial features can further enhance the model's ability to capture complex, non-linear relationships within the data. Multicollinearity, a potential source of instability, should be identified and mitigated by removing highly correlated features in our dataset, and regularization techniques such as L1 or L2 regularization can be applied to prevent overfitting.

In addition to feature engineering and preprocessing, model evaluation and fine-tuning play pivotal roles. Employing K-Fold cross-validation provides a robust assessment of the model's generalization performance can reduce the risk of overfitting to specific subsets of the data. Hyperparameter optimization, including adjusting learning rates, is a critical step in refining the model's architecture. Residual analysis, involving a thorough examination of the differences between predicted and actual values, ensures the model aligns with the underlying data distribution. Experimentation with ensemble methods, and creating new features contribute to a comprehensive approach for refining the model's accuracy.

### **Proposed Timeline**

This is [our proposed timeline](https://docs.google.com/spreadsheets/d/1ZIS8XA_fs862QNVlRjXboMSVjAnlntGr/edit#gid=1490824648)

### **Contribution Table**

| Name                    | Contribution                                                              |
| ----------------------- | ------------------------------------------------------------------------- |
| Abdul-Falik Assa        | Data Collection, Methods, Results & Discussions                           |
| Alexus Bernard Brooklyn | Data Collection, Methods, Introduction/ Background, Results & Discussions |
| Parker Sargis Hakobyan  | Data Collection, Methods, Results & Discussions                           |
| Rafy Muhammad Akbar     | Data Collection, Methods, Github Page, Results & Discussions              |
| Wentao Yue              | Data Collection, Pre-processing Data, Methods                             |

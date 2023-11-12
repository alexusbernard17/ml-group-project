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

The dataset we used for data collection was gathered from the NBA official website, which contained NBA games from 2012 up until 2023. We used a Python based API web scraper to collect data from around 9 years and various seasons from 2012 to 2021. To make data more efficient, we selected players in each season to collect data from. The features we are most interested in looking at are the win shares and player efficiency rating. An important observation from the outcome that we want to investigate further is that how win shares can greatly impact a single player's morality and potentially their performance within the next games they play. As an additional feature, we will add the value over replacement players to see its potential influence on its respective current game. We are trying to use correlation matrix to give us a comprehensive view of different variables in the dataset. For data cleaning, first use panda is a method to help us detect if our dataset contains missing values, then we remove the duplicate rows. We also remove non-important features and unuseful columns. Then we change some of the feature or column names to make data understandable. Below shows the final cleaned dataset. The detailed table of data can be found in Github.

![Data Collection](/data-collection.jpeg)
![Clean Data](/clean-data.jpeg)

### **Methods**

**Gaussian Naive Bayes**:
We employed a Gaussian Naive Bayes model to forecast the player performance. The implementation was carried out using the scikit-learn library.

**Support Vector Machines (SVM)**:
Collect and preprocess relevant player data, split it into training and testing sets, and choose SVM parameters such as kernel type and hyperparameters. We trained a Support Vector Machine (SVM). The scikit-learn library was utilized for the implementation of the SVM.

**LightGBM Regressor**
Install LightGBM, set regression parameters, and create LightGBM datasets. Train the model and evaluate its performance using mean squared error on the testing set. Analyze feature importance to understand the factors influencing player performance.

### **Results and Discussions**

By the end of development, this algorithm should have a prediction accuracy of at least 50 percent for each player performance category, measured using standard classification metrics. We will test this model during the upcoming NBA season. The insights gained from our model can be valuable to NBA teams, sports bettors, and fantasy sports enthusiasts. The predictions made by our model will be biased by past historical data and will not take into account unforeseen events such as injuries, suspensions, etc.

### **Peer Reviewed References**

1. **The application of machine learning and deep learning in sport: predicting NBA players’ performance and popularity** \
   _Summary_: \
   This study focuses on using data analysis techniques to predict players' future performance and their likelihood of being selected for the NBA All-Star game, a prestigious event in the National Basketball Association (NBA) league. Traditional Machine Learning and Deep Learning methods were applied for prediction. However, Deep Learning's performance was found to be less effective due to the relatively small and structured dataset with limited predictor variables. The results, obtained through Regression and Classification Analysis, showed that scoring is the most crucial factor for primary players in any team, and it significantly influences a player's popularity.

   The NBA is a highly profitable sports league, and this study aimed to evaluate the application of Machine Learning and Deep Learning in analyzing basketball player data. The study's objectives included predicting players' future performance and their popularity, particularly their selection for the NBA All-Star game. The popularity of players has a significant impact on their franchises' brands and the league's overall revenue. The research applied CRISP-DM methodology, which consists of six phases, to construct ML and DL models, with a focus on the first five phases. The study also discussed the limitations of using Deep Learning on relatively small and structured datasets for basketball data analysis.

   _Reference_: \
    Nguyen Hoang Nguyen, Duy Thien An Nguyen, Bingkun Ma & Jiang Hu (2022) The application of machine learning and deep learning in sport: predicting NBA players’ performance and popularity, Journal of Information and Telecommunication, 6:2, 217-235, DOI: 10.1080/24751839.2021.1977066

2. **Predicting NBA Players Performance** \
   _Summary_: \
   Predicting outcomes in sports and athlete performances is an ideal domain for machine learning due to the wealth of readily available data in major leagues like the NBA, NFL, and MLB. These sports offer data that is often randomly distributed, making it an appealing dataset for prediction. The NBA, in particular, stands out for machine learning applications because player performance across various positions can be assessed using the same set of statistics, unlike sports like the NFL where different positions are evaluated using distinct metrics. Furthermore, the use of machine learning for predicting individual athlete performances naturally extends to forecasting game outcomes. By predicting the scoring abilities of each player and aggregating them, it becomes possible to create an accurate win-loss classifier. This project aimed to develop a model using linear regression (with Naïve Bayes and SVM implementations for comparison) to predict the number of points NBA players would score against a given opponent.

   _Reference_: \
    K. Wheeler, “Predicting NBA Player Performance,” Stanford University, https://cs229.stanford.edu/proj2012/Wheeler-PredictingNBAPlayerPerformance.pdf (accessed Oct. 5, 2023).

3. **Predicting the Outcomes of NBA Games** \
   _Summary_: \
   This paper speaks about the use of machine learning algorithms to predict the outcome of NBA games. The study used a supervised learning model. They evaluated the player and team performances using team efficiency indices. During the comparisons, the observed team was rewarded for each selected feature that it outperformed its rival. The model used data from the 2014-2018 NBA seasons. The average accuracy of the algorithm was 66% with an optimal accuracy of 78%

   _Reference_: \
    T. Horvat, J. Job, R. Logozar, and Č. Livada, “A Data-Driven Machine Learning Algorithm for Predicting the Outcomes of NBA Games,” Symmetry, vol. 15, no. 4, p. 798, Mar. 2023, doi: 10.3390/sym15040798

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

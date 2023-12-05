---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: base
---

## Final Report

[Introduction/Background](#introductionbackground) \
[Problem Definition](#problem-definition) \
[Data Collection](#data-collection) \
[Methods](#methods) \
[Results and Discussions](#results-and-discussions) \
[Conclusion](#conclusion) \
[Peer Reviewed References](#peer-reviewed-references) \
[Proposed Timeline](#proposed-timeline) \
[Contribution Table](#contribution-table)

## **Introduction/Background**

We will be working on a ML project where we are predicting an NBA Player’s Performance. We will mainly focus on predicting their points for specific games. So far, some research and implementation have been performed to predict a player’s performance, however there is no solid evidence if it has actually been implemented by real professionals and NBA Team’s Front Offices. We were inspired by the research conducted by Kevin Wheeler and the documentation he provided. The dataset we currently plan to use will be a combination of the player’s stats (per game), as well as the opponent's team defensive statistics.

We had multiple literature reviews on some of the potential methods/ implementation we wanted to work on for this project, and we were also impressed on how the NBA are now transitioning to this AI and ML era and how beneficial it would be not only for NBA Teams and the Players, but also for its fans. The application of machine learning and deep learning in sport: predicting NBA players’ performance and popularity by Nguyen Hoang Nguyen, Duy Thien An Nguyen, Bingkun Ma & Jiang Hu, Predicting the Outcomes of NBA Games by T. Horvat, J. Job, R. Logozar, and Č. Livada, as well as Predicting NBA Players Performance by Kevin Wheeler.

## **Problem Definition**

Basketball Player Evaluation Metrics are essential for analyzing NBA players' performances objectively. They break down a player's contributions into categories like scoring efficiency, individual value, and adjust plus-minus, providing insights for coaches and teams to make informed decisions. These metrics aid in player development and strategic planning. They also facilitate fair player comparisons, crucial in the diverse NBA. Metrics influence contract negotiations, scouting, and the draft, helping identify talent. Moreover, they engage fans by offering insights beyond on-court actions, enriching the overall experience.

## **Data Collection**

The dataset we used for data collection was gathered from the NBA official website, which contained NBA games from 1996 up until 2023. We used a Python based API web scraper to collect data from around 9 years and various seasons from 2012 to 2021. In addition, the MVP dataset is from the Basketball Performance website which shows all the MVP of the year. To make data more efficient, we selected players in each season to collect data from. The features we are most interested in looking at are the value over replacement players and win shares.

An important observation from the outcome that we want to investigate further is that how win shares can greatly impact a single player's morality and potentially their performance within the next games they play. As an additional feature, we will add the player efficiency rating to see its potential influence on its respective current game. We are trying to use correlation matrix to give us a comprehensive view of different variables in the dataset. For data cleaning, first use panda is a method to help us detect if our dataset contains missing values, then we remove the duplicate rows. We also remove non-important features and unuseful columns. Then we change some of the feature or column names to make data understandable. Below shows the final cleaned dataset. The detailed table of data can be found in Github.

![Data Collection](/data-collection.jpeg)
![Clean Data](/clean-data.jpeg)

Dataset Links:
[https://docs.google.com/spreadsheets/d/1bh-x5K7iBCv77ziqiPlaP8FnXWLJtqhI75LLbUF4d2s/edit#gid=884741645](https://docs.google.com/spreadsheets/d/1bh-x5K7iBCv77ziqiPlaP8FnXWLJtqhI75LLbUF4d2s/edit#gid=884741645)
[https://docs.google.com/spreadsheets/d/1TddPNUiZ9ojr-q_wrhDBtvX0DRF0NjsQFcDNTvTCWhE/edit#gid=125670641](https://docs.google.com/spreadsheets/d/1TddPNUiZ9ojr-q_wrhDBtvX0DRF0NjsQFcDNTvTCWhE/edit#gid=125670641)

## **Methods**

### **Linear Regression**

In the situation of predicting player performance, Linear Regression provides a clear understanding of the relationships between variables. It is particularly useful when the relationships between features and performance are relatively straightforward and can be adequately represented by a linear equation. Linear Regression also allows for easy interpretation of coefficients, providing insights into the direction and strength of the relationships between specific player attributes and overall performance. Its simplicity and transparency are the advantageous for gaining a basic understanding of the factors influencing NBA player success.

### **Random Forest**

Random Forest, as an ensemble learning algorithm, is a good choice for NBA player analysis. Its strength lies in its ability to build multiple decision trees independently and then combine their predictions to create a robust and accurate model. In the context of NBA player evaluation, Random Forest's ensemble approach helps mitigate overfitting and enhances the model's generalization to new data. Additionally, the algorithm provides valuable insights into feature importance, aiding in the identification of key player attributes that significantly contribute to overall performance. With Random Forest's robustness to missing values and ease of tuning hyperparameters, it emerges as a reliable tool for extracting actionable information from the diverse and dynamic datasets associated with NBA player statistics.

### **XGBoost**

XGBoost is a powerful machine learning algorithm that is particularly well-suited for NBA player analysis and prediction. Its ability to handle non-linear relationships and capture complex patterns in the data makes it ideal for modeling the intricate and multifaceted nature of player performance. XGBoost's sequential learning process, where each tree corrects the errors of the previous ones, enables it to iteratively improve its predictions, providing a nuanced understanding of the factors influencing a player's success on the basketball court. Moreover, XGBoost's efficiency and scalability make it a practical choice for processing large datasets, ensuring that it can effectively analyze extensive historical player data to generate meaningful insights for player evaluation and prediction.

## **Results and Discussions**

We chose to build our prediction model using three methods - Linear Regression, Random Forest, and XGBoost. We chose these three models because they are relatively simple to implement and are computationally efficient. Additionally, we chose to use these models because they are well suited for binary classification problems, which is the type of problem we are trying to solve. After finally deciding and implementing Linear Regression, Random Forest, and XGBoost Regressor for our prediction methods to create, train, and test our model, here are the final results:

![Result 1](/merged_table.jpeg)
![Result 2](/merged_pie_chart.png)

As we can see, among our three methods, the XGBoost Regression model had the best accuracy among the other 2 methods. The results of our predictive models provide valuable insights into their performance. In terms of Linear Regression, we observed an average Mean Absolute Error (MAE) of 0.145, indicating the average absolute difference between the predicted and actual values. The R-squared value of approximately 0.47 suggests that around 47% of the variance in the data is explained by the model. The prediction accuracy, computed as 64.29%, reflects the proportion of correct predictions out of the total instances. Our linear regression model for predicting NBA MVP outcomes may experience low accuracy because it might fail to fully capture the multifaceted nature of basketball performance. Linear regression assumes a linear relationship between input features and the target variable, which might simplify the intricate dynamics that contribute to MVP-worthy performances in basketball. Factors such as player efficiency, team success, leadership qualities, and clutch performances may have nonlinear and interacting effects, making linear regression less effective in discerning the nuanced patterns that determine MVP selections.

Moving on to the Random Forest model, it demonstrated improved performance compared to Linear Regression. With an average MAE of 0.104, the model exhibited a reduced error in predictions. The R squared value increased to approximately 0.61, indicating a higher degree of variance explained by the model. The prediction accuracy also improved to 73.81%, showcasing the effectiveness of Random Forest in capturing complex relationships within the data.

Similarly, the XGBoost model delivered competitive results with an average MAE of 0.107. The R-squared value of around 0.59 indicates a robust explanatory power of the model. Notably, the prediction accuracy reached 76.19%, surpassing both Linear Regression and Random Forest. These results highlight the superior predictive capabilities of XGBoost Regression in our context, suggesting its suitability for our prediction task. Overall, the comparative analysis underscores the importance of selecting the appropriate regression model based on the specific characteristics and requirements of the dataset.

Based on the data presented in the pie charts, it is evident that all three models have produced somewhat comparable accuracy, which indicates satisfactory performance for our specific use case. However, it should be noted that the efficacy of each model cannot be generalized, as they have their unique strengths and limitations. For instance, we have observed that Linear Regression and Random Forest are computationally efficient and straightforward to implement. On the other hand, XGBoost are the most suitable option for handling non-linearly separable datasets, but XGboost are computationally expensive and comparatively more complex than the other two models.

![Result 3](/merged_bar_chart.jpeg)

Also, after looking at the bar chart data visualization, we can see that some of the players who actually won the MVP were never predicted by any of our models. Players like Steve Nash, Hakeem Olajuwon, and Charles Barkley was never once predicted in any of our models, since they may not have the most compelling statistic for that particular season, however their impact, leadership, non-statistical contribution to the team, and also the team’s success also plays a role for players to win the MVP. Hence, it is difficult for a machine learning model to fully predict and accurately predict a MVP winner for the NBA because there’s just too many variables and external factors that have to be weighed in by the actual selection committee. Sometimes there are also human and emotional factors that weigh into the actual decisions in sports and especially in the NBA, which could not be predicted by a computer with data and statistics only.

## **Conclusion**

| Model                   | Average MAE | Average R Squared | Accuracy |
| ----------------------- | ----------- | ----------------- | -------- |
| Linear Regression       | 0.145281    | 0.471695          | 0.642857 |
| Random Forest Regressor | 0.104024    | 0.607992          | 0.738095 |
| XGBoost Regressor       | 0.107421    | 0.586598          | 0.761905 |

As shown above in the table, the accuracy of models for predicting NBA MVP players, the linear regression model achieved a 64% accuracy, while the random forest model showed improvement with 73%, and the XGBoost model surpassed both, reaching 76%. Overall, we have found that the XGBoost models performed the best. However, we have observed that the accuracy of the models is relatively consistent across all three models, which indicates that the models are not exhibiting any bias and are performing consistently across all selected features. We were initially surprised to note that XGBoost did not perform as strongly as we had hypothesized, since XGBoost is the most suitable option for handling non-linearly separable datasets. In the future, we would like to explore other models such as LightGBM to see if we can achieve a higher accuracy. Additionally, we would like to explore other methods of preprocessing the data, such as using PCA or using a different method of dimensionality reduction.

## **Peer Reviewed References**

1. **The application of machine learning and deep learning in sport: predicting NBA players’ performance and popularity** \
   _Summary_: \
   This study focuses on using data analysis techniques to predict players' future performance and their likelihood of being selected for the NBA All-Star game, a prestigious event in the National Basketball Association (NBA) league. Traditional Machine Learning and Deep Learning methods were applied for prediction. However, Deep Learning's performance was found to be less effective due to the relatively small and structured dataset with limited predictor variables. The results, obtained through Regression and Classification Analysis, showed that scoring is the most crucial factor for primary players in any team, and it significantly influences a player's popularity.

   The NBA is a highly profitable sports league, and this study aimed to evaluate the application of Machine Learning and Deep Learning in analyzing basketball player data. The study's objectives included predicting players' future performance and their popularity, particularly their selection for the NBA All-Star game. The popularity of players has a significant impact on their franchises' brands and the league's overall revenue. The research applied CRISP-DM methodology, which consists of six phases, to construct ML and DL models, with a focus on the first five phases. The study also discussed the limitations of using Deep Learning on relatively small and structured datasets for basketball data analysis.

   _Reference_: \
   Nguyen, H. N., Nguyen, D. T. A., Ma, B., & Hu, J. (2022). The application of machine learning and deep learning in sport: Predicting NBA players’ performance and popularity. Journal of Information and Telecommunication, 6(2), 217-235. https://doi.org/10.1080/24751839.2021.1977066

2. **Predicting NBA Players Performance** \
   _Summary_: \
   Predicting outcomes in sports and athlete performances is an ideal domain for machine learning due to the wealth of readily available data in major leagues like the NBA, NFL, and MLB. These sports offer data that is often randomly distributed, making it an appealing dataset for prediction. The NBA, in particular, stands out for machine learning applications because player performance across various positions can be assessed using the same set of statistics, unlike sports like the NFL where different positions are evaluated using distinct metrics. Furthermore, the use of machine learning for predicting individual athlete performances naturally extends to forecasting game outcomes. By predicting the scoring abilities of each player and aggregating them, it becomes possible to create an accurate win-loss classifier. This project aimed to develop a model using linear regression (with Naïve Bayes and SVM implementations for comparison) to predict the number of points NBA players would score against a given opponent.

   _Reference_: \
    Wheeler, K. (n.d.). Predicting NBA Player Performance. Stanford University. Retrieved October 5, 2023, from https://cs229.stanford.edu/proj2012/Wheeler-PredictingNBAPlayerPerformance.pdf

3. **Predicting the Outcomes of NBA Games** \
   _Summary_: \
   This paper speaks about the use of machine learning algorithms to predict the outcome of NBA games. The study used a supervised learning model. They evaluated the player and team performances using team efficiency indices. During the comparisons, the observed team was rewarded for each selected feature that it outperformed its rival. The model used data from the 2014-2018 NBA seasons. The average accuracy of the algorithm was 66% with an optimal accuracy of 78%

   _Reference_: \
    Horvat, T., Job, J., Logozar, R., & Livada, Č. (2023). A Data-Driven Machine Learning Algorithm for Predicting the Outcomes of NBA Games. Symmetry, 15(4), 798. https://doi.org/10.3390/sym15040798

## **Proposed Timeline**

This is [our proposed timeline](https://docs.google.com/spreadsheets/d/1ZIS8XA_fs862QNVlRjXboMSVjAnlntGr/edit#gid=1490824648)

## **Contribution Table**

| Name                    | Contribution                                                |
| ----------------------- | ----------------------------------------------------------- |
| Abdul-Falik Assa        | Data Visualization, Final Presentation PPTX, Conclusion     |
| Alexus Bernard Brooklyn | Data Visualization, Final presentation PPTX, Conclusion     |
| Parker Sargis Hakobyan  | Final presentation pptx, Result and Discussions, Conclusion |
| Rafy Muhammad Akbar     | Final presentation pptx, Results and Discussions, Github    |
| Wentao Yue              | Methods, Final presentation pptx, Result and Discussion     |

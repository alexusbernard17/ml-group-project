---
#
# By default, content added below the "---" mark will appear in the home page
# between the top bar and the list of recent posts.
# To change the home page layout, edit the _layouts/home.html file.
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
#
layout: base
---

[Introduction/Background](#introductionbackground) \
[Problem Definition](#problem-definition) \
[Methods](#methods) \
[Potential Results and Discussions](#potential-results-and-discussions) \
[Peer Reviewed References](#peer-reviewed-references) \
[Proposed Timeline](#proposed-timeline) \
[Contribution Table](#contribution-table) \
[Checkpoint](#checkpoint) \
[Presentation Video](#presentation-video)

## **Introduction/Background**

We will be working on a ML project where we are predicting an NBA Player’s Performance. We will mainly focus on predicting their points for specific games. So far, some research and implementation have been performed to predict a player’s performance, however there is no solid evidence if it has actually been implemented by real professionals and NBA Team’s Front Offices. We were inspired by the research conducted by Kevin Wheeler and the documentation he provided. The dataset we currently plan to use will be a combination of the player’s stats (per game), as well as the team and opponent’s team stats. We will cover this more in depth on the methods section.

## **Problem Definition**

Basketball Player Evaluation Metrics are essential for analyzing NBA players' performances objectively. They break down a player's contributions into categories like scoring efficiency, individual value, and adjust plus-minus, providing insights for coaches and teams to make informed decisions. These metrics aid in player development and strategic planning. They also facilitate fair player comparisons, crucial in the diverse NBA. Metrics influence contract negotiations, scouting, and the draft, helping identify talent. Moreover, they engage fans by offering insights beyond on-court actions, enriching the overall experience.

## **Methods**

$$ \theta=(X^T X)^{-1}X^T y $$

We are planning to use linear regression to predict the number of points each player would score against a specific opponent, as indicated by the equation. The training dataset encompassed statistics from all games played by each player over the past three seasons. In the equation, represented the parameter vector, X was the training set with rows representing each game and columns as features, and y represented the training outcomes. After calculating regression parameters for each player using their three-season game data, these parameters were used to predict scoring outcomes against future opponents. The dataset we will be using is going to be a combination of the player’s statistics, team’s statistics, and opponent’s statistics which will be covered in more detail on the Checkpoint section.

We are planning to utilize the sckit-learn library to calculate and perform the linear regression calculations for our prediction, as well as the Basketball Reference API to get these datasets.

## **Potential Results and Discussions**

By the end of development, this algorithm should have a prediction accuracy of at least 50 percent for each player performance category, measured using standard classification metrics. We will test this model during the upcoming NBA season. The insights gained from our model can be valuable to NBA teams, sports bettors, and fantasy sports enthusiasts. The predictions made by our model will be biased by past historical data and will not take into account unforeseen events such as injuries, suspensions, etc.

## **Peer Reviewed References**

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
    [https://cs229.stanford.edu/proj2012/Wheeler-PredictingNBAPlayerPerformance.pdf](https://cs229.stanford.edu/proj2012/Wheeler-PredictingNBAPlayerPerformance.pdf)

3. **Predicting the Outcomes of NBA Games** \
   _Summary_: \
   This paper speaks about the use of machine learning algorithms to predict the outcome of NBA games. The study used a supervised learning model. They evaluated the player and team performances using team efficiency indices. During the comparisons, the observed team was rewarded for each selected feature that it outperformed its rival. The model used data from the 2014-2018 NBA seasons. The average accuracy of the algorithm was 66% with an optimal accuracy of 78%

   _Reference_: \
    T. Horvat, J. Job, R. Logozar, and Č. Livada, “A Data-Driven Machine Learning Algorithm for Predicting the Outcomes of NBA Games,” Symmetry, vol. 15, no. 4, p. 798, Mar. 2023, doi: 10.3390/sym15040798

## **Proposed Timeline**

This is [our proposed timeline](https://docs.google.com/spreadsheets/d/1ZIS8XA_fs862QNVlRjXboMSVjAnlntGr/edit#gid=1490824648)

## **Contribution Table**

| Name                    | Contribution                               |
| ----------------------- | ------------------------------------------ |
| Abdul-Falik Assa        | Potential Results & Discussions, Research  |
| Alexus Bernard Brooklyn | Introduction/Background, Methods, Research |
| Parker Sargis Hakobyan  | Video                                      |
| Rafy Muhammad Akbar     | Github Page, Research                      |
| Wentao Yue              | Problem Definition, Research               |

## **Checkpoint**

This is an example of a dataset we will be using for our project. In this example, we will be looking at LeBron James’ stats for the past 3 seasons and the team’s stats as well.

- LeBron James 2020-2021, 2021-2022, 2022-2023 Season Player Stats [(Reference)](https://www.basketball-reference.com/players/j/jamesle01.html)
- Los Angeles Lakers 2020-2021 Season Team Stats [(Reference)](https://www.basketball-reference.com/teams/LAL/2022.html)
- Los Angeles Lakers 2021-2022 Season Team Stats [(Reference)](https://www.basketball-reference.com/teams/LAL/2022.html)
- Los Angeles Lakers 2022-2023 Season Team Stats [(Reference)](https://www.basketball-reference.com/teams/LAL/2022.html)

Dataset we currently plan on using:

1. **Team Stats**

   - Pace: Average possessions per game
   - OPTS: Opponents points scored
   - OFG%: Opponents field-goal %
   - OTOR: Opponents turnover rate
   - DRR: Percentage of defensive rebounds made
   - O%Rim: Opponents shots taken near rim
   - O%Short: Opponents shots taken within 10 feet
   - OXeFG%: Expected FG% allowed
   - OeFG%: Effective FG% allowed
   - TRR: Total rebound rate

2. **Player’s Stats**

   - MINS: Minutes played
   - FGA: Shots attempted
   - FTA: Free throw shots attempted
   - eFG%: Effective FG% (weighted for 3PA)
   - TS%: True FG% (adj. for FT and 3PA)
   - OffRtg: Offensive rating (measure of points produced per 100 possessions)

## **Presentation Video**

# DataScienceBlog
Udacity Data science blog post project files

## Motivation

The purpose of this repository is to present my workings for the Udacity Data Science Nano degree Data Blog Assignment.

I wanted to take a look at what factors cause people to respond as being happy. The happiness survey is a survey done for eacxh country which presents a few metrics and shows how these metrics influence the happiness score. By Analysing the data I wanted to see if factors influencing happiness stay constant through time as well as look at the size of impact. Can happiness be predicted and what do people need in order to be happy?

I've looked at the dataset overall but an interesting hypothesis to look at further could be seperating this data by GDP, as it appears at lower income Generosity is a major factor but in higher income countries it appear to be GDP per capita.

## The data

The source of the data for these files were from Kaggle:
https://www.kaggle.com/unsdsn/world-happiness

The data is separated into 5 csv files, one for each year from 2015 to 2019. Happiness has been determined in these csv by the following:
  1. Perception of government trust
  2. Generosity
  3. GDP per capita
  4. Health/life expectancy
  5. Social Support
  6. Freedom to make life choices

Each of these factors are given a score by country by how much they impact a happiness score.

## Preparation of data

There was only one null value in the entire set based on corruption for the year 2018. I took the mean of the column and inserted in. The reason is in the fdile there is little variance in that factor so by taking the mean it should not materially skew the results. 
Each csv had slightly different headings and so I made assuptimons. For example Family was in 2015 but in 2019 they removed that column and added one called Social Support. I understood the two to be similiar. It was clear that the surveys were trying to convey the same metric but the measurement has become more specific with time. 
I made these assumptions in order to append the data sets to run a full regression over time.

## Modelling the data

By fitting a linear regression model, I obtained R scores of 1. This suggested that the data explaained the scores in their enitirety. I also looked at the correlation co-efficients to see if I could find anything about the income and its impact on the models. As the model was based on other models I used a test split of 30% for the data and used most of the data for training the model.

## Evaluation

I discovered through the analysis that the factors did change over time. The most consistently highly weighted factor was the perception of government corruption and freedom to make life choices. The less corruption was perceived and the more freedom over life choices the better the happiness score. The 2016 dataset however stood out in that perception of corruption was the lowest factor whereas in all other years it was the highest.
This is consistent with the findings when appending all the years.
Looking at correlation it showed that generosity and GDP per capita were negatively ocrrelated. It appears that the wealthier countries put more weighting on GDP but less on generosity, whereas the lower income countries have generaosity as a major factor in their happiness score.





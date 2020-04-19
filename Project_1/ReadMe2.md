# Project 1: SAT & ACT Analysis 

## Problem Statement

Both ACT and SAT scores are used for college admissions decisions and granting scholarships in United States. It seems that ACT is taking the lead in participation rates. 
As the new format for the SAT was released in March 2016, this project will examine the newly formatted SAT and ACT in terms of aggregate SAT and ACT scores and participation rate in 2017 and 2018 from each state of United States. Once we have identified the correlations or underlying patterns amongst the participation rate and scores of both tests systems, we will recommend about how the College Board might work to increase the participation rate in a state.

## Executive Summary

---
### Datasets
We will use two provided datasets for this project:
- [2017 SAT Scores](https://github.com/PeggyMan/DSI_projects/blob/master/Project_1/data/sat_2017.csv)
- [2017 ACT Scores](https://github.com/PeggyMan/DSI_projects/blob/master/Project_1/data/act_2017.csv)

The data are about the average SAT and ACT scores by state, as well as participation rates in 2017.

the source for the SAT data [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/), and the source for the ACT data [here](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows). 

#### Additional Data
For the data of the average SAT and ACT scores by state, and participation rates in 2018.
2018 state-by-state average results and participation for the SAT are available in PDF reports [here](https://reports.collegeboard.org/sat-suite-program-results/state-results). 2018 ACT state-by-state mean composite scores and participation rates are [here](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf) .

#### Data Dictionary
| Feature                   | Type   | Dataset   | Description                                                  |
| ------------------------- | ------ | --------- | ------------------------------------------------------------ |
| State                     | object | SAT & ACT | The name of 50 states in the United States of America.       |
| sat17_participation       | float  | SAT       | The percent of students taking SAT in 2017                   |
| sat17_reading and writing | float  | SAT       | The average English combination of reading and writing score of each state in 2017 Scored between 200 and 800. |
| sat17_math                | float  | SAT       | The average Mathematics score of each state. Scored between 200 and 800. |
| sat17_total               | float  | SAT       | The average total score (combining Evidence-based Reading and Writing and Math)of each state. Max score is 1600. |
| act17_participation       | float  | ACT       | The percent of students of each state taking ACT in 2017     |
| act17_english             | float  | ACT       | The average English score of each state in 2017 Scored scale from 1 to 36. |
| act17_math                | float  | ACT       | The average Mathematics score of each state in 2017 Scored scale from 1 to 36. |
| act17_reading             | float  | ACT       | The average Reading score of each state in 2017 Scored scale from 1 to 36. |
| act17_science             | float  | ACT       | The average Science score of each state in 2017 Scored scale from 1 to 36. |
| act17_composite           | float  | ACT       | The average of score of four section (consisting of English,Math,Reading,Science)of each state, also on a scale from 1 to 36. |




## Conclusions and Recommendations
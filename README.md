# **Project 1: SAT & ACT Analysis**

**Table of Content:**

* [Problem Statement](#Problem-Statement)
* [Executive Summary](#Executive-Summary)
  * [Recommendation](#Recommendation)
  * [Datasets](#Datasets)
  * [Data Dictionary](#Data-Dictionary)
* [Conclusions and Suggestions](#Conclusions-and-Suggestions)
  * [Suggestions](#Suggestions)



## **Problem Statement**

Both ACT and SAT scores are used for college admissions decisions and granting scholarships in United States. It seems that ACT is taking the lead in participation rates.  We have to increase the participation rate of SAT. 

As the new format for the SAT was released in March 2016, this project will examine the newly formatted SAT and ACT in terms of aggregate SAT and ACT scores and participation rate in 2017 and 2018 from each state of United States. 



## **Executive Summary**

We have identify the correlations or underlying patterns amongst the participation rate and scores of both tests systems by cleaning data,  visualising the statistics number, like the mean, minimum and maximum rate of the participation,  by using different types of charts.

We have 3 key findings:
- Inverse correlation of participation rate and the total/composite score. When we consider a state to increase participation rate, we have to also monitor the total score. 
- The higher ACT particiption, the lower SAT particiption. 
- States in midwest tends to dominated ACT and the coastal states are more likely to have high participation rate.



### Recommendation

We would recommend to increase the participation rate of California.  As California has low ACT participation rate, 31% in 2017 and 27% in 2018.  On the other hand, the trend of SAT participation rate in the state is increasing from 53% to 80%. 

Though this is not in the lowest range,  it is still have potential to attract more individuals to take the test due to the high population of the high school students. According to SAT annual report of California, the number of high school students is 431,009. 

On the contrast, Iowa has low participation rate of 2% in SAT. The number of high school students is 35,032.
Moreover, California is a coastal state so it might be more likely to achieve a higher participation rate.



### Datasets

We will use the following two provided datasets for this project:
- [2017 SAT Scores](https://github.com/PeggyMan/DSI_projects/blob/master/Project_1/data/sat_2017.csv)
- [2017 ACT Scores](https://github.com/PeggyMan/DSI_projects/blob/master/Project_1/data/act_2017.csv)

The data are about the average SAT and ACT scores by state, as well as participation rates in 2017. The source for the SAT data is available [here](https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/), and the source for the ACT data is available [here](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows). 

For the data of the average SAT and ACT scores by state and participation rates in 2018. Average state-by-state results and participation for the SAT are available in [this report](https://reports.collegeboard.org/sat-suite-program-results/state-results). 2018 ACT state-by-state mean composite scores and participation rates are [this report](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf).



### Data Dictionary

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



## **Conclusions and Suggestions**

### Suggestions

- Collaborate with the states' department of education. The ultimle goal is to convince the state governemtn accepting  SAT as mandatory test in all schools and sponsorship of exam or study fee. 

- Promote the utility of online SAT practice resoucese like SAT School Day and Khan Academy. 

- Broaden the participant base, we can target on working adults in the community who are interested in taking the test and do not have the support of traditional schooling. Our online resources will be handy. 
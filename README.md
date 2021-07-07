README

# What is the difference between Data Analysts and Data Scientists?


### Overall idea
Understand the difference between the Data Scientist and the Data Analyst role

### Reasoning
For people at the beginning of their career in data, it can be difficult to understand the difference between data scientists and data analysts. Having recently applied again for jobs myself, I got the impression that the definition varied between companies. To get a clear picture of the difference it is therefore necessary to draw insights from a much larger amount of data than the job ads I read during my job search and insights from my interviews. Using the datasets listed above, I am analysing the overlap between the two roles and what tools/tech characterise each job.

### Main questions
* Is Data Analyst and Data Scientist the same role?
* If they are different, what is the difference?
* Do job ads reflect this difference accurately?

### Blog post
I published a blog post that relates to the analyses in this notebook here: XXX
The blog post does not draw on all of the analyses present in this notebook.

### Structure of notebook:
The notebook consists of three main sections:
* Preparations (e.g. importing libraries, reading in the data, defining functions)
* Part 1 - The Stackoverflow Data
* Part 2 - The Kaggle Job Data

##### Part 1 addresses the following questions:
* How distinctive are the Data Analyst and the Data Scientist roles from each other (Question 1.1.1) and from other roles in the wider field (Question 1.1.2)?
* Do tools used by Data Analysts differ from tools used by Data Scientists (Question 1.2)?
* Do tools that Data Analysts and Data Scientists want to use next year differ (Question 1.3)?

Sections 1.1.1, 1.2 and 1.3 each contain a 3-way split analysis and a 2-way split analysis. This refers to the definition of the samples:
* In the **3-way split analysis**, respondents are defined as *Data Analyst only*, *Data Scientist only* and *Data Analyst and Data Scientist*. The "only" means that roles *other* than the Data Analyst/Data Scientist role can still be included, i.e. someone who is a Data Analyst and a back-end Developer still counts as *Data Analyst only*. The 3-way split is necessary to obtain independent samples for Data Analysts and Data Scientists to allow for significance testing.
* In the **2-way split analysis**, repondents are defined as *Data Analyst* and/or *Data Scientist*. A respondent who is both is in both samples. The samples are therefore overlapping, i.e. not independent, and no significance testing was done.

##### Part 2 addresses the following question:
* Do tool/tech requirements in job ads differ for Data Analysts and Data Scientists (Question 2.1)?

### Other questions one could look at
* Stackoverflow: Do people in smaller companies have to take on more different roles?
* Stackoverflow: Do either Data Scientists or Data Analysts wish to use more *new* tools next year?
* Stackoverflow: Does either group want to use more of the tools that are important for the other role next year, indicating that this group seeks to develop into the other role?
* Kaggle: Do tool/tech requirements become more or less similar the more senior a role is?

### Data sources
Link to Stackoverflow dataset: https://insights.stackoverflow.com/survey - downloaded 2020 survey results on 30/06.
Link to Kaggle dataset: https://www.kaggle.com/andrewmvd/data-scientist-jobs from user _Larxel_. Downloaded on 30/06.

### Licensing
The Stackoverflow dataset was published under the Open Database License (ODbL).
The Kaggle Dataset's license was not specified at source.

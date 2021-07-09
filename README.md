README

# What is the difference between Data Analysts and Data Scientists?

### Libraries
The code uses the following libraries:
* numpy
* pandas
* matplotlib.pyplot
* matplotlib_venn
* re
* scipy.stats (ttest_ind_from_stats)
* holoviews (opts, dim) - using bokeh

## Intro
### Overall idea
Understand the difference between the Data Scientist and the Data Analyst role

### Reasoning
For people at the beginning of their career in data, it can be difficult to understand the difference between data scientists and data analysts. Having recently applied again for jobs myself, I got the impression that the definition varied between companies. To get a clear picture of the difference it is therefore necessary to draw insights from a much larger amount of data than the job ads I read during my job search and insights from my interviews. Using the datasets listed above, I am analysing the overlap between the two roles and what tools/tech characterise each job.

### Main questions
* Is Data Analyst and Data Scientist the same role?
* If they are different, what is the difference?
* Do job ads reflect this difference accurately?

### Results
I published a blog post that relates to the analyses in this notebook here: XXX
The blog post does not draw on all of the analyses present in this notebook.

In summary, the data shows that Data Analyst and Data Scientist roles are rather distinct from each other. They are differentiated in their usage of tools/tech, where Data Analysts are heavier on SQL, BI tools/dashboards and Excel, and Data Scientists use more Python and Machine Learning tools.

## File descriptions
This repository contains one notebook in the 'code' folder, the .gitignore and the README. See below to how to best set yourself up to run the notebook.

## How to use this notebook:
### Setting yourself up to run the notebook
You need to download the data if you want to run the notebook. Please create a directory called 'data' that is at the same level as 'code' directory. Create a directory within 'data' called 'stackoverflow_survey' and save the datafile from Stack Overflow as *survey_results_public.csv* in it. Create a second directory withon 'data' called 'kaggle_ds_jobs' and save the datafile from Kaggle as *DataScientist.csv* in it.

### Structure of notebook:
The notebook consists of three main sections:
* Preparations (e.g. importing libraries, reading in the data, defining functions)
* Part 1 - The Stack Overflow Data
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
* Stack Overflow: Do people in smaller companies have to take on more different roles?
* Stack Overflow: Do either Data Scientists or Data Analysts wish to use more *new* tools next year?
* Stack Overflow: Does either group want to use more of the tools that are important for the other role next year, indicating that this group seeks to develop into the other role?
* Kaggle: Do tool/tech requirements become more or less similar the more senior a role is?

## Data
### Data sources
Link to Stack Overflow dataset: https://insights.stackoverflow.com/survey - downloaded 2020 survey results on 30/06.
Link to Kaggle dataset: https://www.kaggle.com/andrewmvd/data-scientist-jobs from user _Larxel_. Downloaded on 30/06.

### Licensing, Authors, Acknowledgement
Must give credit to Stack Overflow for the data. The Stack Overflow dataset was published under the Open Database License (ODbL).
The data in the Kaggle dataset is web scraped and provided for open use by the Author under MIT License.

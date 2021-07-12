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
I published a blog post that relates to the analyses in this notebook here:
https://medium.com/@leopold.judith/whats-the-difference-between-data-analysts-and-data-scientists-28533910d9c0
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

## Further References
You can also find these references directly in the code, where the respective snippets are marked.

**Acknowledgement for use of libraries:**
**numpy**
Harris, C.R., Millman, K.J., van der Walt, S.J. et al. "Array programming with NumPy", Nature 585, 357–362 (2020). DOI: 0.1038/s41586-020-2649-2.

**pandas**
Jeff Reback, jbrockmendel, Wes McKinney, Joris Van den Bossche, Tom Augspurger, Phillip Cloud, … chris-b1. (2021, June 22). pandas-dev/pandas: Pandas 1.2.5 (Version v1.2.5). Zenodo. http://doi.org/10.5281/zenodo.5013202

Data structures for statistical computing in python, McKinney, Proceedings of the 9th Python in Science Conference, Volume 445, 2010, p.56 - 61, editors: Stefan van der Walt and Jarrod Millman. DOI: 10.25080/Majora-92bf1922-00a

**matplotlib**
J. D. Hunter, "Matplotlib: A 2D Graphics Environment", Computing in Science & Engineering, vol. 9, no. 3, pp. 90-95, 2007. DOI: 10.5281/zenodo.4475376

**re**
Van Rossum, G. (2020). The Python Library Reference, release 2021.7.6. Python Software Foundation.

**holoviews**
Philipp Rudiger, Jean-Luc Stevens, James A. Bednar, Bas Nijholt, Jon Mease, Andrew, … Lukas Barth. (2021, May 20). holoviz/holoviews: Version 1.14.4 (Version v1.14.4). Zenodo. http://doi.org/10.5281/zenodo.4775303

**matplotlib_venn**
Konstantin Tretyakov. Published under MIT license, release 0.11.6. Python Software Foundation.

**scipy**
Pauli Virtanen, Ralf Gommers, Travis E. Oliphant, Matt Haberland, Tyler Reddy, David Cournapeau, Evgeni Burovski, Pearu Peterson, Warren Weckesser, Jonathan Bright, Stéfan J. van der Walt, Matthew Brett, Joshua Wilson, K. Jarrod Millman, Nikolay Mayorov, Andrew R. J. Nelson, Eric Jones, Robert Kern, Eric Larson, CJ Carey, İlhan Polat, Yu Feng, Eric W. Moore, Jake VanderPlas, Denis Laxalde, Josef Perktold, Robert Cimrman, Ian Henriksen, E.A. Quintero, Charles R Harris, Anne M. Archibald, Antônio H. Ribeiro, Fabian Pedregosa, Paul van Mulbregt, and SciPy 1.0 Contributors. (2020) SciPy 1.0: Fundamental Algorithms for Scientific Computing in Python. Nature Methods, 17(3), 261-272.

**Acknowledgements for use of entries in forums, blogs and similar:**

Please find the according sections in the code marked with the respective number

Please note that Stack Overflow content is is publicly accessible under the Creative Commons Attribution-ShareAlike license, more information can be found here: https://stackoverflow.com/help/licensing

{1} Source: Stack Overflow Question by Boris, 18/03/2021. Profile: https://stackoverflow.com/users/3064538/boris Answer by Alex Martelli, 04/06/2021. Profile: https://stackoverflow.com/users/95810/alex-martelli Link to question: https://stackoverflow.com/questions/952914/how-to-make-a-flat-list-out-of-a-list-of-lists

{2} Source: Stack Overflow Question by mkln, 19/09/2013. Profile: https://stackoverflow.com/users/2775630/mkln Answer from offbyone, 08/708/2014. Profile: https://stackoverflow.com/users/2808975/offbyone Link to question: https://stackoverflow.com/questions/18889588/create-dummies-from-column-with-multiple-values-in-pandas

{3} Source: Programming education website finxter, no date: "Python endswith() Tutorial - Can we use regular expressions?" Blog entry by Dr. Christian Mayer: https://blog.finxter.com/regex-endswith-python/

{4} Source: Stack Overflow Question by thatMeow, 17/12/2016. Profile: https://stackoverflow.com/users/7292363/thatmeow Answer by Psidom, 18/12/16. Profile: https://stackoverflow.com/users/4983450/psidom Link to question: https://stackoverflow.com/questions/41203959/conditionally-format-python-pandas-cell

{5} Source: Stack Overflow Question by TheyChymera, 17/11/2013. Profile: https://stackoverflow.com/users/1893275/thechymera Answer by Cleb, 24/04/2018. Profile: https://stackoverflow.com/users/1534017/cleb Link to question: https://stackoverflow.com/questions/20025882/add-a-string-prefix-to-each-value-in-a-string-column-using-pandas

{6} Source: scentellegher, 10/10/2018: "Beautiful bar plots with matplotlib" Blog entry by Simone Centellegher: https://scentellegher.github.io/visualization/2018/10/10/beautiful-bar-plots-matplotlib.html

{7} Source: Stack Overflow Question by Tuutsrednas, 06/02/17. Profile: https://stackoverflow.com/users/7508150/tuutsrednas Answer by Ramon, 03/05/2020. Profile: https://stackoverflow.com/users/10647085/ramon

{8} Source: holoviews.org Documentation of how to create a chord chart with example: https://holoviews.org/reference/elements/bokeh/Chord.html

{9} Source: CoderzColumns, 12/07/2020: "How to Plot Chord Diagram in Python [holoviews]?" Used to understand design options for chord chart, specifically node color Blog entry by Sunny Solanki: https://coderzcolumn.com/tutorials/data-science/how-to-plot-chord-diagram-in-python-holoviews

{10} Source: GitHub Question by brettChapman, 23/10/2018. Profile: https://github.com/brettChapman Answered by philippjfr, 26/11/2018. Profile: https://github.com/philippjfr Link to question: https://github.com/holoviz/holoviews/issues/3097

{11} Source: Stack Overflow Question by user3084006, 13/12/2013. Profile: https://stackoverflow.com/users/3084006/user3084006 Answer by alko, 13/12/2013. Profile: https://stackoverflow.com/users/1265154/alko Link to question: https://stackoverflow.com/questions/20574257/constructing-a-co-occurrence-matrix-in-python-pandas

{12} Source: Stack Overflow Question by EmJ, 12/08/2019. Profile: https://stackoverflow.com/users/10704050/emj Answer by jezrael, 12/08/2019. Profile: https://stackoverflow.com/users/2901002/jezrael Link to question: https://stackoverflow.com/questions/57456069/how-to-convert-a-co-occurrence-matrix-to-networkx-graph

{13} Source: Stack Overflow Question by user1083734, 02/07/2013. Profile: https://stackoverflow.com/users/1083734/user1083734 Answer by Kirell, 30/11/2015. Profile: https://stackoverflow.com/users/699854/kirell Link to question: https://stackoverflow.com/questions/17426292/what-is-the-most-efficient-way-to-create-a-dictionary-of-two-pandas-dataframe-co

{14} Source: Stack Overflow Question by Darknight, 19/12/2012. Profile: https://stackoverflow.com/users/929894/darknight Answer by Martijn Pieters, 19/12/2012. Profile: https://stackoverflow.com/users/100297/martijn-pieters Link to question: https://stackoverflow.com/questions/13954841/sort-list-of-strings-ignoring-upper-lower-case

{15} Source: Stack Overflow Question by Vishal K Nair, 28/01/2018. Profile: https://stackoverflow.com/users/6485714/vishal-k-nair Answer by Andrew Hare, 28/01/2018. Profile: https://stackoverflow.com/users/34211/andrew-hare Link to question: https://stackoverflow.com/questions/48488712/case-insensitive-regex-in-python

**Acknowledgements for websites used to create tool list:**

no author, no date, Datapine.com: https://www.datapine.com/articles/best-bi-tools-software-review-list

Rinu Gour, 22/05/2019, "Top 5 BI Tools Widely used for Data Visualization" in towards data science: https://towardsdatascience.com/top-5-bi-tools-that-you-must-use-for-data-visualization-7ccc2a852bd3

Peter Sayer and Thor Olavsrud, 15/01/2021, "Top 12 BI tools of 2021" on CIO: https://www.cio.com/article/3322749/top-business-intelligence-bi-tools.html

Bernard Marr, 22/05/2020, "The 9 Best Analytics Tools For Data Visualization Available Today" on Forbes: https://www.forbes.com/sites/bernardmarr/2020/05/22/the-9-best-analytics-tools-for-data-visualization-available-today/?sh=36ebb06a4743

Pam Baker, 15/03/2015, "The Best Data Visualization Tools for 2020" on pcmag: https://uk.pcmag.com/cloud-services/83744/the-best-data-visualization-tools-for-2020

Erin Gilliam Haije, 06/11/2019, "Top 15 Business Intelligence Tools in 2021: An Overview" on mopinion.com: https://mopinion.com/business-intelligence-bi-tools-overview/

no author, no date, "Top Rated Business Intelligence (BI) Products" on trustradius.com: https://www.trustradius.com/business-intelligence-bino

no author, no date, "Statistical Analysis Software" on Capterra.com: [Selection] https://www.capterra.com/statistical-analysis-software/

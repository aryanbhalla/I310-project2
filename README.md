****                      **PROJECT 2- DATA BIAS**


**INTRODUCTION**
 
 Bias is ever present in all forms of data, big and small. It exists in various forms, and can be explicit or implicit. The aim of this project is to test data for potential biases, using simple data manipulation techniques and hypothesis testing. The data has been sourced from Perspective API, which was created by researchers using an algorithm which was trained using machine learning. The aim of the API was to score comments across the internet for a toxicity score, which was arrived at using human made parameters. The algorithm was fed comments made by users from various sources across the internet, including but not limited to The New York Times and Wikipedia forums. These comments range in the thousands, varying in languages.
  Each of these comments was scored using the following parameters: toxicity, severe toxicity, obscentiy, threats, insults and identity hate. These paramters were then used to arrive at an aggregate toxicity score as a probability, ranging from 0 to 1. The higher the rating of the comment, the more likely it is that a user who reads the comment will find it toxic and want to leave the conversation.
  The makers of the API, the Perspecitve team, have acknowledged the errors they have made in training the algorithm. Additionally, the interpretation of bias is something that has deliberately been left subjective in the analysis of this project. The hypothesis introduced has been analyzed and then linked to the presence of bias. However, for the purpose of this project, a qualitative analysis on bias has been made, considering the fact that the parameters used vary in importance from person to person.
  
 
**API Documentation: 
****The data presented here was collected through a Google form and processed through a .CSv file. As a result, there is no API licensing to report.

**License**: 
**The following data is protected by an MIT license on the GitHub repository of the author. The source data was collected through Perspective API and is protected by known licensing agreements, including those in place with Alphabet inc. and its subsidiaries.

**ANALYSIS**
    To test the API for bias, a hypothesis was used. Based on the given parameters of toxicity, severe toxicity, obscene, insult and identity hate, the data was given a toxicity score, as mentioned above. Data manipulation was performed in order to explore the dataset and set up a viable hypothesis for testing. After reading the API into the notebook, code was written to get the toxicity score of indivdual comments, as well as to return the mean toxicity score across all comments. Additional data parsing operations, such as finding out the number of all comments, and finding correlations between different parameters, alongside manual inspection of the data, was done. After analysis of the findings, the hypothesis arrived at was the following: The toxicity score of a comment decreases with the character length of a comment.
    
Before importing the data frame into the Jupyter Notebook and performing an analysis, a manual inspection of the data was done. During this process, some discrepancies between the data was found. 

**BIAS IN THE DATA**
    Although performance based on different data sets was not looked at, inspection of the data as well as the hypothesis revealed some interesting findings. One thing that was noticed in the data was that some words that could objectively be classified as hate speech or as insults were not given scores in those parameters. Additionally, another thing that was seen was that the algorithm had trouble distinguishing paramteres that were impleied rather than explicitly stated. the algorithm also failed if users would write comments that would not explicitly use swear words but were still high in some of the toxicity parameters.
    What we also found was that the distribution of toxicity in the data was highly concentrated in comments that were shorter in length. Bias in the data is prevalent in multiple forms, and there were numerous entries that were given a higher toxicity score than necessary and which I disagreed with.
    To get a better idea of the data, some simple data parsing and manipulation techniques were performed. The data frame improted into Python was sorted by score, and then a code was implemented to get the toxicity score of individual comments for the purposes of research. Following that, other relationships were tested for bias, such as the comments which were socred for both toxic and severe toxic parameters. The mean of all scores was also calculated, and so was the correlation between the toxicity score and all parameters.
    As mentioned by the Perspective development team, the algorithm was trained on comments made on the New York Times and Wikipedia comments. Based on public documentation, looking at the results as well as data examination, it can be inferred that the bias in the data comes from an exhaustive data set limited to few platforms. While innovative and useful, the bias could be better tackled if data were to be brought in from other sources.
    
    
**    **HYPOTHESIS TESTING****
Based on the above findings, the pearson correlation between scores and parameters, as well as the mean toxicity score, which was 0.24, the threshold established above which scores were considered toxic was 0.4. When the relationshi between character length and toxicity score was plotted, it was discovered that toxicity scores started trending downward. This led to the hypthosesi discussed:
As character length increases, the toxicity score tends to decrease.
In order to test this hypothesis, a linear regression was run with string length as the explantory and score as the response variables respectively. The resulting line of best fit was a horizontal line through data which led to not many outliers. The graph, found in the notebook, can also be seen below:



![image](https://user-images.githubusercontent.com/99366030/157987377-96227e83-58d1-444d-b594-3f427812307c.png)

However, to verify the results, a dummy regression was run. However, the dummy variable returned a line of best fit much more different than the one found in the initial set of variables:


![image](https://user-images.githubusercontent.com/99366030/157987624-42801124-4582-4799-a2be-8db5bb02e0b3.png)

This revealed no concrete relationship betweem character length and toxicity score.


**RESULTS**
The hypothesis test found that there was no linear relationship between character length and toxicity score. The line of best fit was horizontal and the dummy regression did not match up with the original. The best estimate is the toxicity score is dispersed all around the probability range, and has nothing to do with character length, thus disproving the hypothesis.

The theory I have as to why the result turned out this way was that I assumed looking at the correlation between parameters and through data parsing that there was some relationship between character length and variables, which turned out to be ill founded. The hypothesis test revelaed the bias and disproved my findings. For more accuracy, the entire toxicity score column was used as a subset of the entire data.

**CONCLUSION**
In summation, there was bias found in the data. I felt as though some labels were misrepresented, and that bias in the model existed due to the algorithm feeding off comments from limited sources. The hypothesis of lesser toxicity scores with longer comments was disproven, and the degree of bias that exists in the data is subjective, varying from person to person.

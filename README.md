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
    
Before importing the data frame into the Jupyter Notebook and performing an analysis, a namueal inspection of the data was done. During this process, some discrepancies between the data was found. 

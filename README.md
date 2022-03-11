**INTRODUCTION**
  Bias is ever present in all forms of data, big and small. It exists in various forms, and can be explicit or implicit. The aim of this project is to test data for potential biases, using simple data manipulation techniques and hypothesis testing. The data has been sourced from Perspective API, which was created by researchers using an algorithm which was trained using machine learning. The aim of the API was to score comments across the internet for a toxicity score, which was arrived at using human made parameters. The algorithm was fed comments made by users from various sources across the internet, including but not limited to The New York Times and Wikipedia forums. These comments range in the thousands, varying in languages.
  Each of these comments was scored using the following parameters: toxicity, severe toxicity, obscentiy, threats, insults and identity hate. These paramters were then used to arrive at an aggregate toxicity score as a probability, ranging from 0 to 1. The higher the rating of the comment, the more likely it is that a user who reads the comment will find it toxic and want to leave the conversation. In the project, the 

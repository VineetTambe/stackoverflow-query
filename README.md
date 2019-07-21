# stackoverflow-query
This program is aimed towards resolving the issue of some query getting 0 results when searched in stackOverFlow

Let’s start with downloading required packages and importing modules. 
We also define constants like ‘k’ for limiting number of solutions and SITE that refers to ‘Stack Overflow’.

We have tried to make the workflow of our program to match that of the StackOverflow website itself.
Therefore, we ask the user for search query. 
Once we get the query, the program extracts tags or keywords from it.
These tags then are used to get questions with the help of StackAPI. Here in the program, we have printed the list of titles of all the questions.
These question titles will be further sorted based on their text similarity score with the user entered query. Then these will be finally displayed to the user in sorted order. As per the website, the output mainly includes the question title, and question body. We also display the question ID in the program to help the user select a question. 
Now, the user selects the question he or she wants the answer for.

We start by fetching list of all the answers to the question selected by the user using StackAPI. We apply filter to obtain the comment body in the JSON object received. 
Then we analyse the comments for their sentiments and obtain a score for each answer. 
We further sort these answers based on the score. 
Finally, we display the question and corresponding list of answers, with their IDs and body,  sorted as they’d appear on the website. 

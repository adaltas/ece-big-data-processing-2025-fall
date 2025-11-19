# Final Project

This is a project doing some basic data analysis of IMDB movie data and associated wiki streaming events. It should be completed by groups of no less than 2 students and no more than 4 students. Each member of the group should have at least a few commits associated in the project repo.  

## Scoring

The code must run and provide the correct answers . 1/2 points  
The remainder will come from notebook organization, code comments, etc .  
For the questions that have answers, please also provide those in markdown cells in the notebook, and/or part of a markdown file in the repo .  
All relevant code should be shared via a shared Git repository. Additionally, you will send an email to joe@adaltas.com when the project has been submitted . Please ensure that the names of all participants are included in the repo and in the submission email . **Note:** For full credit the code must run with little to no extra input from the end user, and, any extra input that is required must be clearly documented and explained. Also note, any question that is at least attempted will be awarded with partial credit provided there is a corresponding explanation of the difficulties faced. 

## Questions
1. [load data from here](https://datasets.imdbws.com/). This should be done using a notebook cell and not a manual process to import the data. For some of the datasets you may get an error that the file is too big. It is acceptable to load these manually if needed, please note files that are expected to be added manually.  
**NOTE:** You may not need all of the datasets, but you will be utilizing most of them . 
2. How many total people in data set?
3. What is the earliest year of birth?
4. How many years ago was this person born?
5. Using only the data in the data set, determine if this date of birth correct. 
6. Explain the reasoning for the answer in a code comment or new markdown cell. 
7. What is the most recent date of birth?  
8. What percentage of the people do not have a listed date of birth?
9. What is the length of the longest "short" after 1900?
10. What is the length of the shortest "movie" after 1900?
11. List of all of the genres represented.
12. What is the highest rated comedy "movie" in the dataset? Note, if there is a tie, the tie shall be broken by the movie with the most votes .
13. Who was the director of the movie?
14. List, if any, the alternate titles for the movie.

## Stream Processing

Choose any five entities from the data set. These can be specific movies, actors, crews, etc, or more abstract concepts such as specific genres, etc. The main criteria is that the entities chosen must have a trackable wiki page. Set up a stream processing job that will track events for the chosen entities from the [wikimedia Events Platform](https://wikitech.wikimedia.org/wiki/Event_Platform/EventStreams_HTTP_Service). These tracking jobs should provide some simple metrics. These metrics should be stored in a database or file (depending on the platform used). At least one of the metrics should be of the "alert" type (meaning some event that would require further action. For instance imagine wanting to be notified each time a specific user makes a change. Capture this "alert" and mimic an alerting system by routing these events to a different file/database.)  These tables/data do not need to be shared, but the structure of the output should be clearly noted in the code and/or markdown cells. Additionally, a brief explanation/overview of this section should be provided in a separate markdown cell or in the project readme.

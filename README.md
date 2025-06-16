# Apple Dashboard
Dashboard made for the Apple Board of Directors 
# Table of Contents: #

* Project overview
* Data Source
* Results
* Challenges In Analysis

  ## Project Overview ##
  This data analysis project aims to provide insights into the performance and trends of movies from 2012 to 2016. By analyzing various aspects of the movie data, we seek to identify patterns, make data-driven recommendations, and gain a deeper understanding of the industry's dynamics.

  ## Data Source ##
  Movie Data: The primary dataset used for this analysis is the "Movie Data Homework.xmls" file, containing detailed information about each movie's performance, actors, directors, etc [Movies Data dashboard.xlsx](https://github.com/user-attachments/files/20756204/Homework.10.dashboard.xlsx)

 ## Tools  ##
* Power Query - I used Power Query for Data Cleaning
* Excel, Pivot Tables - I used them for Data Analysis, creating reports and Visualizations
  
## Data Cleaning and Preparation ##
In the initial data preparation phase, we performed the following tasks:

 * Data loading and inspection.
 * Handling errors, missing values.
 * Data cleaning and formatting. The Excel file, after the data cleaning & preparation process, can be downloaded here [Movies Data Ready for Dashboard.xlsx](https://github.com/user-attachments/files/20756475/Movies.Data.Ready.for.Dashboard.xlsx)
   
## Exploratory Data Analysis ##
* Which genres were the most profitable these years?
* Which actors were the most successful?

### Results and Findings ###
As an example: Best profitable movie was: with a Budget of... Box Office Revenue was 102,000,000 USD. The genre of this movie was 
![image](https://github.com/user-attachments/assets/966130fe-c619-43a1-9da7-e68b52f5c09c)

The best actor was... The best director...
![image](https://github.com/user-attachments/assets/071f1f4f-3953-439e-ade5-62d6636526b3)

## Challenges in Analysis ##
### M Language ###
One of interesting features/ challenges I was working with was a specific code for Grouping in M language which enabled me to Combine genres together for further analysis. We had 2 column for genres, but we needed to combine them and have the same format, for example action/comedy, not comedy/action.
``` = Table.Group(#"Sorted Rows1", {"Movie Title"}, 

                                            {{"Combined Genre", each Text.Combine([Concat Genre], " / "), type text},

                                            {"AllData", each _, 

                                type table [Movie Title=nullable text, Release Date=nullable date, Wikipedia URL=nullable text,
Concat Genre=nullable text, Director=nullable text, Actor First=nullable text, Actor Second=nullable text, Actor Third=nullable
 text,Actor Fourth=nullable text, Actor Fifth=nullable text, #"Budget ($)"=nullable number,
 #"Box Office Revenue ($)"=nullable number]}

                                            }
```
## Excel Dashboard ##
Can be downloaded here [Movie Data Dashboard.xlsx](https://github.com/user-attachments/files/20756810/Homework.10.dashboard.xlsx)

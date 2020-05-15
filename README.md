
<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Tarsiers
## Female recognition in the film direction

Project module 01

- Ana Paula Detsch
- Brian Meyer
- Raphaela Sinanovic

Data Analysis 03-20, Berlin, 04/10/2020


## Content

- [Project Description](#project-description)
- [Questions & Hypotheses](#questions-hypotheses)
- [Dataset](#dataset)
- [Database](#database)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)


## Project Description
Women are underrepresented in many working areas, for example in the film industry. There are many female actors, but what about directing roles? 
Using data research, inspection, cleaning and analysis we could analyze the women's presence in directring roles inside the film industry.


## Questions & Hypotheses
- How is the development of female vs. male award winners?
- Is there a difference in the popularity of:
    - female and male directed films?
    - Female and male directors?
        - And of those who won or were nominated?


## Dataset

### 1.1. Database
- source of data:
    - source: https://www.kaggle.com
   
- The folowing database were used:
    - The Academy Awards, 1927-2015
        - https://www.kaggle.com/theacademy/academy-awards
    - Golden Globe Awards, 1944-2020
        - https://www.kaggle.com/unanimad/golden-globe-awards
  
 - We also added manually the winners of Acamedy Awards in the category Director for the last 4 years (2016-2019)
     - source: 
     
### 1.2. Web scraping
- Web scraping to create a list of directors names.
    - source: https://en.wikipedia.org/wiki/List_of_film_and_television_directors

### 1.3. API
- The Movie Database
    - https://developers.themoviedb.org/3/getting-started
    - People - get details: keyword, key
        - returns: Person details and top 3 rated movies (nested).
    - Request made iterating by list of names, normaliying and try/except.
   
   
## Database

To be able to answer our questions we combined our datsets into one main dataset: df_tmdb.pkl


- To be able to compare the award nominees and winners with the gender of the directors, we first merged the golden globe data with the academy awards winners --> "Merging_awards.ipynb"
- To extract only the directors from the TMDB-dataset "df_all.pkl" we merged it with the list of directors from wikipedia "movie_director_names.ipynb" -->
- Finally, we joined "Merging_awards.ipynb" with the "df_all.pkl" (contains The Movie Database Information)


## Workflow

1. Brainstorming and Alignement on topics and possible questions
2. Research of relevant data from different sources 
3. Comparing data sources and decision which data sources to use
4. Extracting and cleaning the data
4. Merging the data
5. Data Analysis
6. Data visualization 
7. Preparing the Presentation 


## Organization

We organized our project by using a trello-board and assigning to-dos to everyone. We had fixed check-ins to discuss problems and share results.


## Links
[Repository](https://github.com/anadetsch/tarsiers)  
[Slides](https://docs.google.com/presentation/d/1pyiCjz33oJ43kqFvKdSZNXEzEoY-p1KKHyHPEMLSi9s/edit?usp=sharing)  
[Trello](https://trello.com/b/9vAPB2OF/data-week-3-project-tarsiers)  


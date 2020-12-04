# Creating the Next Blockbuster Movie Using Data Science
This project was completed as part of Flatiron School's Data Science Bootcamp (November 2020)

In this report, I perform an analysis on a dataset of 625 movies and their features such as production budget, box office gross, release date, studio, popularity and words of mouth. From this, my goal is to determine what factors contribute to a movie being successful and help my client at Microsoft create the next blockbuster movie. 

## The Deliverables
There are 5 deliverables for this project:

1. A well documented Jupyter Notebook containing any code and comments explaining it.

            - Part 1: Data cleaning & preparation from provided data
            
            - Part 2: Data cleaning & preparation from scraped data
            
            - Part 3: Data analysis and visualization + actionable insights + conclusion & future works
            
2. An organized README.md file that describes the contents of the repository.
3. A short PowerPoint presentation (delivered as a PDF export) giving a high-level overview of the methodology used and recommendations for non-technical stakeholders.
4. A Blog Post which can be found at: https://btramduong0810.github.io/
5. A Video Walkthrough of my non-technical presentation, can be found at:

# **Notebook Table of Contents**

## PART I: Data Cleaning and Preparation From Provided Data

### **1.  Introduction**

1.1  Business Statement

### **2.  Data Preparation From Provided Data**

I.2.1 Methodology

I.2.2 Data Sources:
      
            - Box Office Mojo
            - IMDB
            - Rotten Tomatoes
            - TheMovieDB.org

I.2.3  Data reading

I.2.4  Data cleaning

            I.2.4.a Production budget & gross:

            - Budget
            - Domestic gross, worldwide gross
            - Studio
            
            I.2.4.b Movie Basics:
            
            - Runtime
            - Genre
            
            I.2.4.c Populatiry / Words of mouth: 

            - Vote count
            - Vote average
            - Popularity       
            - Language
           
            I.2.4.d Production Crew: 

            - Director
            - Writer

I.2.5  Joining the dataframes

             - Production budget & gross: movie_budgets_gross_df
             - Movie basics: release date, genre, runtime: title_basics_df
             - Popularity/ Words of mouth: vote count, vote average, popularity score: title_basics_rating_df
             - Production crew: director, writer: names_titles_df
             - All together: merged_df_1

II.2.6 Quick data analysis

## PART II: Data Cleaning and Preparation From Scraped Data

### **1.  Introduction**

1.1  Business Statement

### **2.  Data Preparation From Scraped Data**

II.2.1 Methodology

II.2.2 Data sources:
      
            - www.the-numbers.com

II.2.3  Data scraping

            - Top 100 grossing movie of each year from 2010 to 2018

II.2.4  Data cleaning

            - Budget
            - Domestic gross, international gross, worldwide gross
            - Genre
            - Source
            - Creative type
            - Production method 

II.2.5  Joining the dataframes

            - Scraped dataset: merged_df_2
            - full_df = merged_df_1 + merged_df_2

II.2.6 Quick data analysis

## PART III: **Data Visualization, Actionable Insights, Conclusion & Future Works**

### **1. Data Visualization**

1.1  Budget vs. Gross

1.2  Genre vs. Gross

1.3  Others: Source, Creative Type, Production Method vs. Gross

1.4  Runtime vs. Gross

1.5  Release time vs. Gross

1.6 Others: Director, Writer, Critic, Publisher vs. Gross

1.7  Popularity / Words of Mouth: 

            - Rating & number of votes vs. Gross
            - Critic review vs. Gross

### **2. Actionable Insights**

### **3.  Conclusion and Future Work**

3.1  Summary of Findings

3.2  Actionable Insights

3.3  Future Works

There are other factors such as star quality, quality of script, special effects, marketing campaign, popularity of the film preceding it (if it's a sequel), competition or lack thereof, competition from non-movie events such as weather or news and sport events that we can do analysis on. 

Director and writer are also interesting to look at.

Moreover, movie researchers has also found that critics have a dual role, where they both influence consumers' movie choice and predict box office performance by reflecting moviegoers' tastes. Unfortunately we won't be investigating these features as they will take up extra time and are all outside the scope of this project.

## Key Findings

## Actionable Insights

# Creating the Next Blockbuster Movie Using Data Science
This project was completed as part of Flatiron School's Data Science Bootcamp (November 2020)

In this report, I perform an analysis on a dataset of 625 movies (2010-2018) and their features such as production budget, box office gross, release date, studio, popularity and words of mouth to see which performed the best in term of ROI worldwide box office. From this, my goal is to determine what factors contribute to a movie being successful and help my client at Microsoft create the next blockbuster movie. 

## Business Statement

**Q1.** Is there a correlation between production budget and profit? If so, how much should Microsoft invest into production to get the highest ROI?

**Q2.** What kind of movie contents, in term of genre, source, creative type, production method, perform the best?

**Q3.** Can popularity or words of mouth, in term of rating and number of votes, affect the performance of a movie?

**Q4.** When is the best time of year to release a movie?

**Q5.** Is runtime a factor in determining the success of a movie?

## The Deliverables
There are 5 deliverables for this project:

1. A well documented Jupyter Notebook containing any code and comments explaining it.

            - Part I: Data cleaning & preparation from provided data
            
            - Part II: Data cleaning & preparation from scraped data
            
            - Part III.A: Data analysis and visualization + actionable insights + conclusion & future works
            
                   Q1. Production budget vs. Profit

                   Q2. Movie contents: genre, source, creative type, production method vs. Profit

                   Q3. Popularity or words of mouth, in term of rating and number of votes vs. Profit
            
            - Part III.B: Data analysis and visualization + actionable insights + conclusion & future works
                           
                   Q4. Release time vs. Profit
                          
                   Q5. Runtime vs. Profit
            
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

I.2.5  Joining the dataframes

             - Production budget & gross: movie_budgets_gross_df
             - Movie basics: release date, genre, runtime: title_basics_df
             - Popularity/ Words of mouth: vote count, vote average, popularity score: title_basics_rating_df
             - Production crew: director, writer: names_titles_df
             - All together: merged_df_1

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

## PART III.A: ** Data Visualization, Actionable Insights, Conclusion & Future Works**

### **1.  Introduction**

1.1  Business Statement

### **2. Data Visualization**

**Question 1:** Is there a correlation between production budget and profit? If so, how much should Microsoft invest into production to get the highest ROI?

            2.1  Budget vs. Profit
                 - General trend
                 - Top 100 performers trend

**Question 2:** What kind of movie contents, in term of genre, source, creative type, production method, perform the best?

            2.2  Genre vs. Profit
            
                 - General distribution vs. Top 100 distribution
                 - Top 100 performers vs. profit
                 - Top 100 performers vs. budget
                 
            2.3  Source vs. Profit
            
                 - General distribution vs. Top 100 distribution
                 - Top 100 performers vs. profit
                 - Top 100 performers vs. budget

            2.4  Creative Type vs. Profit
            
                 - General distribution vs. Top 100 distribution
                 - Top 100 performers vs. profit
                 - Top 100 performers vs. budget
                 
            2.5  Production Method vs. Profit
            
                 - General distribution vs. Top 100 distribution
                 - Top 100 performers vs. profit
                 - Top 100 performers vs. budget
                 
**Question 3:** Can popularity or words of mouth, in term of rating and number of votes, and the popularity of a studio affect the performance of a movie?

            2.6 Rating & number of votes vs. Profit
                 
                 - Top 100 performers trend
                 
            2.6.a Rating & number of votes vs. Genre
            
            2.6.b Rating & number of votes vs. Source
            
            2.6.c Rating & number of votes vs. Creative Type
            
            2.6.d Rating & number of votes vs. Production Method
                 
## PART III.B: **Data Visualization, Actionable Insights, Conclusion & Future Works**

### **1.  Introduction**

1.1  Business Statement

### **2. Data Visualization**

**Question 4:** When is the best time of year to release a movie, in term of month and day of the week?

            2.7.a  Release time vs. Profit
                 - General trend
                 - Top 100 performers trend
            
            2.7.b Number of movies released per month
            
**Question 5:** Is runtime a factor in determining the success of a movie?

            2.8  Runtime vs. Profit
                 - General trend
                 - Top 100 performers trend
                 
**Extra:** What is the best studio to work with?

            2.9 Studio vs. Profit
                 - General trend
                 - Top 100 performers trend

**Extra:** What is the most popular language?
            
            2.10 Language 

### **3. Actionable Insights**

### **4.  Conclusion and Future Work**

##  Summary of Key Findings

##  Summary of Actionable Insights

##  Future Works

There are other factors such as star quality, quality of script, special effects, marketing campaign, popularity of the film preceding it (if it's a sequel), competition or lack thereof, competition from non-movie events such as weather or news and sport events that we can do analysis on. 

Director and writer are also interesting to look at.

Moreover, movie researchers has also found that critics have a dual role, where they both influence consumers' movie choice and predict box office performance by reflecting moviegoers' tastes. Unfortunately we won't be investigating these features as they will take up extra time and are all outside the scope of this project.


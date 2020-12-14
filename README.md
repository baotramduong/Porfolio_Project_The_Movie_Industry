# Creating the Next Blockbuster Movie Using Data Science
This project was completed as part of Flatiron School's Data Science Bootcamp (November 2020)

Film entertainment is big business in the United States and it was estimated that the film entertainment business generated $35.3B in revenue in 2019 (Watson, 2020). The United States is among the biggest film industries in the world in general but also in terms of tickets sold per year, ranking behind China and India.

Microsoft sees all the big companies creating original video content, and they want to get in on the fun. They have decided to create a new movie studio, but the problem is they don’t know anything about creating movies. They have hired Flatiron Data Science team to help them better understand the movie industry. Our team is charged with doing data analysis and creating a presentation that explores what type of films are currently doing the best at the box office. We will then translate those findings into actionable insights that the CEO can use when deciding what type of films they should be creating.

In this report, we will investigate factors associated with commercially successful movies. This report gives a comprehensive evaluation on factors influencing the box office success of a movie such as production budget, domestic gross, international gross, worldwide gross, genre, source, creative type, production method, vote count, vote average, popularity , release time, runtime, studio, language. The business statements are formulated based on these attributes.

## Business Statement

**Q1.** Is there a correlation between production budget and profit? If so, how much should Microsoft invest into production?

**Q2.** What kind of movie contents, in term of genre, source, creative type, production method, perform the best?

**Q3.** Is there a correlation between popularity and positive words of mounth (average rating) and profit? How do they affect the performance of a movie?

**Q4.** When is the best time of year to release a movie?

**Q5.** Is there a correlation between runtime and profit? What is the best runtime?

## The Deliverables
There are 5 deliverables for this project:

1. A well documented Jupyter Notebook containing any code and comments explaining it.

            - Part I: Data cleaning & preparation from provided data
            
            - Part II: Data cleaning & preparation from scraped data
            
            - Part III.A: Data analysis and visualization Q1 - Q3
            
                   Q1. Production budget vs. Profit

                   Q2. Movie contents: genre, source, creative type, production method vs. Profit

                   Q3. Popularity or words of mouth, in term of rating and number of votes vs. Profit
            
            - Part III.B: Data analysis and visualization Q4 - Q5 
            + actionable insights + conclusion & future works
                           
                   Q4. Release time vs. Profit
                          
                   Q5. Runtime vs. Profit
            
2. An organized README.md file that describes the contents of the repository.

             - README.md: describes the content and organization of content.
             - LICENSE.md: Learn.co Educational Content License
             - module1_project_rubric.pdf: describes requirements for this project.
             - zippedData folder: contains all provided data from Flatiron, additional scraped data, 
             and all figures for visualization.
             - Part I: Jupyter notebook
             - Part II: Jupyter notebook
             - Part III.A: Jupyter notebook
             - Part III.B: Jupyter notebook

3. A short PowerPoint presentation (delivered as a PDF export) giving a high-level overview of the methodology used and recommendations for non-technical stakeholders. Can be found at: 

https://docs.google.com/presentation/d/1z4NpXFo0wAAY2fHN5nDiM_VXM7UZJ-0R4Mn7mjt8WzQ/edit?usp=sharing

4. A Blog Post which can be found at: 

https://baotramduong.medium.com/data-science-vs-the-movie-industry-8e5645d1c88c

5. A Video Walkthrough of my non-technical presentation, can be found at:

# **Notebook Table of Contents**

## PART I: Data Cleaning and Preparation From Provided Data

### **1.  Introduction**

1.1  Business Statement

### **2.  Data Preparation From Provided Data**

I.2.1 Methodology

             1. Get data from provided data
             3. Gather all attributes to answer questions: budget, domestic gross, 
             international gross, worldwide gross, vote count, vote average, 
             popularity , release time, runtime, studio, language
             4. Deal with missing and null values
             5. Deal with duplicates
             6. Correct datatypes if needed

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
             - Popularity/ Words of mouth: vote count, vote average, 
             popularity score: title_basics_rating_df
             - Production crew: director, writer: names_titles_df
             - All together: merged_df_1

## PART II: Data Cleaning and Preparation From Scraped Data

### **1.  Introduction**

1.1  Business Statement

### **2.  Data Preparation From Scraped Data**

II.2.1 Methodology

             1. Scrape additional data from www.the-numbers.com
             2. Gather all attributes to answer questions: genre, source, 
             creative type, production method
             3. Deal with missing and null values
             4. Deal with duplicates
             5. Correct datatypes if needed
             
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

## PART III.A: Data Visualization, Actionable Insights, Conclusion & Future Works

### **1.  Introduction**

1.1  Business Statement

### **2. Data Visualization**

### **Methodology:**

            1. Using seaborn package and matplotlib to visualize data
            2. Get the General Movies trend/ distribution of all movies 
            using distribution plot and/or bar plot.
            3. Get distribution of Top 100 Movies to see what is done differently to reach higher success 
            using distribution plot and/or bar plot and/or scatter plot and/or line plot.
            4. See if there is a correlation/ linear relationship between variables and calculate for Pearson correlation coefficient.
            4. Do analysis on the mean average using box plot.
            5. Do analysis on each category using swarm plot.
            6. Compare all movies all at once using rel plot.

**Question 1:** Is there a correlation between production budget and profit? If so, how much should Microsoft invest into production to get the highest ROI?

            2.1  Budget vs. Worldwide Profit
            
                 2.1a. Budget
                 
                       2.1ai. General trend
                       2.1aii. Top 100 performers trend
                       
![alt text](../master/zippedData/budget_distribution_distplot.png?raw=true)                       

                 2.1b. Profit
                        
                        2.1bi. Domestic Profit, International Profit, Worldwide Profit
                        2.1bii. Top 100 performers with respect to Worldwide Profit

![alt text](../master/zippedData/budget_vs_profit_lmplot.png?raw=true)

![alt text](../master/zippedData/budget_vs_profit_scatterplot.png?raw=true)

![alt text](../master/zippedData/budget_range_vs_100_profit_boxplot.png?raw=true)

**Question 2:** What kind of movie contents, in term of genre, source, creative type, production method, perform the best?

            2.2  Genre vs. Worldwide Profit
            
                 2.2a. General distribution vs. Top 100 distribution
                 2.2b. Top 100 performers vs. Worldwide Profit
                 2.2c. Top 100 performers with respect to Production Budget and Worldwide Profit

![alt text](../master/zippedData/genre_vs_100_profit_boxplot.png?raw=true)

![alt text](../master/zippedData/genre_budget_profit_relplot.png?raw=true)

            2.3  Source vs. Worldwide Profit
            
                 2.3a. General distribution vs. Top 100 distribution
                 2.3b. Top 100 performers vs. Worldwide Profit
                 2.3c. Top 100 performers with respect to Production Budget and Worldwide Profit

![alt text](../master/zippedData/soure_vs_100_profit_boxplot.png?raw=true)

![alt text](../master/zippedData/source_budget_profit_relplot.png?raw=true)

            2.4  Creative Type vs. Worldwide Profit
            
                 2.4a. General distribution vs. Top 100 distribution
                 2.4b. Top 100 performers vs. Worldwide Profit
                 2.4c. Top 100 performers with respect to Production Budget and Worldwide Profit

![alt text](../master/zippedData/creative_type_vs_100_profit_boxplot.png?raw=true)

![alt text](../master/zippedData/creative_type_budget_profit_relplot.png?raw=true)

            2.5  Production Method vs. Worldwide Profit
            
                 2.5a. General distribution vs. Top 100 distribution
                 2.5b. Top 100 performers vs. Worldwide Profit
                 2.5c Top 100 performers with respect to Production Budget and Worldwide Profit

![alt text](../master/zippedData/production_method_vs_100_profit_boxplot.png?raw=true)

![alt text](../master/zippedData/production_method_budget_profit_relplot.png?raw=true)

**Question 3:** Can popularity or words of mouth, in term of rating and number of votes, and the popularity of a studio affect the performance of a movie?

            2.6. Popularity vs. Worldwide Profit
                
                2.6a. General distribution vs. Top 100 distribution
                2.6b. Genres with respect to Popularity & Worldwide Profit
                2.6c. Sources with respect to Popularity & Worldwide Profit
                2.6d. Creative Types with respect to Popularity & Worldwide Profit
                2.6e. Production Method with respect to Popularity & Worldwide Profit

![alt text](../master/zippedData/popularity_vs_profit_lmplot.png?raw=true)

![alt text](../master/zippedData/popularity_vs_profit_scatterplot.png?raw=true)

![alt text](../master/zippedData/genre_popularity_profit_relplot.png?raw=true)

![alt text](../master/zippedData/source_vs_popularity_profit_relplot.png?raw=true)

![alt text](../master/zippedData/creative_type_popularity_profit_relplot.png?raw=true)

![alt text](../master/zippedData/production_method_popularity_profit_relplot.png?raw=true)

            2.7. Rating & number of votes vs. Worldwide Profit
                
                2.7a. General distribution vs. Top 100 distribution
                2.7b. Genres with respect to Average Rating & Worldwide Profit
                2.7c. Sources with respect to Average Rating & Worldwide Profit
                2.7d. Creative Types with respect to Average Rating & Worldwide Profit
                2.7e. Production Method with respect to Average Rating & Worldwide Profit                            

![alt text](../master/zippedData/rating_vs_profit_lmplot.png?raw=true)

![alt text](../master/zippedData/average_rating_vs_profit_scatterplot.png?raw=true)

![alt text](../master/zippedData/genre_rating_profit_relplot.png?raw=true)

![alt text](../master/zippedData/source_rating_profit_relplot.png?raw=true)

![alt text](../master/zippedData/creative_type_rating_profit_relplot.png?raw=true)

![alt text](../master/zippedData/production_method_rating_profit_relplot.png?raw=true)

## PART III.B: **Data Visualization, Actionable Insights, Conclusion & Future Works**

### **1.  Introduction**

1.1  Business Statement

### **2. Data Visualization**

### **Methodology:**

            1. Using seaborn package and matplotlib to visualize data
            2. Get the general trend/ distribution of all movies using distribution plot and/or bar plot.
            3. Get distribution of Top 100 movies to see what is done differently to reach higher success 
            using distribution plot and/or bar plot and/or scatter plot and/or line plot.
            4. Do analysis on the mean average using box plot.
            5. Do analysis on each category using swarm plot.
            6. Compare all movies all at once using rel plot.
            
**Question 4:** When is the best time of year to release a movie, in term of month and day of the week?

            2.8.  Release time vs. Worldwide Profit
            
                 2.8a. General trend                
                 2.8b. Top 100 performers trend
            
            2.8c. Number of movies released per month

![alt text](../master/zippedData/release_month_vs_profit_lineplot.png?raw=true)

![alt text](../master/zippedData/release_month_vs_100_profit_boxplot.png?raw=true)

![alt text](../master/zippedData/release_month_vs_100_profit_swarmplot.png?raw=true)

![alt text](../master/zippedData/num_movies_released_vs_profit_100_catplot.png?raw=true)

**Question 5:** Is runtime a factor in determining the success of a movie?

            2.9  Runtime vs. Worldwide Profit
            
                 2.9a. General trend
                 2.9b. Top 100 performers trend     
                 2.9c. Top 100 performers with respect Worldwide Profit

![alt text](../master/zippedData/runtime_vs_profit_lmplot.png?raw=true)

![alt text](../master/zippedData/runtime_distribution_distplot.png?raw=true)

![alt text](../master/zippedData/runtime_vs_profit_scatterplot.png?raw=true)

**Extra:** What is the best studio to work with?

            2.10 Studio vs. Worldwide Profit
            
                 2.10a. General trend
                 2.10b. Top 100 performers trend
                 2.10c. Top 100 performers with respect to Production Budget & Worldwide Profit

![alt text](../master/zippedData/studio_vs_100_profit_boxplot.png?raw=true)

![alt text](../master/zippedData/studio_budget_profit_relplot.png?raw=true)

### **3. Actionable Insights**

### **4.  Conclusion and Future Work**

##  Summary of Key Findings

**Question 1:** Is there a correlation between production budget and profit? If so, how much should Microsoft invest into production?

            Budget vs Profit: 
            - r2 = 0.358
            - Production budget is positively correlated with worldwide profit.
            
            - The average production budget in general is $68M.
            - The average worldwide profit in general is $179M.
            
            - The average production budget in top 100 performers is $151M.
            - The average worldwide profit of the Top 100 performers is $624M.
            
            Decision: $150M and up

**Question 2:** What kind of movie contents, in term of genre, source, creative type, production method, perform the best?

            Genre
            - The average worldwide profit for Action genre is $692M.
            - The average worldwide profit for Adventure genre is $591M.
            - The average worldwide profit for Thriller/Suspense genre is $587M.
            - The average worldwide for Musical genre is $502M.
            Decision: Action and Adventure

            Source
            - The average worldwide profit for Based on Comic/Graphic Novel source is $682M.
            - The average worldwide profit for Based on Fiction Book/Short Story source is $610M.
            - The average worldwide profit for Original Screenplay source is $591M.
            Decision: Based on Comic Graphic/ Novel

            Creative Type
            - The average worldwide profit for Super Hero creative type is $683M.
            - The average worldwide profit for Based on Science Fiction creative type is $595M.
            - The average worldwide profit for Contemporary Fiction creative type is $705M.
            Decision: To be decided between Super Hero vs. Contemporary Fiction

            Production Method
            - The average worldwide profit for Animation/Live Action production method is $692M.
            - The average worldwide profit for Live Action production method is $606M.
            - The average worldwide profit for Digital Animation production method is $606M.
            Decision: To be decided between Animation/ Live Action vs. Live Action

**Question 3:** Is there a correlation between popularity and positive words of mounth (average rating) and profit? How do they affect the performance of a movie?

            Popularity: 
            - r2 = 0.274
            - Popularity is positively correlated with worldwide profit.
            - Top 100 movies score a 25 on average.
            - Bottom 100 movies score a 13.2 on average.

            
            - Action & Adventure is the most popular genre.
            Decision: Action & Adventure

            - Based on Comic Graphic/ Novel is the most popular source.
            Decision: Based on Comic Graphic/ Novel

            - Super Hero is the most popular creative type.
            Decision: Super Hero is picked over Contemporary Fiction

            - Animation/Live Action is the most popular production method.
            Decision: Animation/Live Action

            Average Rating: 
            - r2 = 0.089
            - Rating is positively correlated with worldwide profit but not strongly.
            - Top 100 movies score a 7.1 on average.
            - General movies score a 6.4 on average.
            - Bottom 100 movies score a 6.1 on average.

            Thriller/Suspense is the highest rated genre.
            - Adventure and Action is the next highest rated genres. 
            Decision: worldwide profit demands Adventure & Action.

            - Original Screen Play is the highest rated source.
            - Based on Comic Graphic/ Novel is the second highest rated source.
            Decision: worldwide profit is high for both categories == combination of both.

            - Science Fiction is the highest rated creative type.
            - Super Hero is second highest rated creative type.
            Decision: worldwide profit is high for both categories == combination of both.
            
            - Animation/Live Action is the higest rated productin method.
            Decision: Animation/Live Action

**Question 4:** When is the best time of year to release a movie?

            Decision: June

**Question 5:** Is there a correlation between runtime and profit? What is the best runtime?

            - r2 = 0.058
            - Runtime is positively correlated with worldwide profit but not strongly.
            - The average runtime in general is 108 minutes
            - The average runtime in top 100 performers is 118 minutes
            Decision: 120 mins and up

**Extra:** What is the best production studio?

            - Universal Studio is the highest grossing studios: $825M
            - Buena Vista aka Walt Disney Motion Pictures is the second highest grossing studio: $723M

##  Summary of Actionable Insights

Results suggest that the following factors are positively associated with a movie success:

            - Production budget = $150M and up
            - Genre = Action & Adventure
            - Source = Based on comic graphic/ novel
            - Creative Type = Super Hero
            - Production Method = Animation/ Live Action
            - Release month = June
            - Runtime = 120 mins and up
            
            - Critics reviews and public rating can be informative.

##  Future Works

Based on Quora and many other suggestions on the Internet:

            1. Do analysis in term of ROI instead of simplified worldwide profit
            2. Do further analysis between domestic market and international market
            3. Motion Picture Association of America (MPAA) rating
            4. Star quality: choosing a film where the main actor has received awards and recognition for acting is one of the best predictors of movie success.  
            In a study published in the Journal of the Academy of Marketing Science, they found that when a movie is first released it is the "star power" of a popular actor that has the strongest impact at the box office (Staff, 2017). 
            5. Quality of script
            6. Special effects, sound design, music
            7. Marketing campaign
            8. Popularity of the film preceding it (if it's a sequel)
            9. Directors 
            10. Writers
            11. Critics
            12. Diversity: female directors, women of color, Black Lives Matter movement, etc.



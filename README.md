# sql_movies_p3

## Project Overview

**Project Title**: Movie Data Analysis
**Level**: Beginner

This project is crafted to demonstrate SQL skills and techniques used in the entertainment industry, specifically in movie data analysis. It involves setting up a movie database, performing data cleaning, exploratory data analysis (EDA), and answering business questions using SQL queries. This project is ideal for newcomers in data analysis, offering a solid foundation in SQL applied to media and entertainment data.

## Objectives

1. **Set Up a Movie Database**: Create and populate a movie database containing data on movies, genres, directors, actors, ratings, and box office collections.
2. **Data Cleaning**: Identify and handle records with missing or null values, ensuring that analysis results are based on clean data.
3. **Exploratory Data Analysis (EDA)**: Perform basic EDA to understand the dataset’s characteristics, such as distribution of ratings, genre popularity, and release trends.
4. **Buisness Analysis**: Use SQL to answer business-related questions, such as identifying popular genres, successful directors, and box office trends, for insights into audience preferences.

## Project Structure

### Data Analysis and Findings

The following SQL queries were developed to answer specific business questions:

**1.Retrieve the names of all the Bollywood movies 
which are of drama genre in the dataset.**
```sql
select movie_name from movies_sql where genre='drama';
```

**2.Retrieve the names of all the Bollywood 
movies of Amir Khan in the dataset.**
```sql
select movie_name from movies_sql where Lead_Star='aamir khan';
```

**3.Retrieve the names of all the Bollywood 
movies which are directed by RamGopal 
Verma in the dataset.**
```sql
select movie_name,director from movies_sql where director='ram gopal verma';
```

**4.Retrieve the names of all the Bollywood 
movies which have been released over 
more than 1000 number of screens in the 
dataset.**
```sql
select movie_name from movies_sql where Number_of_Screens>1000;
```

**5.Retrieve the names of all the Bollywood 
movies which have generated Revenue(INR)
more than 700000000 in the dataset.**
```sql
select movie_name from movies_sql where revenue>700000000;
```

**6.Retrieve the names of all the Bollywood 
movies which have budget less than 1cr in 
the dataset.**
```sql
select movie_name from movies_sql where budget<10000000;
```

**7.Retrieve the names of all the Bollywood 
movies which are flop in the 
dataset.(flop=revenue – budget).**
```sql
select movie_name from movies_sql where (revenue-budget)<0;
```

**8.Retrieve the names and profit of all the 
Bollywood movies in the
dataset.(profit=revenue – budget)**
```sql
select movie_name from movies_sql where (revenue-budget)>0;
```

**9.Retrieve the names and loss of all the 
Bollywood movies in the
dataset.(loss=revenue – budget)**
```sql
select movie_name,(revenue-budget) from movies_sql where (revenue-budget)<0;
```

**10. Retrieve the names of all the Bollywood 
movies which have been released on 
holidays in the dataset.**
```sql
select movie_name from movies_sql where Release_Period='holiday';
```

**11. Retrieve the names of all the Bollywood 
movies which have lead star as Akshay 
Kumar and directed by Priyadarshan in the
dataset.**
```sql
select movie_name from movies_sql where Lead_Star='akshay kumar' and Director='priyadarshan';
```

**12. Retrieve the names of all the Bollywood 
movies starting with ‘a’ in the dataset.**
```sql
select movie_name from movies_sql where Movie_Name like 'a%';
```

**13. Retrieve the names of all the Bollywood 
movies ending with ‘a’ in the dataset.**
```sql
select movie_name from movies_sql where Movie_Name like '%a';
```

**14. Retrieve the names of all the Bollywood 
movies having ‘a’ at second place of the 
name in the dataset.**
```sql
select movie_name from movies_sql where Movie_Name like '_a%';
```

**15. Retrieve the names of all the Bollywood 
movies having music of amit trivedi in the
dataset.**
```sql
select movie_name from movies_sql where Music_Director='amit trivedi';
```

**16. Retrieve the names of all the comedy 
movies of Akshay Kumar in the dataset.**
```sql
select movie_name from movies_sql where Lead_Star='akshay kumar' and genre='comedy';
```

**17. Retrieve the names of movies and star 
name starring khan in the dataset.**
```sql
select movie_name,Lead_Star from movies_sql where Lead_Star like '%khan';
```

**18. Retrieve all the information of movies 
race and race2 in the dataset.**
```sql
select * from movies_sql where Movie_Name in ('race','race 2');
```

**19. Retrieve the names of all the thriller 
Bollywood movies in the dataset.**
```sql
select movie_name from movies_sql where genre='thriller';
```

**20. Retrieve the names and budget of all the 
Bollywood movies according to the highest 
budget to lowest budget in the dataset.**
```sql
select movie_name,budget from movies_sql order by budget desc;
```

**21. Retrieve the names and budget of top 5 
Bollywood movies with highest budget in 
the dataset. **
```sql
select movie_name,budget from movies_sql order by budget desc limit 5;
```

**22. Retrieve the names of top 10 Bollywood 
movies with highest revenue generation in 
the dataset.**
```sql
select movie_name,revenue from movies_sql order by revenue desc limit 10;
```

**23. Retrieve the names of top 5 movies of 
salman khan in the dataset.**
```sql
select movie_name,revenue from movies_sql where Lead_Star='salman khan' order by revenue desc limit 5;
```

**24. Retrieve the names of top 5 floped movies 
in the dataset.**
```sql
select movie_name,(revenue-budget) from movies_sql where (revenue-budget)<0 order by (revenue-budget) limit 5;
```

**25. Retrieve the names of top 5 hit movies in 
the dataset.**
```sql
select movie_name,(revenue-budget) from movies_sql where (revenue-budget)>0 order by (revenue-budget) desc limit 5;
```

**26. Which is the second movie released on 
maximum screens.**
```sql
select movie_name,Number_of_Screens from movies_sql order by Number_of_Screens desc limit 1,1;
```

**27. Which is the 10th movies with highest 
budget.**
```sql
select movie_name,budget from movies_sql order by budget desc limit 9,1;
```

**28. Which is the 2nd movie of Amitabh 
Bachchan with highest budget.**
```sql
select movie_name from movies_sql where Lead_Star='amitabh bachchan' order by budget desc limit 1,1;
```

**29. Which are the flopped movies of Akshay
Kumar.**
```sql
select movie_name,(revenue-budget) from movies_sql where (revenue-budget)<0 and Lead_Star='akshay kumar';
```

**30. With which director Sharukh Khan have 
given the biggest hit movie**
```sql
select movie_name,director from movies_sql where Lead_Star='shahrukh khan' order by revenue desc limit 1;
```

## Findings

1. **Genre Popularity**: The analysis reveals trends in genre popularity over time, highlighting which genres are most appealing to audiences.
2. **High-Grossing Movies**: Identification of movies with box office collections above a certain threshold, providing insights into high-performing releases and the types of movies that perform best commercially.
3. **Director and Actor Performance**: Evaluation of top directors and actors based on movie ratings and box office success, showcasing those with the most successful films and influence on movie popularity.
4. **Audience Preferences**: Analysis of ratings and genres across different age groups and demographics, helping to understand target audiences better.

## Conclusion
This project is an effective introduction to SQL for data analysts, covering database setup, data cleaning, EDA, and business-driven SQL queries in a movie database. The findings can guide entertainment industry decisions by highlighting trends in genre popularity, successful movie traits, and audience preferences.

## How to Use

1. **Clone the Repository**: Clone this project repository from GitHub.
2. **Set Up the Database**: Run the SQL scripts provided in the database_setup.sql file to create and populate the database.
3. **Run the Queries**: Use the SQL queries provided in the analysis_queries.sql file to perform your analysis.
4. **Explore and Modify**: Feel free to modify the queries to explore different aspects of the dataset or answer additional business questions.

## Author - Meet Limbani
This project is part of my portfolio, showcasing the SQL skills essential for data analyst roles. If you have any questions, feedback, or would like to collaborate, feel free to get in touch!

### Stay Updated and Join the Community
For more content on SQL, data analysis, and other data-related topics, make sure to follow me on social media and join our community:

- **LinkedIn**: [Connect with me professionally](https://www.linkedin.com/in/meet-limbani-6258bb285/)

Thank you for your support, and I look forward to connecting with you!

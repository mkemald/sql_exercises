# Here are some SQL exercises that provided with Chatgpt. I used one of the datacamp databases "Netflix Database". There is one prompt and you can make infinite exercises.

PROMPT:
I want you to be a SQL expert. I have dataset contains {Explain what is your database name and contains what kinds of data. Don't forget to giving field names.}. Ask 5 exercises question that I will try to make correct query for each one of them. Each questions should be with answers and answers should be in SQL code format. Difficulty level of this question will be {Choose easy, normal or hard.}.



SAMPLE QUESTIONS:


/* What are the top 10 movies or TV shows with the highest rating on Netflix?*/

SELECT title, rating
FROM table_name
ORDER BY rating DESC
LIMIT 10;

/* How many movies and TV shows have been added to Netflix each year since 2015? */

SELECT YEAR(date_added) AS year, COUNT(*) AS count
FROM table_name
WHERE YEAR(date_added) >= 2015
GROUP BY YEAR(date_added);

/* What are the top 5 most popular genres of movies and TV shows on Netflix in the United States? */

SELECT genre, COUNT(*) AS count
FROM table_name
WHERE country = 'United States'
GROUP BY genre
ORDER BY count DESC
LIMIT 5;

/* Which director has made the most movies or TV shows on Netflix? */

SELECT director, COUNT(*) AS count
FROM table_name
GROUP BY director
ORDER BY count DESC
LIMIT 1;

/* What is the average duration of TV shows on Netflix? */

SELECT AVG(duration)
FROM table_name
WHERE type = 'TV Show';


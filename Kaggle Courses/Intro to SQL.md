# Introduction to SQL

## 1. Introduction

The focus of this tutorial is to use Google's BigQuery database service.

In BigQuery, each dataset is contained in a corresponding project. In this case, our hacker_news dataset is contained in the bigquery-public-data project. To access the dataset,

    We begin by constructing a reference to the dataset with the dataset() method.

    Next, we use the get_dataset() method, along with the reference we just constructed, to fetch the dataset.

The image below consolidates all the concepts for BigQuery.

![Google BigQuery Concepts](https://i.imgur.com/biYqbUB.png)

## Group By, Having, Count() Clause

**COUNT()** is an example of an aggregate function, which takes many values and returns one. (Other examples of aggregate functions include **SUM()**, **AVG()**, **MIN()**, and **MAX()**.)

GROUP BY takes the name of one or more columns, and treats all rows with the same value in that column as a single group when you apply aggregate functions like COUNT().

HAVING is used in combination with GROUP BY to ignore groups that don't meet certain criteria.

Note that because it tells SQL how to apply aggregate functions (like COUNT()), it doesn't make sense to use GROUP BY without an aggregate function. Similarly, if you have any GROUP BY clause, then all variables must be passed to either a

* GROUP BY command, or
* an aggregation function.

Consider an example.

    SELECT parent, COUNT(id)
    FROM `bigquery-public-data.hacker_news.comments`
    GROUP BY parent

The above query will work. The below one will not.

    SELECT author, parent, COUNT(id)
    FROM `bigquery-public-data.hacker_news.comments`
    GROUP BY parent

It will the following error.

    SELECT list expression references column (column's name) which is neither grouped nor aggregated at

## Order By Clause

So far, you've learned how to use several SQL clauses. For instance, you know how to use **SELECT** to pull specific columns from a table, along with **WHERE** to pull rows that meet specified criteria. You also know how to use aggregate functions like **COUNT()**, along with **GROUP BY** to treat multiple rows as a single group.


    **ORDER BY** is usually the last clause in your query, and it sorts the results returned by the rest of your query.

## **Dates**

The **DATE** format has the year first, then the month, and then the day. It looks like this:

    YYYY-[M]M-[D]D

* YYYY: Four-digit year
* [M]M: One or two digit month
* [D]D: One or two digit day

So 2019-01-10 is interpreted as January 10, 2019.

The **DATETIME** format is like the date format ... but with time added at the end.

## Extract

An Example of Extract

![Extract Example from Kaggle](https://i.imgur.com/PhoWBO0.png)

Another Example
![Extract Example from Kaggle](https://i.imgur.com/A5hqGxY.png)

## Joins

In general, when you're joining tables, it's a good habit to specify which table each of your columns comes from. That way, you don't have to pull up the schema every time you go back to read the query.

![Join between Pets and Owners](https://i.imgur.com/fLlng42.png)

The type of **JOIN** we're using today is called an **INNER JOIN**. That means that a row will only be put in the final output table if the value in the columns you're using to combine them shows up in both the tables you're joining. For example, if Tom's ID number of 4 didn't exist in the pets table, we would only get 3 rows back from this query. There are other types of **JOIN**, but an **INNER JOIN** is very widely used, so it's a good one to start with.

### **Example: How many files are covered by each type of software license?**

We'll work with two tables in the database. The first table is the licenses table, which provides the name of each GitHub repo (in the repo_name column) and its corresponding license.

![repo-licence-query](https://i.imgur.com/QeufD01.png)

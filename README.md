# Project--Hadoop-9

<table>
  
**In this project we will integrate Apache Spark with Cassandra and it's gonna be amazing combo you goona have in your toolkit after this project**.<br></br>

Lets start by learning about Spark and Cassandra.<br></br>

**What is Spark?** <br></br>

Apache Spark™ is a multi-language engine for executing data engineering, data science, and machine learning on single-node machines or clusters.<br></br>

**What is Cassandra?** <br></br>

Apache Cassandra is an open source NoSQL distributed database trusted by thousands of companies for scalability and high availability without compromising performance. Linear scalability and proven fault-tolerance on commodity hardware or cloud infrastructure make it the perfect platform for mission-critical data.<br></br>

**Dive into the overall implementation and structure of this integration starting with basic steps taken step by step**:<br></br>

At first We have our cassandra database which is empty which we have created in Hadoop Cluster using following command:<br>

**Step-1:** **Creating the Database for cassandra**<br>
CREATE KEYSPACE movielens WITH replication = {"class":"SimpleStrategy",'replication_factor':'01'} and durable_writes=true;<br></br>

**Step-2:** **Using database movielens and creating table inside it of users**<br>
USE movielens;<br></br>

**Step-3:** **Creating table users in Cassandra with the columns names and datatypes in it**<br>
CREATE TABLE users (user_id int, age int, gender text, occupation text, zip text, primary_key (user_id));<br></br>


**Step-4:** **Verifying whether everything is set up or not?** <br>
DESCRIBE TABLE users;<br></br>

**Step-5:** **Selecting all rows from table users**<br>
SELECT * from users;<br></br>

**Step-6:** After this all worked fine jump to the python code file on getting to know about how to do integration from spark to cassandra.<br></br>

**Main Insights of Project**:<br></br>

First we made the dataframe from the u.user file which is uploaded alongside the code file. Go through the dataset before jumping to the code. Then we writed the dataframe 
with all the configuration needed into Cassandra. We can check whether it is writed in Cassandra or not using 'SELECT * from users;' command.<br></br>

Secondly we read the Dataframe from cassandra and then we create views and even run sql queries on that.<br></br>






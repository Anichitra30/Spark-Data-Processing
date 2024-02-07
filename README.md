# Spark-Data-Processing

## Part 1

[Airbnb](http://airbnb.com/) is an online marketplace for arranging or offering lodgings.

In this part we will use Spark to analyze data obtained from the Airbnb website. The purpose of the analysis is to extract information about trends and patterns from the data. 
Part 1 has 2 sections:

### Section 1: Loading, describing and preparing the data

There's quite a lot of data. Make sure that you can load and correctly parse the data, and that you understand what the dataset contains. You should also prepare the data for the analysis in part two. This means cleaning it and staging it so that subsequent queries are fast.

### Section 2: Analysis

In this part our goal is to learn about trends and usage patterns from the data. You should give solutions to the tasks defined in this notebook, and you should use Spark to do the data processing. You may use other libraries like for instance Pandas and matplotlib for visualisation.

### Guidelines

Processing data should be done using Spark. Once data has been reduced to aggregate form, you may use collect to extract it into Python for visualisation.
Your solutions will be evaluated by correctness, code quality and interpretability of the output. This means that you have to write clean and efficient Spark code that will generate sensible execution plans, and that the tables and visualisations that you produce are meaningful and easy to read.
You may add more cells for your solutions, but you should not modify the notebook otherwise.


## Part 2 - Web traffic 

In this part our task is to analyze a stream of log entries. A log entry consists of an [IP address](https://en.wikipedia.org/wiki/IP_address) and a [domain name](https://en.wikipedia.org/wiki/Domain_name). For example, a log line may look as follows:

192.168.0.1 somedomain.dk

One log line is the result of the event that the domain name was visited by someone having the corresponding IP address. Our task is to analyze the traffic on a number of domains. Counting the number of unique IPs seen on a domain doesn't correspond to the exact number of unique visitors, but it is a good estimate.

Specifically, we should answer the following questions from the stream of log entries.

How many unique IPs are there in the stream?
How many unique IPs are there for each domain?
How many times was IP X seen on domain Y? (for some X and Y provided at run time)
The answers to these questions can be approximate!

We should also try to answer one or more of the following, more advanced, questions. The answers to these can also be approximate.

How many unique IPs are there for the domains ?
How many times was IP X seen on domains ?
What are the X most frequent IPs in the stream?
We can also use algorithms and data structures.

Furthermore, we also discover:

Document the accuracy of answers when using algorithms that give approximate answers
Argue why we are using certain parameters for our data structures
This notebook is in three parts. In the first part we are given an example of how to read from the stream (which for the purpose of this project is a remote file). In the second part we implement the algorithms and data structures that we intend to use, and in the last part we use these for analyzing the stream.

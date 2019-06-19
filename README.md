# Wrangling WeRateDogs 

## Table of Contents
<ul>
<li><a href="#intro">Introduction</a></li>
<li><a href="#gathering">Gathering The Data</a></li>
<li><a href="#access">Accessing The Data</a></li>
<li><a href="#cleaning">Cleaning The Data</a></li>
<li><a href="#analizing">Analizing and Visualizing</a></li>
<li><a href="#predict">Predicting</a></li>
</ul>

<a id="intro"></a>
# Introduction

This project Real-world data rarely comes clean. Using Python and its libraries, I will gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. This is called data wrangling. This task is intended for Udacity Nanodegree Data Wrangling Project.

The dataset that I will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. The data separated in 3 part, 1 from a local file which provided by Udacity, second data from Udacity server, and the last one from twitter API.

The goal: wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information. Additional gathering, then assessing and cleaning is required for "Wow!"-worthy analyses and visualizations.

<a id="gathering"></a>
# Gathering The Data

In this part, I gather 3 types of file resources. First file from a local file which provided by Udacity. The second file from Udacity Server, and the last data from Twitter API.

<a id="access"></a>
# Accessing The Data

In this part, I do some task that is:
- Check the length of data
- Check the type of data
- Check the value of data
- Check the missing value of data
- Check stat describe data

The issue I am founded are:
quality issues:

- Axist not original tweet
- tweet_id format in third data doesn't like first data so maybe it can make some problem if we join the two table
- tweet_id position in the third table not the same as the other table, so we can't easily see the id
- timestamp in the first table not in DateTime format
- The missing value was not uniformly, sometime NaN but some other None
- There are exist columns that have >90% missing value, also exist dog name that just has 1 character ('a')
- Cols retwitted and favorited have the same value in all row
- Cols source have HTML format
- Cols expanded_urls and jpg_urls have duplicated value

tidiness issues:

- Stage of a dog must be 1 col instead of 4 cols
- Join all data is needed to make easier for analysis
  
<a id="cleaning"></a>
# Cleaning and Tidying The Data

In the cleaning section, I just solve the problem from section "Accessing The Data".

<a id="analizing"></a>
# Analyzing and Visualizing Data 

In this section, I answer some question, that is:
- Is there any outlier in the data?
- How about the correlation between variables?
- Do the retweet count and favorite count increase with time?
- Does the rating increase with time?
- Is the rating affect the number of favorite and retweet count?
- How much each algorithm predict the picture is a dog?
- What are the most popular dog names?
- What is the most popular dog predict?
- What is the most popular dog predict when all algorithm predicts the same dog?

<a id="predict"></a>
# Predict dog_stage

In this section, I predict missing dog_stage from third file I have.

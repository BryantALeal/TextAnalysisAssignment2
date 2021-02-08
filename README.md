# Text Analysis Assignment 2 :beers:
A repo for code used for completing project 2 in Text Analysis where we were to analyze user sentiment on beer reviews from <a href='https://www.beeradvocate.com/beer/top-rated/'> Beer Advocate's </a>:beer: top 250 beers. Specifically, we needed to collect around 25 reviews for each beer in the top 250. This means we had over 6,250 rows of unstructured data in total! :smile:  <br><br>
The code is split off into different sections that I will describe in detail below:
<ol type="a">
  <li>Webscraper</li>
  <br>The webscraper uses a combination of two packages, Selenium and Beautiful Soup. Both of these were used because of their individual benefits. For example, Beauitful Soup makes parsing through HTML easy. This enabled us to parse for each beer's URL. With those URLs, we were able to automate the process with selenium by clicking through each of those URLs and scrape a beer's name, user rating, and user comments/reviews. Once complete, the data needed to be split since all comments were one combined into one item in a list. We also needed to cean the data as some HTML code remained in the comments. Once complete, the dataframe was written as a CSV file and passed on for analysis.
  
  <li>Word Frequency Analysis</li> <br>
  Further data pre-processing is needed to peform analysis on the data. The words need to be rid of certain characters such as dashes and underscores. Once we are sure that the data is purely words, we removed common english stop words such as I, me, my and myself. These words, in terms of frequency, appear often yet provide no value in terms of analysis, so they are removed. After this, we created another function that will put everything together.
  
  <li>Cosine Similarity</li>
  <li>Sentiment Analysis</li>
  <li>Evaluation Score</li>
  <li>Spacy Simliarity</li>
  <li>Analysis of Results</li>

</ol>

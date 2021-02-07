# TextAnalysisAssignment2
A repo for code used for completing project 2 in Text Analysis where we were to analyze user sentiment on beer reviews from <a href='https://www.beeradvocate.com/beer/top-rated/'> Beer Advocate's </a> top 250 beers. Specifically, we needed to collect around 25 reviews for each beer in the top 250. This means we had over 6,250 rows of unstructured data in total.  <br><br>
The code is split off into different sections that I will describe in detail below:
<ol type="a">
  <li>Webscraper</li>
  <br>The webscraper uses a combination of two packages, Selenium and Beautiful Soup. Both of these were used because of their individual benefits. For example, Beauitful Soup makes parsing through HTML easily. This enabled us to parse for each beer's URL. With those URLs, we were able to automate the process of clicking through each of those URLs and scrape a beer's name, user rating, and user comments/reviews. Once complete, the data needed to be split since all comments were one combined into one item in a list. We also needed to cean the data as some HTML code remained in the comments. Once complete, the dataframe was written as a CSV file and passed on for analysis.
  
  <li>Word Frequency Analysis</li>
  
  <li>Cosine Similarity</li>
  <li>Sentiment Analysis</li>
  <li>Evaluation Score</li>
  <li>Spacy Simliarity</li>
  <li>Analysis of Results</li>

</ol>

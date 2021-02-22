# Text Analysis Assignment 2 :beers:
A repo for code used for completing project 2 in Text Analysis where we were to analyze user sentiment on beer reviews from <a href='https://www.beeradvocate.com/beer/top-rated/'> Beer Advocate's </a>:beer: top 250 beers. Specifically, we needed to collect around 25 reviews for each beer in the top 250. This means we had over 6,250 rows of unstructured data in total! :smile:  <br><br>
The code is split off into different sections that I will describe in detail below:

<ol type="a">
  <li>Webscraper</li>
  <br>The webscraper uses a combination of two packages, Selenium and Beautiful Soup. Both of these were used because of their individual benefits. For example, Beauitful Soup makes parsing through HTML easy. This enabled us to parse for each beer's URL. With those URLs, we were able to automate the process with selenium by clicking through each of those URLs and scrape a beer's name, user rating, and user comments/reviews. Once complete, the data needed to be split since all comments were one combined into one item in a list. We also needed to cean the data as some HTML code remained in the comments. Once complete, the dataframe was written as a CSV file and passed on for analysis.
  
  <br><li>Word Frequency Analysis</li> <br>
  Further data pre-processing is needed to peform analysis on the data. The words need to be rid of certain characters such as dashes and underscores. Once we are sure that the data is purely words, we removed common english stop words such as I, me, my and myself. These words, in terms of frequency, appear often yet provide no value in terms of analysis, so they are removed. After this, we created another function that will put everything together.
  
  <br><li>Cosine Similarity</li><br>
  The data is now ready to be analyzed by calculating the cosine similarity scores where a review will be tokenized and put into a matrix using sklearn's CountVectorizer. A function, cosine_sim_vectors, reshapes the vectors in the array into a straight line, and returns the consine similarity between the two vectors.
  
  <br><li>Sentiment Analysis</li><br>
  Similarity score will tell us how similar a review is to a certain features, but it will not tell us if this review is negative or positive, which reveals a lot more information than smiliarity score alone. To produce a Sentiment Analysis score, the VADER sentiment analysis tool was used. In essence, VADER will match words to an emotional "score" and these scores will be summed to create a sentiment score. In this situation, the review is removed of all punctuation, split into words and identify the feature of interest. Once that is done, the words will be analyzed for sentiment and will be added to the data frame.
  
  <br><li>Evaluation Score</li><br>
    An evaluation score was created as a prliminary evaluation metric that sums the cosine similarity score with the average sentiment of each product. Based on this metric, we identified Double Shot, Morning Wood, and Ten FIDY- Bourbon Barrel Aged as the "top" products based on the features taste, sweet, and head - where head is the layer of foam on top of the beer.
  
  
  <br><li>Spacy Simliarity</li><br>
  SpaCy, a python package that provides a high powered NLP tool, is used as another way to compute similarity score. Using the same evaluation metric as before, the top three beers are Double Shot, Morning Wood, and The Abyss.
  
  <br><li>Analysis of Results</li><br>
  The top three products to be recommended based on highest average user rating are Chemtrailmix, It Was All A Dream, and SR-71. All three of these had very low cosine similarity scores, but relatively high spacy similarity scores. The average sentiment scores for the three are across the board - for example, Chemtrailmix (the beer with the highest average user rating) has an average sentiment score of .21, which is very low. The second highest, It Was All A Dream, is higher at .83, and the third highest beer in terms of user rating had an average sentiment score of .52. It does not seem that all of these products would meet the requirements of our user since the similarity scores are not very high for the attributes that were used in this analysis.
  

</ol>

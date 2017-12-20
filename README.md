#Fall 2017
# Sentiment-evaluation
Dataset: http://cs.stanford.edu/people/alecmgo/trainingandtestdata.zip
From the given dataset the sentiment value and tweet are read in.
Cleaning of tweet:
-Convert all letters into lowercase.
-Convert all occurences of 'www.website' or 'https:website//' to URL . For example http :
==twitpic:com=2y1zl becomes URL.
-Remove additional white spaces.
-Remove all punctuation.
-Convert @username to AT-USER
-Replace duplicate words - e.g. 'very very' should be replaced by very.
#########################################################################################
After cleaning up the data unigram features are extracted from the bag of words which is created
above.
Example of unigram feature:
Consider we have the tweets "John likes to watch movies. Mary likes movies too." and the tweet
"John also likes to watch football games". The bag of words (Steps 1-6) gives us
(John,likes,to,watch,movies,Mary,too,also,football,games.)
To now extract unigram features, in the tweet "John likes to watch movies. Mary likes movies
too." count the number of times each word appears in the bag of words. Thus, the feature vector
would look like [1, 2, 1, 1, 2, 1, 1, 0, 0, 0]. John occurs once in the tweet, likes occurs twice
and so on.
###########################################################################################
Follwing algorithms are run to train an SVM:
PEGASOS 
AdaGrad

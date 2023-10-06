In the provided code, I created a Python script to accomplish the following tasks:

1. **Read Data Files:** The code begins by reading two input text files: `nice_words.txt` and `tweets.txt`. This step is crucial because it retrieves the necessary data for sentiment analysis. 

   - `nice_words.txt` contains a list of words typically associated with kindness.
   - `tweets.txt` contains a collection of tweets that need to be ranked based on their level of kindness.

   I used the `with open(filename, 'r')` construct to safely open and read the contents of these files.

2. **Define a Function for Counting Nice Words:** A function named `count_nice_words(tweet)` is defined. This function takes a tweet as input, splits it into words, and counts the number of words in the tweet that are also found in the list of nice words. This function is used to determine the kindness score of each tweet.

3. **Iterate Through Tweets:** The script then iterates through each tweet in the `tweets` list and applies the `count_nice_words()` function to calculate the kindness score for each tweet. The results are stored in a dictionary called `tweet_scores`, where the key is the tweet text, and the value is the kindness score.

4. **Sort Tweets by Kindness Score:** The `sorted()` function is used to sort the tweets in descending order based on their kindness scores. This step ensures that the tweet with the highest kindness score appears first in the sorted list.

   - `sorted_tweets = sorted(tweet_scores.items(), key=lambda x: x[1], reverse=True)` performs the sorting operation.

5. **Display the Results:** Finally, the script displays the sorted tweets along with their corresponding kindness scores. Each tweet is printed along with the count of nice words found in it.

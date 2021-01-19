# What do you Tweet?
My humble attempt at observing the twitter activity by analyzing the textual content of the tweets of my tech savvy cousin.

## Objectives
- To understand and analyze the trend in tweeting behaviour.
- Perform Topic Modeling to identify key topics
- Visualize trends in the hashtags and key topics tweeted.

## Data Collection
Using the [GetOldTweets3](https://pypi.org/project/GetOldTweets3) from the got python package the complete archive of the user twitter activity is retrieved. Tweets can be retreived by using the below code with the twitter handle mentioned as part of the parameter

```python
import GetOldTweets3 as got
tweetCriteria = got.manager.TweetCriteria().setUsername("")\
                                           .setMaxTweets(2)
tweet = got.manager.TweetManager.getTweets(tweetCriteria)[0]
```

## Implementation
- Used GetOldTweets3 to retreive tweets
- Performed data and text cleaning by removing stopwords
- Created a wordcloud of key words tweeted
- Extracted hashtags from the tweets and plotted the usage frequency of different hashtags using matplotlib
- Performed Latent Dirichlet Allocation topic modeling on the tweets to identify the key topics observed evidently in the tweets

## Results
- LDA topics are visualized along with the hashtag usage frequencies across all the tweets

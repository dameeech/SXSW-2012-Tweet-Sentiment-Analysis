# SXSW 2012 Tweet Sentiment Analysis

![Screen Shot 2021-09-14 at 9 52 13 PM](https://user-images.githubusercontent.com/32643842/133357488-81ac50ba-5f7f-4922-8361-151382411732.png)

## Business Case
Perform a sentiment analysis of the South by Southwest 2012 festival based on tweets sent by attendees. Make recommendations for the next event based on the findings.

Our initial dataset had over 9,000 tweets with each tweet having a sentiment associated with it. During exploratory data analysis, we chose to concentrate on positive and negative tweets. This reduced our tweet count to 3548 tweets. 84% of these tweets had a positive sentiment and therefore, of note, our dataset is heavily skewed toward a positive sentiment. 

## EDA

Of the words in the corpus of all tweets, SXSW was represented equally in positive, negative, and even the discarded neutral tweets implying that its presence in a tweet did not affect the sentiment of the tweet but rather was in reference to the user being present at the festival. Ipad, Apple, Google, store and iphone were the most frequently used words in positive tweets. Similarly, ipad, Google, iphone, and Apple along with App were the most frequently used in negative tweets. This was unsurprising considering Apple and Google are the largest tech giants on the planet.

### Positive, Negative and Neutral Word Clouds
<p float="center">
  <img width="33%" src="https://user-images.githubusercontent.com/32643842/133357756-1c74d4a8-097e-4a69-882d-ff5b56b99d51.png" alt>
  <img width="33%" src="https://user-images.githubusercontent.com/32643842/133357763-07665439-2880-498c-b7ee-a34917b9435e.png" alt>
  <img width="33%" src="https://user-images.githubusercontent.com/32643842/133357774-a42c152c-3f31-40c9-8e74-dda192586e8c.png" alt>
</p>

After our initial data exploration we decided to plug the tweets into a classification model to get some deeper insights into how people felt about specific things during the festival. Since our data was overwhelmingly positive, we had to work hard to minimize that imbalance to get the most accurate model. Following exhaustive classification modeling, we concluded that our random forest classification model performed the best with an overall accuracy of 88%. While that is not what we would call stellar performance, our goal was not to create a flawless model for future sentiment analysis. We needed the model to show us what specific things were talked about in a positive and negative way.

### Feature Importances
![top_positive_words](https://user-images.githubusercontent.com/32643842/133358079-a2bd71ec-34b3-40ec-b5da-df66ae62be9e.png)
![positive_fi](https://user-images.githubusercontent.com/32643842/133358043-a809059f-5f5c-44b0-b89f-802f8f903f41.png)

We compared the most frequent words in positive and negative tweets with the feature importances of words obtained from our model. As these bar graphs reveal, Apple and #Apple are both frequently used terms in addition to weighing heavily as to the overall positivity of an individual tweet. Google additionally showed to be important, however, although the word counts for Google and Apple are similar, Apple’s importance far outstrips that of Google. Notably, Pop-Up - which is referencing a pop up venue at the festival - has a significant influence on positive tweets especially when considering its relatively small word frequency.

For the equivalent comparison in regards to negative tweets, the word counts for Google and Apple are again similar yet Google’s influence on negative tweets eclipses that of Apple by about 13 times. It’s clear that people were not happy about Google’s overwhelming presence at the festival. As to whether this displeasure was in regard to the recently built Google Village at SXSW or about their newly introduced privacy policy, the tweets do not elucidate. As a last point, the word ‘people’ was one of the driving factors in determining negative sentiment which suggests that most attendees are not the biggest fans of people or crowds in general and is ironic in juxtaposition to the much hyped social networking apps, Highlight and Glancee, that were introduced at this year’s festival. It could also suggest that they found the event to be too crowded which we can take as a sign that the festival continues to be a big draw.

![tri_rfc_negative_fi](https://user-images.githubusercontent.com/32643842/133358274-638fde87-8da3-4230-a364-42970d661b8e.png)
![negative_fi](https://user-images.githubusercontent.com/32643842/133358287-782f86c9-00d9-4f42-836a-78a759a94a00.png)

## Summary And Recommendations

In conclusion we can confidently say that based on our analysis the 2012 festival was a rousing success! By extracting individual words from our model we can see that Apple was particularly well received. We recommend prioritizing Apple next year for primetime panels and events. At the same time Google was a key driver of negative sentiment. While we can’t recommend banning the software giant outright, we would caution about how much time we would spend promoting their appearance at the next festival. On a more practical note, Pop-Up venues were unequivocally a big hit and should definitely be brought back and expanded on in the next year.

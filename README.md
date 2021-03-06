<h1 align='center'> Restaurant Review Classifiaction using NLP </h1>

## Project Motivation

In the modern day, public discussion and critiquing of products and services occurs beyond dedicated mediums, and now also takes place in the realm of social media.

What if a potential customer has already decided that they don’t want to visit a restaurant because of a friend’s tweet or Facebook review? 

Online restaurant reviews are currently found on Yelp, TripAdvisor, and Google Reviews. A new customer might find which restaurant they want to go to by browsing any one of these review sites. However, opinions are shared constantly on social media platforms and are read by their followers. The knowledge of what these followers think about local restaurants, from reading these online posts, could help us better understand the general public's perception of certain restaurants.

By using NLP, on existing restaurant reviews from Yelp, I have created a model that can predict if the authors public message on social media are positive or negative.

## Data Source

Used data from Kaggle: https://www.kaggle.com/omkarsabnis/yelp-reviews-dataset

## Approach

The data was imbalanced with the majority of the data being positive reviews. To prevent bias in the model I used SMOTE to synthesize more negative reviews, thus balancing the data classes. To analysis the text I used a TF-IDF Vectorizer, paired with a text pre-processing script to remove stop words and punctuation. I compared the performance of three machine learning algorithms (Naive Bayes Multinomial, Logistic Regression, and Random Forests) and performed parameter tuning on each to maximise performance.

## Results

Using a tuned Logistic Regression, I managed to predict if social media posts about restaurants were negative or positive to a 89% accuracy.

By combining data from social media about a restaurant, the model would be used to identify areas with a positive and negative outlooks on the business. The business could then deploy targeted strategies to these different groups to increase the publics option of the business, therefore increasing profits.

## Example Reviews

The below examples are from a Twitter hashtag search of one of my favourite local restaurants. 

<p align="center">
  <img src="https://github.com/RamonJWS/Yelp_Review_NLP/blob/master/examples.PNG" width=1500>
</p>

## Future Improvements

The system designed is currently a batch learning algorithm, to truly deploy this model it would need to be paired with a data scraping tool that would feed mini batches into an online version of the algorithm. This would then constantly classify peoples opinions of the restaurant, which is key as opinions can change. This classified data could be used with a clustering algorithm to find out niche markets and help the business make better decisions in real time.

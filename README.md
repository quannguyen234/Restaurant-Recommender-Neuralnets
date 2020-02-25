# Foodstruck - Dating App for Food Lovers

### Project Objectives 
- "Match" users using Natural Language Processing and Content-Based Recommendation System
- Recommend restaurants to the "matched users" using Collaborative Filtering System 
- Improve accuracy on recommendations using Neural Network Embeddings

### Dataset
Open Dataset from Yelp:
- 6 600 000+ Reviews/Rating
- 190 000+ Businesses
- 1 600 000+ Users

### Exploratory Data Analysis and Data Processing
![](Images/num_rev_before.png)

Because the range of number of review per user was huge (Maximum: 13000 reviews, Minimum: 1 review), and there were a lot of outliers, I decided to only get the users who have more than 60 and less than 120 reviews. 
Another feature engineering I did was to get only the businesses in Las Vegas. The reason was that there were many cities in this Yelp dataset, and the number of busisnesses per city was very different with Las Vegas having the most restaurants (30 000+).


![](Images/num_review_after.png) 

After pre-processing, there are:
- Users: 31 000+
- Businesses: 18 000+
- Reviews: 700 000+
</br>


![](Images/rating_distribution_after.png)

Another thing I want to mention is that the rating distribution is left skewed. I think the reason is because of "5-star rating bias" where people only rate places they like but do nothing for the restaurants that they don't like.

## "Match" User

The idea is that if 2 people have the same taste in food and talk about something in the same way, the chance for them to like each other would be likely higher.

In this step, I performed Natural Language Processing on user's reviews to see how similar they are, and then group them together.

**Process:**
- Create Bag of Words (BoWs) for each user's reviews
- TF-IDF Vectorize the BoWs 
- Compute Cosine Similarity
- Using Cosine Similarity to group the users together









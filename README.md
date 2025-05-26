# DataMining_Homework05
# Data Preparation

Downloaded and extracted the `ml-100k.zip` dataset.  
Loaded the `u.data` file using `pandas.read_csv()` with a tab separator.  
Constructed a utility matrix with users as rows and items as columns, where each value represents a user's rating for a specific item.

# Problem 1 – User Similarity and Rating Prediction

Centered the utility matrix by subtracting each user's mean rating to normalize preferences.  
Missing values were filled with 0 to allow cosine similarity calculations.  
Computed cosine similarity between users based on the centered ratings.  
Identified the top 10 users most similar to a target user.  
Predicted the target user’s rating for a specific item by averaging the ratings of that item from similar users.

# Problem 2 – User-Item Profile Similarity

Reused the centered utility matrix to extract user profiles for two specific users.  
Built an item profile vector for the target movie using the same rating space to ensure matching dimensions.  
Computed cosine similarity and distance between each user profile and the item profile.  
Compared the results to determine which user the recommender system would more likely suggest the movie to.

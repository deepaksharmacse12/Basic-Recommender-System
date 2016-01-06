# Basic-Recommender-System

## Usage

## Collaborative Filtering
1. `recommendations.sim_distance(recommendations.critics,'Lisa Rose','Gene Seymour')` : gives
similarity score between 'Lisa Rose' and 'Gene Seymour'.
2. `recommendations.sim_pearson(recommendations.critics,'Lisa Rose','Gene Seymour')` : gives 
Pearson correlation score between 'Lisa Rose' and 'Gene Seymour'.
3. `recommendations.topMatches(recommendations.critics,'Toby',n=3, similarity = sim_pearson)` : returns the best matches
of similar users for 'Toby' from the 'recommendations.critics' dictionary with pearson score as similarity measure
and top '3' results.
4. `recommendations.getRecommendations(recommendations.critics,'Toby',similarity=recommendations.sim_distance)` :
get recommendation for 'Toby', not only we get a ranked list of movies, but also a guess at what rating would be.
5. `recommendations.transformPrefs(recommendations.critics)` : returns dictionary with key values as movie and value as
dictionary of pair of person and rating (swap the people and items).

## Item-Based Filtering
6. `recommendations.calculateSimilarItems(recommendations.critics)` : builds the item similarity dataset, run frequently
enough to keep the item similarities up to date.
7. `recommendations.getRecommendedItems(recommendations.critics,itemsim,'Toby')` : gets recommendation for 'Toby' 
based on 'recommendation.critics' as rating dictionary and 'itemsim' as item similarity dataset.

## MovieLens Dataset
8. `prefs=recommendations.loadMovieLens( )` : load the dataset into prefs dictonary object.
9. `recommendations.getRecommendations(prefs,'87')[0:30]` : returns top 30 results of user based recommendations for
user with id '87'.
10. 

# Netflix-And-TV-Show-Clustering
# Our Goal

By creating clusters, we will be able to comprehend the shows that are alike and different from one another. These clusters can be used to provide customers with individualized show recommendations based on their preferences.

This project aims to classify and group Netflix shows into specific clusters in such a way that shows in the same cluster are similar to one another and shows in different clusters are different.

 # Problem Statement -
This dataset consists of tv shows and movies available on Netflix as of 2019. The dataset is collected from Flixable which is a third-party Netflix search engine.

In 2018, they released an interesting report which shows that the number of TV shows on Netflix has nearly tripled since 2010. The streaming service’s number of movies has decreased by more than 2,000 titles since 2010, while its number of TV shows has nearly tripled. It will be interesting to explore what all other insights can be obtained from the same dataset.

Integrating this dataset with other external datasets such as IMDB ratings, rotten tomatoes can also provide many interesting findings.

# Dataset
The dataset used in this project is sourced from Flixable, a third-party Netflix search engine. The data includes information on all movies and TV shows available on the streaming platform as of 2019, with a total of 7787 records and 12 attributes. Each attribute provides specific information about the movie or TV show. 

 # Data Pipeline
# 1.Know Your Data: The first step in this project was to examine the various features of the dataset, understand the structure of the data and identify any patterns or trends. We looked at the shape of the data, the data types of each feature, and a statistical summary.

# 2.Exploratory Data Analysis: We conducted an exploratory analysis of the data to identify patterns and dependencies, and to draw conclusions that would be useful for further processing.

# 3.Data Cleaning: We checked for duplicated values in the dataset and then addressed any null values and outliers by imputing empty strings and dropping some of the null rows.

# 4.Textual Data Preprocessing: We used techniques such as stop word removal, punctuation removal, conversion to lowercase, stemming, tokenization, and word vectorization to prepare the textual data for clustering. We also used Principal Component Analysis (PCA) to handle the curse of dimensionality.

# 5.Cluster Implementation: We used K-Means and Agglomerative Hierarchical clustering algorithms to cluster the movies and determine the optimal number of clusters.

# 6.Content-Based Recommendation System: We built a content-based recommendation system using the similarity matrix obtained from cosine similarity, which will provide the user with 10 recommendations based on the type of movie/show they have watched.


 # In this project, you are required to do
Exploratory Data Analysis

Understanding what type content is available in different countries

Is Netflix has increasingly focusing on TV rather than movies in recent years.

Clustering similar content by matching text-based features

 # Attribute Information
 
 # 1.show_id : Unique ID for every Movie / Tv Show

 # 2.type : Identifier - A Movie or TV Show

 # 3.title : Title of the Movie / Tv Show

 # 4.director : Director of the Movie

 # 5.cast : Actors involved in the movie / show

 # 6.country : Country where the movie / show was produced

 # 7.date_added : Date it was added on Netflix

 # 8.release_year : Actual Releaseyear of the movie / show

 # 9.rating : TV Rating of the movie / show

 # 10.duration : Total Duration - in minutes or number of seasons

 # 11.listed_in : Genere

  # 12.description: The Summary description
  
#   Conclusion

In this project, we tackled a text clustering problem in which we had to categorize and group Netflix shows into specific clusters in such a way that shows in the same cluster are similar to one another and shows in different clusters are not.


There were approximately 7787 records and 11 attributes in the dataset.

We started by working on the missing values in the dataset and conducting exploratory data analysis (EDA).

It was discovered that Netflix hosts more movies than television shows on its platform, and the total number of shows added to Netflix is expanding at an exponential rate. Additionally, most of the shows were made in the United States.

The attributes were chosen as the basis for the clustering of the data: cast, country, genre, director, rating, and description The TFIDF vectorizer was used to tokenize, preprocess, and vectorize the values in these attributes.

10000 attributes in total were created by TFIDF vectorization. The problem of dimensionality was dealt with through the use of Principal Component Analysis (PCA). Because 3000 components were able to account for more than 80% of the variance, the total number of components was limited to 3000.

Utilizing the K-Means Clustering algorithm, we first constructed clusters, and the optimal number of clusters was determined to be 4. The elbow method and Silhouette score analysis were used to get this.

The Agglomerative clustering algorithm was then used to create clusters, and the optimal number of clusters was determined to be 5. This was obtained after visualizing the dendrogram.

The similarity matrix generated by applying cosine similarity was used to construct a content-based recommender system. The user will receive ten recommendations from this recommender system based on the type of show they watched.

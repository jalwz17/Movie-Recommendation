# Collaborative_Filtering_Movie_Recommendation
> [!IMPORTANT]
> The dataset (CSV) Files are too large to be uploaded into Github, thus, please refer to this link if you would like to access the files.
>
> https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset/data 

### Introduction to Study:

This is a dataset that is focused on the metadata for movies. It contains around 26 million ratings from around 270,000 users for the 45,000 movies. This study aims to identify trends and patterns of the metadata containing a large amount of movies. Then create a model that would look over the categorical aspects of the dataset of the inputted movie to recommend movies that users would take interest in. Furthermore, using collaborative filtering, there would be another model that utilizes deep learning that can take insights from similar users who watched similar movies and ratings to recommend a movie. 

### Process and Challenges:

When first reading the files (```movies```, ```credits```), there were some poorly inputted data, which were removed. As for a few of the categorical columns like ```genres``` and ```original_title```, it was formatted in a different way, which required splitting the text and placing commas to separate them. After cleaning the data, many graphs and visualizations are made to showcase the connections between variables in the dataset. 

The first movie recommendation model utilizes a weighted average. This had a formula that was taken from IMDB that calculates the rating with a weight, as some votes don't have the same impact. Once the weighted average was calculated, the model can now use cosine similarity and the weight to find similar movies to the selected movie. It also shows the similarity score, how similar it is to the movie, and the final score, what the predicted rating would be.

> [!NOTE]
> This is the formula: (WR) = (v ÷ (v+m)) × R + (m ÷ (v+m)) × C

The next second model took a different approach, which is known as collaborative filtering. This would take the ratings of other users and find recommend a movie that had a good rating from similar users. This required the set up of another dataset, called ```ratings```. First of all, there was a need to construct a user profile of the selected user, which contains all of their movies watched and ratings. Then using cosine similarity once again to calculate and find the top 5 most similar users from the dataset batch. Tensorflow Keras was used as a neural network model to determine predicting ratings of high-rated movies from similar users. Thus, the top 5 movies from that list would be recommended to that particular user. 

A challenge that was prevalent in this study was a need to learn about cosine similarity, which is a metric used to determine the cosine distance between two objects and is used commonly in recommendation systems such as movie and book recommenders. As this was the first recommender system project, there was a lack of knowledge about cosine similarity, which took lots of time to try to understand and implement into the code. 

The implementation of deep learning and neural networks in this study was also an obstacle that took lots of time to debug and decipher what was happening behind the scenes. Due to the formatting of the dataset in the beginning, there is a possibility that there was a lack of care for certain columns and variables that made it more difficult to implement deep learning models. Also, there were some packages that had issues running on the coding platform which required to use of different methods, but luckily those were sorted out pretty quickly. 

> [!WARNING]
> Another challenge in this study was that the dataset was very large, as the second model had a dataset with the size of (10969249, 7), which required random batches to lessen the time and make it easier to compute. Luckily, it was easy to separate the large dataset into batches, but that made a few iterations lacking accuracy as it's in batches and not actually using the entire dataset to scan for similar users. 

### Observations and Interpretations:

The USA is very dominant in the production of movies as it almost reached the amount of producing 20,000 movies. Do note that this dataset is an old dataset, therefore, the USA will most definitely cross that amount in the present. With the establishment of Hollywood, it's safe to assume that most of the movie and film productions are held in the USA where the USA companies invest and produce them. As well as English being a universal language, films are created in English in the USA that are already catered to a majority of the world's population. 

> [!NOTE]
> This graph shows the large gap that the USA is leading in the production of movies[^1].
> 
> This graph shows the primary language in movies[^2].

It's interesting to see that the top genre across movies is Drama, which is followed by Comedy and Thriller. Regardless, there is still a big gap between these three genres. Movies might place Drama inside as they tap into the complexities of emotions, relationships, and experiences that the audience can feel. These highlighted aspects of storytelling keep the audience engaged and invested in the movie, which is probably the reason why Dramas are the most common genre in movies. Most people watch movies and stay watching as they are curious and as previously mentioned, invested in it, thus having drama makes it relatable and dives deep to connect with them on a more personal level, especially from the actors, storyline, music, and backgrounds. 

> [!IMPORTANT]
> The Drama genre leads as the number 1 genre in movies. The function that was used to organize the genres did a total summation of the genres provided, which means that even if the movie doesn't have drama as the main genre, it's still mentioned in the genre listing[^3].

It's also worth mentioning that throughout the study, lots of users were selected to test the performance of the model. An observation that was made was that the more movies that the user has watched, the higher the ratings are usually predicted by the collaborative filtering model. It would be assumed that due to the larger amount of data to train the model with, there would also be a larger amount of possible recommendations. Thus when the predicting modeling is done, the top 5 recommendations would have a very high predicted rating. 

 ### Conclusion:

Based on the collaborative filtering movie recommendation model, for the user with the ID of 4, the following movies are recommended with predicted ratings ranging from 5 to 4.725:
1. The Goddess
2. Dog Day Afternoon
3. Frances
4. License to Wed
5. I Love You to Death

Due to the lack of knowledge of cosine similarity, there could have been more fine-tuning and testing to improve the accuracy of the movie recommendations. Also, with a more powerful device, there could easily be a better way to access the large amounts of data of ratings from users that can make it easier to find similar users to the selected users that would provide more movie recommendation options.

Some other areas of interest would be to combine Natural Language Processing (NLP) into the collaborative filtering model to further personalize the recommendations based on the previously watched movies' overviews with the provided options. This can also be applied to the genres, actors, crews, etc.

Looking to the future, this study could have been fed some personal ratings from myself and output a few recommendations for myself to try. Then, I could personally validate the model based on the predicted ratings and recommended movies.  

### Footnotes:
[^1]: [Top Production Countries](https://github.com/jalwz17/Movie-Recommendation/assets/95889788/0b47a45b-fcdd-42e0-9130-ddbbec7f4500)
[^2]: [Primary Language in Movies](https://github.com/jalwz17/Movie-Recommendation/assets/95889788/750d72c6-ed28-4452-8efd-950a4c83cb0e)
[^3]: [Top Genres](https://github.com/jalwz17/Movie-Recommendation/assets/95889788/edb4c5d6-075d-4f36-b1c2-64cdf8520f3c)

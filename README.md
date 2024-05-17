# Collaborative_Filtering_Movie_Recommendation
> [!WARNING]
> There is no information about athletes for team competitions that consist of more than 2 participants. Only team records.
> 
> There are no results for qualification rounds. For instance, event 100-m men contains only final results without semi-finals and other hits.

### Introduction to Study:

The 2024 Olympics known as Paris 2024 are scheduled to take place from July 26 to August 11, 2024. The Olympic Games are a very popular, multicultural celebration to share in the world of sports and so much more. As there have been many changes and modifications to the Olympics, the focus of this study is to identify trends in the performance of countries over time. This study focused on the future performances such as the 2024 Olympics, of top-performing countries in the Olympics with the calculation of the total medals won. In this study, it’s hypothesized that the accumulation of previous medals correlated with an increased potential for winning an equal or greater amount of medals in the future Olympic Games. 

### Process and Challenges:

Initially, the three datasets (```athletes_data```, ```hosts_data```, ```medals_data```) are merged to form ```olympic_data```, containing around 17,000 rows of data. The cleaning consisted of removing columns that had more than 20% of null values. There were also a few data entries that needed to be renamed, so that was done with a class map. Some important variables primarily used were ```medal_type``` (gold, silver, or bronze), ```game_season``` (Winter or Summer), ```game_year```, ```athlete_year_birth```, ```discipline_title``` (the overall discipline groups), ```country_name```, ```athlete_full_name```. These variables allowed the creation of functions and visualizations that showcased the countries’ information on their athletes and medals, and how those are correlated with their success in the Olympics. 

Throughout this study, a challenge that was encountered was how to effectively present the data in a comprehensible manner. After a few trials, a function called ```plot_heatmap``` was created that displayed how the number of appearances a discipline made in the Olympics. In the grid layout heatmap, a green box (discipline was played) or a white box (discipline not played). 

> [!NOTE]
> This graph shows the Olympic Summer Season and disciplines are listed in alphabetical order[^1]. Some newly added Summer disciplines: Cycling BMX Freestyle, Karate, Skateboarding, Sport Climbing, and Surfing.

Another important function is ```plot_trends``` which generates a bar chart of the country’s totals of medals (gold, silver, bronze, or all) by each Olympic game for the season (Summer, Winter, or both). It provided a more individualized overview of the country as well as the trend of the medals won at the Olympics. 

Another challenge arose due to limited experience in handling time series datasets, so there was time dedicated to researching to understand the necessary concepts and techniques. Afterward, there were difficulties with the integration, as the time series prediction models and the ```olympic_data``` setup didn’t complement each other. After careful debugging, the time series models successfully predicted 4 Olympic Games (2024 2026, 2028, 2030).

### Observations and Interpretations:

The USA is very dominant in the Olympics with a total of up to 2442 medals, with Germany trailing behind by 868 medals. This massive lead may have been due to the boycott from the Soviet Union and their allies against the 1984 Olympics. This boycott led the USA to have reduced competition and it boosted their total medal counts to make them the medal count leaders of the Olympics. Also, this Olympics was held in the USA, and they could have done well due to their home-court advantage. Out of the 5 Olympics that were held in the USA, the USA has won 4 of those Olympics. The home-court advantage could have led to more national pride and motivation to perform far better than their competitors. 

> [!NOTE]
> This graph shows the sudden spike for the USA in 1984 and the immediate drop from the Soviet Union and Germany[^2].

Due to the Olympics's separation of the Summer and Winter seasons, each season happens every 2 years, and the graphs showed a cyclical pattern. As there are more disciplines in the Summer season, the common pattern is a spike up during the Summer Olympics and a drop in the Winter Olympics. On the contrary, Norway has shown an inverse to this pattern as they demonstrated exceptional performance in a majority of the Winter Olympics. Thus, they are taking a majority of the medals in the winter and this could be due to their cultural importance in winter sports as it often snows in Norway. In addition, the stunning scenery and backgrounds in Norway could have promoted a more outdoor lifestyle, which exposed their athletes to outdoor winter sports. Followed up with their strong overall legacy in winter sports, definitely served as an inspiration for them to continue to perform well. This can be seen in their top two disciplines, which are cross-country skiing and speed skating, signaling their investment into winter sports. 

> [!IMPORTANT]
> Unlike the rest of the top-performing countries in the Olympics, only Norway shows the opposite performance to the cyclical performance the other countries have. This graph can be interpreted that as Norway won lots of medals in the Winter Olympics and there are fewer disciplines during those games, it's safe to say that Norway is winning a majority of those medals, signaling their dominance in the winter sports[^3].

China has never gotten an Olympic medal until the 1984 Olympics. As mentioned earlier about the lesser competition during the 1984 Olympics, China was able to make its mark. This could have been a way where ‘success breeds success’ and it might be paired with a recent president change around that time, the government might have had a shift in their investments after winning around 25 medals in the 1984 and 1988 Olympics. They have then a strategic focus on certain key sports, where they have been known as a powerhouse in those sports, such as table tennis. Their concentrated efforts continue to maximize their medal-winning potential through talent identification as China strengthens its already winning disciplines. From the looks of the upward trend on their medal counts in the Olympics, China must be able to recruit and develop great athletes in their dominant disciplines, so they continue to perform very well and secure even more medals every Olympics. 

> [!NOTE]
> This graph shows how China had only success after the 1984 Olympics and has been performing very well afterward[^4].

The median Olympic athlete's year of birth from this dataset is between the years 1991 to 1996. Therefore the newer generation of Olympic athletes would be around 25 years old and younger. The performance analysis of the newer generation revealed that most if not all of the medals they have won were gold medals. This shows that young athletes have lots of potential and success from their early specialization in their disciplines. They must have had better teaching, training techniques, and training equipment which exponentially increases the number of young athletes competing at the highest level. In addition, the young athletes are also prioritizing their country’s top disciplines. For example, both Katie Ledecky and Robert Finke are in swimming, which is USA’s second top discipline. 

> [!NOTE]
> This graph shows the distribution of all the birth years of the athletes in bins[^5].

 ### Conclusion:

Based on the time series prediction model results[^6], the USA will win the most amount of medals (98 medals) in the 2024 Summer Olympics. It was hypothesized that there is a correlation between the accumulation of medals from the past, signaling previous success, and future performances. This showed that they already had the experience of winning, therefore, they should be able to replicate that for future Olympic Games. Following the 2024 Olympics, it is predicted that Germany will lead in the 2026 Winter Olympics (32 medals), China will lead in the 2028 Summer Olympics (107 medals), and Norway will lead in the 2030 Winter Olympics (30 medals). As previously observed, China has been the rising star in the Olympics since the 1984 Olympics and Norway has always shown dominance in the Winter Olympics. 

For future research, obtaining more data regarding the events that contain more than 2 athletes would change the predictions as this current prediction model is projecting less due to less amount of data regarding team events and disciplines. In addition, the factors were very limited in the prediction of the future medal amounts as it’s not just based on previous medals won. So being able to add more data into the prediction dataset would be better, such as the amount of new disciplines being added to the Olympics, the number of young and veteran athletes, and also more data about the country itself. This data would consist of GDP, training programs, coaches, and investments, which would be very helpful to make a more accurate prediction. 

### Footnotes:
[^1]: [Plot Heatmap Function](https://github.com/jalwz17/Olympic_Medals_Analysis/assets/95889788/3b21e984-42bc-4629-af60-01ff3a71889c)
[^2]: [Medal Counts by Country Over the Years](https://github.com/jalwz17/Olympic_Medals_Analysis/assets/95889788/f427397c-214c-4db7-ad25-1694a5eac88c)
[^3]: [Number of All Medals Won by Norway during Both Seasons](https://github.com/jalwz17/Olympic_Medals_Analysis/assets/95889788/95aee862-52cf-4970-8383-64bac8e17f14)
[^4]: [Number of All Medals Won by China during Both Seasons](https://github.com/jalwz17/Olympic_Medals_Analysis/assets/95889788/4ea634cd-9f34-4b8d-94e0-a806bdf04ee8)
[^5]: [Count of Athletes by Year of Birth with Trend Line](https://github.com/jalwz17/Olympic_Medals_Analysis/assets/95889788/3ef473c7-9efd-458f-94e9-2a6ede441d1f)
[^6]: [Example: SARIMAX Prediction for USA](https://github.com/jalwz17/Olympic_Medals_Analysis/assets/95889788/73c9babb-16e6-476e-9ff2-fd77446f22b8)

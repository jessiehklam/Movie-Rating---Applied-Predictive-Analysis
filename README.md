# MOVIES ANALYSIS - APPLIED PREDICTIVE ANALYTICS

## Introduction

Rating is common basis for movie selection. Thus, the goal of this analysis is to find the possible factors that will affect the rates of movies, such as popularity, genre, and budget. For this purpose, we obtained the Movies Dataset from Kaggle, and we run a logistic regression to find out the key variables that leads to a successful movie. Our results show that “Educational” genre and popularity have a statistically significant effect on movies’ rating.

In the dataset, the top 20% of movies have a 7 or higher rating, so we marked a movie to be “good” if its rating is greater than or equal to 7. Since the mean average rating is around 6.5, this threshold is a reasonable value to benchmark a great movie. 

### Count of Movies by Genres
![](https://i.imgur.com/nAn0wA4.png)
#### For analysis, we classified 15 plus genres to 4 main categories, that are Entertainment, Action, Education, and Others.
•	Entertainment: Comedy, Drama, Animation, Mystery, Family and Romance
•	Action: Horror, Triller, Action, Crime, Western and Adventure
•	Education: Documentary, History and War
•	Others: Fantasy, Foreign, Science Fiction, and Music


### World Cloud of Movie title
![](https://i.imgur.com/LsAC75N.png)

### Count of Movies by Release Years
![](https://i.imgur.com/NDOX0u7.png)

## Regression



| Predictors         | Coefficient | Statdard Error | z-Value | p-value  |
| ------------------ |:----------- | -------------- |:------- |:-------- |
| intercept          | -2.508      | 5.44E-02       | -46.084 | 2.00E-16 |
| budget             | -3.29E-08   | 1.94E-09       | -16.969 | 0.0314   |
| popularity         | 0.009       | 4.23E-03       | 2.152   | 2.00E-16 |
| runtime            | 0.005       | 4.33E-04       | 12.411  | 2.00E-16 |
| genreEducation     | 1.537       | 5.19E-02       | 29.608  | 2.00E-16 |
| genreEntertainment | 0.688       | 3.78E-02       | 18.188  | 8.79E-11 |
| genreOthers        | 0.501       | 7.73E-02       | 6.486   | 2.00E-16 |
| vote count         | 0.001       | 6.70E-05       | 20.08   | 2.00E-16 |

## Limitations
While the model above provided us with multiple insights. However, given the dataset and the procedures we took to analyze the meta-movie dataset, we want to mention some limitations that our model may contain:
1.	Multiple columns like “budget” and “revenue” have a certain amount of zero-value, according to the movie dataset description, these zero-values do not represent the movie had no budget nor revenue, instead, zero-values are the direct result of the data cannot be measurable, despite the reasons behind the unmeasurable data, zero-values posed significant influences to our model performance.
2.	To generate straightforward insights, we took a direct approach to only deem votes as the good-or-not measurement. This may be misleading, given specific categories of movies’ (like war, documentary, and history) audience groups may be much smaller than entertainment movies’ counterparts, the votes may not precisely represent certain movies’ quality.
3.	Prior to building the model, we took a daring approach to generate over 19 genres of movies into 4 categories for the convenience of model processing. This may pose a negative influence on precision. As we combine similar genres of movies into one category, fewer variables are created but a broader spectrum of movies to analysis may cause failure to identify the quality genre if it is among fewer quality genres.


## Recommendations
Despite the above limitations, the significance of our model’s findings should not be ignored.

●	Based on our findings, “budget” has a slightly negative relationship with the movies’ rating. It seems budget has little to do with the movie’s rating and higher budget may not add value to the movie itself. However, as what we have mentioned in the limitation part, there are over 30,000 zeros in “budget” in our original dataset, which will significantly affect its importance. As a result, even though budget seems not to be an important factor in our model, we still need further investigation to prove this finding.

●	Besides, the result shows that “popularity” will positively affect the movies’ ratings. Thus, we can go on some marketing campaigns to increase the awareness of movies, which may be helpful for increasing their ratings.

●	According to our model’s results, “Educational” movies (Documentary, History, and War) are likely to achieve decent ratings. Choosing these three genres of movies would receive good reviews and votes in greater possibility compared to other movies. Thus, ‘Educational’ movies are our best recommendation for movie makers. If we look at the movies that have the highest rating in the three genres (“Planet Earth II”, “The Human Condition: No Greater Love”, “Night and Fog”), we’ll find they are about humanism and environmental issues. This finding shows the issues that people concern most; therefore, if the director can add these elements in their movie, it would make their movies be well-reviewed. 

●	Specific genres of movies like fantasy, foreign, science and music that fall to the “Others” category may perform not well regarding the voting average. Thus, we recommend that while making these genres of movies, keep this finding in mind and do not be disappointed when rating may not be expected. It’s worth noting that the foreign movies got lower ratings than other genres. This illustrates that the foreign movies are not that popular in the US movie market, while those movies usually have good popularity or ratings in their home country so that they can be introduced to other countries. In this case, if we want to improve their ratings, the possible actions we can take are:
	Add English substitutes in every foreign movie.
	Going on some marketing campaigns to increase their popularity.
	Making better movie trailers to attract more audiences.

#### In summary, we include the essence factors in our model to evaluate how people give their ratings to the movies. Even though we think the model works well, there’s still many factors that make a movie great: “the overall value”, “novel ideas” and the “chemistry between actors”. Any future directors and producers must take all the factors into account when creating their next opus. 

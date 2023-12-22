## Ending our Journey
Returning to solid ground after a thrilling exploration of the cinematic cosmos, we now find ourselves equipped with knowledge acquired along this fascinating journey. Initially, we concluded that not all countries and languages were equal in their success. In the same breath, we unearthed that both movie runtime and budget are positive influencers of score. Then, as passionate movie fans, we were eager to explore the intricacies of movie genres. Our analysis focused on the 16 most popular genres, and we were ecstatic when we discovered the paradox that the most prevalent genres often do not secure the highest scores. We hypothesized that this was because people like novelty, but what do you think about this intriguing result? Once we had cracked the secrets of genres, we transitioned to the nuanced world of movie series. There we discovered that sequels in general perform much better than other movies, but that surprisingly sequels fell short of their predecessors in the overwhelming majority of cases. Transitioning to the emotional land of endings we were surprised to find out that they have virtually no impact on scores. Subsequently, we were proud to explore the novel concept of diversity and examine trends concerning movie success. Yet the results left us with mixed feelings as we found that ethnic diversity was positive, but gender balance was negative. Finally, we were happy to finish with actors and producers where we proposed a novel way of ranking them.

Now, as we stand at the crossroads of our cinematic exploration, the time has come to consolidate our findings. We will embark on a comprehensive analysis, employing linear regression with all our features to unveil the intricate interplay of factors influencing movie scores. This holistic approach allows us to examine the collective impact of various elements and identify the features with the highest weights in shaping the success of a movie.

# Linear Regression:
While we embark on this linear regression that will participate in building our final formula there are multiple things that we must consider. Firstly, it is essential that all our features be normalized so that the learned weights will reflect better the importance of each feature. Then the big question that we must answer is the following: What features are we going to include? One could say that we should include all of them as we want the most accurate model possible; however, in light of the influence that we found gender imbalance to have on movie score, we chose to ignore it in our model. Indeed, we do not want to propagate unethical analytics that could be used to perpetuate inequality. Additionally, we chose not to include whether a movie is a sequel from a movie series as our findings showed that sequels are nuanced and can't simply be applied to any movie to have success. In the end, we have a set of 123 features.

# Results
The R-squared value is a statistical measure that represents the proportion of the variance in the dependent variable (in this case, movie score) that is explained by the independent variables (features) in the linear regression model. The R^2 value ranges from 0 to 1, with 0 indicating that the model does not explain any variance, and 1 indicating that the model perfectly explains the variance in the dependent variable.

In our case, an R^2 value of 0.29 means that approximately 29% of the variability in movie scores can be explained by the features included in our linear regression model. While it doesn't account for the entirety of the variance, it indicates a substantial portion of the variation is accounted for, providing a reasonable level of confidence in the results obtained. But what are the findings?

In the graph below, we presented the top 20 (in green) and worst 21 (in red) features that influence movie score the most positively and negatively respectively. Note that the y axis represents the weight of that parameter in the linear regression, so the higher the absolute value, the more influence it has.

![Weights](/assets/images/Dark_Weight_Features.png)

## Building our Formula for a Great Movie

The linear regression model analysis sheds light on the intricate tapestry of factors influencing movie scores, offering a nuanced understanding of what contributes to cinematic success. At the forefront, the positive impact of runtime suggests that audiences tend to appreciate movies with longer durations, allowing for more in-depth storytelling or character development. Moreover, the emphasis on ethnic diversity, as indicated by the second highest weight for the ethnic count, underscores the growing recognition of the importance of representation in cinema, contributing positively to audience engagement and appreciation.

Additionally, we found that genre preferences play a pivotal role, with Drama, Animation, Romance, and Science Fiction emerging as genres positively correlated with higher scores and thus movie success. Interestingly, our statistics showed that Drama and Romance were the first and second most abundant genre types; however, Animation and Science Fiction movies are among the least common which means that there would be much to gain from developing more movies in those domains! 

Interestingly, the positive influence of certain countries, such as Japan, the United States, and Hong Kong, suggests that the geographical origin of a film can impact its perceived quality. Conversely, movies from Mexico, Canada, Russia, and Switzerland have a bad history of movie popularity. Notably, the global nature of the film industry is questioned, as significant contributors such as India and China exhibit a substantial negative impact on scores. Quantity does not mean quality!

The complex landscape of language preferences is evident, with French movies receiving very positive recognition, while Hindi films and indie productions face a more challenging landscape. A seemingly contradictory result lies in Bollywood’s success when Hindi films perform so badly. We don’t know the Indian cinematographic landscape enough to figure out why that is.

Additionally, our previous analysis reflected that the top actor in a cast is a great predictor of a movie’s score. This finding reflects the importance of having A-list actors!

Finally, we’d like to add that as we discovered in this data story, sequels navigate a nuanced landscape. Indeed, they can achieve much better results than the general movies; however, that is only if the prequel is successful. Yet one must be prepared for a regression as they rarely perform better than the predecessors!

In conclusion, the derived formula encapsulates a multi-faceted understanding of movie success, considering factors ranging from runtime and ethnic diversity to genre, country of origin, and language. 

### Closing remarks

As we bring this cinematic journey to a close, we invite you, the reader, to reflect once again on the intricacies of your cinematic preferences. Our exploration into the realms of movie scores, genres, and diverse features has unraveled many mysteries of the cinematic universe. If anything, we shed light on the complexities of this world, yet we hope that we succeeded in providing you with a better understanding of it. We encourage you to continue this exploration discovering new worlds, forging connections with unforgettable characters, and embarking on new journeys. Remember! Enjoy the moments of laughter and tears as you create everlasting memories.

As the credits roll on this data story, we thank you for joining us!

Anthony Kalaydjian,
Anton Balykov,
Yara Sabbagha,
Eric Saikali,
Aymeric de Chillaz

# Good or Bad Ending
Transitioning into the exploration of how the type of movie ending influences its success, we invite you to reflect on those moments when you left a theater with tears streaming down your face or laughter echoing in your ears. The strong emotions that you can get in the closing scenes are likely to leave a lasting impression. For instance, the sad farewell to Iron Man left many viewers (including us) in tears, evidence of the power of an emotional ending. It remains noteworthy that movie-goers desire different emotions from various genres. Indeed, a Horror movie with a happy ending would probably be disappointing, whereas it is exactly what we love in their Animated counterparts. Additionally, we could also expect the intensity of the sentiment to have an influence, as the impression of a high-intensity ending leaves a mark.

## Sentiment Extraction
But how can we extract the intensity and sentiment of endings from the data that we have? Navigating, through our dataset, we found a creative solution. Firstly, we determined that we could extract the endings from the last three sentences of the plot descriptions, which we had in our data. Then all we had to do was to use open-source models to extract the sentiment from the text. Easy!

To give you more visibility on the matter, here’s an example that’ll surely help. We will take the example of the world-renowned masterpiece, The Lion King. 

![Wiki](/assets/images/Warning_Symbol.png)
https://pa1.narvii.com/6384/b8ec2ccdb91f2623f22202c9b56e9637cd59abf3_hq.gif

_"Scar survives the fall, but is attacked and killed by the hyenas, who overheard his attempt to betray them. With Scar and the hyenas gone, Simba descends from the top of Pride Rock where he is acknowledged by the pride as the rain falls again. Sometime later, Pride Rock is restored to its former glory and Simba looks down happily at his kingdom with Nala, Timon, and Pumbaa by his side; Rafiki presents Simba and Nala's newborn cub to the inhabitants of the Pride Lands and the circle of life continues."_

You can find above the text that our method extracts as the “ending”. It is fair to say that the death of the villain and the hero’s happy ending are included and quite detailed. But now let's see what sentiment is detected here, seeing as we would qualify it as a positive ending. The predicted value is 0.8519 for the compound end sentiment, in a range going from [-1; 1], where -1 is a very negative sentiment and 1 is the opposite.

We apply this method to all our movies and plot the following heatmap of ending sentiment versus movie score.

{% include folder/heatmap_ending_compound_sentiment.html %}

Intriguingly, the heatmap reveals the presence of hot spots, the movie endings are agglomerated in 3 spots, very negative, very positive, or neutral. Moreover, this graph shows little to no correlation between the movie score and the ending’s sentiment, whether negative or positive, as data suggest a consistent dispersion of movie points around the score of 65. While this plot reinforces the notion that movie scores, in general, aren't strongly correlated with ending sentiment, it doesn't necessarily contradict our earlier hypothesis. Indeed, we expected certain genres such as Horror movies to be more prone to a side of the spectrum. To put this claim to the test, let's delve into the sentiment distribution within different genres!

{% include folder/correlation_Sentiment.html %}

Our initial attempt to assess correlations using Pearson Correlations faced challenges, with low statistics indicating minimal linear correlation. Furthermore, the majority of p-values exceeded our confidence level of 0.05, preventing us from rejecting the null hypothesis. Could the correlations not be linear? In that case, Pearson would not fit the task. Considering this eventuality, Mutual Information was computed, yet that yielded the same conclusion: movie success does not depend on the sentiment of its ending! Note that a Mutual Information of 0 essentially means that the two are independent. 

Then to push our analysis further, we considered the ending’s intensity as an influencer of movie score. Same as before, we plot movie density as a function of score and sentiment intensity.

{% include folder/heatmap_sentiment_intensity.html %}

Once again, no clear pattern comes out of this plot other than that the overwhelming majority of movies are categorized as high-intensity. This is not great for our analysis as unbalanced data limits our insights. Still, we compute a statistical test notably a Pearson correlation and Mutual Information to test for non linear correlations. 

{% include folder/correlation_Intensity.html %}

Once again, the results show that there is no significant correlation between the two. In fact, some genres such as “Adventure” have no mutual information with the score! In essence, our initial hypotheses were completely wrong. The sentiment of a movie’s ending whether it be good/bad or intense/calm, does not influence its success!



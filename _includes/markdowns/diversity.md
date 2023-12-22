# Movie Diversity 

Ready to spice up our movie formula? Let’s move on to a topic that is becoming increasingly pivotal with time: movie diversity. When watching a movie, we want to match with the characters which is facilitated by physical resemblance, common origins, or similar gender identities. So come with us to analyze how we measure diversity, and how it contributes to movie success. 

First, please note that for this study, we needed more information about the movie actors, so we scraped the Wikidata website. The dataset generated includes information about actors’ ethnicity and gender: [wiki data sparql link](https://query.wikidata.org/sparql). 

## Ethnicities: 
Now, how diverse do you think are actors’ ethnicities in the movie industry? One would have thought that the most common ethnicity is “White” (human racial classification), but it turns out that it’s actually “Indian”. 

{% include folder/ethnic_category.html %}

As you can see, some of these ethnicities seem similar, like “American” and “Lebanese American”. Therefore, we decided to generate a network graph presenting ethnicities similarities in the entire film industry (similar ethnicity names are connected with a gray line). Three distinct clusters appear: in the middle, we have the well-known ethnicities, the small “line” on the left represents some extremely close ethnicity names, and the ethnicities forming the outside oval are all unique in a certain way, and don’t resemble other ones. 

{% include folder/ethnic_network.html %}

Next, we define a diversity threshold: movies with at least three different ethnicities are considered diverse. 

{% include folder/unique_ehnicity_tags_per_movie.html %} 
{% include folder/ehnicity_tags_per_movie.html %} 

As seen on the left histogram, movies all have more than 3 different ethnicities. However, that is not actually true. For example, some movies say they cast actors from 2 ethnicities “American German and German American”, but these are technically the same, so they should not be counted twice. Which is why we also established the histogram on the right, after having removed these duplicates. We notice that most movies cast actors from 2 to 4 different ethnicities. This distribution reflects producers’ effort towards making their movies more inclusive, grouping actors from different cultural backgrounds. 

Now, does being more inclusive mean being more successful? It seems like it! After doing some statistical tests, we obtain that with 95% confidence, the mean movie score of inclusive movies (number of ethnicities above threshold) falls within the range [66.0940, 66.6166]. The mean movie score of exclusive movies, however, is between [62.5040, 63.7419]. This can also be seen in the below point plot. 

{% include folder/ethnic_inclusivity.html %}


## Genders: 
Join us now while we delve into another integral inclusivity feature: gender representation. Movies most often mirror society, and its dynamics. As gender equality gained importance in real life, it also did in movies, moving from traditional roles to more inclusive and nuanced ones. Again, for this analysis, we defined a range determining if a movie is balanced or imbalanced: if the proportion of male actors is between 0.4 and 0.6, the film is considered balanced, otherwise it is imbalanced. It turns out that 11.38% of the movies are gender imbalanced in favor of women, and 88.62% are gender imbalanced in favor of men. 

Below, you can see the number of movies per percentage of male actors. It looks like a gaussian distribution centered around 0.65, which explains the 88.62% value. 
![THANKS ANTHONY](/assets/images/needed.jpg)

We then obtained surprising results: gender imbalanced movies had an average mean movie score within [67.6733, 68.5867], which is higher than [65.6577, 67.1005], within which gender balanced movies’ mean movie score lie, both with 95% confidence. 

{% include folder/inclusivity.html %}

So till now, movies with more gender imbalance have been more successful. However, this is unethical, and in a world where we are all constantly fighting for equal gender rights and representation, we will not encourage producing movies with more male actors, than female actresses. We advocate for a diverse and gender inclusive and balanced filmmaking industry that is more creative and authentic, that reflects our society and that connects with a broader and more diverse audience. 



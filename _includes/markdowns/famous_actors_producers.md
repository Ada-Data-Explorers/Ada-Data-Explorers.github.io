# Famous Actors

The intuition tells us that the cast of the movie has to have a significant influence on its success. If the funniest duo, The Rock and Kevin Hart, were acting in a movie, not only are we all going to watch it, exploding the box office revenue, but also the movie will naturally be a success. 

We want to somehow come up with the actor’s popularity for given actors and we know that many movies in our dataset were made long before social media and Google Trends (😅).
Since the two abundant data sources that are available to us are dataset of movies and dataset of actors, we definitely have to stick to them and utilize them at most.

Let us define the actor’s popularity as follows: 
1. For each movie, it is the mean value of scores of the movies in which the current actor played in, until this current movie’s production time. 
2. We take into consideration only the previous 5 movies, due to the fact that some actors were in the film industry long before their new appearances on the big screen.

Who do you think are the most popular actors? 
Well, after taking the mean popularity over all their movies, it unsurprisingly turned out that among the top-10 most popular actors, there are: **Tom Hanks, Harrison Ford, Brad Pitt, Robert De Niro and Johnny Depp**.

The main question remains unchanged: do actors' popularity scores affect the movie score so drastically?

Let’s look together at the plot of actors’ popularities as well as mean movie scores over the respective years. 95% confidence intervals are also shown for convenience. 

### actors' popularity plot

It is obvious that the movie score indeed depends on the actor's previous roles and whether he played in well-scored movies. However, it is also clear that this score can significantly vary, especially for the years when the particular actor played in numerous movies. 

This may, with high probability, be due to other features covered above. Furthermore, since the metric itself is defined as a derivative of the movie score, it is natural for it to follow the score trend.

Thanks to visual similarities it is tempting to try to predict the actual movie score based solely on actors’ popularity and see how these predictions work.

### Dummy ML model plot 

Unsurprisingly, it didn’t turn out well. In fact, popularity of an actor is defined only using his previous movies (an actor who played in 1 movie is less popular than an actor who played in 3, even if these 3 had somewhat lower movie scores). The only good predictions are for the last few years. This is mainly due to the accumulated nature of the defined metric: the more high-scoring movies there are among the 3 last ones, the higher the actor’s popularity. Quite interestingly, the predictions are relatively closer to the actual movie score around the 1950’s, after World War II. The war led to a peak in the filming industry, which therefore caused a rise in the demand for actors to play in those war related movies. In that period, some movies had huge casts (over 40 actors), but of course not all of them were popular. This makes it much easier to estimate the movie score with only actors’ popularity. 

What is also interesting is that this model shows that previously there were many unknown actors in most of the movies. For the recent years, on the contrary, either actors in casts are well-known and popular or the fraction of new actors is much smaller. It is also true that we have a lot of movies (1388) after 2010 and the fraction of actors with zero popularity is low for this period, so the model predicts more accurately.

# Famous Producers

Behind every good movie is a good producer, right? This leads us to this new analysis, revolving around Producers’ Fame. 

Defining the similar metric used for actors’ popularity, but now for movie producers shows almost the same results. In the top-10 producers of all time, there are: **Steven Spielberg, Woody Allen, Martin Scorsese, Alfred Hitchcock and Ridley Scott**.

### producers' popularity plot

Here again, it seems like the producers’ popularity hugely depends on the movie score of previous movies they produced, variation of the scores of those movies and on the length of the producers’ careers.


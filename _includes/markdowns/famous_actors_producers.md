## Famous Actors
Intuitively, the cast of a movie has a significant influence on its success. Indeed, if an A-list actor announces their new movie then many of their fans will rush to cinemas to watch the newest masterpiece. This is especially true for successful actor duos. For instance, if the funniest duo (in our opinion of course😂), The Rock and Kevin Hart, act in a movie, not only would we all go watch it, exploding the box office revenue, but also the movie would naturally be a success.

In light of this information, we want to come up with a metric for measuring an actor’s popularity. Ideally, we would like to use Google Trends however many movies in our dataset were made long before social media 😅. But fear not, as we have found a clever solution to solve this issue

Defining actor popularity as the mean value of scores from their 5 previous movies seems like a strong solution. Considering a limited window of the most recent films offers a snapshot of an actor's current influence in the industry.

Now to validate the strength of this system, we’d like to check that top names can be found. Who would you want to feature in the most popular actors?

Well, after taking the mean popularity over all their movies, it unsurprisingly turned out that among the top-10 most popular actors, there are: **Tom Hanks**, **Harrison Ford**, **Brad Pitt**, **Robert De Niro**, and **Johnny Depp**. These seasoned actors have consistently delivered performances that resonate with audiences, earning them enduring popularity throughout their careers.

The main question remains unchanged: do actors' popularity scores affect the movie score?

Let’s look together at the plot of actors’ popularity as well as mean movie scores over the respective years. 95% confidence intervals are also shown for convenience. 

## TODO TOM HANKS OVER THE YEARS PLOT

Looking at these plots, we can see that the actors start at 0, but quickly reach top scores due to the nature of our metric. Furthermore, since the metric itself is defined as a derivative of the movie score, it is natural for it to follow the score trend.

The visual similarities in the two curves tempt us to try and predict movie score based solely on actors’ popularity. The big question becomes: Can we define an accurate movie score predictor based solely on the actors in its cast?
# Predictor
The predictor that we propose takes the score of the top actors and returns their average. motivated to find the best model, we can tweak the number of actors considered in our mean. 
## TODO ML DUMMY PERFORMANCE PLOT
The graph above represents the mean movie score over the years and the mean predictions for the same years, both with a 95% confidence interval. Note that you can change views to see how the model performs when you consider different numbers of actors. 

The results when considering a single actor are quite impressive. In other words, predicting the score of a movie as the top actor score in its cast is a terrific predictor. It is worth noting that before the 1940s our prediction was terrible, which is probably because at the beginning of our data, actors are unseen and thus have very low scores.

These findings underscore the significant influence that actors can wield in shaping a movie's success. Shedding light on why some of them are paid so well!

## Famous Producers

Behind every good movie is a good producer, right? This leads us to this new analysis, revolving around Producers’ Fame. 

Defining the similar metric used for actors’ popularity, but now for movie producers shows almost the same results. Among the top 10 producers of all time, there are: **Steven Spielberg**, **Woody Allen**, **Martin Scorsese**, **Alfred Hitchcock**, and **Ridley Scott**.

## TODO CLINT EASTWOOD POPULARITY OVER THE YEARS

Here again, it seems like the producers’ popularity hugely depends on the movie scores of previous movies they produced, the variation of the scores of those movies, and on the length of the producers’ careers.

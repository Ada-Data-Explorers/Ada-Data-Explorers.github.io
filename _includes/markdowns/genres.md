# Genres

Our quest for the perfect movie formula leads us here, to the vast and diverse world of genres. Genres are the core of cinematic diversity, shaping a film's storyline, tone, and emotional connection: elements that immerse you in a new world. 
So stay with us while we explore the impact of the 16 most popular genres on the movie score. There is so much more to discover together! 

To get a global view of our data, let’s start by looking at the 4x4 subplots representing the distribution of the movie score per genre.

![4x4 Plots](/assets/images/distribution_of_movie_score_per_genre.png)

From these 4x4 subplots, some trends begin to arise. It seems like our movies are very imbalanced in their genres. Interestingly, it also seems like the less frequent genres are centered around higher movie scores than the more frequent ones. That’s intriguing, isn’t it? We are curious to know how that is possible, so we are going to look into the exact frequency of movies per genre through a pie chart, and then visualize movie score statistics per genre through box plots. 

{% include folder/proportion_of_movies_per_genre.html %}

This pie chart unveils intriguing patterns, showcasing the prevalence of Drama and Comedy genres and the relatively rare occurrence of Animation and Sport genres. The dominance of drama and comedy films can be attributed to their widespread appeal and capacity to connect with varied audiences. Drama, often reflecting societal values and addressing social issues, resonates on a universal scale, while comedy offers entertainment and a form of escapism through humor and laughter beyond cultural barriers. 

Confronted with these findings, a question emerges: Could the prolific release of movies in certain genres be attributed to a strategic understanding by directors of their greater success? So now that we have a better knowledge of movie-genre proportions, let’s see if the abundance of a genre correlates with the movie scores it achieves. With that in mind, we will use boxplots to visualize the distributions of movie scores for each genre. 

![Box Plots All](/assets/images/box_plot_of_movie_score_per_genre.png)

{% include folder/general_stats_df.html %}

As we can see in the boxplots and table above, the War film, Animation, and Period Piece genres have the three highest median scores, while Drama and Comedy have amongst the worst medians. Moreover, The Godfather, a movie that belongs to the Crime, Drama, Family, and Period Piece genres, has the maximum score, and it’s a Comedy movie, Underground Comedy Movie, that has the worst score. 
Could this be due to the fact that the number of movies per genre is not the same? Are our results biased, invalid? 

To answer this concern, we repeat the analysis twice: 
* Once considering only the movies in the top 20 percentile for each genre
* Once considering only 518 randomly picked movies for each genre. We thought you might ask why 518? Well, the least frequent genre contains 518 movies. This way, we compare the genres with the same number of movies, so the same sample size. 

1. Considering only the movies in the top 20 percentile for each genre

![box_plot_of_movie_score_per_genre_top_20.png](/assets/images/box_plot_of_movie_score_per_genre_top_20.png)

{% include folder/general_stats_df20.html %}

2. Considering only 518 randomly picked movies for each genre

![box_plot_of_movie_score_per_genre_random_518.jpg](/assets/images/box_plot_of_movie_score_per_genre_random_518.png)

{% include folder/general_stats_df518.html %}

Applying both methods, Animation, Fantasy and War film genres still have the highest means and median, and Drama and Comedy still have among the worst means and medians.

This trend that less popular genres are scoring higher in terms of average and median scores could be explained by genre expectations and audience saturation in frequent genres and the potential novelty and niche appeal within the least frequent ones, which attracts a more targeted audience. Moreover, movies that have a combination of multiple genres, like The Godfather, have appeared to be really successful. They blend together the best of these worlds, appealing to many more tastes and preferences and satisfying a broader audience. Ultimately, to make the perfect movie, producers should focus on innovation, surpassing genre expectations, and targeting a specific and dedicated audience, no matter the movie genre. At the end of the day, we, spectators, wouldn’t be impressed by 10 different movies that have almost the same story, right?  



# Movie Sequels

Let's now venture into the realm of sequels. A movie's typical duration, spanning from one and a half to three hours, often feels too short a time to dive into a world and create profound relationships with its characters. We’d like you to think about the character that you love the most. Was that relationship built across multiple films or just a single one? Movie series offer a solution, providing a canvas to witness the evolution of characters over time. Many of the most iconic blockbusters fall into that category: Star Wars, Avatar, and the Marvel Cinematic Universe movies. This begs the question: are sequels, in general, a crucial element in the formula for a successful movie?

Firstly, we compare sequels with movies that are not sequels to see if the score distributions are significantly different in the two groups. 

### Box Plot Sequels

The above box plots seem to show that sequels boast significantly better movie scores than their non-sequel counterparts. However, it is important to note that there are much fewer sequels, prompting a statistical investigation. Consequently, we perform a t-test to back up our findings with some statistics. With an extremely small p-value of  e-38, much smaller than a typical significance level of 0.05, and a t-statistic of 12.8826, we find that there is a significant difference between the two populations’ scores.

Adding another layer to our analysis, we are interested in comparing how well prequels perform compared to sequels within a movie series. To analyze this we subtract the prequel’s score from all the movies that came after it in a movie series. This yields very interesting results as we can see in the following plot that the overwhelming majority of sequels fall short of their predecessors. This paradoxical observation might be attributed to the perception that movie series lack creativity, thus influencing critics to assign lower ratings.

### Histogram

Our findings are captivating because they paint a nuanced relationship between sequels and movie scores. We saw that sequels are more likely to have higher scores than their counterparts. Yet, we found that sequels generally underperform compared to their prequels. These insights seem contradictory right? A possible explanation would be that a movie is more likely to have a sequel if the previous one was received well. Therefore, merely creating a sequel isn't a guaranteed formula for success; however, if the prequel garnered a positive score, it might offer a relatively secure path.


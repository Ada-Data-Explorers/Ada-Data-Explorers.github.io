## Small Features

### Country and Language

Does language influence the score? Does the country of release influence the score?

## Graph: Total Score throughout the years per country

### Movie Run Time 

We set out to understand the relationship between the length of a movie and its score. What do you think we’re going to find? Filming a movie is expensive so each additional minute comes at a significant cost! Intuitively it would seem that longer movies should have higher budgets, and that may influence the quality of the movie. So we expect to find a small correlation between the length of the movie and its score. Now let's see if we are right!

But, before we dive into the intricacies of our analysis, a crucial step awaits: removing the outliers. A few of our data samples have runtimes of over 500 minutes and have the potential to skew our analysis! Chances are, you’ve likely never come across a movie with such a long runtime, so let's remove these extreme cases. Now that we have a cleaner dataset, we proceed to put our intuition to the test. 

Testing for Pearson correlation between movie runtime and score results in a statistic at 0.3124 and a zero p-value. This test implies that we can assert a medium correlation between the two with very high confidence. Great, our intuition was right! Now to make the journey even more captivating, and this analysis further convincing, here’s a visualization that provides the evidence supporting our claims.

{% include folder/score_vs_runtime.html %}

### Movie Budget

While there undoubtedly exist cinematic gems crafted on modest budgets, it's essential to acknowledge that financial constraints often shape the scope and scale of a project. What would you do if you became a director? Picture yourself in their chair. Perhaps you’d dream of enlisting A-list actors, assembling an exceptionally talented team, and utilizing innovative equipment. However, the reality is that these come at a high cost. Unless you’ve had past successes, finding the funds for your film will be very challenging. In this context, we sense a relation between a director’s status and the budgets at their disposal. This premise lays the foundation for our hypothesis that budget and score are correlated, which we will now prove!

{% include folder/score_vs_budget.html %}

Looking at the movies with the highest budgets we detect something strange: some of them are in the tens of billions! A quick internet search reveals the culprit: our data contains budgets in various currencies. To maintain the integrity of our analysis, we choose to discard movies with budgets surpassing the record holder: Pirates of the Caribbean: On Stranger Tides (2011) boasting a budget around around 300 million dollars. The Pearson correlation that follows yields a statistic equal to 0.3122 and an infinitesimal p-value around 1.3677e-206 which indicates a substantial correlation with very high confidence. 

Note that, similar to box office revenue, budgets must undergo adjustment for inflation to ensure comparability across different years. In addition, it's imperative to acknowledge that while our filtering successfully removed extreme budgets, there may still be inaccuracies in our dataset. As previously emphasized, the quality of our analysis is intricately tied to the integrity of our data. Hence, in this scenario, it's important to approach our results with a degree of caution, recognizing the potential limitations in the dataset.

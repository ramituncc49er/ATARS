# Serendipity-Based Re-ranking of Items

<p align="center">
  <img src="pipeline3.png" height="100">
</p>

User-dependant Serendipity of an item (restaurant, hotel or hair salon) is defined as the sum of the utility values of all the atypical aspects found across all the reviews of that item, where each utility value is divided by the total similarity of that aspect with all atypical aspects, including itself.

<p align="center">
  <img src="serendipity_function.png" height="70">
</p>

Assuming a normalized aspect to aspect similarity measure $sim(a, \hat{a}) \in [0,1]$, with a value of 1 if and only if $\hat{a} = a$, this means that:
- When all aspects are identical, each utility value in the sum above is divided by the total number of atypical aspects for that item, effectively producing a mean utility.
- When each aspect has zero similarity with other aspects, each utility value in the sum above is divided by 1, effectively producing a sum of utilities.

Also, a user-independant measure of surprise is for an item (restaurant, hotel or hair salon) is defined by setting the utility value to 1 for all atypical aspects of that item.

<p align="center">
  <img src="surprise_function.png" height="70">
</p>

By setting the utility to a constant, the resulting surprise measure reflects only the aggregate surprise caused by all of the item's atypical aspects, and ignores their potential relevance to the user.

Code for calculating the serendipity and surprise scores of items can be found at `./scoring_items_for_serendipity.ipynb`.

We find the Kendall $\tau$ correlations between the system generated and the ground truth serendipity-based rankings, for each domain. Additionally, we also show the correlation between the original star-based ranking and the ground truth serendipity-based ranking. Analogous results are measured for when star-based and serendipity-based or surprise-based scores are combined to produce the final ranking.

Code for measuring Kendall $\tau$ correlations can be found at `./kendall_tau_correlation.ipynb`.

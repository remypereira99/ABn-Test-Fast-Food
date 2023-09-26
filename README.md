**Introduction**
In this notebook I use Anastasiia Chebotina's 'Fast Food Marketing Campaign A\B Test' dataset from Kaggle to analyse the results of a fictional A/B/n test. The dataset lays out the scenario and task below:

**Scenario**
A fast-food chain plans to add a new burger to its menu. However, they are still undecided between three possible marketing campaigns for promoting the new burger.
In order to determine which promotion has the greatest effect on sales, the new burger is introduced at locations in several randomly selected markets. A different promotion is used at each location, and the weekly sales of the new burger are recorded for the first four weeks.

**Task**
Evaluate A/B testing results and decide which marketing strategy works the best.

**Structure**
The structure of this notebook is as follows:
1. Define hypothesis statement
2. Collect data
3. Omnibus test
4. Post-hoc test
5. Conclusions
6. References
   
In Section 1 I define the hypothesis statement for the A/B/n test: 'we believe that at least one of the three marketing promotions will result in significantly higher sales of the burger in the first four weeks across randomly selected stores'. I determine the most appropriate test for this hypothesis is an omnibus test followed by a pairwise comparison test.
In Section 2, I take a look at the data collected for the experiment. In a real A/B/n test, I would collect the primary data myself. In this case, the data is already provided in the Kaggle dataset, so I use this section to do a brief EDA (Exploratory Data Analysis) to get a feel for the data, and run any necessary cleaning.
In Section 3 I run an omnibus test on the three samples to determine if there is any significant difference ebtween them. I begin by testing the assumptions for ANOVA, and find that the data fails to satisfy the normality condition. I therefore run the non-parametric alternative - Kruskal-Wallis test. This test determines that the difference between the medians of each sample are indeed significant.
In Section 4 I run post-hoc tests to identify which promotion(s) have a significantly higher average sales compared to the others. The result is that stores using promotion A and C have significantly higher sales than promotion B.
In Section 5 I discuss the implications of this result for the initial hypothesis statement.

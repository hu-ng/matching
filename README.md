# Logistic Regression and Matching

For an assignment in my Causal Inference course, the bulk of the work is focus on using __logistic regression__, __propensity-score matching__, and __genetic matching__ (popular methods for choosing comparison units in observational studies) and answer the following causal question: "What is the effect of UN intervention on peacebuilding efforts 2 years and 5 years after the end of war?". Data was from [Doyle and Sambanis (2000)](https://www.jstor.org/stable/2586208?seq=1#page_scan_tab_contents)

## Logistic regression:

An additive model was used to predict the probability of successful peacebuilding (variable encoded as "1" for Success and "0" for Failure) for observed wars in the dataset. Because there were drastic differences in characteristics between the control units - wars that did not receive UN intervention, and the treatment units - those the received the intervention, the comparison between the two groups were not "apples to apples", so the treatment effect was not reliable.

## Propensity-score matching:

Matching in general uses the characteristics of the treated and control units to pick treatment-control pairs that are most "alike", so as to produce treatment and control groups that are most similar, thus improving the reliability of our estimates. Propensity-score matching is a type of matching that uses the probability of being assigned to treatment to match. A propensity-score is considered to "condense" chosen characteristics of a unit into a single number, so it might not be very effective in deciding the level of match between two units. The results in this case reflects this criticism: the similarity between the two groups is not high enough for the estimates to be believable.

## Genetic-matching:

Considered to be the most "advanced" of the matching family, genetic matching uses a genetic algorithm to decide the "weights" for variables being used to match on, with the assumption that variables do not have the same importance. Using genetic matching, the similarity between treatment and control groups were much higher, but even with a good match, the treatment effect was statistically insignificant.



# Good Film // Bad Film

By: Emma Bernstein and Robert Boscacci

Constructs a classifier to predict whether or not a film will be received well — based on the plot synopsis, the social media popularity of its leading actors, its genre, and some other pre-release indicators.

___
## Process


We passed 5k+ movies from a Kaggle dataset into the OMdB API to get even more metadata. Here's a tiny peek at what we started with:

![](https://github.com/emmabernstein1/Good-Movie-Bad-Movie/blob/master/Images/data.png)

We checked for redundant features and inspected correlation coefficients on a baseline logistic regression model:

![](https://github.com/emmabernstein1/Good-Movie-Bad-Movie/blob/master/Images/correl.png)

![](https://github.com/emmabernstein1/Good-Movie-Bad-Movie/blob/master/Images/coefs.png)


We even topic-modeled the plot synopses in order to extract latent unstructured features:

![](https://github.com/emmabernstein1/Good-Movie-Bad-Movie/blob/master/Images/topics.png)

Our ultimate XGBoost classifier significantly outperformed a scrappy naive bayes classifier, and that same naive bayes classifier thankfully outperformed a baseline/dummy classifier.

![](https://github.com/emmabernstein1/Good-Movie-Bad-Movie/blob/master/Images/ROC.png)

This shows what factors play important roles in critically acclaimed movies.
Moving forward, we could look into what factors play important roles in a movie's commercial success and compare the results.

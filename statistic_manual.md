Statistic Manual
================
1 January 2023

# Hands on: Statistical Introduction to a low flow analysis

## How to follow this Guide

To be able to take as much as possible from this guide to be able to
analyze

## Section 1: The goal of the Analysis

The goal of this analysis is to detect whether one can observe a trend
of observed discharge data. Ahead of the analysis it is important to
discuss

In this Analysis a linear model was choosen to express a trend
\#expected a linear corr between time and discharge \#Source

## Section 2: Descriptive Statistics: The Variety of the Dataset

Although there is not one model that fits best to all datasets, we
decided to stick to the linear model to be able to compare the outputs
with each other. Of course we are very likely to loose information by
trying to summarize the entire dataset in straigh lines of different
slopes. For example: It could be possible that due to an increasing
number of extreme heat events since 2000 there might have also more
water scarcity events since 2000. But if we only adjust a straight line
from 1860 to 2000 we might loose information. Other models? This is an
important and right point that leads us directly to a whole debate. All
around the sentence:

To put it in George E. P. Box words: “All models are wrong, but some are
useful”

Overfitting debate

## Section 3: Prediction or statistical Inference?

The overall assumption that there is any kind of relation between the
discharge Value (Y) and the Time (X) we can write in a general form:

Y= f(X)+ε (3.1)

Independently of the example to analyze discharge data, f(X) is not
known but fixed and ε is an error term, independetn of X and has zero as
a mean. From f we learn what x can tell us about y. At this point it
should be mentioned that f could be constructed of more than one input
variable. In many cases estimating f is very important, like:

1.  For Prediction

One can easily think of a situation where the input (x) is available but
one can’t make any assumptions concerning y. Therefor we need to make a
prediction $\hat{y}$ of y finding $\hat{f}$ that provides the most
accuracy for y. In this case one can treat $\hat{f}$ like a **black
box**. Therefor $\hat{f}$ will not be the perfect guess for our function
f(x). How good our estimations of $\hat{y}$ for y are depends on the
**reducible** and the **irreducible** error. The closer $\hat{f}$ is to
f the more we can reduce this **reducible** error. Nevertheless y is a
function of ε (1.1) therefore it is not possible to only predict it with
x (or f(x)). This gap is described as the irreducible error. For a
preduction one can set ε=0 as it may contain unmeasured quantities that
might hold additional information for the prediction, but as they are
not measured there is no way to conlude them into our prediction.
Therefore the prediction term is:

$\hat{y}=\hat{f}(x)$ (3.2)

2.  For Inference

Oftentimes we want to assess the relation between y and x
($x_1, x_2,..., x_n$). In this case it is our goal to find out what f is
although we dont want to make predictions for y.

Of course there is modeling consisting of prediction and inference at
the same time as well. Depending on our goal or problem we can think of
different ways to specify f. A linear model allows assumptions of
statistical inference on first sight but might not always be appropriate
for predictions.

## Section 4: The Linear model

From our assumptions we were able to construct f(x): a linear
function.The term “linear” refers to the linear model parameters
(weights, and coefficients).

A linear model is constructed from a linear function: $y = w_0 + w_1* x$
(4.1)

A better notation would be: $\hat{y}(x) = w_0 + w_1* x$ (4.2)

Because as mentioned above (Section 3) $\hat{a}(x)$ clarifies that we
speak about a prediction of Y (dependent on x). It is important to keep
in mind that the predictors/ parameters are unknown and need to
estimated in a way that the resulting model fits the data as good as
possible. **As good as possible** can also be expresses numerically by
determining the error:

$e_i=y_i-\hat{y}_i$. (4.3)

e represents the ith residual (distance between the ith response
variable and predicted variable). To avoid the problem that negativ
residuals cancel out the positive residuals the **RSS: residual sum of
sqaures is defined**:

$RSS=e_1^2+e_2^2+...e_n^2$ (4.4)

By minimizing the **RSS** we obtain the best $w_0$ and $w_1$, this is
described be the **Linear Least Squares Approach**:

$w_1=\frac{\sum_{i=1}^{n} (x_i-\overline{x})(y_i-\overline{y}}{\sum_{i=1}^{n} (x_i-\overline{x})^2}$
(5)

$w_0=\overline{y}-w_1\overline{x}$ (4.5)

\[LSI\].

To build a model from the linear function (4.1) we construct a
probability distribution around the linear model by adding noise:

$p(y|x,w,ε)=w_0+w_1*x+ε$

In this case:

1.  $w_0, w_1$ are our cofficents/ parameters: $w_0$ is the intercept
    and $w_1$ the slope of our model
2.  $x$ is our predictor
3.  $ε$ is our noise

We distinguish between Univariate models (with just a single predictor)
and Multivariate models with more than one predictor \[korup, lecture
Linear models\]. As soon as we have multiple predictors it is more
complicated to interpreatate the coefficients as they are dependent on
the other variables in the model \[Data Analysis Andrew Gelman \]

The noise

# Sources:

- \[Data Analysis Andrew Gelman \]
- Korup
- LSI : Learning stat\_ introduction
- 

---
layout: post
title:  "ml scratch - logs"
subtitle: "long due boyzzz"
date:   2021-06-22 12:56:45
categories: [ai]
---

## 2021-06-22 12:56:45

It has been quite a long hiatus from doing something worthwhile.

A long time ago, along with the songs of tri mandili, the youtube algorithm decided to recommend me this gem of a [video](https://www.youtube.com/watch?v=o64FV-ez6Gw) by Joel Grus. Naturally,  I made a repo and started to write an ml library from scratch. Annnnnnd I had forgotten about it a week later.

So, this is a try to bring life to the repo and complete the library to a usable level. I will be logging all raw thoughts and reasoning that come into my mind here. Hopefully, it's readable.

Let's set some goals and context for the library:
-	Writing better python, cause I don't think I write good code
-	A little insight into some ml algorithms, a revision is some sense
-	And the most important, having one complete project I can brag about

So with that set aside, what should be the algorithms included:
-	linear regression (duh)
-	classification(logistic, svm, desition tree, bagging, and boosting)
-	NNs (well, it started with this, so I ough to complete this)

Hmmm, it seems doable. So, on with the code.

## 021-06-22 2:31:00

Linear regression seems to be the most natural one to start with. So we have some features with which we try to predict an output. The features are independent variables, and the output is the dependent variable (as we suppose it's dependent on the features).  Linear regression assumes that the dependent variable has a linear relationship with the independent variables. How does the realtionsship look like:

![](http://www.sciweavers.org/tex2img.php?eq=y%20%3D%20%20m_%7B1%7D%20%20x_%7B1%7D%20%2B%20%20m_%7B2%7D%20%20x_%7B2%7D%20%2B%20...%20%2B%20m_%7Bn%7D%20%20x_%7Bn%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)


## 2021-06-28 1:45:00

After a short CPR we will be continuing this blog.

Next we try to optimise with gradient descent to find the best value of the weights and the intercept. We start with random values and run through the gradient descent algorithm till we reach the optimal values. Ideally we stop after we fine a small enough error. We'll do that here.

What will we use to evaluate this? Mean squared error. We take all the actual y and the predicted y and find the square of the difference between them and take the average over all the datapoints(we will take some data points for each batch). Our goal is to minimize this. 

Algorithm:
-   Random initialization of the weights (w0,w1,w2....wn; here w0 is the intercept)
-   Partial differentialte the linear equation wrt. each of the variables. So for n variables we will get n+1 equations(w0 also included).
-    This would give the change of the error term with respect to the weights.

![](http://www.sciweavers.org/tex2img.php?eq=m_%7B1%7D%20%20%3D%20m_%7B1%7D%20-%20%5Calpha%20%20%5Cfrac%7B%5Cpartial%20J%28m_%7B0%7D%2Cm_%7B1%7D...m_%7Bn%7D%29%7D%7B%5Cpartial%20m_%7B1%7D%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

- We keep updating the value until convergence.

You can find the code in [here](https://github.com/sreyaschaithanya/ml_scratch).

### Code:

As one of the goals for us is to write good code, I shall be structuring the repo in such a way it looks like a library with reusable components for the algorithms to come. I will be taking inspirations form scikitlearn and other such libs.

For now the structure is having a different directory for each class of algorithms. We'll have one for linear now and write a base class. We can inherit this class and overwrite the functions with whatever fits.


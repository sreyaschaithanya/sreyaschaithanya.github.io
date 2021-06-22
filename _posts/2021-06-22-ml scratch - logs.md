---
layout: post
title:  "ml scratch - logs"
subtitle: "long due boyzzz"
date:   2021-06-22 12:56:45
categories: [ai]
---

2021-06-22 12:56:45

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

2021-06-22 2:31:00

Linear regression seems to be the most natural one to start with. So we have some features with which we try to predict an output. The features are independent variables, and the output is the dependent variable (as we suppose it's dependent on the features).  Linear regression assumes that the dependent variable has a linear relationship with the independent variables. How does the realtionsship look like:
!equation(http://www.sciweavers.org/tex2img.php?eq=y%20%3D%20%20m_%7B1%7D%20%20x_%7B1%7D%20%2B%20%20m_%7B2%7D%20%20x_%7B2%7D%20%2B%20...%20%2B%20m_%7Bn%7D%20%20x_%7Bn%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)


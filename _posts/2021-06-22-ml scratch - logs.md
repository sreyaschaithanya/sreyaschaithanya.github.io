---
layout: post
title:  "ml scratch - logs"
subtitle: "long due boyzzz"
date:   2021-01-15 23:56:45
categories: [ai]
---

It has been quite a long hiatus from doing something worthwhile.

A long time ago, along with the songs of tri mandili, the youtube algorithm decided to recommend me this gem of a video (https://www.youtube.com/watch?v=o64FV-ez6Gw) by Joel Grus. Naturally,  I made a repo and started to write an ml library from scratch. Annnnnnd I had forgotten about it a week later.

So, this is a try to bring life to the repo and complete the library to a usable level. I will be logging all raw thoughts and reasoning that come into my mind here. Hopefully, it's readable.

Let's set some goals and context for the library.
-	Writing better python, cause I don't think I write good code
-	A little insight into some ml algorithms, a revision is some sense
-	And the most important, having one complete project I can brag about

So with that set aside, what should be the algorithms included in this lib:
-	linear regression (duh)
-	classification(logistic, svm, desition tree, bagging, and boosting)
-	NNs (well, it started with this, so I ough to complete this)

Hmmm, it seems doable. So, on with the code.
___

A blockquote:

> We are Hitchhikers in the road of open source knowledge.

## The rigged coin

So Bob invites Alice to a game of coin toss. He says that we use a coin of his choise to play the game as he does not trust Alice. But trust cuts both ways. So to make sure the coin is fair, Alice designs an experiment:
-   Toss the coin n times
-   Record the number of heads and tails
-   See if the number conforms to an ideal coin

So if we fix n as 1000, we toss the coin 1000 times and record the number of heads and tails in an array.

{% highlight python %}
n = 1000
tosses = [random(1,0) for i in n]
heads_n = sum(tosses)
tails_n = n - heads_n
{% endhighlight %}


A list:

- Praesent nisi elit, bibendum ut consectetur ac, aliquet in nunc
- Donec ante est, volutpat in mi et, pulvinar congue dolor.
- Quisque ultrices pulvinar sollicitudin.
- Duis elementum odio eu euismod suscipit.
- Integer enim lorem, interdum sit amet consectetur non, bibendum eget neque.

A numbered list:

1. Praesent nisi elit, bibendum ut consectetur ac, aliquet in nunc.
2. Donec ante est, volutpat in mi et, pulvinar congue dolor.
3. Quisque ultrices pulvinar sollicitudin.
4. Duis elementum odio eu euismod suscipit.
5. Integer enim lorem, interdum sit amet consectetur non, bibendum eget neque.

Definition list:

Curabitur cursus magna eu sem cursus
: ac ultrices urna pharetra.
: Duis scelerisque ipsum eu luctus elementum.

Pellentesque habitant morbi tristique senectus
: Curabitur malesuada lacus ac gravida porttitor
: Duis sodales feugiat lorem et mollis.

Want to suggest something? Please [Send me a request](https://github.com/kronik3r/daktilo/issues/new).
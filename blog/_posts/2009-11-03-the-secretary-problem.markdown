--- 
layout: post
title: The Secretary Problem
published: true
meta: 
  _edit_last: "5862988"
tags: []

type: post
status: publish
---

Suppose a secretary has to call $n$ candidates for a job interview. She can 
choose to call them in a random order. Assuming she does so, and the situation 
is take him or loose him(ie after having interviewed a person, she has to 
immediately tell him whether she will take him or not). An additional 
assumption is that all candidates will have distinct interview scores. So the 
question is "What is her best strategy?"(ie the one that maximizes the 
probability that she gets the candidate with the best score)

Tne strategy is to interview half the people, find the best score and accept 
the next guy with a higher score. So if the best guy is in the second half and 
second best guy is in the first half which happens with probability $1/4$, she 
will be able to get the best candidate. One could generalize the above and 
decide to find the best score among the first $ k$ candidates and choose the 
next guy who beats this score. With some asymptotic analysis, the probability 
of finding the best guy comes to $\alpha\ln(1/ \alpha)$ where $\alpha = k/n$.([see](http://en.wikipedia.org/wiki/Secretary_problem#Deriving_the_optimal_policy)). This is maximized when $\alpha = 1/e$ giving a success probability of $1/e$.
It can be proved that this is the best that can be achieved.

The probabilists way of stating this is a sequence of random variables $X_1 \cdots X_n$ of scores. Since all candidates have different scores, $X_1 \cdots X_n$ is a random permutation of the scores(as we assumed that she calls candidates in a random order, and lets also assume that the scores are independent of what time they are taken). To make things slightly more complicated, let $ Y_i$ be the indicator random variable for $X_i< \max(X_1\cdots X_{i-1})$.  After having seen $X_1 \cdots X_{i-1}$(these form $ i-1$ distinct numbers with $ i$ gaps between them),  $ X_i$ is equally likely to be in anyone of  the gaps. Therefore

$$ \Pr[Y_i = 1] = \Pr[X_i &lt; \max(X_1\cdots X_{i-1})]  = \frac{1}{i}$$


> **Claim :** $ Y_i$ is independent of $ Y_1 \cdots Y_{i-1}$

**Proof :** Following the logic which gave the probability above, whether $ X_i$ is the maximum of whats seen till now doesnt depend on the ordering of $ X_1 \cdots X_{i-1}$. We want to know what the best stratergy is. Suppose we have already seen $ X_1 \cdots X_n$, we have no option but to choose the $ n$th candidate.

If $ Y_n = 1$, with probability $1$ we have the best guy, else its $0$. For later purposes lets define $ V(n,1)=1,V(n,0)=0$ Now again Whats the best strategy to follow once we have seen $ X_1 \cdots X_{n-1}$.

If $ Y_n = 1$,
1. with probability $ n-1/n$ we have the best guy
2. if we skip this guy with probability $ \Pr[Y_n=1|Y_{n-1}=1]\times 1 + \Pr[Y_n=0|Y_{n-1}=1]\times 0$ it will be found in the next step if the best strategy is followed from next step.

So we can compute these 2  values and choose the option with higher probability.  Let $ V(n-1,1) = \max $ above 2 values
If $ Y_n = 0$,

1. with probability $ 0$ we have the best guy
2. if we skip this guy with probability $ \Pr[Y_n=1|Y_{n-1}=1]\times 1 + \Pr[Y_n=1|Y_{n-1}=1]\times 0$ it will be found in the next step if the best strategy is followed from next step.

So the best thing is to skip. Let $ V(n-1,1) = $ second value. And we can continue this inductively. Suppose $ V(i+1,b)$ be the probability of success if the best strategy is  followed from step $ i+1$ given $ Y_{i+1}=b$. $ V(i,b) = \max \{ i/n , \Pr[Y_{i+1}=1|Y_{i}=b]\times V(i+1,1) + \Pr[Y_n=0|Y_{n-1}=1]\times V(i+1,0) \}$

If $ b=1$ then $ V(i,1)= \max \{ i/n , \frac{1}{i+1}\times V(i+1,1) + \frac{i}{i+1}\times V(i+1,0) \} $ else $ V(i,0)=i/n$  (ie if current is not the best among the candidates so far seen, he is definitely not best among all and so  we skip, hoping that best guy is yet to come).

As $ i/n$ is increasing in $ i$, and it can be proved that $ \frac{1}{i+1}\times V(i+1,1) + \frac{i}{i+1}\times V(i+1,0)$ is decreasing(i think after some threshold) at some point they cross. So from this point onwards we will choose the first guy that has best score so far(ie max is obtained for option 1). But we had already proved that best among such strategies is obtained by setting the threshold point to $ 1/e$ to obtain a probability of getting best guy as $ 1/e$.[this is slightly rough write up, i hope to improve it later]




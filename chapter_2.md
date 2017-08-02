### 2.1:

0.75 (.5 from greedy and .5*.5 from randomly selecting the optimal)

### 2.2: 

e step definitely occurs at step 5 as action 3's expected reward was 0 at that point and action 3 was chosen. May have occured at step 1 depending on how the e greedy algorithm works when all actions are at an equal score of 0 and how algorithm decides on the first action. Definitely occured at step 2 as at that point action 2 was chosen even though action 2's Qa was equal to 0 and action 1's Qa was equal to 1. On step 3, it depends on the tie breaker rules as action 1 and action 2 had equal scores (and either could have been chosen randomly). On step 4, the greedy choice was action 2 which was chosen (though it could have been a random choice).

### 2.3:

Best cumulative probability of selecting the optimal actions belongs to .1 e greedy then .01 e greedy then greedy assuming the 1000 step time frame. Same for best cumulative reward. Past the 1000 time step, 0.01 e greedy can surpass .1 e greedy. greedy settles into a roughly 33% optimal rate and about 1 average reward.

Based on figure 2.1, for greedy choice it seems like half the time one of the negative expected rewards (5 of the 10 bandits have a mean less than 0) would be chosen as the greedy and thus force greedy to keep selecting randomly until one of the 5 positive ones was chosen and the positive one managed to maintain a positive Qa. The other half the time a positive bandit was chosen and assuming a positive Qa was maintaned, that bandit would be exploited greedily. Only 5 of the positive bandits can be stabilized on and the best one seems to be chosen roughly 1/3 of the time under these circumstances. For epsilon .1 this jumps to roughly 80% at 1000 time steps as bandits 3 and 5 are the two attractive options and enough sampling would gradually cause all the other bandits to show lower expected reward. Epsilon .01 gets to around 50% optimal rate at 1000 time step, as the explore rate is a tenth of the explore rate of .1 .

I'm not sure how to express this mathematically at each time step. After time step 1, 10% of the time. After that, there would be some confidence intervals but I'm uncertain how to get it. If the rewards were deterministic, quantative solution would be able to find. Greedy: 1/10 at t1.  5/10*1/9 at t2. 5/10*4/9*1/8 at t3, etc. e-greedy you use similar math except the e probabilities increase finding the optimal one by e * 1/k at every t (assuming the optimal one has not been chosen).

### 2.4:

alpha * Rn + (1-alpha)(sum(alpha_i * R_i))

sum from i = 1 to i = n - 1

### 2.5 and 2.8:
See jupyter notebook for this chapter: https://github.com/AurelianTactics/reinforcement_learning_an_introduction_2nd_edition_exercises/blob/master/chapter_2.ipynb

### 2.6: 
This happens when the optimal bandit is hit upon last, receives some good initial rewards, and the other bandits did not pull well. There are no more optimistic bandits to pull and the other bandits will not look as good as the optimal one for a brief period until the optimal bandit's rewards being to outweigh the initial wildly optimistic initial value.

### 2.7	
https://en.wikipedia.org/w/index.php?title=Logistic_regression&oldid=755697139#As_a_.22log-linear.22_model


# 3.1:	
Cleaning the kitchen. Reward at clean state. Differing states include dirty dishes, full dishwasher, cooking utensils/food left out. Reward at no food being put out. Reward at kitchen being still dirty but still somewhat functional/not stressful. Actions include minor cleanup, partial cleanup, full clean up, and cleaning actions that occur at low frequency (ie clean the oven every x months etc.)
	
Programming an AI in turn based video game. Reward for actions that increase AI's chance of winning and negative rewards that lesson it (or just rewards at the end of successful/failed game). States are the different spaces the game can take. Actions are the actions the AI can take.
	
City planning. Reward is a complicated function that takes into account tax base, opinion of town populace, and individual motivations of key actors in the city gov't. Actions are different regulations and enforcements town can take. States are the current environment of the town and its populace.

# 3.2:
No. Thinking of my limited understanding of behavioral economics (books on Kahnman and Tversky) and irrational actors in Game Theory, trying to functionally approximate rewards can be foolish or nonsensical in many situations. Also, I guess strong nihilism can override many assumptions and make all actions/states seem basically the same.

# 3.3:
I don't think there is a right way. I think it depends on the problem and what assumptions you are willing to make. The more uncertainty and doubt you add into your actions and sensors, the more difficult the problem becomes as you are potentially adding many probability distributions. I would draw the line at what is generally considered convention as that allows any results/analysis that is done to be talked about in a productive way. That is unless of course drawing the line at a different point leads to an interesting enough point of discussion or finding that the benefit of the results are readily apparent or that discussion can still occur. Pragmatically, the fundamental reason for preferring one location is the value of the results obtained I guess.

# 3.4:
Return would be 0 if the game is solved, -1 otherwise. Successful states are not rewarded, only the last unsuccessful state is punished (though depending on the learning formula, this negative reward could flow to other states).

# 3.5:
The problem may be too difficult for the robot to solve and thus the robot never sees the rewards. Another issue is that by not giving a small negative reward over time/over movements the robot may never realize that it should be seeking a reward. You have communicated to the agent that hanging around doing nothing and not finding the reward is not a negative activity.

# 3.6:
G4 = 2

G3 = 3 + .5 * 2 = 4

G2 = 6 + .5 * 3 + .25 * 4 = 8.5

G1 = 2 + .5 * 6 + .25 * 3 + .125 * 2 = 6

G0 is 2

|Rt+1|	gamma|	discounted reward|	
| ------------- |:-------------:| -----:|
|-1|	1|	-1|	
|2|	0.5	|1|	
|6|	0.25|	1.5|	
|3|	0.125|	0.375	|
|2|	0.0625|	0.125	|

# 3.7:
G1 = 7 * 1/(1-.9) = 70

G0 = 2 + .9 * 70 = 63

# 3.8:
No, have no information on prior states and no approximation of them. Only have the current state.
In the second case, yes as your current state has all information about prior states.

# 3.9:
Have to add a term that accounts for the probability of receiving the reward given that the stochastic action was taken, ie the probability that action leads to the state that produces that reward.

STOPPED HERE 

# 3.10:
s	a	s'	r	p(s',r|s,a)

high	search	high	rsearch	alpha

high	search	low	rsearch	1-alpha

high	wait	high	rwait	1

high	wait	low	rwait	0

high	recharge	high	0	0

high	recharge	low	0	0

low	search	deplete	-3	1-beta

low	search	low	rsearch	beta

low	wait	deplete	-3	0

low	wait	low	rwait	1

low	recharge	high	0	1

low	recharge	low	0	0

low 	recharge	deplete	-3	0

# 3.11:
change 3.14 from gamma * vpi(s') to gamma * qpi(s',a')

# 3.12:
0.75	
=0.25 * 2.3 + 0.25 * 0.4 + 0.25 * -0.4 + 0.25 * 0.7

# 3.13:
= Rt+1 + c + g * Rt+2 + g * c + g^2 * Rt+3 + g^2 * c...
= sum(gamma^k * (Rt+k+1) + gamma^k * c)
= c * 1/(1-gamma) + =0.25 * 2.3 + 0.25 * 0.4 + 0.25 * -0.4 + 0.25 * 0.7
vc = c/(1-gamma)
The intervals in between are the important parts, not the sign.

# 3.14:
Yes it would have an effect. Like if there was a small negative reward to punish taking too long to finish the maze or taking incorrect steps and a reward of 1 to finish the maze and then 10,000 was added to each reward the maze runner would be incentivised to not finish the maze (and instead collect large reward by being in the maze).

# 3.15:
vpi(s) = sum( Epi[q(a,s)] ) for all s

vpi(s) = pi(a1|s) * qpi(s,a1)+ pi(a2|s) * qpi(s,a2) + pi(a3|s) * qpi(s,a3)

# 3.16:

# 3.17:
0 at the hole
-1 on the green
-2 in larger countour enclosing the green
-3 in larger countour enclosing the -2 contour. The tee is enclosed in this contour

# 3.18:
0 at the hole
-1 on the green
-2 in contour enclosing the green but not the sand
-inf in the sand
-3 in contour enclosing the sand and the -2 contour
for -4 to -6, these contours enclose the smaller contours until the tee is included in the -6 contour

# 3.19:

# 3.20:
reward of 10 every 5 steps. Let g = gamma^5. 10 * 1/(1-g)=
24.4194281

# 3.21:
for gamma = 0, left is optimal as the +1 reward will be the only reward that is not fully discounted				
in general,				
left is	1 + 1 * (1/(1-gamma^2))			
right is	2 * gamma * (1/(1-gamma^2)			
				
left	right	gamma		
5.263157895	9.473684211	0.9		
1.333333333	1.333333333	0.5		
				
so right is optimal for 0.9 and both are optimal for 0.5				
				
# 3.22:
? given above (3.18)
v * s = max qpi * (s,a) for a in A(s)

# 3.23:
q * (s,a) = sum(p(s',r|s,a)[r + gamma * v * (s')]
sum over s',r

# 3.24:
pi * = q * (s,a) for all s,a
ie take the highest optimal-action value at each step

# 3.25:
wouldn't 3.19 work?

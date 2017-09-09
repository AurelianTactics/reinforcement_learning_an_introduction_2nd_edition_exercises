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
Rt+1	gamma	discounted reward	
-1	1	-1	
2	0.5	1	
6	0.25	1.5	
3	0.125	0.375	
2	0.0625	0.125	
		2	
G0 is 2

G4 = 2
G3 = 3 + .5 * 2 = 4
G2 = 6 + .5 * 3 + .25 * 4 = 8.5
G1 = 2 + .5 * 6 + .25 * 3 + .125 * 2 = 6

		

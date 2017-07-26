# 1.1	

Yes it would learn a different policy. Against an imperfect opponent, the algorithm would learn to exploit the imperfect behaviour. Against an opponent who learns, behaviour would shift over time as prior policies that lead to rewards would no longer be effective.											
												
# 1.2												
We can take advantage of the symmetries by reducing the state space. Ie treat symmetrical moves as belonging to the same state space and thus allow learning to proceed faster.	

However if the opponent does not take advantage of the symmetries, then in that case neither should we. There may be opportunities to exploit the opponent if he has a weakness in one state space but not in another (even if they are symmetrical). It is not true that symmetrically similar states should have the same value.											
												
# 1.3												
It depends on the game and how optimal the greedy player is. If the greedy player is playing optimally or near optimally, it will generally outperform, but if the greedy player never sufficiently explores then it will be outperformed by some opponents. Some scenarios:											
Greed player vs. non greedy: greedy player generally wins as the non greedy player continues to explore and never exploits the optimal strategy									
Greedy player vs. gradually greedy player: greedy player outperforms at the beginning but the gradually greedy player generally plays better as it gets more greedy and will outplay the greedy player later in the game (with maybe some exceptions when the gradually greedy player does some exploration)									
												
# 1.4												
When you don't learn from the exploratory moves, it should converge to 1 as the optimal probability will be found. When you do, it'll be less than 1 as with some probability you'll explore and choose a non optimal move.	The better one to learn and the one that would result in more wins are the optimal probabilities											
												
# 1.5												
Maybe differentiate draws from losses and punish losses larger as losses are further from optimal behaviour than draws are.								

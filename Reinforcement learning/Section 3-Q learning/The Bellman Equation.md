# Introduction

s -> state
A -> action
R -> Reward
y -> discount

$$V(s)=max_a(R(s,a)+\gamma V(s'))$$

	Given a maze and a robot where the robot is given a reward +1 when he reaches the flag and the reward of -1 when he reaches the fire. We can assign the every block in the maze a value that can help the robot to find the location of reward irrespective of our starting location.

---

|     |      |     | +1  |
| --- | ---- | --- | --- |
|     | #### |     | -1  |
|     |      |     |     |
The agent try to navigate the above match randomly but when we the agent reaches the reward that triggers a reaction and agent try to find how he reached the location and starts assigning value to each blocks (*#### represent block that is inaccessible)

| V=0.81 | V=0.9  | V=1    | R=+1   |
| ------ | ------ | ------ | ------ |
| V=0.73 | ####   | V=0.9  | R=-1   |
| V=0.66 | V=0.73 | v=0.81 | V=0.73 |
*Taking value of y(gamma)=0.9*

# Markov Decision Process (MDP)
A stochastic process would be called as the Markov Process, If the probability of the future event only depends on the present state and is not affected by how we reach the present state.

Now, MDP is a mathematical framework for modelling decision making for a Markov Process.
[[Markov's Decision Process.excalidraw]]

We can extend our Bellman equation to include the MDP as follows:
$$V(s)= max_a(R(s,a) + \gamma *\sum_{s'}P_a(s,s')V(s'))$$

$P_a(s,s')$ -> it is the probability for reaching state s' from state s by doing an action a.
## Quality factor (Q value)
A quality factor basically quantifies the quality of taking an action when at state s. It is denoted by Q(s, a) and the value is determined as follows:-
$$Q(s, a) = R(s,a)+\gamma * \sum_{s'}P_a(s,s')* V(s')$$
Now from this formulae we can see that the value of state is just the max of all possible Q(s, a)
$$V(s) = argmax_a(Q(s,a))$$
$$Q(s, a) = R(s,a)+\gamma * \sum_{s'}P_a(s,s')* max_{a'}(Q(s'a'))$$

## Temporal Difference
An iterative approach to calculate the Q value because we are unaware of the Probability of the actions for different states.

To simplify first let us use the Q value as the :-
$$Q(s,a) = R(s,a) + \gamma * max_a(Q(s',a'))$$
Let's say our agent is on the $n^{th}$ run at state $s$ and makes an action $a$ then calculate the value for Q after and before the action has been taken

| Before   | After                            |
| -------- | -------------------------------- |
| $Q(s,a)$ | $R(s,a)+\gamma*max_{a'}Q(s',a')$ |

The temporal difference then is calculated as -
$$TD(a,s) = [R(s,a)+\gamma*max_{a'}Q(s',a')] - [Q(s,a)]$$

Now we can train our model by updating the $Q(s,a)$ using the temporal difference
$$Q_{t}(s,a)=Q_{t-1}(s,a) + \alpha TD_{t}(a,s)$$
### Additional Reading
- [Simple Reinforcement Learning with Tensorflow Part 0: Q-Learning with Tables and Neural Networks](https://medium.com/emergent-future/simple-reinforcement-learning-with-tensorflow-part-0-q-learning-with-tables-and-neural-networks-d195264329d0)
- [The Reinforcement Learning Problem](http://incompleteideas.net/book/Chap3PrePub.pdf)
- [THE THEORY OF DYNAMIC PROGRAMMING](https://www.ams.org/journals/bull/1954-60-06/S0002-9904-1954-09848-8/S0002-9904-1954-09848-8.pdf)
- [A survey of applications of Markov Decision Process by DJ white](https://www.it.uu.se/edu/course/homepage/aism/st11/MDPApplications3.pdf)
- [Markov Decision Processes: Concepts and Algorithms](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=968bab782e52faf0f7957ca0f38b9e9078454afe)
- [Learning to Predict by the Methods of Temporal Differences](https://link.springer.com/content/pdf/10.1007/BF00115009.pdf)

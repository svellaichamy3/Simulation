### Game setup:
The setup is a 2-member game and each member takes turns to play. Their actions are dictated by the roll of the die. Both of them start with the resource of a few coins and as the game progresses, the one who runs out of coins (when he does not have coins he is supposed to put in), the game ends and the person loses. 

### Method & Findings
We find that the average number of cycles taken for the game to end is 8.875 after multiple Monte-Carlo simulations. We plot a histogram to see the distribution of cycle length and conclude that it follows log normal distribution (Shapiro-Wilk Normality).

![Distribution](https://github.com/svellaichamy3/Simulation/blob/main/Probability%20Game/images/Distributions.PNG)

Plot to check normality

![LDistr](https://github.com/svellaichamy3/Simulation/blob/main/Probability%20Game/images/Distributions_log.PNG)

Plot for log normal distribution

Regarding the beginning advantage, we find no significant beginner’s advantage. We conduct several experiments by modifying the game rules and observe the cycle length and beginner advantage. We also find out how good the random number generator is by generating a histogram and two-dimensional plot to ensure if the generator is biased and scatterplot.  

Plots to check if the random number generator is biased:

We see each number occuring with approximately equal frequency - 
![Bias1](https://github.com/svellaichamy3/Simulation/blob/main/Probability%20Game/images/bar.PNG)


Pairs of consecutive rolls donot show repetitive behaviour - 
![Bias2](https://github.com/svellaichamy3/Simulation/blob/main/Probability%20Game/images/dot.PNG)


### Code:  
Game_Simulation_Code.ipynb - Game logic implementation with Monte-Carlo simulated runs and distribution tests
Game_Simulation_Experiments.ipynb - Code for experiments on different initialization strategies and its impact on simulated runs.



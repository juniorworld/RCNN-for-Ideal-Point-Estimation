# RCNN-for-Ideal-Point-Estimation
A RCNN model for estimating the ideological positions of social media users, based on what they say and with whom they interact. The dimensionality of ideological space is treated as an unknown parameter whose value is optimized through multiple runs of parameter-tuning.<br>

## Rationale
<b>Assumption 1.</b> People's ideological position is a function of what he/she says. Words reveal minds. Different words reveal different minds.<br>
<b>Assumption 2.</b> The tie strength between two people is a function of their ideological distance. People tend to interact with someone holding similar opinions as theirs. The more similar two people are, the more frequent they would repost each other.<br>
<b>Assumption 3.</b> The tie strenght between two people also depends on individuals' personal characteristics. For example, their social influence and the out-reaching propensity.<br>
## Operationalization
We integrate the three assumptions with an operationalization design as follows:<br>
Repost frequency W<sub>ij</sub> between user i and user j was negatively correlated with their ideological distance, whilst controlling for reposter’s outreach efforts In'<sub>j</sub> and originator’s influence Out'<sub>i</sub>.
- User influence can be evaluated by the number of times the user has been reposted by others.
- User's reacho out propensity can be evaluated by the number of time the user has reposted others.
- Above two features are highly right-skewed. Therefore, log-transformations are applied over the raw values to make them more compliant to normality.
<br>
<div style="text-align:center"><img src="https://juniorworld.github.io/RCNN-for-Ideal-Point-Estimation/Formula.png" width="500"></div>

## Flow chart of the Model
<div style="text-align:center"><img src="https://juniorworld.github.io/RCNN-for-Ideal-Point-Estimation/general_framework.png" width="600"></div>
Figure 1. General framework of the hybrid model.  Input data is a pair of 1000x200 embedding matrices, one from reposter and the other from originator.  Ideology estimator takes a user's embedding matrix as input and returns an estimated ideological point of the user, based on which the pairwise ideological distance is calculated.  Weighted indegree of reposter and weighted outdegree of originator are added as control variables.  Model’s weights are optimized to get better predictions for normalized weights.
<br><br>
<div style="text-align:center"><img src="https://juniorworld.github.io/RCNN-for-Ideal-Point-Estimation/RCNN-Ideology.png" width="600"></div>
Figure 2. Inner structure of the ideology estimator.  The estimator has three hidden layers, one gated recurrent units (GRU) layer, one one-dimensional (1D) convolutional layer and one simple recurrent layer.  The number of hidden units in GRU, the number and the height of filters in the 1D convolutional layer, the pool size, and the number of hidden units in the simple recurrent layer are five hyperparameters whose values were chosen according to results of hyperparameter tuning.

## Working Paper
[Zhu Y. & Fu K.W. (2020) Mapping Ideological Landscape of Social Media: A Neural Network Approach. Paper presented at 2020 ICA Annual Conference.](https://juniorworld.github.io/RCNN-for-Ideal-Point-Estimation/Yuner%20Zhu%20&%20KW%20FU_Mapping_Ideology_Lanscape.pdf)

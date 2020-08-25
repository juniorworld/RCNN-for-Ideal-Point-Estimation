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
<img src="/Formula.png" width="500"><br>

## Flow chart of the Model
<img src="/general_framework.png" width="600"><br>
<img src="/RCNN-Ideology.png" width="600"><br>

## Working Paper
[Zhu Y. & Fu K.W. (2020) Mapping Ideological Landscape of Social Media: A Neural Network Approach. Paper presented at 2020 ICA Annual Conference.](/Yuner%20Zhu%20&%20KW%20FU_Mapping_Ideology_Lanscape.pdf)

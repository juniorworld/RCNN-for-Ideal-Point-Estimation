# RCNN-for-Ideal-Point-Estimation
A RCNN model for estimating the ideological positions of social media users, based on what they say and with whom they interact. The dimensionality of ideological space is treated as an unknown parameter whose value is optimized through multiple runs of parameter-tuning.<br>

## Rationale
<b>Assumption 1.</b> We assume the normalized repost frequency W<sub>ij</sub> between user i and user j was negatively correlated with their ideological distance, whilst controlling for reposter’s outreach efforts In'<sub>j</sub> and originator’s influence Out'<sub>i</sub>. In other words, people would tend to repost someone holding similar opinions as theirs. The more similar two people are, the more frequent they would repost each other. However, the repost frequency will also depend on individual user's attribute, like social influence and the propensity to reach out to others.
- this
<b>Assumption 2.<b> People's ideological positions are 
<img src="/Formula.png" width="500" align="middle">
<img src="/general_framework.png" width="600" align="middle"><br>
<img src="/RCNN-Ideology.png" width="600" align="middle"><br>
Working paper:[Zhu Y. & Fu K.W. (2020) Mapping Ideological Landscape of Social Media: A Neural Network Approach. Paper presented at 2020 ICA Annual Conference.](/Yuner%20Zhu%20&%20KW%20FU_Mapping_Ideology_Lanscape.pdf)

# RCNN-for-Ideal-Point-Estimation
A RCNN model for estimating the ideological positions of social media users, based on what they say and with whom they interact. The dimensionality of ideological space is treated as an unknown parameter whose value is optimized through multiple runs of parameter-tuning.<br>

## Rationale
We assume the normalized repost frequency ¯(W_ij ) between user i and user j was negatively correlated with their ideological distance, whilst controlling for reposter’s outreach efforts 〖In'〗_j and originator’s influence 〖Out'〗_i. 
<img src="/Formula.png" width="600" align="middle">
<img src="/general_framework.png" width="600" align="middle"><br>
<img src="/RCNN-Ideology.png" width="600" align="middle"><br>
Working paper:[Zhu Y. & Fu K.W. (2020) Mapping Ideological Landscape of Social Media: A Neural Network Approach. Paper presented at 2020 ICA Annual Conference.](/Yuner%20Zhu%20&%20KW%20FU_Mapping_Ideology_Lanscape.pdf)

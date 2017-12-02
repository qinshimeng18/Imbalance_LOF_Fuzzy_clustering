# Imbalance_LOF_Fuzzy_clustering  
> put data in the codes file to correctly load data
# 1. ***Classification Task (60 marks)***  

## Training Enviroment  
Python 2.7, sklearn, numpy, pandas, collections, imblearn  
## Features engineer  
- Unbalance Data  
- Fulling NaN  
|Column | NaN Percentage|  
new_speed  0.9  
old_speed  0.9  
new_time  0.8  
old_time  0.8  
> Because these features have value only when certain actions occur, I fill 0 to this feature. 2.Generate features :
- Feature  
> watched_videos  
  session  
  load_video  
  pause_video  
  play_video  
  seek_video  
  speed_change_video  
  stop_video  
  time_scale_sum  
  avg_acts_sess  
- Meaning  
> Number of watched videos per person  
  Number of used sessions per person  
  Number of actions for every person  
  Number of actions for every person  
  Number of actions for every person  
  Number of actions for every person  
  Number of actions for every person  
  Number of actions for every person  
  Sum of skipped time during watched video for every user  
  Average number of actions per person take by using one session  
- Outliers detection  
I use LocalOutlierFactor packet to calculate the LOF , and then cut 0.08 outliers of all samples. Time_scale_sum max value is reduced by LOF.

- Resample  
Class to perform over-sampling using SMOTE and cleaning using ENN.
Combine over- and under-sampling using SMOTE and Edited Nearest Neighbors.
- Model  
Using RandomForest to classify the unbalanced data.
- Reference  
# 2. Fuzzy clustering with EM algorithm  
# 3. Outlier detection with LOF  

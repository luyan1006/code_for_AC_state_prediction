# code_for_AC_state_prediction
This is the code for the paper submitted to "Energy and Buildings", "Predicting household air conditioners’ on/off state considering occupants’ preference diversity: A study in Chongqing, China".

Due to some reasons, we can't open source our data used in this study, so we only open source the code and presented running results with Jupyter Notebook to show some example of the data form of data used in this study.

## The folder "1_Feature_generation"
This forlder contains the code for how to generate features used for PCA and clustering analysis in this study. 

## The folder "2_Clustering"
This forlder contains the code for:
1. Data set preparation for the clusering
2. how to perform PCA
3. how to perform clustering and visiualization of clusetering results

## The folder "3_Prediction"
This forlder contains the code for:
1. Data set preparation for the prediction data set
2. Grid search progress
3. how we trained model and tested model
4. present evalution results on testing dataset
5. visulize the results of prediction performance on testing data set

## The folder "4_final_model"
This forlder aims to give reference for researchers who want to use our proposed model for AC on/off state prediction when they need to set inputs in simulation model.
Contains of this forlder includes:
1. the output model (training by our data) for AC on/off prediction, which includes "v_wm.joblib","scaler_wm_pre.joblib","xgb_wm_pre.joblib","v_fs.joblib","scaler_fs_pre.joblib","xgb_fs_pre.joblib". Among them. "_wm" represents the "wall-mounted" AC, while "_fs" represents the "floor-standing" AC
2. "demo_wm.csv" and "demo_fs.csv" are the exampled input data that need to input to the model. "thermal_type" represents the occupants thermal preference pattern obatined in our study (0:TP1, 1:TP2, 2:TP3, 3:TP4). "schedule_type" represents the occupants schedule preference pattern obtained in our study (0:SP1, 1:SP2, 2:SP3). "daytype" represents whether it is a workday, "0" represents "holiday", "1" represents workday. "tout" represents hourly outdoor temperature. "hour" represents the hour of a day.
3. "AC_prediction_demo.ipynb" presents how to use the model to predict the AC on/off state with “demo.csv”
4. "demo_model_result.csv" is the prediction result with "demo.csv".


__If you have any problems about it, feel free to contact Lu Yan (yanlu2029@126.com)__

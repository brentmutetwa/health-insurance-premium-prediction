#Health Insurance Premium Prediction

This project predicts medical insurance costs using Random Forest regression.
The analysis is based on the Kaggle: US Health Insurance Dataset, which
includes demographic and health-related variables.
Exploratory data analysis revealed that smoking status is the dominant driver of insurance costs, with
additional contributions from age and BMI. These relationships are largely non-linear, which is what
motivated the use of a tree-based model.
The model was evaluated using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
Compared to a baseline model, the Random Forest achieved a substantial reduction in prediction error.
Further improvements were obtained through hyper-parameter tuning, resulting in additional decreases in
both MAE and RMSE.
The final model was presented using ipywidgets, enabling interactive prediction of insurance premiums based
on user inputs.


#Click the badge below to open the notebook in Google Colab:

https://colab.research.google.com/drive/1q_T3E1scqp47RYt_w-rE-yY3HODi5gNZ?usp=sharing

#Description

- Predicts insurance charges based on age, BMI, smoking status, etc.
- Uses Random Forest Regressor with hyperparameter tuning


Dataset from Kaggle: [US Health Insurance Dataset](https://www.kaggle.com/datasets/teertha/ushealthinsurancedataset)


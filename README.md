# Explainable-AI-Driven-Machine-Learning-Framework
In this study, dimensionality reduction techniques are employed to extract key features from disorganized data, and a machine learning model is developed to scientifically explain the complex relationships between composition and performance. Explainable AI (XAI) through SHapley Additive exPlanations (SHAP) is further applied to identify critical components influencing material performance and the underlying decision-making processes, based on this, extensive predictive data were obtained through high-throughput computing. Additionally, experimental validation combined with local interpretability of Local Interpretable Model-Agnostic Explanations (LIME) is used to assess the reliability of the model’s predictions. 

# Getting started
Development environment: python 3.11.5

To use the model, make sure you have the following environment, or you can set up a conda environment:

```
conda env create -n xaiML 
conda activate xaiML
pip install numpy pandas scikit-learn xgboost matplotlib seaborn shap lime
```
Here are the versions of each package:

| Package Name           | Version    |
|------------------------|------------|
| lime                   | 0.2.0.1    |
| matplotlib             | 3.6.2      |
| matplotlib-inline      | 0.1.6      |
| numpy                  | 1.23.5     |
| pandas                 | 1.5.2      |
| scikit-learn           | 1.2.0      |
| seaborn                | 0.12.1     |
| shap                   | 0.41.0     |
| xgboost                | 1.7.2      |

Please pay particular attention to the version of the SHAP, which may affect the summary plot if the version is inconsistent.

# PCA and PCC
Implementation of PCA and PCC methods are in the 'feature_selection.ipynb' of 'code' folder. 

You can see the results directly, or reload data for processing. You also can use these code to process your own data, please make sure the columns correct. The saved Excel file is in the 'data' folder.

For PCA, if you want to check the importance of multiple principal components, just change the 'n_components' parameter.

For PCC, visualization of heat maps is difficult to observe due to the large number of features. It is recommended to save the data to Excel and use other software to draw images or analyze.

# Model 
The implemented model is in the 'model.ipynb' of 'code' folder. Including models, SHAP, high-throughput computing and LIME.

Only the HV results are shown in the jupyter notebook. KIC is similar to HV, it only needs to be uncommented to run. To avoid conflicts, please comment the corresponding HV code when executing KIC's prediction.

The grid search process for tree-based mdoel and svr are slow and can take one or more hours. The optimal hyperparameters can be found in the cell. If you do not want to conduct grid search, you can directly use them.

Interpretable models (SHAP/LIME) are also implemented in the corresponding model implementation code and can be viewed directly.

The component data generated according to the range can be obtained directly and saved in the Excel file and it is already in 'data' folder. Because of the large amount of data, please make sure you have enough space to store and open files. 

All the saved Excel files are in the 'data' folder.

# Data Availability
Data will be made available on request. Please contact yj3023@ic.ac.uk



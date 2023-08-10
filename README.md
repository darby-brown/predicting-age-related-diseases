# **Identifying Age-Related Conditions**

## Project Overview

- Can we predict the presence of any of three age-related conditions?  
	- The current diagnosis approach is a long and intrusive process. 
	- We can shorten this process using predictive modeling.
	- Keep patient details private by collecting only key characteristics and encrypting their data.
## Data sources
- The data and question we want to answer are based on a Kaggle competition: https://www.kaggle.com/competitions/icr-identify-age-related-conditions/discussion/409715
- The data found on that website comes from InVitro Cell Research. It has three csv files: 
	- *train.csv*
	- *test.csv*
	- *greeks.csv*
- The test.csv file was not used in this project. Most models only used the train.csv dataset, which has the following characteristics: 

**train.csv**
- Full dataset shape is (617, 56)
- The features are all anonymized health characteristics
- The labels are a binary target: 
	- 1: the patient has one of the three age-related conditions
	- 0: the patient does not have any age-related conditions
    
**greeks.csv**
- Contains 3 experimental conditions and date when data was collected
    

## Python packages used

- **General Purpose:** `os`
- **Data manipulation:** `pandas, numpy`
- **Data visualization:** `matplotlib`
- **Machine Learning:** `scikit, tensorflow, scipy, random, yellowbrick, IPython, Xgboost`

## Code structure

```
.

├── 0_Kaggle

│   ├── Data

│   │   ├── greeks.csv

│   │   ├── test.csv

│   │   └── train.csv

│   ├── sample_notebook.ipynb

│   └── sample_submission.csv

├── 1_Literature

│   ├── 0_Random_Forests

│   │   ├── A_Heart_Disease_Prediction_Model_using_SVM-Decisio.pdf

│   │   ├── Decision trees and their use in medicine.pdf

│   │   ├── Machine learning-based prediction of postoperative mortality in emergency colorectal surgery- A retrospective, multicenter cohort study using Tokushukai Medical Database.pdf

│   │   └── Using_Machine_Learning_Algorithm_as_a_Method_for_I.pdf

│   └── 1_Neural Networks

│       └── Grassman et al 2018.pdf

├── 2_Data

│   ├── greeks.csv

│   └── train.csv

├── 3_EDA

├── 4_Preprocessing

│   ├── 0_data_preprocessing.ipynb

│   └── 1_RF_feature_importance.ipynb

├── 5_Models

│   ├── 0_Random_forests

│   │   ├── 0_sklearn_rf_kfolds_pca.ipynb

│   │   └── 1_RF_downsampling.ipynb

│   ├── 1_XGBoost

│   │   └── empty_file_to_track_folder.rtf

│   ├── 2_Logistic_regression

│   │   └── empty_file_to_track_folder.rtf

│   ├── 3_Perceptron

│   │   └── empty_file_to_track_folder.rtf

│   └── 4_Multilayer_perceptron

│       └── empty_file_to_track_folder.rtf

└── 6_Presentations

    ├── Baseline Presentation.pptx

    ├── Images

    │   ├── Grassman et al 2018.jpeg

    │   └── Podgorelec et al 2022.png

    └── baseline_presentation_feedback.md

```


## Results and evaluation
Best model: 
- Multilayer perceptron

## Future work

**Limitations of this work:**

- Class imbalance
- Possible data leakage, due to downsampling techniques  
- Sample sample size

**Future:** 

- Ensemble learning with metadata to predict classes
- Fairness:  there could be bias because of age-related diseases difference between men and women

## Acknowledgements/References

We want to thank Professor Cornelia Ilin for her suggestions on ways to improve our models. 

 **References**

- Akabane, Shota, et al. "Machine learning-based prediction of postoperative mortality in emergency colorectal surgery: A retrospective, multicenter cohort study using Tokushukai Medical Database." (2023).
- Alageel, Nojood, et al. "Using Machine Learning Algorithm as a Method for Improving Stroke Prediction." _International Journal of Advanced Computer Science and Applications_ 14.4 (2023).
- Grassmann, Felix, et al. "A deep learning algorithm for prediction of age-related eye disease study severity scale for age-related macular degeneration from color fundus photography." _Ophthalmology_ 125.9 (2018): 1410-1420.
- Mythili, T., et al. "A heart disease prediction model using SVM-decision trees-logistic regression (SDL)." _International Journal of Computer Applications_ 68.16 (2013).
- Podgorelec, Vili, et al. "Decision trees: an overview and their use in medicine." _Journal of medical systems_ 26 (2002): 445-463.
# Brain Tumor Classification
This project aims to find the ***Best Machine Learning model*** to fit the **Brain Tumor data** points using Scikit-Learn.

## Training dataset
Training dataset has MRIs of following classes.
1. giloma_tumor
<img src="https://user-images.githubusercontent.com/115199510/207057717-2b246175-fc80-4f4e-8061-c49f4f847617.jpg" width="200" height="200"/>
2. meningioma_tumor
<img src="https://user-images.githubusercontent.com/115199510/207058986-e6e86c7b-6b69-4c7a-9c27-6f557bf0d609.jpg" width="200" height="200"/>
3. no_tumor
<img src="https://user-images.githubusercontent.com/115199510/207059633-b6a94ee7-b132-4bf1-93be-9ac5a73490b9.jpg" width="200" height="200"/>
4. pituitary_tumor
<img src="https://user-images.githubusercontent.com/115199510/207060080-5c0d2198-628c-4605-a517-908332930229.jpg" width="200" height="200"/>

## Model used
This project used ***VotingClassifier*** algorithm with
1. **RandomForestClassifier**
2. **ExtraTreesClassifier**
3. **RidgeClassifier**

***VotingClassifier*** used default parameters.


**< Hyper-parameters >**

1. **RandomForestClsassifier**
- n_estimators=30
- class_weight='balanced'
- max_depth=23
- max_features=3
- n_jobs=-1
- random_state=2742

2. **ExtraTreesClassifier**
- n_estimators=65
- max_depth=30
- max_features=1
- min_samples_split=3
- n_jobs=-1
- random_state=3438

3. **RidgeClassifier**
- alpha=0.34

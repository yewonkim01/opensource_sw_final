# Brain Tumor Classification with sklearn
This project aims to find the ***Best Machine Learning model*** to fit the **Brain Tumor data** points using Scikit-Learn.

# Congifuration instructions
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
1. **ExtraTreesClassifier**
2. **KNeighborsClassifier**
3. **RidgeClassifier**


## Hyper-parameters


1. **ExtraTreesClsassifier**
- n_estimators=100
- max_depth=30
- max_features=3
- min_samples_split=3
- n_jobs=-1
- random_state=1774

```python
et = ExtraTreesClassifier(n_estimators = 100,
                          max_depth = 30,
                          max_features = 1,
                          min_samples_split = 3,
                          n_jobs = -1,
                          random_state = 1774)
```



2. **KNeighborsClassifier**
- n_neighbors=1

```python
knn = KNeighborsClassifier(n_neighbors= 1)
```




3. **RidgeClassifier**
- alpha=0.34

```python
rg = RidgeClassifier(alpha = 0.32)
```


## Final model
***VotingClassifier*** used default parameters.
~~~python
vote = VotingClassifier(estimators = [('et', et),
                                      ('knn', knn),
                                      ('rg', rg)])

vote.fit(X_train, y_train)
y_pred = vote.predict(X_test)
~~~

# Operating instructions
Please run from the top.

I attached the pickle file. Please run the file.


# License
This project uses the following license : MIT


# Contact
yewon kim

e-mail : kyw9791@naver.com

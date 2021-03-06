# :trophy: Kaggle competition Machine Learning

![](./images/portada.jpg?style=centerme)

---

## :loudspeaker: **Machine Learning for predicting the price of diamonds** 

### :computer: **Core technical concepts and inspiration**

- Python 3.7.3
- Pandas 0.24.2
- Plotly 4.8.2
- Matplotlib 3.2.1
- Seaborn 0.10.1
- Numpy 1.18.1
- Scikit-learn 0.23.2
- Joblib 0.16.0
- xgboost 1.2.0
- lightgbm 2.3.0 
- catboost 0.24
- h2o 3.30.1.1

### :newspaper: **Insights**


#### Variables



__We have in the diamonds datasheet:__

* Three `category` variables, cut, colot and clarity
* Six `float64` variables, carat, depth, table, x, y and z
* One `int64` vaiables, price.

__Main Insights:__

* Correlation > 0.96 between **X**, **Y**, **Z**, **Carat**, **Price**.

* **X**, **Y**, **Z** form the size and **Carat** is the weight, therefore they are correlated.

* In correlations one to one variable, the only one that correlates with **Price** is **Carat**.

* We could see in the relationship between **Depth** and **Cut** that the worst qualities of **Cut** are in the extremes and the best in the middle, showing a relationship between **Depth** and **Cut**.

* We could see that the worst qualities of the combinations **Cut**-**Color**-**Clarity** needs less carat for achieve more prices, showing a relationship between **Cut**-**Color**-**Clarity** with **Price**.

* We see a clear ladder in the barplot of the Average Price per the combinations of **Cut**-**Color**-**Clarity**, better **Cut**-**Color**-**Clarity** the average of price is lower, showing that is difficult to obtain a diamond with a high quality (High**Cut**-High**Color**-High**Clarity**) and high weight (**Carat**).


__Machine Learning Testing:__

* Test 1 - StackingRegressor

* Test 2 - H20 

* Conclusions:

The best result is obtained with simple models within the boosting regressor family, the most important thing is to do the train, test and validation well with a 60%, 20%, 20% of the datasheet to verify that the RMSE result in train is not too far from the others (test, validation).

I calculated the RMSE proxy which is a coefficient between the RMSES of the train and the mean of the RMSE test and validation, if this is 1 the RMSE of the train is the same as the RMSE of test and validation, 0 is very different.

Therefore, the important thing is to lower the RMSE without the proxy RMSE coefficient falling too low.

Another important thing is to seek inside the datasheet and create your own variables.



### :file_folder: **Folder structure**
```
└── project
    ├── __trash__
    ├── .gitignore
    ├── README.md
    ├── images
    ├── notebooks
    │   ├── NotebookML001.ipynb
    │   └── NotebookML002.ipynb
    │   └── NotebookML003.ipynb
    │       
    └── data
        ├── raw
        ├── processed
```



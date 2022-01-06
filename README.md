# Trading_Using_Machine_Learning

---

## Trading Prediction Analysis: 
 
### Tuning the Baseline Trading Algorithm
* Slicing data into different periods:

### Baseline Predictions: 
#### Slow SMA window = 4 / Fast SMA window = 100 / Training Data Window = 3 months
![Screen shot of classification report 2month](https://user-images.githubusercontent.com/89755088/148332678-b0aebbdd-c198-4cb3-bc01-0fa387747345.png)
![baseline_returns.png](https://user-images.githubusercontent.com/89755088/148336663-d07c6b25-6743-43c7-b9d8-b26e3e54d900.png)

### 2 Month Slice Predictions:
#### Slow SMA window = 4 / Fast SMA window = 100 / Training Data Window = 2 months
![Screen shot of classification report 2month](https://user-images.githubusercontent.com/89755088/148332678-b0aebbdd-c198-4cb3-bc01-0fa387747345.png)
![baseline_returns_2month.png](https://user-images.githubusercontent.com/89755088/148336853-0e697704-a9ba-478c-8f41-dcfd7f074307.png)

### 7 Month Slice Predictions:
#### Slow SMA window = 4 / Fast SMA window = 100 / Training Data Window = 7 months
![Screen shot of classification report 7month](https://user-images.githubusercontent.com/89755088/148333070-4d480333-6159-40c7-bb4f-9071d556329a.png)
![baseline_returns_7month.png](https://user-images.githubusercontent.com/89755088/148337012-11512d23-ee92-4db3-af60-310331b511f3.png)

### Question/Answer:
### What impact resulted from increasing or decreasing the training window?
#### 2 month slice:

Decreasing the training window to 2 months did not have any significant impact on the results. The accuaracy remained at 55% and the recall values did not change. The precision value however for a sell position reduced from 43% to 39%

#### 7 Month slice:

Increasing the training window to 7 months did increase the accuracy 1% from 55% to 56%. The recall value for a buy postition decreased by 1% from 96% to 95% and for the sell position increased by 1% from 4% to 5%. The precision value for the buy position stayed the same however for the sell position it increased by 2% from 43% to 45%. 

We do see an improvment in the prediction model by increasing the training window.

---
## Tuning the trading algorithm by adjusting the SMA input features. 
* Adjusting one or both of the windows for the algorithm.

### Slow SMA window = 30 / Fast SMA window = 180 / Training Data window = 3 months:
![Screen shot of classification report 30/180 window](https://user-images.githubusercontent.com/89755088/148346543-27cbbdf1-5f6b-43b7-8619-7bf562b59dea.png)
![baseline_returns_30_180.png](https://user-images.githubusercontent.com/89755088/148348428-7b2666bb-00e3-4b6f-a6a7-d2f586d706d7.png)

### Slow SMA window = 5 / Fast SMA window = 60 / Training Data window = 3 months:
![Screen shot of classification report 5/60 window](https://user-images.githubusercontent.com/89755088/148346917-ba63b7a2-514b-4adc-bff9-beb9f42dfc9f.png)
![baseline_returns_5_60.png](https://user-images.githubusercontent.com/89755088/148348193-6a671ee8-ae74-4e86-9c72-40fffc363fd3.png)

### Question/Answer:
### What impact resulted from increasing or decreasing either or both of the SMA windows?

#### Slow SMA window = 30 / Fast SMA window = 180:



#### Slow SMA window = 5 / Fast SMA window = 60









---
## Technologies

This program runs on [Python 3.7](https://www.python.org/) and utilizes:
* [Jupyter Lab](https://jupyter.org/install)
* [Pandas](https://pandas.pydata.org/)
* [numpy](https://numpy.org/)
* [sklearn](https://scikit-learn.org/stable/)
* [hvplot](https://pyviz-dev.github.io/hvplot/)

---
## Installation Guide

The dependencies needed to run the program:

```python
import pandas as pd
import numpy as np
from pathlib import Path
import hvplot.pandas
import matplotlib.pyplot as plt
from sklearn import svm
from sklearn.preprocessing import StandardScaler
from pandas.tseries.offsets import DateOffset
from sklearn.metrics import classification_report
```

---
## Usage

To utilize the machine learning trading program, open `machine_learning_trading_bot.ipynb` in Jupyter Lab 

---
## Contributors

Thomas Leahy, thomasleahy6@gmail.com

Starter Code provided by © 2020 - 2021 Trilogy Education Services, a 2U, Inc. brand.

---
## Licence
MIT Licence

2022 Thomas Leahy

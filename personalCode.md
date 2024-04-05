<h1 style="font-size: 3rem; color: red">My Python Personal Codes</h1>


```python
#My Codes for files- Name: data_analysis.py
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```


```python
#My Codes for dataset manipulations
import csv
import pandas as pd
#Sample data for this demostration
data = [
    ['Name', 'Age', 'Location'],
    ['Celestine Chuks', 38, 'Lagos'],
    ['Levi Nna', 30, 'Abuja'],
    ['Oliver Obi', 37, 'Edo']
]
#Defining the file name
file_name = 'simple.csv'
#Writing to the csv file 
with open (file_name, 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)
    print(f'Data written to {file_name}, successfully. ')
    print(data)
```

    Data written to simple.csv, successfully. 
    [['Name', 'Age', 'Location'], ['Celestine Chuks', 38, 'Lagos'], ['Levi Nna', 30, 'Abuja'], ['Oliver Obi', 37, 'Edo']]
    


```python
data = pd.read_csv('simple.csv')
```

#My code for basic exploration and feedback
print("Shape of dataset: " data.shape)
print("Column in the dataset: " data.column)
print("Summary statistics: \n " data.describe())

#My Codes for data processing and checking missing values
missing_values = dataisnull().sum()
print("Missing values: \n " missing_values)

#My code for filling missing values
data.fillna(data.mean(), inplace = True)

#My Codes for feature engineering
data['New_feature'] = data['feature1'] * data['feature2']


```python

```

#My Codes for data visiualization
import pandas as pd
import matplotlib.pyplot as plt

plt.figure(figsize = (8, 4))
plt.scatter(data['feature1'], data['feature2'], c = data['target'], cmap = 'magenta')
plt.title('scatter plot of Feature 1 vs Feature 2')
plt.xlabel('Feature1')
plt.ylabel('Feature2')
plt.colorbar(label='Target')
plt.show()


```python

```

#My Codes for model building
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score

X = data[['feature1', 'feature2', 'new_feature']]
y = data['target']

X_train, X_test, y_train, y_test = train_test_split
(X, y, test_size = 0.2, random_state = 42)

model = LogisticRegression()
model = fit(X_train, y_train)



```python

```

#My Code for model evaluation
y_pred = model.predict(X_test)
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy of the model: ", accuracy)

# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required libraries and load the car emission dataset using Pandas.

### Step2
Choose Weight and Volume as input variables (X) and CO2 as the output variable (Y).

### Step3
Create a Linear Regression model and train it using the selected input and output data.

### Step4
Calculate and display the regression coefficients and intercept.

### Step5
Give the car weight as 3300 and volume as 1300 as input, then predict and display the CO₂ emission using the trained model.

## Program:
```
import pandas as pd
url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"
df = pd.read_csv(url)
df.to_csv("/content/car (1).csv", index=False)
print("Dataset loaded successfully.")
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("/content/car (1).csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```

## Output:
<img width="606" height="57" alt="image" src="https://github.com/user-attachments/assets/72fc92a5-50b5-4ff9-8845-b9f819180c2f" />

## Result:
Thus the multivariate linear regression is implemented and predicted the output using python program.

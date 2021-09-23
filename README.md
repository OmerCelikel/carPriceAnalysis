# carPriceAnalysis
In this project, information of 100,000 vehicles for sale in England was examined. A price estimation has been made for a new vehicle to be offered for sale.

## Downloading and reading the data I will use

```python
# Mercedes data frame from merc.csv
df = pd.read_csv("/kaggle/input/used-car-dataset-ford-and-mercedes/merc.csv")
df.head()
```

## Missing Values
I don't have missing values. If It were...
```python

# checks if it has a null cell
df.isnull().sum()

# fill missing values with mean column values
dataset.fillna(dataset.mean(), inplace=True)

# count the number of NaN values in each column
print(dataset.isnull().sum())
```


## Categorical Variables
```python
from sklearn.preprocessing import OneHotEncoder
from sklearn import preprocessing

# Encode target labels with value between 0 and n_classes-1.
label_encoder = preprocessing.LabelEncoder()

df['model']= label_encoder.fit_transform(df['model']) 
df['transmission']= label_encoder.fit_transform(df['transmission']) 
df['fuelType']= label_encoder.fit_transform(df['fuelType']) 
```

## Error Metric
I used MSE -> measures how far the data are from the model’s predicted values.

```python
model.compile(optimizer = "adam", loss = "mse")

Verinizi train-validation-test diye bölmek (burada validation ve test'in gerçek hayatı yansıtması çok önemli)
Olabildiğince fazla model denemek ve metriğimizde en iyi yapanı seçmek

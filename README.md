# carPriceAnalysis
In this project, information of 100,000 vehicles for sale in England was examined. A price estimation has been made for a new vehicle to be offered for sale.

## Downloading and reading the data I will use

## Missing Values

```python
# fill missing values with mean column values
dataset.fillna(dataset.mean(), inplace=True)
# count the number of NaN values in each column
print(dataset.isnull().sum())
```


## Categorical Variables


İlgilendiğiniz probleme göre error metriğine karar vermek (derste gördüğümüz RMSE-RMSLE gibi)
Verinizi train-validation-test diye bölmek (burada validation ve test'in gerçek hayatı yansıtması çok önemli)
Olabildiğince fazla model denemek ve metriğimizde en iyi yapanı seçmek

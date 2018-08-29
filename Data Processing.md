

# 1. Data Processing
  ### Importing library

      import numpy as numpy
      import panda as panda
      import matplotlib as matplotlib

  ### Reading the csv file in Dataset
  
    
    myDataSet = panda.read_csv('DataSet.csv');          // read_csv() will read the data into the DataFrame and iterating or breaking of the file into chunks.
    
  ### Read all the columns expects the last one
    
    values = myDataSet.iloc[:,:-1].values
    
   ### Read the last columns only
    
    lastColValues = myDataSet.iloc[:,3].values
    
   ### Handle Missing data in the fields - Integer
   * Replace by the Mean of values in the column that contains the missing data
   ```
   from sklearn.preprocessing import Imputer
   imputer = Imputer(missing_values = 'NaN', strategy ='mean' axis = 0)
   imputer = imputer.fit(values[:, INDEX_WHERE_IS_COLUMN/RANGE_OF_COLUMN_LAST_ONE_EXCLUDE(1:3)])
   values[:, 1:3] = imputer.transform(values[:,1:3])
   ```
   strategy='mean/median/mode'
     
  ### Data Categorization 
  ML is basically uses the mathematical equation. So we need to change or caegorize the String fields into the Number.
  LabelEncoder : Encode labels with value between 0 and n_classes-1.
  
  ```
  from sklearn.preprocessing import LabelEncoder, OneHotEncoder
  labelencoder_X = LabelEncoder()
  X[:, 0] = labelencoder_X.fit_transform(X[:, 0]) # this method takes first column , index. Column which we need to categories
  onehotencoder = OneHotEncoder(categorical_features = [0])
  X = onehotencoder.fit_transform(X).toarray()
  ```
  

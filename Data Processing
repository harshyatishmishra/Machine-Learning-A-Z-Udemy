
Use Spyder and Python

1. Data Processing
  ### Importing library###
      ```
      import numpy as numpy
      import panda as panda
      import matplotlib as matplotlib
      ```
  ### Reading the csv file in Dataset###
    ```
    myDataSet = panda.read_csv('DataSet.csv');          // read_csv() will read the data into the DataFrame and iterating or breaking of the file into chunks.
    ```
  ### Read all the columns expects the last one###
    ```
    values = myDataSet.iloc[:,:-1].values
    ```
   ### Read the last columns only###
    ```
    lastColValues = myDataSet.iloc[:,3].values
    ```
   ### Handle Missing data in the fields - Integer###
    * Replace by the Mean of values in the column that contains the missing data
   ```
   from sklearn.preprocessing import Imputer
   imputer = Imputer(missing_values = 'NaN', strategy ='mean' axis = 0)
   imputer = imputer.fit(values[:, INDEX_WHERE_IS_COLUMN/RANGE_OF_COLUMN_LAST_ONE_EXCLUDE(1:3)])
   values[:, 1:3] = imputer.transform(values[:,1:3])
   ```
   strategy='mean/median/mode'
     
    

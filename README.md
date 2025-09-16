##### PROBLEM 1

Start coding the program by importing the PANDAS library. THis will allow access to numerous syntaxes that shall perform the process of the following problems.
The syntax below is used to store the datas in the excel file into the variable "car". Everytime that this variable is called, the data will be displayed in a spreadsheet format.

``` 
import pandas as pd

cars = pd.read_csv('cars (1).csv')
cars
```

##### PROBLEM 2
Store the data set into the variable car to be accessed later on the program. 

For objective 'a' use .iloc synatx and slicing to display the first five odd-numbered columns in the spreadsheet. 
Save the result in the "odd_column" variable to make it easier to call. 

```
odd_columns = cars.iloc[:, 1::2]

result = odd_columns.head()
result
```

Objective 'b' asks to show the row that contains the model Mazda RX4. Therefore, call row 0 and column 1.

```
cars[0:1]
```

Objective 'c' is basically an easier and quick way of showing the very first row of the table. The following syntax filters the row where it is equal to the model and displays the columns under it.

```
cars.loc[cars['Model']=='Camaro Z28', ['Model', 'cyl']]
```

For the last objective 'd', the slicing directly selects rows with the index numbers 1, 28, and 18 and then shows only the Model cyl and gear of the  columns from those rows.
```
cars.loc[[1,28,18],['Model', 'cyl', 'gear']]
```



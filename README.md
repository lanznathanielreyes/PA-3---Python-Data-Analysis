##### PROBLEM 1

Start coding the program by importing the PANDAS library. THis will allow access to numerous syntaxes that shall perform the process of the following problems.
The syntax below is used to store the datas in the excel file into the variable "car". Everytime that this variable is called, the data will be displayed in a spreadsheet format.

```Python
import pandas as pd  # Imports the pandas library for working with data tables.

cars = pd.read_csv('cars (1).csv')  # Reads the CSV file named 'cars (1).csv' into a DataFrame called cars.
cars  # Displays the entire cars DataFrame.

odd_columns = cars.iloc[:, 1::2]  # Selects every other column starting from index 1 (all odd-numbered columns).

result = odd_columns.head()  # Takes the first 5 rows of the selected odd columns and stores them in result.
result  # Displays the result (first 5 rows of odd-numbered columns).

cars[0:1]  # Displays only the first row of the cars DataFrame.
```

##### PROBLEM 2
Store the data set into the variable car to be accessed later on the program. 

For objective 'a' use .iloc synatx and slicing to display the first five odd-numbered columns in the spreadsheet. 
Save the result in the "odd_column" variable to make it easier to call. 

```Python
import pandas as pd  # Imports the pandas library for working with data tables
odd_columns = cars.iloc[:, 1::2]  # Selects every other column starting from index 1 (all odd-numbered columns).

result = odd_columns.head()  # Gets the first 5 rows from the selected odd-numbered columns.
result  # Displays the result DataFrame.

cars[0:1]  # Displays only the first row of the cars DataFrame.

cars.loc[cars['Model'] == 'Camaro Z28', ['Model', 'cyl']]  # Filters the DataFrame to rows where Model is 'Camaro Z28' and shows only 'Model' and 'cyl' columns.

cars.loc[[1, 28, 18], ['Model', 'cyl', 'gear']]  # Selects rows with index 1, 28, and 18, showing only 'Model', 'cyl', and 'gear' columns.

```
Version 2

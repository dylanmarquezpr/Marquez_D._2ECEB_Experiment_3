# Experiment 3 - Pandas

Name:  Dylan Rvy A. Marquez  
Section: 2ECE-B  
Date: 09/07/2025  

## OVERVIEW
This experiment introduces the Pandas library in Python, which is used for handling and analyzing structured data. Pandas provides tools to load datasets, explore their structure, and extract information using indexing, slicing, and filtering.  

#### The experiment covers two problems:  
1. Loading and displaying parts of a dataset.  
2. Extracting specific data from the dataset using subsetting and indexing.  

Through these tasks, the experiment demonstrates how Pandas simplifies working with tabular data (such as CSV files), making it easier to manage and analyze compared to raw Python lists or arrays.  

## 1. PROBLEM 1
#### Objective:

Load the `cars.csv` file into a Pandas DataFrame named `cars`, then display both the first and last 5 entries of the dataset.  

## TABLE : 
<img width="352" height="633" alt="Screenshot 2025-09-07 223250" src="https://github.com/user-attachments/assets/b2f856ab-ba3f-4a61-913e-33c23b891ea4" />



### PROCEDURE:

#### 1. Import the Pandas library.  
```python
   import pandas as pd
```
#### 2. Load the dataset from a CSV file into a DataFrame.

```python
cars = pd.read_csv("cars.csv")
```

#### 3. Display the first five entries using .head().

```python
cars.head()
```

### OUTPUT:
<img width="707" height="222" alt="Screenshot 2025-09-07 224051" src="https://github.com/user-attachments/assets/fb181731-f162-4085-9cc9-e455ba34a2eb" />


The first five rows show the top entries of the dataset. The purpose of using .head() in Pandas is to quickly look at the first few rows of a dataset. By default, it shows the first five entries, which gives us an overview of the column names, the type of values stored in each column, and the general structure of the dataset. This is useful because when working with large files, it would not be practical to display the entire dataset just to understand its format.


#### 4. Display the last five entries using .tail().

```python
cars.tail()
```

### OUTPUT:
<img width="680" height="221" alt="Screenshot 2025-09-07 224137" src="https://github.com/user-attachments/assets/11a24f3d-a55c-44d1-a1b5-3fc4a63b1570" />

The last five rows show the bottom entries of the dataset. The method .tail() is used to look at the last few rows of the dataset, also defaulting to five rows. This is important because sometimes datasets contain notes, missing values, or irregular entries at the end that may not be obvious from the top portion.

## 2. PROBLEM 2
#### Objective:

Using the same DataFrame cars, extract information through slicing, indexing, and filtering.

### PROCEDURE:

#### (a) Display the first 5 entries but only the odd-numbered columns.

```python
cars.iloc[0:5, ::2]
```
### OUTPUT:
<img width="400" height="213" alt="Screenshot 2025-09-07 224241" src="https://github.com/user-attachments/assets/03ab5e59-a57e-411b-b112-faf612193954" />

This command uses .iloc to select rows and columns by their numeric position. The slice 0:5 chooses the first five rows, while ::2 picks every other column, resulting in the odd-numbered columns.  

#### (b) Retrieve the row for the car model Mazda RX4.

```python
cars.loc[cars['Model'] == 'Mazda RX4']
```

### OUTPUT:
<img width="634" height="73" alt="Screenshot 2025-09-07 224249" src="https://github.com/user-attachments/assets/24ec8012-5258-4e82-9df9-dd913e452ce8" />

Here, .loc is used to filter rows based on a condition. The condition cars['Model'] == 'Mazda RX4' searches the Model column and finds the row where the model matches exactly. The result is displayed that is a row of information specific to the Mazda RX4.

#### (c) Find how many cylinders the Camaro Z28 has.

```python
cars.loc[cars['Model'] == 'Camaro Z28', ['cyl']]
```

### OUTPUT:
<img width="78" height="69" alt="Screenshot 2025-09-07 224325" src="https://github.com/user-attachments/assets/e14b92e9-dd3b-44bf-bbbd-f47c2dd1c950" />

This query looks specifically at the Camaro Z28 and returns only the cyl column. By adding ['cyl'], the output is narrowed down to just the cylinder information instead of the whole row. 

#### (d) Show the cylinders and gear type for the models Mazda RX4 Wag, Ford Pantera L, and Honda Civic.

```python
cars.loc[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']), ['Model','cyl','gear']] 
```

### OUTPUT:
<img width="256" height="148" alt="image" src="https://github.com/user-attachments/assets/d333be73-a2bf-456d-9b9e-0343420a4425" />


The .isin() function checks whether the Model column matches any value from a given list of car names. Then, .loc selects only those rows and restricts the output to the Model, cyl, and gear columns. This produces a small, table showing the requested details for three specific car models.


## CONCLUSION
This experiment basically shows how Pandas can be used to handle and analyze structured data efficiently. Problem 1 introduced the basic functions of loading a dataset and previewing its contents with `.head()` and `.tail()`, which are important for fast checking the structure of data. Problem 2 applied indexing, slicing, and filtering ways to extract specific information such as rows, columns, and values based on conditions. The experiment showed how Pandas simplifies working with tabular data and can be utilize for data analysis in engineering and research applications.





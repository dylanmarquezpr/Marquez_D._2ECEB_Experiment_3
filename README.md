# Experiment 3 - Pandas

Name:  Dylan Rvy A. Marquez  
Section: 2ECE-B  
Date: 09/07/2025  

## OVERVIEW
This experiment introduces the Pandas library in Python, which is used for handling and analyzing structured data. Pandas provides tools to load datasets, explore their structure, and extract meaningful information using indexing, slicing, and filtering.  

The experiment covers two problems:  
1. Loading and displaying parts of a dataset.  
2. Extracting specific data from the dataset using subsetting and indexing.  

Through these tasks, the experiment demonstrates how Pandas simplifies working with tabular data (such as CSV files), making it easier to manage and analyze compared to raw Python lists or arrays.  

## 1. PROBLEM 1
#### Objective:

Load the `cars.csv` file into a Pandas DataFrame named `cars`, then display both the first and last 5 entries of the dataset.  

### PROCEDURE:

1. Import the Pandas library.  
```python
   import pandas as pd
```
2. Load the dataset from a CSV file into a DataFrame.

```python
cars = pd.read_csv("cars.csv")
```

4. Display the first five entries using .head().

```python
cars.head()
```

### OUTPUT:

The first five rows show the top entries of the dataset.


5. Display the last five entries using .tail().

```python
cars.tail()
```

### OUTPUT:

The last five rows show the bottom entries of the dataset.

## 2. PROBLEM 2
#### Objective:

Using the same DataFrame cars, extract information through slicing, indexing, and filtering.

### PROCEDURE:

(a) Display the first 5 entries but only the odd-numbered columns.

```python
cars.iloc[0:5, ::2]
```
(b) Retrieve the row for the car model Mazda RX4.

```python
cars.loc[cars['Model'] == 'Mazda RX4']
```
(c) Find how many cylinders the Camaro Z28 has.

```python
cars.loc[cars['Model'] == 'Camaro Z28', ['cyl']]
```
(d) Show the cylinders and gear type for the models Mazda RX4 Wag, Ford Pantera L, and Honda Civic.

```python
cars.loc[cars['Model'].isin(['Mazda RX4 Wag', 'Ford Pantera L', 'Honda Civic']), ['Model','cyl','gear']] 
```






s

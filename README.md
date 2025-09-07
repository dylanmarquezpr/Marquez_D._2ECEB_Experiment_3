# Experiment 3 - Pandas

**Name:** Dylan Rvy A. Marquez  
**Section:** 2ECE-B  
**Date:** 09/07/2025  

## OVERVIEW
This experiment introduces the Pandas library in Python, which is used for handling and analyzing structured data. Pandas provides tools to load datasets, explore their structure, and extract meaningful information using indexing, slicing, and filtering.  

The experiment covers two problems:  
1. Loading and displaying parts of a dataset.  
2. Extracting specific data from the dataset using subsetting and indexing.  

Through these tasks, the experiment demonstrates how Pandas simplifies working with tabular data (such as CSV files), making it easier to manage and analyze compared to raw Python lists or arrays.  

## 1. PROBLEM 1
**Objective:**  
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

5. Display the last five entries using .tail().

```python
cars.tail()
```





s

# Python for exploratory data analysis (EDA): 

## Table of Content
  * [Python](#python)
  * [Python Installation](#installation)
  * [Python Basics](#basic python code)

## Python

Python is an interpreted, high-level, general-purpose programming language. Created by Guido van Rossum and first released in 1991. Its language constructs and object-oriented approach aim to help programmers write clear, logical code for small and large-scale projects. It supports multiple programming paradigms, including procedural, object-oriented, and functional programming. Python has a rich set of libraries that helps solve many programming problems including machine learning. Also, python programming is easy to learn.

## Installation

Anaconda

If you are primarily doing data science work, Anaconda is a good option. Anaconda is popular because it brings many of the tools used in data science and machine learning with just one install.

1. Search Anaconda on the browser and open the link with the address https://anaconda.org/ .
2. Download Anaconda from the Anaconda homepage by selecting the operating system configuration.
3. Install Anaconda.
4. Create your virtual python environment using the following commands on the conda command prompt.
  (base)$ pip install virtualenv
  (base)$ virtualenv -p /usr/env_path virtualenv_name
  (base)$ source virtualenv_name/bin/activate
  (virtualenv_name)$ pip install pandas
  (virtualenv_name)$ deactivate
5. Open Jupyter Notebook on your browser and start coding.

Another way to install python is to download appropriate Python executable as per your operating system from https://www.python.org/ website and install it in your system.

## Basic python code

The code will help one to start with python language. I covered basic string manipulation, list, dictionary, tuple, set, numpy, pandas, and data visualization.
Please refer the code file [Python_Basics].

### String manipulation

str = ' I love coding in Python ' # Declare variable and assign values

print(str)            # Print the variable ( I love coding in Python )

print(str.lstrip())   # Remove white space from left (I love coding in Python )

print(str.rstrip())   # Remove white space from right ( I love coding in Python)

print(str.strip())    # Remove white space from both sides (I love coding in Python)

print(str.upper())    # Make all upper case ( I LOVE CODING IN PYTHON )

print(str.lower())    # Make all lower case ( i love coding in python )

print(len(str))       # Length of variable (25)

str = 'I love coding in Python'

print(str[0])        # Get the first character (I)

print(str[-1])       # Get the last character (n)

print(str[2:6])       # Get charcaters 2 to 5. The possition 6 is not inclusive. (love)

print(str[-21:-17])   # Start from backward. Here it is from -21. (love)

print(str[:13])       # Read from beginning till a particular position. (I love coding)

print(str[::-1])      # Reverse a string. From the end and one step from end. (nohtyP ni gnidoc evol I)

### Arithmetic operators

x, y = 3, 2                  # x = 3 and y = 2 

print('x + y = ', x + y)     # x + y =  5

print('x - y = ', x - y)     # x + y =  1

print('x * y = ', x * y)     # x * y =  6

print('x / y = ', x / y)     # x / y =  1.5

print('x % y = ', x % y)     # x % y =  1

print('x // y = ', x // y)   # x // y =  1 # Floor division - Excludes decimals

print('x ** y = ', x ** y)   # x ** y =  9 # Exponent - left operand raised to the power of right

### List in Python

my_empty_list = []            # We can declare an empty list

print(my_empty_list)          # []

my_list = [ 'Lion' , 'Dog' , 'Cat' , 9.5 , 15] # List can have multiple data types

print(my_list)

print(my_list[0])             # First element in the list (Lion)

print(my_list[-1])            # Last element in the list (15)

print(my_list[1:3])           # ['Dog', 'Cat']

print(my_list.pop())          # pop removes last element if no index is specified

print(my_list)                # 15 is removed from the list (['Lion', 'Dog', 'Cat', 9.5])

my_list.append( 'Panda' )     # Adding an element to the list 

print(my_list)                # ['Lion', 'Dog', 'Cat', 9.5, 'Panda']

my_list.remove( 9.5 )         # we can use remove to remove an element.

print(my_list)                # ['Lion', 'Dog', 'Cat', 'Panda']

str_from_list = " ".join(my_list) # We can build a string using all list items

print(str_from_list)          # Lion Dog Cat Panda

### List Comprehension

list_of_words = [word for word in str_from_list.split()] # Instead of writing loop, we can use one line.

print(list_of_words)          # ['Lion', 'Dog', 'Cat', 'Panda']

even_number = [x for x in range(1,10) if x % 2 == 0] # Even number between 1 to 8. 10 is not inclusive.

print(even_number)           # [2, 4, 6, 8]

### Dictionary in Python

my_dict = {'Name' : 'Palash Aich' , 'Age' : 35, 'Hobby' : 'Travel'}

print(my_dict)            # {'Name': 'Palash Aich', 'Age': 35, 'Hobby': 'Travel'}

print(my_dict['Name'])    # Palash Aich

my_dict['Profession' ] = 'Data Scientist' # Adding an element

print(my_dict)            # {'Name': 'Palash Aich', 'Age': 35, 'Hobby': 'Travel', 'Profession': 'Data Scientist'}

print(my_dict.keys())     # ['Name', 'Age', 'Hobby', 'Profession']

print(my_dict.values())   # ['Palash Aich', 35, 'Travel', 'Data Scientist']

del my_dict['Age']        # Deleting an element

print(my_dict)            # {'Name': 'Palash Aich', 'Hobby': 'Travel', 'Profession': 'Data Scientist'}

### Set and Tuple in Python

my_set_1 = set(['Lion', 'Dog', 'Cat', 'Dog']) # set contains only unique elements

print(my_set_1)     # {'Lion', 'Cat', 'Dog'}

my_set_2 = set(['Lion', 'Panda', 'Cat', 'Panda']) 

print(my_set_2) # {'Panda', 'Lion', 'Cat'}

print(my_set_1.intersection(my_set_2))    # Common elements in 2 sets {'Lion', 'Cat'}

print(my_set_1.union(my_set_2))           # Unique list from 2 sets {'Lion', 'Cat', 'Panda', 'Dog'}

print(my_set_1.difference(my_set_2))      # set1 - set2. {'Dog'}

### Tuple

my_tuple = ()      # Empty Tuple

print(my_tuple)    # ()

my_tuple = ('Lion', 'Panda', 'Cat', 'Panda')

print(my_tuple)    # ('Lion', 'Panda', 'Cat', 'Panda')

### Functions in Python

def my_addition(x, y):    # Declare the function
    return x + y          # Return values from function

print(my_addition(2,3))   # Call the function


### Recursive function
Finding n factorial

def factorial (n):
    if n > 1:
        return n * factorial(n - 1)
    else:
        return n

print(" Factorial is: ", factorial(3)) # Call the function for the value 3

### Numpy - useful library in python for data science

Let's understand how to use library in python.
You may need to install it using [pip install numpy] command in command prompt.

import numpy as np    # np is alias

print(np.array([1, 2, 3, 4, 5, 6]))       # One dimensional array

print(np.array([[1, 2, 3], [4, 5, 6]]))   # Two dimensional array

print(np.zeros(4, dtype = np.int))        # Array of zeros with integer data type

print(np.ones((4, 3)))                    # Array of 4 rows and 3 columns with all ones 4 X 3.
      
print(np.arange(0, 25, 5))                # Array of numbers from 0 to 20 with a step of 5

print('\n')       # New line

### Array Slicing

my_array = np.arange(1, 21).reshape(4,5)  # An array consists of 1 to 20 in 4 X 5 dimension

print(my_array)

print(my_array.shape)        # Shape of the array (4, 5)

print(my_array[1, 1])        # Slice 2nd row and 2nd column

print(my_array[:, 1])        # Slice all rows and 2nd column

print(my_array[:, :2])       # Slice all rows and first 2 columns

### Pandas - usefull library in python for data science

import pandas as pd     # Import library

print(pd.Series([1, 2, 3, 4, 5]))     # Series in pandas

print(pd.Series([0, 1, 2], index = [ 'f' , 's' , 't' ]))    # Series with setting index

### Dataframe in pandas that consists row and column

df = pd.DataFrame({ 'name' : [ 'Palash' , 'Samar' , 'Keshu' , 'Dristi' ], 'age' : [30, 25, 9,
8], 'occupation' : [ 'Data Scientist' , 'Data Engineer' , 'NLP Engineer' , 'ML Engineer' ]})

print(df.head(3))  # print first 3 rows from dataframe df

### A pandas dataframe by importing files
#df = pd.read_csv( 'path/my_file.csv' )

df.set_index( 'name', inplace = True )               # set name as index

df.sort_index(axis = 0, ascending = False )          # sort by index

df.sort_values(by = 'occupation', ascending = False, inplace = True) # sort by occupation in descending order

print('\nSorting in dataframe\n')

print(df)

### Get details from a dataframe

print(df.info())         # Get metadata summary

print(df.describe())     # Get statistical summary

print('\nColumns in dataframe\n')

print(df.columns)        # Get column name in a daraframe columns

### Slicing a dataframe

print(df['occupation'])           # Get values of name column

print(df[['age', 'occupation']])  # Get values of name and occupation column

print(df[1:3])                  # 2nd and third row in the dataframe
print(df[1::2])                 # Alternate rows from index 5

### Index based slicing

print('\nIndex based slicing')

df.iloc[0, 1]         # Element in 3rd row and 2nd column

df.iloc[1]            # All columns of 2nd row

df = pd.DataFrame({ 'name' : ['Palash' , 'Samar' , 'Keshu' , 'Dristi'], 
                   'age' : [30, 25, 22, 29], 
                   'occupation' : [ 'Data Scientist' , 'Data Engineer' , 'NLP Engineer' , 'Data Engineer'],
                   'salary' : [3000, 2500, 9000, 8000]})

df1 = pd.DataFrame({'name' : ['Palash' , 'Samar' , 'Keshu' , 'Dristi'], 
                   'region' : [ 'APAC' , 'AMERICA' , 'EMEA' , 'APAC']})

### Join 2 dataframe based on a common column

df_merged = pd.merge(df, df1, how = 'inner', on = [ 'name' , 'name'])

print(df_merged)

### Concatenate dataframes one below other

print('\nConcatenate dataframe\n')

print(pd.concat([df, df1], axis = 1)) # axis 0 is rows and 1 is column

### Add a new column in a dataframe

print('\nColumn update in dataframe\n')

df[ 'salary_in_thousand' ] = df.salary / 1000

print(df)

### Aggregate data

print('\nAggregate data \n')

print(df.groupby(['occupation'])['salary'].sum())

### applying an operation to a column

print('\nPivoting dataframe\n')

print(df_merged.pivot_table(values = 'salary', index = 'occupation', columns ='region', aggfunc = 'sum'))

### Data visualization in Python

import matplotlib.pyplot as plt

df = pd.DataFrame({ 'name' : ['Palash' , 'Samar' , 'Keshu' , 'Dristi'], 
                   'age' : [30, 25, 22, 29], 
                   'occupation' : [ 'Data Scientist' , 'Data Engineer' , 'NLP Engineer' , 'Data Engineer'],
                   'salary' : [3000, 2500, 9000, 8000]})

plt.figure(figsize=(6,4))    # Setup image size

plt.barh(df.occupation, df.salary, color = 'blue', height = 0.4) 

plt.show()

print('\n**** Seaborn Library ****\n')

import seaborn as sns

df = pd.DataFrame({ 'name' : ['Palash' , 'Samar' , 'Keshu' , 'Dristi'], 
                   'age' : [30, 25, 22, 29], 
                   'occupation' : [ 'Data Scientist' , 'Data Engineer' , 'NLP Engineer' , 'Data Engineer'],
                   'salary' : [3000, 2500, 9000, 8000]})

plt.figure(figsize=(6,4))    # Setup image size

sns.barplot(df.occupation, df.salary)

plt.show()

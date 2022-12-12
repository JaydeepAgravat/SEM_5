# 1. Explain String functions, String Slicing and String Formatting in Python.

## String 

- String is Ordered Sequence of character such as “darshan”, ‘college’, “રાજકોટ” etc..
- Strings are arrays of bytes representing Unicode characters.
- String can be represented as single, double or triple quotes.
- String with triple Quotes allows multiple lines.
- String in python is immutable.
- Square brackets can be used to access elements of the string, Ex. “Darshan”[1] = a, characters
can also be accessed with reverse index like “Darshan”[-1] = n.
```python
x = " D a r s h a n "
index = 0 1 2 3 4 5 6
Reverse index = 0 -6 -5 -4 -3 -2 -1
```

## String Functions
```
count()	Returns the number of occurrences of a substring in the string.
find()	Returns the lowest index of the substring if it is found
index()	Returns the position of the first occurrence of a substring in a string
title(), lower(), upper() will returns capitalized, lower case and upper case string respectively.
istitle(), islower(), isupper() will returns True if the given string is capitalized, lower case and
upper case respectively.
strip() method will remove whitespaces from both side of the string and returns the string.
rstrip() and lstrip() will remove whitespaces from right and left side respectively.
isalnum() method will return true if all the characters in the string are alphanumeric (i.e either
alphabets or numeric).
isalpha() and isnumeric() will return true if all the characters in the string are only alphabets
and numeric respectively.
isdecimal() will return true is all the characters in the string are decimal.
```
##### Example
```python
x = "Darshan"
ca = x.count('a')
print(ca)
=> 2
```

## String slicing

- We can get the substring in python using string slicing, we can specify start index, end index
and steps (colon separated) to slice the string.

##### Syntax

```
x[startindex:endindex:steps]
```

##### Example
```python

x = 'darshan institute of engineering and technology, rajkot, gujarat, INDIA'

subx1 = x[0:7]
subx2 = x[49:55]
subx3 = x[66:]
subx4 = x[::2]
subx5 = x[::-1]

print(subx1)
print(subx2)
print(subx3)
print(subx4)
print(subx5)

Output : darshan
Output : rajkot
Output : INDIA
Output : drhnisiueo niern n ehooy akt uaa,IDA
Output : AIDNI ,tarajug ,tokjar ,ygolonhcet dna gnireenigne fo etutitsni nahsrad
```

# String Formatting

- str.format() is one of the string formatting methods in Python3, which allows multiple
substitutions and value formatting.
- This method lets us concatenate elements within a string through positional formatting.

```python

x = '{} institute, rajkot'
y = x.format('darshan')

print(y)
print(x.format('ABCD'))

Output : darshan institute, rajkot
Output : ABCD institute, rajkot
```

- We can specify multiple parameters to the function.

```python

x = '{} institute, {}'
y = x.format('darshan','rajkot')

print(y)
print(x.format('ABCD','XYZ'))

Output : darshan institute, rajkot
Output : ABCD institute, XYZ
```

- We can specify the order of parameters in the string.
```python

x = '{1} institute, {0}'
y = x.format('darshan','rajkot')

print(y)
print(x.format('ABCD','XYZ'))


Output : rajkot institute, darshan
Output : XYZ institute, ABCD
```

- We can also specify alias within the string to specify the order.

```python
x = '{collegename} institute, {cityname}'

print(x.format(collegename='darshan',cityname='rajkot'))

Output : darshan institute, rajkot
```

- We can format the decimal values using format method.

```python

per = (438 / 500) * 100
x = 'result = {r:3.2f} %'.format(r=per)
print(x)

Output : result = 87.60 %
```

# 2. Explain List, Set, Tuple and Dictionary in Python.

- There are four built-in data structures in Python - list, dictionary, tuple and set.

| Name       | Type | Description                                                                             | Example                                           |
|------------|------|-----------------------------------------------------------------------------------------|---------------------------------------------------|
| List       | list | Ordered Sequence of objects, will be represented with square brackets [ ]               | Example : [ 18, “darshan”, True, 102.3 ]          |
| Dictionary | dict | Unordered key : value pair of objects , will be represented with curly brackets { }     | Example : { “college”: “darshan”, “code”: “054” } |
| Tuple      | tup  | Ordered immutable sequence of objects, will be represented with round brackets ( )      | Example : ( 18, “darshan”, True, 102.3 )          |
| Set        | set  | Unordered collection of unique objects, will be represented with the curly brackets { } | Example : { 18, “darshan”, True, 102.3 }          |

# 3. List and Explain steps of Data Science Pipeline.


- Data science pipeline requires the data scientist to follow particular steps in the preparation, analysis and presentation of the data.

- General steps in the pipeline are :
1. Preparing the data
2. Performing data analysis
3. Learning from data
4. Visualizing 
5. Obtaining insights

#### 1. Preparing the data

- The data we access from various sources may not come directly in the structured format.
- We need to transform the data in the structured format.
- Transformation may require changing data types, order in which data appears and even the creation of missing data

#### 2. Performing data analysis

- Results of the data analysis should be provable and consistent.
- Some time single approach may not provide the desired output, we need to use multiple algorithms to get the result.
- The use of trial and error is part of the data science art.

#### 3. Learning from data

- As we iterate through various statistical analysis methods and apply algorithms to detect patterns, we begin learning
from the data.
- The data might not tell the story that you originally thought it would.

#### 4. Visualizing

- Visualizing means seeing the patterns in the data and then being able to react to those patterns.
- It also means being able to see when data is not part of the pattern.

#### 5. Obtaining insights

- The insights you obtain from manipulating and analyzing the data help you to perform real world tasks. 
- For example you can use the result of an analysis to make a business decision.

# 4. List and Explain different programming styles (programming paradigms) in python.

- There are four main Python coding styles: imperative, functional, object-oriented, and procedural.
- `1.Functional`:
  - Every statement is treated as a mathematical equation and any forms of state or mutable data are avoided. 
  - The main advantage of this approach is that it lends itself well to parallel processing because there is no state to consider.
  - Many developers prefer this coding style for recursion and for lambda calculus.
- `2.Imperative`:
  - Computation is performed as a direct change to program state.
  - This style is especially useful when manipulating data structures and produces elegant yet simple code. 
  - Python fully implements this paradigm.
- `3.Object-oriented`:
  - Relies on data fields that are treated as objects and manipulated only through prescribed methods.
  - Python doesn’t fully support this paradigm because it can’t implement features such as data hiding (encapsulation), which many believe is a primary requirement of the object-oriented programming paradigm.
  - This coding style also favors code reuse.
- `4.Procedural`:
  - Tasks are treated as step-by-step iterations where common tasks are placed in functions that are called as needed. 
  - This coding style favors iteration, sequencing, selection, and modularization.
  - Python excels in implementing this particular paradigm.

# 5. Explain Series and DataFrame in Pandas with example and differentiate Numpy and Pandas.

## Series

Series is an one-dimensional* array with axis labels.

It supports both integer and label-based index but index must be of hashable type.

If we do not specify index it will assign integer zero-based index.

###### Syntax

```
import pandas as pd
s = pd.Series(data,index,dtype,copy=False)

Parameters
data  = array like Iterable
index = array like index
dtype = data-type
copy  = bool, default is False
```

###### Example

```python
import pandas as pd
s = pd.Series([1, 3, 5, 7, 9, 11])
print(s)

output :
0 1
1 3
2 5
3 7
4 9
5 11
dtype: int64
```

- We can then access the elements inside Series just like array using square brackets notation.

```python
import pandas as pd

s = pd.Series([1, 3, 5, 7, 9, 11])
print("S[0] = ", s[0])

b = s[0] + s[1]
print("Sum = ", b)

output :
S[0] = 1
Sum = 4
```

- We can specify the data type of Series using dtype parameter.

```python
import pandas as pd

s = pd.Series([1, 3, 5, 7, 9, 11], dtype='str')
print("S[0] = ", s[0])

b = s[0] + s[1]
print("Sum = ", b)

output:
S[0] = 1
Sum = 13
```

- We can specify index to Series with the help of index parameter.
```python
import numpy as np

import pandas as pd

i = ['name','address','phone','email','website']

d = ['darshan','rj',123','d@d.com','darshan.ac.in']

s = pd.Series(data=d,index=i)

print(s)

output : 
name     darshan
address  rj
phone    123
email    d@d.com
website  darshan.ac.in

dtype: object
```

## Data Frame

- Data frames are two dimensional data structure, i.e. data is aligned in a tabular format in rows and columns.
- Data frame also contains labelled axes on rows and columns.
##### Features of Data Frame :
1. It is size-mutable
2. Has labelled axes
3. Columns can be of different data types
4. We can perform arithmetic operations on rows and columns.
##### Structure

<img src="https://media.geeksforgeeks.org/wp-content/uploads/finallpandas.png" width=70%>

##### Create Dataframe

- A pandas DataFrame can be created using various inputs like −
1. Lists
2. dict
3. Series
4. Numpy ndarrays
5. Another DataFrame

###### Example : Creating DataFrame from dict of lists

```python
  import pandas as pd

# intialise data 
data = {'Name':['Tom', 'nick', 'krish', 'jack'],
        'Age':[20, 21, 19, 18]}

# Create DataFrame
df = pd.DataFrame(data)

# Print the output.
print(df)
```

```Python
    Output:
      Name  Age
  0    Tom   20
  1   nick   21
  2  krish   19
  3   jack   18
```

## Pandas vs Numpy

| PANDAS                                                                                  | NUMPY                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| When we have to work on Tabular data, we prefer the pandas module.                      | When we have to work on Numerical data, we prefer the numpy module.                 |
| The powerful tools of pandas are Data frame and Series.                                 | Whereas the powerful tool of numpy is Arrays.                                       |
| Pandas consume more memory.                                                             | Numpy is memory efficient.                                                          |
| Pandas has a better performance when a number of rows is 500K or more.                  | Numpy has a better performance when number of rows is 50K or less.                  |
| Indexing of the pandas series is very slow as compared to numpy arrays.                 | Indexing of numpy Arrays is very fast.                                              |
| Pandas offer a have2d table object called DataFrame.                                    | Numpy is capable of providing multi-dimensional arrays.                             |
| It was developed by Wes McKinney and was released in 2008.                              | It was developed by Travis Oliphant and was released in 2005.                       |
| It is used in a lot of organizations like Kaidee, Trivago, Abeja Inc. , and a lot more. | It is being used in organizations like Walmart Tokopedia, Instacart, and many more. |
| It has a higher industry application.                                                   | It has a lower industry application.                                                |

# 6. Explain read_csv and read_excel functions in pandas with example.

### Read CSV in Pandas

- read_csv() is used to read Comma Separated Values (CSV) file into a pandas DataFrame.
- some of important Parameters :
```
filePath : str, path object, or file-like object

sep : separator (Default is comma)

header: Row number(s) to use as the column names.

index_col : index column(s) of the data frame.
```
#### Example of Read CSV
```python
dfINS = pd.read_csv('Marks.csv',index_col=0,header=0)

print(dfINS)
```

```python
PDS Algo SE INS
101 50 55 60 55.0
102 70 80 61 66.0
103 55 89 70 77.0
104 58 96 85 88.0
201 77 96 63 66.0
```

## Read Excel in Pandas

- The XLSX and XLS file extensions are used for Microsoft Excel spreadsheets
- Read an Excel file into a pandas DataFrame.
- Supports xls, xlsx, xlsm, xlsb, odf, ods and odt file extensions read from a local filesystem or URL. Supports an option to read a single sheet or a list of sheets.
- some of important Parameters :
```
excelFile : str, bytes, ExcelFile, xlrd.Book, path object, or file-like object

sheet_name : sheet no in integer or the name of the sheet, can have list of sheets.

index_col : index column of the data frame.
```
#### Example of Read Excel
```python
file = 'records.xlsx'

sheet1 = pds.read_excel(file, 
                        sheet_name = 'student',
                        index_col = 0)
  
sheet2 = pds.read_excel(file, 
                        sheet_name = 'teacher',
                        index_col = 0)
  
newData = pds.concat([sheet1, sheet2])

print(newData)
```

###### output :
<img src="https://media.geeksforgeeks.org/wp-content/uploads/20200211145643/output219.png" width=10%>

# 7. Explain Web Scrapping with Example using Beautiful Soup library.

### Web Scraping:
- In simple terms, Web scraping, web harvesting, or web data extraction is an automated process of collecting large data(unstructured) from websites.
- The user can extract all the data on particular sites or the specific data as per the requirement.
- The data collected can be stored in a structured format for further analysis.

### Uses of Web Scraping:
- Social Media Sentiment Analysis
- Lead Generation in Marketing Domain
- Market Analysis, Online Price Comparison in eCommerce Domain
- Collect train and test data in Machine Learning Applications

### Steps involved in web scraping:

1. Find the URL of the webpage that you want to scrape
2. Select the particular elements by inspecting
3. Write the code to get the content of the selected elements
4. Store the data in the required format

### BeautifulSoup 
- Python library for getting data out of HTML, XML, and other markup languages.
- Beautiful Soup is a library that makes it easy to scrape information from web pages.


### Example

```python
import requests
import bs4

req = requests.get('https://www.darshan.ac.in/DIET/CE/Faculty')
soup = bs4.BeautifulSoup(req.text,'lxml')
allFaculty = soup.select('body > main > section:nth-child(5) > div > div > div.col-lg-8.col-xl-9
> div > div')

for fac in allFaculty :
  allSpans = fac.select('h2>a')
  print(allSpans[0].text.strip())
```

##### Output:

```
Dr. Gopi Sanghani
Dr. Nilesh Gambhava
Dr. Pradyumansinh Jadeja
Prof. Hardik Dosh
Prof. Maulik Trivedi
Prof. Dixita Kagathara
```

# 8. Explain Bag of Word model.

<a href="https://ibb.co/DM03gxr"><img src="https://i.ibb.co/DM03gxr/bOw.png" alt="bOw" border="0"></a>

# 9. Explain join and merge functions in pandas with example.

- **The main difference between join vs merge would be; join() is used to combine two DataFrames on the index but not on columns whereas merge() is primarily used to specify the columns you wanted to join on, this also supports joining on indexes and combination of index and columns.**

### Join in Pandas

- df.join() method will efficiently join multiple DataFrame objects by index(or column specified) .

- Join columns of another DataFrame.

- some of important Parameters :
```
dfOther : Right Data Frame

on (Not recommended) : specify the column on which we want to join (Default is index)

how : How to handle the operation of the two objects.

left: use calling frame’s index (Default).

right: use dfOther index.

outer: form union of calling frame’s index with other’s index (or column if on is specified), and sort it.lexicographically.

inner: form intersection of calling frame’s index (or column if on is specified) with other’s index, preserving the order
of the calling’s one.
```
```python
# importing pandas module
import pandas as pd 
  
# Define a dictionary containing employee data 
data1 = {'Name':['Jai', 'Princi', 'Gaurav', 'Anuj'], 
        'Age':[27, 24, 22, 32]} 
    
# Define a dictionary containing employee data 
data2 = {'Address':['Allahabad', 'Kannuaj', 'Allahabad', 'Kannuaj'], 
        'Qualification':['MCA', 'Phd', 'Bcom', 'B.hons']} 
  
# Convert the dictionary into DataFrame  
df1 = pd.DataFrame(data1, index=['K0', 'K1', 'K2', 'K3'])
  
# Convert the dictionary into DataFrame  
df2 = pd.DataFrame(data2, index=['K0', 'K2', 'K3', 'K4'])
 
# joining dataframe
res = df1.join(df2)


print(df1)
print(df2) 
print(res)

```
- Output :
<img src="https://media.geeksforgeeks.org/wp-content/uploads/finaljoin11.jpg">

### Merge in Pandas

- Merge DataFrame or named Series objects with a database-style join.
- Similar to join method, but used when we want to join/merge with the columns instead of index.
- some of important Parameters :
```
dfOther : Right Data Frame

on : specify the column on which we want to join (Default is index)

left_on : specify the column of left Dataframe

right_on : specify the column of right Dataframe

how : How to handle the operation of the two objects.

left: use calling frame’s index (Default).

right: use dfOther index.

outer: form union of calling frame’s index with other’s index (or column if on is specified), and sort it.
lexicographically.

inner: form intersection of calling frame’s index (or column if on is specified) with other’s index, preserving the order
of the calling’s one.
```

```python
# importing pandas module
import pandas as pd 
 
# Define a dictionary containing employee data 
data1 = {'key': ['K0', 'K1', 'K2', 'K3'],
         'Name':['Jai', 'Princi', 'Gaurav', 'Anuj'], 
        'Age':[27, 24, 22, 32],} 
   
# Define a dictionary containing employee data 
data2 = {'key': ['K0', 'K1', 'K2', 'K3'],
         'Address':['Nagpur', 'Kanpur', 'Allahabad', 'Kannuaj'], 
        'Qualification':['Btech', 'B.A', 'Bcom', 'B.hons']} 
 
# Convert the dictionary into DataFrame  
df1 = pd.DataFrame(data1)
 
# Convert the dictionary into DataFrame  
df2 = pd.DataFrame(data2) 
  
 
# using .merge() function
res = pd.merge(df1, df2, on='key')
 
print(df1)
print(df2) 
print(res)
```
- output :
<img src="https://media.geeksforgeeks.org/wp-content/uploads/abhifinal.jpg">

# 10. Explain how to deal with missing data in Pandas.

- There are many methods by which we can deal with the missing data, some of most commons are listed below,

1. dropna, will drop (delete) the missing data (rows/cols)
2. fillna, will fill specified values in place of missing data
3. interpolate, will interpolate missing data and fill interpolated value in place of missing data.

```python
# Remove all rows with NULL values

import pandas as pd
df = pd.read_csv('data.csv')
df.dropna(inplace = True)
```

```python
# Replace NULL values with the number 130

import pandas as pd
df = pd.read_csv('data.csv')
df.fillna(130, inplace = True)
```

```python
# Replace NULL values with the number between the previous and next row

import pandas as pd
df = pd.read_csv('data.csv')
newdf = df.interpolate(method='linear', inplace = True))
```

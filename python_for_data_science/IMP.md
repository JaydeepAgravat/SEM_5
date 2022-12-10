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

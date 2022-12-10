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





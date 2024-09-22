Let's start with reading external files. Let’s say you have a CSV file named _favorite_colors.csv_ that looks like the following:

name; occupation; favorite_color  
Jacob Smith; Software Engineer; Purple  
Nora Scheffer; Digital Strategist; Blue  
Emily Adams; Marketing Manager; Orange

```python
>>> import csv
>>>
>>> with open('favorite_colors.csv') as file:
...     reader = csv.reader(file, delimiter=';')
...     for row in reader:
...             print(row)
['ï»¿name', 'occupation', 'favorite_color']
['Jacob Smith', 'Software Engineer', 'Purple']
['Nora Scheffer', 'Digital Strategist', 'Blue']
['Emily Adams', 'Marketing Manager', 'Orange']
```

######  'ï»¿name'   ????????????

A more useful method for reading CSVs while recognizing headers to identify the columns is the  `DictReader()`  method. This method knows the first line is a header and saves the rest of the rows as **dictionaries** with each key as the column name and the value as the column value.


```python
>>> import csv
>>>
>>> with open('favorite_colors.csv') as file:
...     reader = csv.DictReader(file, delimiter=',')
...     for row in reader:
...         print(row['ï»¿name'] + " works as a " + row['occupation'] + " and their favorite color is " + row['favorite_color'])
...
Jacob Smith works as a Software Engineer and their favorite color is Purple
Nora Scheffer works as a Digital Strategist and their favorite color is Blue
Emily Adams works as a Marketing Manager and their favorite color is Orange
>>>
```



To see files in directory under PYTHON :

```python
>>> import os
>>> os.listdir()
['.git', 'favorite_colors.csv']
>>>
```



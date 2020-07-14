---
layout: post
title: Python Notes
categories: notes python
last_modified_at: 2019-07-14 11:19:55
---

Notes on Python as I learn and improve my understanding.

## Differences

Any String is by default a list of characters.


##Data Structures

Python's in built data sets are list, dict and sets.


```python

list = [1,2,3,'hi',[2,3,4]]
# mix data type list
# list is collection of objects

dictionary = {'k1':'v1' , 'k2':'v2'}
# Key value pair

tuple = (1,2,3)
# tuples are fixed values and cannot be assigned

set = {1,2,3,1,2,1,2,1,2,1,2,1,3}
# set can have only unique values
# for above result is only 1,2,3

```

All above can be accessed using [] and index.
index from 0 and end not included
[0:3] gives 0,1,2 and not 3

[0:-2] all but last two.

**List Comprehension**

Defines list in one line, for eg, to find squares

`sqr = [x**2 for x in range(5)]`

This gives list with squares of numbers 0 to 4

## Functions

Can have defaults

```python
def my_square(num):
  """
  This is DocString
  Can be multiline
  THis func squares a number
  """
  return num**2
```

### Map and Filter

Map is used to apply a function to a list.

```python
seq = [1,2,3,4,5]
map(my_square,seq)
```

It computes my_square for all items in seq.

**Lambda**

This is used to define a function in a line.

`lambda num: num*2`

That means passing variable : return statement.

Useful for use in map.

#### Filters

Filter is used to filter items in seq based on function/lambda

eg: to get even values

`filter(lambda num: num%2 == 0,seq)`

## Web Dev Libs
Flask
- light weight web framework
- FlaskRESTful - extention for REST framework

sqlite3
- store to local db

Shelve
- Persistant object storage library

Pickle
- Dump objects to file and load back

Pandas
- Data maipulation
- Pandas vs Dask vs Spark
  - less than a gb, use pandas
  - upto 100 gb, use pandas with chunk or dask or pyspark
  - more than 100gb, pyspark for sure, upto peta bytes
  - [Pandas, Dask or PySpark - Medium](https://medium.com/datadriveninvestor/pandas-dask-or-pyspark-what-should-you-choose-for-your-dataset-c0f67e1b1d36)
- Superfast Pandas, make data transformation in pandas upto 7237 times faster:
  - use iterrow
  - use apply(lambda)
  - use pandas vectorization, loc(filters here)
  - use numpy vectorization, pass as numpy.array, converts to C code.
  - [Making pandas loop faster](https://towardsdatascience.com/how-to-make-your-pandas-loop-71-803-times-faster-805030df4f06)


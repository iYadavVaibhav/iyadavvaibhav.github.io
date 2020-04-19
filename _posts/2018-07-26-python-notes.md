---
layout: post
title: Python Notes
categories: notes python
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

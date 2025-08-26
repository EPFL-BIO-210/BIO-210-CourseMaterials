# Python Introduction I

## Python's core built-in objects

|     |     |
| --- | --- |
| Object type: | Examples: |
| *Numbers* | 123, 3.14, math.pi, ... |
| *Strings* | 'abc', 'EPFL', "Geneva", ... |
| *Lists* | [1, [2, 'troi'],4], list(range(99) |
| Dictionaries | {'Apples': 200, 'Pears': 123.5}, dict(hours=10) |
| Tuples | (x,y,z), (1, [2, 'troi'],4) |
| Sets | set('abc'), {'E','P','F','L'} |
| Other core types | Booleans, types, None |
| Files | open('data.txt'), open(r('/home/alex/abc.bin'),'wb')
| Program unit types | Functions, modules, classes |

For more details check out the [Python docs!](https://docs.python.org/3/library/stdtypes.html#)

Here, we briefly summarize Numbers, Strings, Lists and Dictionaries.

## Numbers in Python

Python's core objects include integers, floating-point, complex numbers, etc.

Types of numbers:
- `int` represents integers, e.g. `2`, `14213555`
- `float` represents reals, e.g. `pi`, `1.0`, `0.000001`
- `complex` represents complex numbeers, e.g. real + imaginary
- `bool` represents Boolean values, `True` and `False`
- `type()` returns the type of Python objects

```python
>>> type(5)           # again, ```>>>```m denotes what you type in a Python shell
int                   # here is the output!
>>> type(3.0)
float
>>> type(True)
bool
>>> complex(1,1)      # define a complex number
(1+1j)                # evaluates to this!
>>> complex(0,1)**2	  # remember: sqrt(-1) = j
(-1,0j)
>>> type(complex(1,1))
complex
```

## Strings

- strings are concatenations of letters, special characters, numbers, and spaces
- they are case sensitive!
- strings can be *defined* by enclosing in quotation marks (") or single quotes (').

Examples:

```python
>>> S = 'Geneva'      # make a 6-character string and assign it to a name
>>> S = "Lausanne"    # make a 8-character string and assign it to a name
>>> S = str(3)        # cast integer 3 to string and assign to name
>>> type(S)
str
```

## Lists

- ordered sequences of objects
- accessible by index
- have no *fixed size* and are very flexible
- a list is denoted by *square brackets* []


Three examples:
```python
list1=[0,1,2,3]
list2=[0,'abc']                               # lists can have mixed types; here int + str
list3=['EPFL','is','in',['Lausanne','VD']]    # they support arbitrary nesting
```

## Dictionaries

Dictionaries are
- collections of key-value pairs that maps from keys to values.
- the keys can be any immutable type, and the values can be any type.
- like lists they can also be mixed and nested
- a dict is denoted by *curly brackets* {}

An example:

```python
inventory = {'Apples': 200, 'Pears': 123.5}
```

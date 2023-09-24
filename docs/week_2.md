# Python Introduction II

## Tuples

- ordered sequences of objects that *cannot* be changed (immutable)
```python
>>> T = (0,1,2,3)     # a 4-item tuple
>>> len(T)
4
>>> T + (5,6)         # concatenation
(0,1,2,3,5,6)
>>> T[0]              # slicing
0
>>> T[0]=3
... error ...
TypeError: 'tuple' object does not support item assignment
```

Why tuples? Their immutability is the point; they are used for control...

```python
>>> x, y = 3, 4       # here we define two variables in one line
>>> print(x,y)
(3,4)
>>> (x,y) = (y,x)     # convenient way to swap values!
>>> print(x,y)
(4,3)
```

## Sets

- unordered collection of unique and immutable objects

Example definitions and operations:
```python {1-3|1-8|1-11}
>>> x = set('abcde')
>>> y = set('bdxyz')
>>> print(x)
{'c', 'e', 'd', 'a', 'b'}
>>> x - y               # difference set
{'a', 'c', 'e'}
>>> x | y               # union
{'a', 'b', 'c', 'd', 'e', 'x', 'y', 'z'}
>>> 'a' in x            # membership in sets
True
```

## Control flow: If variants

```python
if <condition>:   # else is not required!
  <expression>
  <expression>
  ...
```
```python
if <condition>:
  <expression>
  <expression>
  ...
else:
  <expression>
  <expression>
  ...
```


```python
if <condition>:
  <expression>
  <expression>
  ...
elif <condition>:
  <expression>
  <expression>
  ...
elif ...: # as many else if as you want!
  <expression>
  <expression>
  ...
else:
  <expression>
  <expression>
  ...
```


## Control flow: while statements

```python
while <condition>:    # while condition is true, carry out indented expr.; then expr._post
    <expression>
    <expression>
    ...

<expression_post>
```

<!--
This code will:
- Check `condition`, if true:
- If True, run all `expressions` inside the code block
- Check `condition` again and
- repeat until `condition` is False, then it runs `expression_post`
-->
---

## Additional control: break statements

- immediately exits the *current* loop
- thus, skips remaining expressions in this loop

```python
while <condition>:
    <expression>
    if <condition>:
      break           # exits while loop!
    <expression>
    ...

<expression_post>
```

## NumPy: Python's foundation of scientific computing

[NumPy](https://numpy.org/doc/stable/user/whatisnumpy.html) is a fundamental package that
- provides multidimensional array objects (e.g. matrix of shape (M x N), but also vectors of shape (N) and tensors of shape (M_1 x M_2 x M_3 ... x M_N))
- with various derived objects and powerful mathematical functions

Numpy arrays, the ndarray object:
- NumPy arrays have a fixed size at creation, unlike Python lists (which can grow dynamically).
- changing the size of an ndarray will create a new array and delete the original.
- arrays can have any dimensionality
- arrays contain numbers of the *same* type (e.g. floats, complex numbers, booleans)
- arrays are sequential objects and can be indexed by the `[]` operator

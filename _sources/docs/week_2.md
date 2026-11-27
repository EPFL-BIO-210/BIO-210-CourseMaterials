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

## Slicing

- Slicing means getting a subset of ordered objects such as lists, tuples, Numpy arrays, ...
- Slicing syntax is as follow: `[start:stop:step]`
- If the object has more than one dimension, the syntax gets repeated for all dimensions separated with `,` (For example, for 2D Numpy arrays the syntax is `[start:stop:step, start:stop:step]` )
- If `start` is not specified, it means from index 0 (first element)
- if `stop` is not specified, it means until the last element
- if `step` is not specified, it means `step=1`
- Here are some examples of slicing:

```python
>>> x = [0,1,2,3]     # a 4-item list
>>> x[0:2]              # slicing to get the first two elements
[0,1]
>>> x[:2]               # if we do not specify the start, it is considered 0
[0,1]
>>> x[0:4:2]               # start=0, stop=4, step=2
[0,2]
>>> x[::2]               # start=0, stop=4, step=2 (same as previous line)
[0,2]
>>> x[::-1]               # start=0, stop=4, step=-1 (negative steps reverse the order of object)
[3, 2, 1, 0]
```

- Here are some examples with Numpy arrays:

```python
>>> x = np.array(
		[[0, 1, 2],
                  [3, 4, 5],
                  [6, 7, 8]])

>>> x[0:2, :]        # for rows: start=0, stop=2, step=1 (i.e. first two rows)
array([[0, 1, 2],   #  for columns: start=0, stop=3, step=1 (i.e. all columns)
       [3, 4, 5]])

>>> x[:,1:]          # for rows: start=0, stop=3, step=1 (i.e. all the rows)
array([[1, 2],       # for columns: start=1, stop=3. step=1 (i.e. column 1 to the end)
       [4, 5],
       [7, 8]])

>>> x[::2,::-1]     # for rows: start=0, stop=3, step=2 (i.e. every second row)
array([[2, 1, 0],   # for columns: start=0, stop=3, step=-1 (i.e. reverse the columns)
       [8, 7, 6]])
```

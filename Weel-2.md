# Week - 1

## Resource

### Video

- Lecture 3: https://www.youtube.com/watch?v=gcg6A9HgiPo&list=PL6BsET-8jgYWmbUDWrNaHgWZ6TUElKBW0&vq=hd1080
- Lecture 4: https://www.youtube.com/watch?v=tQR5ejQWuis&list=PL6BsET-8jgYVcca9trmJVoPpqgd1b3sO-&vq=hd1080
- Lecture 5: https://www.youtube.com/watch?v=Dk1GgPrLYyM&list=PL6BsET-8jgYU9mRSxd06NZTQrBBDDmMAT&vq=hd1080

### Reading

- [1.5 Control](https://composingprograms.com/pages/15-control.html)
- [1.6 Higher-Order Functions](https://composingprograms.com/pages/16-higher-order-functions.html)



## Notes



To evaluate the expression `<left> and <right>`:

1. Evaluate the subexpression `<left>`.
2. If the result is a false value `v`, then the expression evaluates to `v`.
3. Otherwise, the expression evaluates to the value of the subexpression `<right>`.

To evaluate the expression `<left> or <right>`:

1. Evaluate the subexpression `<left>`.
2. If the result is a true value `v`, then the expression evaluates to `v`.
3. Otherwise, the expression evaluates to the value of the subexpression `<right>`.

To evaluate the expression `not <exp>`:

1. Evaluate `<exp>`; The value is `True` if the result is a false value, and `False` otherwise.





##  High-Order Function Design 高阶函数



![image-20190703132022986](http://ww4.sinaimg.cn/large/006tNc79ly1g4mkxhczixj316e0p447m.jpg)

Don't repeat your self

```python
def area(r, shape_const):
    assert r > 0, 'length must bigger than 0'
    return r * r * shape_const

def area_circle(r):
    return area(r, pi)

def area_sqaure(r):
    return area(r, 1)

```



Function as argument

```python
# coding: utf-8 

# Run: python3 -m doctest -v summation.py

def summation(n, term):
    """ Sum the first N terms of a sequence
    """
    total, k = 0, 1
    while k <= n:
        total, k = total + term(k), k + 1
    return total

def sum_naturals(n):
    """ Sum the first N natural numbers

    >>> sum_naturals(5)
    15
    """
    return summation(n, lambda x: x)

def sum_cubes(n):
    """ Sum the first N cubes of natural numbers
    
    >>> sum_cube(5)
    225
    """
    return summation(n, lambda x: pow(x, 3))
```

Function as a return value



```python
# coding: utf-8

def make_adder(n):
    """ Return a function that takes one arg K, return K + n

    >>> three_adder = make_adder(3)
    >>> three_adder(4)
    7
    """
    def adder(k):
        return k + n
    return adder

```


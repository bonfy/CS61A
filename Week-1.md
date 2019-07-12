# Week - 1

##	Resource

### Video

* Lecture 1: https://www.youtube.com/watch?v=pIbldGLvZi8&index=1&list=PL6BsET-8jgYWAxSjQsIHKdks2Jl1TD1W0&vq=hd1080

* Lecture 2: https://www.youtube.com/watch?v=I5mJCLY_WPk&list=PL6BsET-8jgYUiEvuczkTLyeOyxyjYbt8I&vq=hd1080

### Reading

* [1.1 Getting Started](https://composingprograms.com/pages/11-getting-started.html)

* [1.2 Elements of Programming](https://composingprograms.com/pages/12-elements-of-programming.html)

* [1.3 Defining New Functions](https://composingprograms.com/pages/13-defining-new-functions.html)

* [1.4 Designing Functions](https://composingprograms.com/pages/14-designing-functions.html)

## Notes

### Statements & Expressions 声明 和 表达式

> Python code consists of expressions and statements

Broadly, computer programs consist of instructions to either

1. Compute some value
2. Carry out some action

Statements typically describe actions. When the Python interpreter executes a statement, it carries out the corresponding action. On the other hand, expressions typically describe computations. 

### Fuctions

Expression -> Function

**All expressions can use function call notation**

所有的表达式 都可以用 function 表示

```Python
>>> 100 + 5
105
>>> 2 * 3
6

>>> from operator import add, mul
>>> add(100, 5)
105
>>> mul(2,3)
6

# multi value
>>> max(1, 2, 3, 4, 5)

# Nesting
>>> mul(add(1, 2), 5)
```



### Objects

A `set` is a type of object, one that supports set operations like computing intersections and membership. 

### Interpreters(解释程序)

Evaluating compound expressions requires a precise procedure that interprets code in a predictable way. A program that implements such a procedure, evaluating compound expressions, is called an interpreter. 

## Errors



The fundamental equation of computers is:

```
computer = powerful + stupid
```

Learning to interpret errors and diagnose the cause of unexpected errors is called ***debugging***. Some guiding principles of debugging are:

* **Test incrementally**
* **Isolate errors**
* **Check your assumptions**
* **Consult others**



### Elements of Progrramming

> A programming language is more than just a means for instructing a computer to perform tasks. The language also serves as a framework within which we organize our ideas about computational processes. Programs serve to communicate those ideas among the members of a programming community. Thus, programs must be written for people to read, and only incidentally for machines to execute.

总结一下就是: 程序首先是写给人看的（把自己的想法与社区交流），机器能执行只是附带的



In programming, we deal with two kinds of elements: functions and data.



*expression*, which applies a function to some arguments.



There is no limit (in principle) to the depth of such nesting and to the overall complexity of the expressions that the Python interpreter can evaluate. However, humans quickly get confused by multi-level nesting. An important role for you as a programmer is to structure expressions so that they remain interpretable by yourself, your programming partners, and other people who may read your expressions in the future.



## Names and Environment

A critical aspect of a programming language is the means it provides for using names to refer to computational objects

 `=` symbol is called the *assignment* operator in Python (and many other languages). Assignment is our simplest means of *abstraction*



Environment： The possibility of binding names to values and later retrieving those values by name means that the interpreter must maintain some sort of memory that keeps track of the names, values, and bindings. This memory is called an *environment*.

```python
>>> a = 1
>>> b = 2
>>> b, a = a + b, b
result: b = 3  a = 2
```

说明： Python 的赋值 是 先全部计算右边，然后再逐个绑定左边 

右边 3 ， 2， 所以 b=3， a=2



抽象：Assignment & Function

Assignment： simple ， bind names to values

Function: more powerful, bind names to expressions 



![image-20190628162018812](http://ww3.sinaimg.cn/large/006tNc79ly1g4gy15k7zgj31ed0u0agi.jpg)

![image-20190701104754849](http://ww3.sinaimg.cn/large/006tNc79ly1g4k5a82hnrj30um0fvmzp.jpg)



**Name Evaluation.** A name evaluates to the value bound to that name in the earliest frame of the current environment in which that name is found.



![image-20190701152359414](http://ww3.sinaimg.cn/large/006tNc79ly1g4kd9de4aej30vh0hvac4.jpg)


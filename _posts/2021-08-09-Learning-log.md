---
title: "Learning Log"
categories:
  - Learning
tags:
  - Daily
---

This post/page is a log of little things I learn on a daily basis

11th August 2021

Statically typed languages:
    For statically typed languages, the type has to be declared while writing the program. Thus the type is know at compile time.
This enables the compiler to generate optimized machine code for the type(less memory) and types don't have to be checked at run-time(faster program)

Dynamically Typed Languages:
    The variable is sort of like a pointer. The variable is bound to object at runtime. Same varible can bind to object of different types.
Dynamic Typic is slow. It helps in implementing other features though.

Strongly Typed Language:
    In evaluation of expressions, error occurs if different types are used, as variables are bound to specific data types. 
Example in Python: cannot add a string and integer

Weakly Typed language: 
    In evaluation of expression, error does not occur if incompatible types are used. 
Example in C: we can add a string to integer


Cython:
Python being dynamically typed, it is very slow - coz types of all the variables are checked at runtime(also GIL, etc.)
To circumvent this, Cython is used. 
Cython is a compiler which works on a language which is superset of Python (Python + additional functionality for C language speeding)
Cython takes in .pyx files - which are very similar to python plus type information and other changes and generates a shared library ".so" file from a .c file(which is also generated)
The shared library contains the python code "translated" to C. It provides the python API which can directly be used.

Interpretor: 
A program which emulates a computer. It coverts compiled code to machine code, thereby making the compiled code platform independent.  

Cython vs CPython:
Cython is a Python Interpretor. It takes python compiled code (.pyc files) and turns them into machine code
CPython is language which has Python as a subset. Cython compiler can compile both python and cython


Introspection: The ability to inspect the code at runtime and see object types 
Reflection: The ability to make modifications(dynamically call classes, methods, attributes, etc. ) at runtime using introspection without knowing the names at compile time
            It allows instantiation of new objects and invocation of methods


timeit:
Python package to accurate measure time taken for implementing a function by running it multiple times
timeit.timeit('''example_original.test(5)''',setup='import example_original', number=100)

References: 
Static vs Dynamic Typing: https://medium.com/android-news/magic-lies-here-statically-typed-vs-dynamically-typed-languages-d151c7f95e2b
Cython: https://www.youtube.com/watch?v=mXuEoqK4bEc&t=25s
Reflection and Introspection in Python : https://betterprogramming.pub/python-reflection-and-introspection-97b348be54d8
Very GOOD: Python Interpretor: https://www.aosabook.org/en/500L/a-python-interpreter-written-in-python.html
Python Interpreter makes .pyc files platform independent(for a given python version): https://stackoverflow.com/questions/30443490/is-pyc-platform-independent
#https://hackernoon.com/i-finally-understand-static-vs-dynamic-typing-and-you-will-too-ad0c2bd0acc7



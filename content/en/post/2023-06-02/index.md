---
title: Decorator Factory in Python
description: >-
  When studying the open source project ‘langchain’, I came across an intriguing
  function: xor_args(), found in the file…
date: "2023-06-02T13:39:06.140Z"
categories: []
keywords: []
featured_image: "neom.jpg"
omit_header_text: true
slug: /@pengbintech/decorator-factory-in-python-1fe94162a37a
---

When studying the open source project ‘langchain’, I came across an intriguing function: _xor_args()_, found in the file ‘_langchain/utils.py_’. This function is an example of a Decorator Factory, a more advanced concept in Python.

```
def xor\_args(\*arg\_groups: Tuple\[str, ...\]) -> Callable:
    """Validate specified keyword args are mutually exclusive."""

    def decorator(func: Callable) -> Callable:
        def wrapper(\*args: Any, \*\*kwargs: Any) -> Callable:
            """Validate exactly one arg in each group is not None."""
            counts = \[
                sum(1 for arg in arg\_group if kwargs.get(arg) is not None)
                for arg\_group in arg\_groups
            \]
            invalid\_groups = \[i for i, count in enumerate(counts) if count != 1\]
            if invalid\_groups:
                invalid\_group\_names = \[", ".join(arg\_groups\[i\]) for i in invalid\_groups\]
                raise ValueError(
                    "Exactly one argument in each of the following"
                    " groups must be defined:"
                    f" {', '.join(invalid\_group\_names)}"
                )
            return func(\*args, \*\*kwargs)

        return wrapper

    return decorator
```

Firstly, let’s understand what a Decorator is in Python. A decorator is a function that modifies or enhances the behavior of another function. For instance, consider this example:

```
@uppercase
def say_hello():
 return "Hello World!"
```

Here, @uppercase is a decorator which alters the function ‘_say_hello()_’, resulting in the string “HELLO WORLD!”. This decorator is implemented via an enclosed wrapper function as shown below:

```
def uppercase(function):
 def wrapper():
 func = function()
 string_uppercase = func.upper()
 return string_uppercase
 return wrapper
```

However, this decorator has a limitation: it doesn't allow passing parameters into the decorated function. This is where Decorator Factories come in.

A Decorator Factory differs from a decorator in that it returns a decorator, not just a function. Let’s modify the ‘_uppercase_’ decorator to accept parameters:

```
def uppercase(username):
 def decorating(fn):
 def wrapper():
 func = function()
 string_uppercase = func.upper()
 return f"{string_uppercase}, {username}"
 return wrapper
 return decorating
```

Applying the decorator factory to ‘_say_hello()_’ would look like this.

```
@uppercase("David")
def say_hello():
 return "Hello World!"
```

The function ‘_say_hello()_’ will now return the string “HELLO WORLD! David”.

Having understood the Decorator Factory in Python, let’s now revisit the function ‘_xor_args()_’.

1.  `xor_args(*arg_groups: Tuple[str, ...]) -> Callable:` - This is the definition of the decorator factory function `xor_args`. It takes one or more tuples of strings as its input arguments. Each tuple represents a group of keyword arguments.
2.  `def decorator(func: Callable) -> Callable:` - This is the definition of the decorator. It will take a function `func` as input.
3.  `def wrapper(*args: Any, **kwargs: Any) -> Callable:` - This is the definition of a wrapper function inside the decorator. This function will replace or wrap the original function `func`.
4.  In the `wrapper` function, it checks whether exactly one argument in each group is not `None`. The `counts` list contains the number of non-None arguments in each group, computed by the list comprehension and the `sum` function.
5.  If there is a group where not exactly one argument is non-None, it raises a `ValueError` with a message indicating which groups are invalid.
6.  If there is no invalid group, it calls the original function `func` with the provided arguments and keyword arguments and returns the result.

By using this Decorator Factory, we can easily enforce complex conditions on the arguments of a function, ensuring that our code is both efficient and easy to read.

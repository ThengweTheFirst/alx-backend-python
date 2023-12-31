# Asynchronous Comprehensions and Generators

This repository contains Python code that demonstrates the use of asynchronous comprehensions and generators. It includes implementations of various tasks that showcase the usage and benefits of these concepts.

## Learning Objectives

By the end of this project, you will be able to explain the following topics without the help of Google:

- How to write an asynchronous generator
- How to use async comprehensions
- How to type-annotate generators

## Requirements

### General

- Allowed editors: vi, vim, emacs
- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using Python 3 (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly `#!/usr/bin/env python3`
- A `README.md` file, at the root of the folder of the project, is mandatory
- Your code should use the pycodestyle style (version 2.5.x)
- The length of your files will be tested using `wc`
- All your modules should have a documentation (`python3 -c 'print(__import__("my_module").__doc__)'`)
- All your functions should have a documentation (`python3 -c 'print(__import__("my_module").my_function.__doc__)'`)
- A documentation is not a simple word, it’s a real sentence explaining the purpose of the module, class, or method (the length of it will be verified)
- All your functions and coroutines must be type-annotated.

## Resources

Read or watch the following resources:

- [PEP 530 – Asynchronous Comprehensions](https://www.python.org/dev/peps/pep-0530/)
- [What’s New in Python: Asynchronous Comprehensions / Generators](https://docs.python.org/3/whatsnew/3.6.html#whatsnew36-pep525)
- [Type-hints for generators](https://docs.python.org/3/library/typing.html#typing.Generator)

## Tasks

### 0. Async Generator

Write a coroutine called `async_generator` that takes no arguments.

The coroutine will loop 10 times, each time asynchronously wait for 1 second, then yield a random number between 0 and 10. The `random` module should be used for generating random numbers.

Example usage:

```python
import asyncio

async_generator = __import__('0-async_generator').async_generator

async def print_yielded_values():
    result = []
    async for i in async_generator():
        result.append(i)
    print(result)

asyncio.run(print_yielded_values())
```

### 1. Async Comprehensions

Import `async_generator` from the previous task and write a coroutine called `async_comprehension` that takes no arguments.

The coroutine will collect 10 random numbers using an asynchronous comprehension over `async_generator`, and then return the 10 random numbers.

Example usage:

```python
import asyncio

async_comprehension = __import__('1-async_comprehension').async_comprehension

async def main():
    print(await async_comprehension())

asyncio.run(main())
```

### 2. Run time for four parallel comprehensions

Import `async_comprehension` from the previous file and write a `measure_runtime` coroutine that will execute `async_comprehension` four times in parallel using `asyncio.gather`.

The `measure_runtime` coroutine should measure the total runtime and return it.

Example usage:

```python
import asyncio

measure_runtime = __import__('2-measure_runtime').measure_runtime

async def main():
    return await measure_runtime()

print(asyncio.run(main()))
```

## Repository

- GitHub repository: [alx-backend-python](https://github.com/ThengweTheFirst/alx-backend-python)
- Directory: 0x02-python_async_comprehension

## Contact

For any questions, concerns, or feedback, please feel free to reach out:

- Name: [Mzwandile Sithebe]
- GitHub: [https://github.com/ThengweTheFirst/]
- Email: [sithebemzwandie40@gmail.com]

Thank you for visiting this repository!

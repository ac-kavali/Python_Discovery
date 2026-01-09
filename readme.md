# Python Programming Language

Python is a popular, high-level, general-purpose programming language known for its clear, **easy-to-read syntax** that often uses English-like words.

## **<span class="color-yellow">Scripted Language</span>**

This means it is a language that is generally **<span class="color-green">interpreted rather than compiled</span>**.

- **<span class="color-cyan">Interpreted</span>:** Python code is executed by the Python interpreter (`python filename.py`) rather than being compiled into machine code first.
- **<span class="color-cyan">High-level and dynamic</span>:** You can write small scripts to automate tasks, manipulate files, work with databases, etc., quickly.
- **<span class="color-cyan">Cross-platform</span>:** You can run Python scripts on almost any OS without worrying about compilation.

## <span class="color-blue">What "interpreted" means</span>

When we say Python is interpreted, we're referring to how your code gets executed. The Python interpreter (whether you invoke it as `python` or `python3`) reads your source code and executes it line by line or statement by statement, translating it into instructions the computer can understand on the fly.

### What is a Program?

Before diving deeper, let's clarify what a **program** actually is:

> **A program is a set of instructions that are loaded into RAM (Random Access Memory) when they are being executed.**

When you run a program:
1. The operating system loads the program's instructions from storage (like your hard drive or SSD) into RAM
2. The CPU (Central Processing Unit) then fetches these instructions from RAM and executes them
3. RAM provides fast, temporary storage that allows the CPU to quickly access the instructions and data it needs

Both `python` and `python3` are themselves programs - they are executable files that contain instructions for interpreting and running your Python code. When you execute `python script.py`, the Python interpreter program is loaded into RAM, and it then reads your `script.py` file and executes your Python code.

### Python Virtual Machine
The Pvm resposible to decode the Bytecode at run time and execute it instruction by instruction.
PVM code is written by c.

### Byte Code
In Python, bytecode is a low-level set of instructions that is portable across different platforms, which means it can be executed on any machine that has a compatible CPython interpreter.

### The Interpretation Process

Here's what happens when you run a Python script:

1. **You invoke the interpreter**: You type `python filename.py` in your terminal
2. **The interpreter program loads**: The Python interpreter itself (the program) is loaded into RAM
3. **Source code is read**: The interpreter reads your `.py` file (plain text source code)
4. **Bytecode compilation**: Python compiles your source code into bytecode (an intermediate representation stored in `.pyc` files)
5. **Execution**: The Python Virtual Machine (PVM) executes the bytecode instructions one by one
6. **Output**: Results are displayed or actions are performed

This differs from compiled languages like C or C++, where:
1. You write source code
2. A compiler translates the entire program into machine code before execution
3. The resulting executable file runs directly on your hardware

### Advantages of Interpreted Languages

- **Rapid development**: Write code and run it immediately without a compilation step
- **Easier debugging**: Errors are caught and reported as the code runs
- **Portability**: The same Python source code can run on different platforms as long as a Python interpreter is available
- **Dynamic typing**: Variable types are determined at runtime, offering flexibility
- **The instructions** (operations) are already implemented and compiled inside the Python interpreter binary (written in C).

### Trade-offs

- **Performance**: Interpreted languages are generally slower than compiled languages because translation happens at runtime
- **Distribution**: To run a Python program, users need the Python interpreter installed (though tools like PyInstaller can package everything together)

## Getting Started

To start using Python:

```bash
# Check if Python is installed
python --version
# or
python3 --version

# Run a Python script
python script.py

# Start interactive Python shell
python
```

1. Python Keywords

These are reserved words in Python — you cannot use them as variable names. You will use some of these frequently:

Control flow: if, elif, else, for, while, break, continue, pass

Functions & Classes: def, return, lambda, class, yield

Error handling: try, except, finally, raise, assert

Modules & Imports: import, from, as

Variables & Scope: global, nonlocal, del

Boolean / Logic: True, False, None, and, or, not, is, in

Other structural: with, async, await

Tip: The full list of keywords can be seen with import keyword; print(keyword.kwlist)

2. Python Data Types & Structures

These are the building blocks you’ll use every day:

Numbers: int, float, complex

Boolean: bool

Strings: str — indexing, slicing, methods like .split(), .join(), .replace()

Collections:

list — mutable, ordered

tuple — immutable, ordered

set — unordered, unique elements

dict — key-value mapping, unordered

NoneType: None (often used as a default value)

3. Functions & Methods

Functions: def my_func(): ...

Lambda / anonymous functions: lambda x: x + 1

Built-in functions: print(), len(), type(), range(), enumerate(), zip()

String/list/dict/set methods — e.g., .append(), .pop(), .split(), .keys(), .values()

4. Object-Oriented Programming Concepts

Classes: class MyClass: ...

Attributes: variables inside a class, e.g., self.name

Methods: functions inside a class, e.g., def greet(self): ...

Instance / Object: obj = MyClass()

Inheritance: class Child(Parent): ...

Special methods: __init__, __str__, __repr__, __len__, __getitem__

5. Loops & Iteration

for item in iterable: ...

while condition: ...

break / continue / else in loops

range() for numeric loops

enumerate() for index + value

Iterating dictionaries: .items(), .keys(), .values()

6. Conditional Logic

if, elif, else

Comparison operators: ==, !=, <, >, <=, >=

Membership: in, not in

Identity: is, is not

Logical: and, or, not

7. Modules & Packages

Importing: import module, from module import something, import module as md

Common built-ins: os, sys, math, random, datetime, json

Third-party (pip): requests, numpy, pandas, etc.

8. File Handling

open(), .read(), .write(), .close()

with open(...) as f: for safe file handling

Reading/writing text vs binary

9. Exception Handling

try: ... except Exception as e: ... finally: ...

Raising errors: raise ValueError("message")

Assertions: assert x > 0, "x must be positive"

10. Comprehensions & Generators

List comprehension: [x*2 for x in my_list]

Dict comprehension: {k:v for k,v in my_dict.items()}

Set comprehension: {x for x in my_set}

Generator expressions: (x for x in range(10))

yield for generator functions

11. Decorators & Higher-order Functions

Passing functions as arguments

@decorator syntax

Common built-ins: map(), filter(), sorted(), reduce()

12. Misc Concepts You’ll Use Daily

Variables & assignment: x = 10

Multiple assignment: a, b = 1, 2

Type conversion: int(), float(), str(), bool()

Slicing: my_list[start:stop:step]

F-strings: f"My name is {name}"

Comments: # single line and """ multi-line """

Boolean evaluation of objects: empty list, None, 0 → False

13. Working with Paths and Files (Modern Way)

pathlib.Path - modern, object-oriented file path handling (preferred over os.path)
Path.exists(), Path.mkdir(), Path.glob(), Path.read_text(), Path.write_text()

14. String Formatting (All Methods)

F-strings: f"{variable}" (you have this)
.format(): "Hello {}".format(name) (still common in older code)
% formatting: "Hello %s" % name (legacy, but you'll see it)

15. Unpacking & Destructuring

*args and **kwargs in function definitions
Unpacking in assignments: first, *rest, last = my_list
Dictionary unpacking: {**dict1, **dict2}

16. Context Managers

with statement (you mentioned it, but expand on it)
Custom context managers using __enter__ and __exit__

17. Common Standard Library Modules (add these to #7)

collections - defaultdict, Counter, namedtuple, deque
itertools - chain, cycle, combinations, permutations
functools - partial, lru_cache, reduce
re - regular expressions
copy - copy(), deepcopy()

18. Type Hints (increasingly common)

Basic syntax: def greet(name: str) -> str:
from typing import List, Dict, Optional, Union, Tuple, Any

19. Virtual Environments

venv, virtualenv, or conda
pip install, pip freeze, requirements.txt

20. Debugging & Testing Basics

print() debugging (still useful!)
pdb - Python debugger (import pdb; pdb.set_trace() or breakpoint())
Basic testing concepts: assert, unittest, pytest

## Further Reading

- Official Python Documentation: [https://docs.python.org](https://docs.python.org)
- Python Tutorial: [https://docs.python.org/3/tutorial/](https://docs.python.org/3/tutorial/)
- Real Python Tutorials: [https://realpython.com](https://realpython.com)

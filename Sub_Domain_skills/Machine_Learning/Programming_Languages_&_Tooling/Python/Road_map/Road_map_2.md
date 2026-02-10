# 🐍 PYTHON MASTER ROADMAP (MOST DETAILED)
(Zero → Core Language → OOP → Advanced → Ecosystem → Production → Expert)

====================================================================
0) SETUP + EXECUTION MODEL (How Python actually runs)
====================================================================

- Install & Versions
  - CPython vs PyPy (what changes)
  - Python versioning (3.x)
  - PATH, python vs python3

- How Code Executes
  - Source (.py)
  - Bytecode (.pyc)
  - Python Virtual Machine (PVM)
  - Import-time execution model

- Memory & Objects (must-know foundation)
  - Everything is an object
  - References (names point to objects)
  - id(), identity vs equality
  - Mutability vs immutability
  - Reference counting + garbage collection basics
  - Shallow vs deep copy

- Environment & Dependencies
  - venv (create/activate/deactivate)  [official tutorial]
  - pip basics
  - requirements.txt
  - Why isolated environments matter  [packaging guide]

====================================================================
1) CORE SYNTAX + BASIC LANGUAGE
====================================================================

- Syntax building blocks
  - Indentation blocks
  - Statements vs expressions
  - Comments (#) + docstrings (""" """)

- Variables & Assignment
  - Assignment = binding a name
  - Multiple assignment
  - Unpacking
  - Swapping
  - Walrus operator (:=)

- Basic I/O
  - input()
  - print()
  - f-strings (format spec mini-language)
  - print: sep, end, file

- Operators
  - Arithmetic
  - Comparison
  - Logical
  - Bitwise
  - Assignment ops
  - Membership: in / not in
  - Identity: is / is not
  - Operator precedence

====================================================================
2) DATA TYPES (VERY DETAILED)
====================================================================

- NoneType
  - None vs False vs 0 vs "" (truthiness)

- Numbers
  - int (arbitrary precision)
  - float (precision + rounding issues)
  - complex
  - bool (subclass of int concept)
  - Decimal (decimal module)
  - Fraction (fractions module)

- Strings (str)
  - Unicode fundamentals
  - Indexing, slicing, step
  - Immutability
  - Common methods
    - find/index, split/join
    - strip
    - replace
    - startswith/endswith
    - count
  - f-strings advanced
    - alignment, width, precision
  - Encoding/decoding
    - .encode(), .decode()
  - Regex (re module)
    - match/search/findall/sub
    - groups, capturing

- Bytes / Bytearray
  - bytes immutable, bytearray mutable
  - binary data handling

====================================================================
3) CONTROL FLOW
====================================================================

- Branching
  - if / elif / else
  - nested if
  - short-circuit evaluation
  - conditional expression (x if cond else y)

- Loops
  - for loop over iterables
  - while loop
  - break / continue / pass
  - loop else clause

- Pattern Matching (Python 3.10+)
  - match-case
  - structural patterns
  - guards

====================================================================
4) CORE DATA STRUCTURES (WITH SUB-THINGS)
====================================================================

- List
  - create, append, extend, insert
  - pop/remove/clear
  - slicing assignment
  - copy() vs [:]
  - list comprehension (basic → nested)
  - sorting
    - sorted() vs list.sort()
    - key functions
    - stability
  - common patterns
    - stack usage
    - two pointers
    - sliding window

- Tuple
  - immutability
  - packing/unpacking
  - tuple as record
  - namedtuple (collections)

- Set / Frozenset
  - uniqueness
  - union, intersection, difference, symmetric difference
  - set comprehension
  - membership speed

- Dict
  - hashing concept
  - keys must be hashable
  - get(), setdefault()
  - items(), keys(), values()
  - dict comprehension
  - merging dicts (| operator)
  - ordering (insertion-order modern Python)

- collections module (high value)
  - deque (queue/stack)
  - Counter
  - defaultdict
  - ChainMap
  - namedtuple

====================================================================
5) FUNCTIONS (DEEP)
====================================================================

- Function basics
  - def, return
  - None return default

- Parameters / Arguments
  - positional-only (/)
  - positional-or-keyword
  - keyword-only (*)
  - default values + gotchas (mutable defaults)
  - *args and **kwargs
  - unpacking in calls

- Scope model (LEGB)
  - local, enclosing, global, builtins
  - global keyword
  - nonlocal keyword

- Functional tools
  - lambda
  - map/filter/reduce
  - any/all
  - enumerate/zip

- Recursion
  - base case, stack depth
  - tail recursion (not optimized in Python)

- Documentation + typing
  - docstrings
  - type hints (intro here, deep later)

====================================================================
6) MODULES + PACKAGES + IMPORT SYSTEM
====================================================================

- Import mechanics
  - import vs from ... import
  - aliasing
  - __name__ == "__main__"
  - sys.path
  - module caching

- Package structure
  - package folders
  - __init__.py
  - relative imports

- Virtual environments & pip
  - venv workflow (create/activate/install) [official docs]
  - pip install / uninstall / freeze
  - requirements.txt workflow  [packaging guide]

====================================================================
7) EXCEPTIONS + ERROR HANDLING (DEEP)
====================================================================

- Error types
  - SyntaxError
  - Runtime exceptions

- try/except patterns
  - multiple except
  - else and finally
  - re-raise
  - raise from (exception chaining)

- Custom exceptions
  - design hierarchy
  - when to use

- Assertions
  - assert vs real error handling

- Debug trace
  - traceback module
  - logging exceptions

====================================================================
8) FILES + OS + PATHS
====================================================================

- File I/O
  - open modes: r/w/a/x + b + t
  - read(), readline(), readlines()
  - write(), writelines()
  - with context manager
  - newline + encoding options

- Data formats
  - JSON (json module)
  - CSV (csv module)
  - pickle (security warning concept)

- Filesystem work
  - pathlib (preferred)
  - os / shutil
  - permissions & file metadata

====================================================================
9) OOP (ULTRA-DETAILED)
====================================================================

- Class basics
  - class definition
  - object instantiation
  - attributes vs methods
  - instance vs class variables
  - self

- Constructors / lifecycle
  - __init__
  - __new__ (advanced)
  - __del__ (rarely needed)

- Methods
  - instance methods
  - @classmethod
  - @staticmethod
  - property (getter/setter/deleter)

- Encapsulation
  - public/protected/private conventions
  - name mangling (__x)

- Inheritance
  - single inheritance
  - multiple inheritance
  - super()
  - MRO (method resolution order)

- Polymorphism
  - duck typing
  - interface-by-convention

- Abstract Base Classes (abc)
  - ABC, abstractmethod
  - protocols concept (typing)

- Dunder / magic methods (huge)
  - representation: __str__, __repr__
  - comparison: __eq__, __lt__, etc.
  - arithmetic: __add__, __mul__, etc.
  - container: __len__, __iter__, __getitem__
  - callables: __call__
  - context manager: __enter__/__exit__
  - attribute access: __getattr__/__getattribute__/__setattr__
  - hashing: __hash__

- Dataclasses
  - @dataclass
  - frozen
  - order
  - default_factory

- Composition vs inheritance
  - dependency injection basics
  - "has-a" vs "is-a"

====================================================================
10) ITERATORS + GENERATORS + CONTEXT MANAGERS
====================================================================

- Iteration model
  - iterable vs iterator
  - iter() and next()
  - StopIteration

- Generators
  - yield
  - generator expressions
  - send(), throw(), close() (advanced)

- itertools module (must know)
  - product, permutations, combinations
  - groupby
  - accumulate
  - chain

- Context managers
  - with statement
  - contextlib (contextmanager, ExitStack)

====================================================================
11) DECORATORS + CLOSURES + META PROGRAMMING
====================================================================

- Closures
  - enclosing scope + nonlocal

- Decorators
  - function decorators
  - decorator with args
  - wraps (functools.wraps)

- Reflection / introspection
  - dir(), getattr/setattr/hasattr
  - inspect module basics

- Metaclasses (expert)
  - type
  - __init_subclass__
  - descriptors (advanced)
  - class decorators

- AST / bytecode (expert)
  - ast module
  - dis module

====================================================================
12) TYPING (MODERN PYTHON)
====================================================================

- Type hints basics
  - annotations
  - mypy/pyright idea

- typing module
  - list[str], dict[str,int]
  - Optional / Union
  - Literal
  - Any
  - Callable
  - TypeVar, Generic
  - Protocol (structural typing)
  - overload

- Runtime vs static types
  - typing is for tooling, not runtime (mostly)

====================================================================
13) STANDARD LIBRARY MASTERY (WHAT TO LEARN INSIDE IT)
====================================================================

- Core utilities
  - math, statistics, random
  - datetime, time
  - pathlib, os, shutil
  - sys

- Data & formats
  - json, csv
  - sqlite3 (embedded DB)
  - pickle (when/why not)

- Networking
  - socket basics
  - http.client (low-level)
  - urllib (requests alternative)

- Processes & CLI
  - subprocess
  - argparse
  - logging (deep usage)
  - configparser

- Concurrency
  - threading
  - multiprocessing
  - concurrent.futures
  - asyncio

(Stdlib is officially documented as a whole)  [official docs]

====================================================================
14) DEBUGGING + TESTING + QUALITY TOOLING (PRODUCTION)
====================================================================

- Debugging
  - print() strategy
  - pdb / breakpoint()
  - IDE debugging

- Logging (must learn properly)
  - loggers, handlers, formatters
  - levels
  - structured logging idea

- Testing pyramid
  - unit tests

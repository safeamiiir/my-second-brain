Poetry list: `poetry env list` or `poetry env list --full-path`
Poetry remove env: `poetry env remove [<my-env-name>]`

Data types:
Primitives

- Integer
- Float
- String
- Boolean
  Collections
- list
- Dict
- tuple
- set

Operations

```python
+
-
*
/
//

```

Arithmetic Precedence

```python
()
**
+x, -x
*, /, //, %
+ -
```

Variables

- variables: case sensitive
- regular way is snake_case
- Dynamic type

type(my_var) -> shows its type

In python everything is a class/object

after `.` you can call a method

#### Data types

##### Strings

- '' or "": '' -> suggested in dictionaries
- they're a list -> you can do `my_var[0]` or even _slicing_: `my_var[1:4]`
- """ anything """ -> the most useful for comments
- immutable
- you can _ strings: "a" _ 3 = "a a a"
- `type(string_var) = str`
- string interpolation:
  - `"Hello" + name + " " + last_name`
  - `"Hello %s %s $i" % (name, last_name, age)`
  - `"Hello {} {} you are {}".format(name, last_name, age)`
  - OR similarly you can do `"Hello {0} {1} you are {2}".format(name, last_name, age)` you can also change the order of the numbers
  - OR `"Hello {nom} {family} you are {sen:1.1f}".format(nom=name, family=last_name, sen=age)` you can also add precision.
  - `f"Hello {name} {last_name}, you are {age:1.1f} years old"

##### Lists

- similar to arrays
- it's ordered
- Don't need to be the same type: str, number, ...
- You can unpack (deconstruct in js)
- functions:
  - len()
  - list1 + list2
  - list \* 2
  - count(a_number)
  - remove()
  - reverse()
  - sort()

##### Dictionary

- They're key/value, key: string or number
- it's unordered BUT from 3.7 it's ordered
- functions:
  - get() -> like a property! useful: `.get("item", -1)` in case we missed the item

##### Tuple

- similar to lists, except that are immutable: `'tuple' object does not support item assignment`
- Why then? quicker/less memory/...

##### Set

- It's only consist of unique items.
- it's unordered
- functions:
  - add(): you can't `add(1, 2) nor add([1, 2])`
  - union(my_second_set)
  - intersection(my_second_set)

##### Boolean

- True, False
- remember we have `and`, `or`, `not` operators
- remember we have ‍‍‍‍‍‍‍‍‍‍`> < >= <=`
- we can do `3 > 2 > 1` unlike js- type() -> `bool`
- function
  - `num.isdigit()` -> `True`
  - `2 in myList` -> `False`

##### File

- `f = open("myfile.txt")`
- type() -> `file`
- function
  - f.open() -> starts
  - f.read() -> reads until end
  - f.read() -> ''
  - f.seek(0)-> moves the pointer
  - f.readlines()
  - f.close() -> end the reading process
- Suggested: `with`

##### Conditions

```python
if condition:
	statement_1
elif condition_2:
	statement_2
else:
	statement_3
```

##### Loops

FOR

```python
# for in
for item in my_list:
	print(item)
```

for in -> list -> items, tuple -> items, dict -> keys (can do list.items() to get key<>value), string -> chars,

WHILE

```python
while condition:
	do_something
```

pass -> DO NOTHING (like a todo)
break -> stop, and leave the loop.
continue -> ignore the rest, get back to the start of the loop.

Shorthands:

```python
# list comprehension
list = [1, 0.45, 9, -1]
doubled_list = [x * 2 for x in list]

# condition
result = 'even' if a % 2 == 0 else 'odd'

# combined
doubled_even_list = [  2 * x if x % 2 == 0 else None for x in list ]
```

Generators:

- `range(m, n, s)` -> Is a generator: gives me a list from m (default = 0) to n with step s (default = 1) -> yields number
- enumerate -> yields tuple
- zip -> yields tuples

```python
#range -> number
start = 1
until = 10
step = 2
for i in range(start, until, step):
	print(i)

# enumerate() -> tuple
my_list = ['hello', 'my', 2, 'nd', 'world']
for item, item_index in enumerate(my_list):
	print(item, item_index)

# zip() -> tuple
my_names = ['Alice', 'Bob', 'Eve']
my_last_names = ['Alici', 'Bobi', 'Evi']
my_age = [25, 12, 30]
for x in zip(my_names, my_last_names, my_age):
	print(x)
```

other nice functions: `min`, `max`, `from random import randint`, ...

##### Methods

help() will show the doc string.
Function names -> snake_case
my_func(n=1) -> how to default the arg
return item_1, item_2 -> return a tuple

Other Notes
`type(None) -> NoneType`
`%% -> jupyter run terminal commands`

you can do:
`a += 1`

`*args` vs `**kwarg`

```python
def my_func(*args):
	print(args)
my_func(1, 2, 3)
# Tuple:
# > (1, 2, 3)

def my_func(**kwargs):
	print(kwargs)
my_func(name='nom', lastname='famly')
# Dict:
# > {'name': 'nom', 'lastname': 'famly'}
```

**Anonymous functions --lambda**
(Map, Filter)

And it's Lazy that's why we need `list`
```Python
a = [1, 2.2, 3.3, 4]

# Map
numbers_squared = map(lambda x: x**2, a)
print(type(numbers_squared))
print(list(only_integer))

# Filter
only_integer = filter(lambda x: int(x) == x, a)
print(type(only_integer))
print(list(numbers_squared))
for item in only_integer:
    print(item)
```


**Scope of variables**

LEGB: Local > Enclosing Function > Global > Built-in
```python
def make_global_var_scope():
	global var_scope
	var_scope = 'Global'
	print(f"[3. Inside function make_global_var_scope()] Scope of var is: ", var_scope)
	
def enclosing_var():
	var_scope = 'Enclosing Function'
	print(f"[2. Inside function enclosing_var()] Scope of var is: ", var_scope)

var_scope = 'Local'
print(f"[1. Before any function call] Scope of var is: ", var_scope)
enclosing_var()
make_global_var_scope()
print(f"[4. After function calls] Scope of var is: ", var_scope)

```


##### OOP:

Method and Attribute

how to instantiate:

```Python
# Define a class
class ClassName():
	class_attribute = "class_level_attr"
	def __init__(self, param1="default_value"):
		# Attribute
		self.param1 = param1
		print("Object created:", self.class_attribute)
		#OR ClassName.class_attribute
	
	# Method			
	def call_param1(self):
		print(f"This is param1", self.param1)
		
# Make an instance
sample_instance = ClassName("some_value")
print("class type:", type(ClassName))
print("instance type:", type(sample_instance))
print(sample_instance.call_param1())
print(sample_instance.class_attribute)
```

You can also do
```python
class Book():
	book_type = "something_0"
	
my_book_1 = Book()
my_book_2 = Book()

my_book_1.book_type = "something_2"
print(my_book_1.book_type)
print(my_book_2.book_type)
# OR
Book.book_type = "something_1"
print(my_book_1.book_type)
print(my_book_2.book_type)
```

Inheritance

```python
class Book():
	my_attr = "my_attr in class Book()"
	def __init__(self, name, pages):
		print("Book() inited")
		self.name = name
		self.pages = pages
		
	def open():
		print("open called in Book")
		
class InheritedWithNoSuprtFromBook(Book):
	def __init__(self):
		print("Roman Book inited with", self.my_attr)

class RomanBook(Book):
	def __init__(self, name, pages, volume):
		Book.__init__(self, name, pages)
		print("Roman Book inited")
		self.volume = volume
	def open():
		print("open called in Roman book")		

my_book = Book("book_name", "book_pages")
InheritedWithNoSuprtFromBook()
my_roman_book = RomanBook("book_name", "book_pages", "2")
```


Abstract class

```python
class Human():
	def __init__(self, name):
		pass
	def jump(self):
		raise NotImplementedError("implement jump")
		
class Man(Human):
	pass
	
user_1 = Man("Amirreza")
user_1.jump()
# Shows that Man().jumo() MUST implement that!
```

Polymorphism: You can run one method with different behaviours!
	Example: File() class with show() method, but for different classes like Pdf(), Png(), Txt()


**Magic methods**
- Or Special methods
- Or Dunder -> (double underscore)
```python
class myClass():
	def __init__(self):
		pass
	
	def __len__(self):
		# can not return of type str() here
		return 12345
	
	def __str__(self):
		return "return str()"
	
	def __del__(self):
	    # can not return() here
		print( "it's deleted")
# __init__
my_class = myClass()

# __str__
print(myClass())
# OR str(myClass())

# __len__
print(len(my_class))

# __del__
del(my_class)
```


OutOfScope:
- Friendship? in C++
- Concrete vs Abstract

**Modules**

```python
import library
from library import function
```

- Module (Library) -> is basically a Python file!
- Package -> is basically a directory with Python files!
	We MUST have a `__init__.py`  to make directory a Package.
	`__name__` is the Package name if you ask this in your `__main__` program!
	
	When useful? if it's imported as a package or it's being as main! like in CLI
- You can import within a function!
```python
def print_now():
	from datetime import datetime
	now = datetime.now()
	print(now)
	
print_now()
  ```

**Error Handling**

Syntax error... (`NameError`)

```python
try:
	prit("there' a syntx error in print")
except:
	print("No error!")
```

Math 
 `> 5 / 0` ->  `ZeroDivisionError`
 ```python
def divis(a, b):
	try:
		return a/b
	except ZeroDivisionError:
		print("b can not be zero")
		return None
	except Exception as e:
		print(f"An other error {e}")
		return None
		
print(divis(1, 2))
print(divis(1, 0))
print(divis("1", 2))
 ```

Look at: [built-in Exceptions](https://docs.python.org/3/library/exceptions.html) in python

```python
try:
	# First try this
except:
	# Show exceptions
else:
	# Will run if no exception
finally:
	# Will be done in any case
```

Python Improvement Proposal (PEP) -> PEP 8

Linter -> (Pylint)  Checks the logic, format, bad practices, ...
Formatter -> (Black) Only corrects the code format!
Testing -> (unittest) Test the functionality


**Decorator**

Unrelated: `is` in python

Write a function in a way that changes the functions functionality in a specific way!

Functions as a first class citizen in python

```python
def say_hello():
	print("Hello there!")

def do(what_to_call):
	what_to_call()

do(say_hello)
```

```python
def my_decorator(f):
	def wrapper():
		f()
		print("I'm a decorator!")
	return wrapper

@my_decorator
def say_hello():
	print("Hello there!")
	
say_hello()
```


**Generator**
TBD


**Interesting modules in Standard library**

```python
import datetime
my_date = datetime.date(2025, 1, 1)
my_date.day
my_date.month
my_date.weekday()
my_date.ctime()

my_time = datetime.datetime(1999, 1, 1, 11, 11)
my_time.ctime()
my_time.date.today()
now_time = datetime.datetime.now()
now_time - my_time

import math
math.pi
math.e
math.inf
math.log
math.degrees()
# Not to do with Math
round()

import random
random.randint(0. 6)
random.random()
random.choice(['a', 'b', 'c'])
random.choices(['a', 'b', 'c'], k =2)
random.sample(['a', 'b', 'c'], k =2)
random.shuffle(['a', 'b', 'c'])


import re
strin = "this is a test again test"
re.search('test', s)
r = re.search('test', s)
re.compile()
r.start()
r.end()
r.group() # Gives the first group in the pattern
r.span()
re.findall('test', s)
re.finditer('test', s)


import decimal

decimal.getcontext()
decimal.getcontext().prec = 3
decimal.Decimal()
decimal.Decimal(0.1) + decimal.Decimal(0.2) != decimal.Decimal(0.3)
decimal.Decimal('0.1') + decimal.Decimal('0.2') == decimal.Decimal('0.3')

import os

# File stuff doable
csv,
gzip,
...

```

How seed works in random?

```python
random.random(5)
random.ranint(1, 6)
random.ranint(1, 6)
random.ranint(1, 6)

random.random(5)
random.ranint(1, 6)
random.ranint(1, 6)
random.ranint(1, 6)
```

**Learn RegEx**

`\d` -> digits, `\D` -> all that is not \d
`\w` -> Alphanumeric words, `\W` all that is not \w
`\s` -> White spaces -> `/S` all that is not \S
`.` -> Accept anything

`+`  ->  1 or more
`*` -> 0 or more
`?` -> 0 or 1
`{3}` -> only 3 ta
`{2, 4}` -> only 2 ta until 4 ta

`^` just in the start 
`()` -> you can groupify
`[this]` -> Anything except `this`

RegEx is Greedy! finds the biggest possible group.
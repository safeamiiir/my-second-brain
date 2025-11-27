> These are my notes from Jadi's [compehensive python course ](https://maktabkhooneh.org/course/%D8%A2%D9%85%D9%88%D8%B2%D8%B4-%D8%A8%D8%B1%D9%86%D8%A7%D9%85%D9%87-%D9%86%D9%88%DB%8C%D8%B3%DB%8C-%D8%A8%D8%A7-%D9%BE%D8%A7%DB%8C%D8%AA%D9%88%D9%86-%D9%85%D9%82%D8%AF%D9%85%D8%A7%D8%AA%DB%8C-mk346/).

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

Some examples
```python
#### Numbers ######
hex(12)
# 0x it's a hex
oct(12)
# 0o it's a hex
bin(12)
# 0b it's a hex

int('12', 2)
# binary

###### Strings ######
my_string = "this is me here"

my_string.title()
my_string.count("e")
my_string.find("e")
my_string.find("not_found") # -1
my_string.center(50, "*")

my_string.is<so_many_options>

s.startswith()
s.endswith()

s.split(' ')
s.partition('is')
''.join(['this', 'is', 'a', 'list'])

###### Sets ######
my_set = {1, 2, 3}
# OR my_set = set()
my_set.add(1)
my_set.add(4)
my_set.remove(1)
my_set.remove(5)
my_set.discard(5)

my_new_set = my_set
# my_new_set is a new reference to my_set !!!
my_new_set.pop()
my_copied_new_set = my_set.copy()

s1 = {1, 2, 3, 4}
s1 = {3, 4, 5, 6}
s1.difference(s2)
s1.difference_update(s2)
s1.intersection(s2)
s1.intersection_update(s2)
s1.isdisjoint(s2)
s1.issubset(s2)
s1.issuperset(s2)
s1.union(s2)
s1.update(s2)


###### Dictionaries ######
d = {'name': 'John', lastname: 'Doe'}
# or d = dict()

# List:
l = [1, 2, 3]
l.append(3)
l.append(5)
l.count(3)
i.insert(3, 4)
l.remove(2)
l.pop()
l.pop(0)

# List comprehension:
[x*2 for x in [1, 2, 3]]

###### Dictionaries ######
# Can do the same dictionary comprehention
{x: x*2 for x in [1, 2, 3]}
{f"k{x}": x*2 for x in [1, 2, 3]}
{k: v for k, v in zip(['a', 'b'], [0, 1])}
my_dict = {k: v for k, v in zip(['a', 'b', 'c', 'd'], range(4))}
my_dict.values()
my_dict.keys()
my_dict.items()

# A common use:
for k, v in my_dict.items()
	prin(k, v)
	
for v in my_dict.values()
	prin(v)

```

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
try `__doc__` to read more about it.
try `dir()` to see all the options in that class.
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

#### More libraries
Web scraping
```python
import request

r = request.get('<url>')

r.status_code
r.url
data = r.text

import bs4

soup = bs4.BeautifulSoup(data)
title = soup.select("title")
title[0].get_text()

```

File: Images
```python
# inatall pillow
from PIL import image

my_image = Image.open("/my-image.jpg")

my_image.show()
my_image.finename()
my_image.format()
my_image.size()
my_image.mode()

my_image.getpixel()
my_image.putpixel()
my_image.putalpha()

my_image.close()
```

Files: CSV
```python
import csv

my_file = open("my_csv_file.csv", encoding="utf-8")

csv_data = csv.reader(my_file)
csv_data_dic = csv.DictReader(my_file)


out_file = open('myNewCsv', mode='w', newline='')
csv_writer = csv.writer(outfile, delimiter="|")
csv_writer.writerow()

my_file.close()
```

Files: PDF
```python
import pyPDF2


pdf = PyPDF2.PdfReader("sample.pdf")
pdf.pages[]
pdf.pages[0].extract_text()

```

Files: Excel
```python
import openpyxl

workbook = openpyxl.load_workbook("sample.xlsx")
worksheet = workbook.active
worksheet["A1"].value
worksheet["A4"].fill

new_wb = openpyxl.Workbook()
ws = new_wb.active
ws["A1"] = "something"
new_wb.save("out.xlsx")

```

JSON
```python
import json

data = {'name': 'asd', 'lastname', 'qwe'}
# s refers to string!
json.dumps(data)
new_data = json.loads(d)
```

**Itertools**
```python
import itertools as it

it.cycle([1, 2, 3])
next(a)
# 1
next(a)
# 2
next(a)
# 3
next(a)
# 1
# ...

nums = [1, 2, 3, 4]
combs = it.combinations(nums, 2)
combs = it.combinations_with_replacement(nums, 2)
print(list(combs))

counter(3, 10)
next(counter)
# 3
next(counter)
# 10
next(counter)
# 23
# ...

acc = it.accumulate(nums)
print(list(acc))

# More
it.product()
it.tee()
it.repeat()
it.chain()
```

#### Virtual Environment
```bash
python3 -m venv venv
source venv/bin/activate
pip freeze > requirements.txt
pip install -r requirements.txt
```

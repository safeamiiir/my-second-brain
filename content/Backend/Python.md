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

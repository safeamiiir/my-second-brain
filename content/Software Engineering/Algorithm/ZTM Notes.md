
# Section 3 – Big O

What is good code?
1. Readability
2. Scalability
	Choose the right Data structure + Algorithms to optimise:  
	- 2.1. Speed
	- 2.2. Memory
### Time and Space Complexity

#### Time Complexity

Big O Asymptotic Analysis.

Why do we measure Big O and not the time?
- Computers have different performances
- Programming languages also have their own performances.

This shows us to know:
1. How many operations a computer have to perform.
2. How many steps it takes in a function.
3. How efficient this code is.
4. Upper bound, worst case scenario of the code execution time.
5. 


![[big-o-complexity.png]]

Section below is from [big-o-cheat-sheet](https://zerotomastery.io/cheatsheets/big-o-cheat-sheet/)

A more comprehensive list could be found: https://bigocheatsheet.com/
##### Big O's
| Big O    | Name         | Description                        | Nore notes                                                                |
| -------- | ------------ | ---------------------------------- | ------------------------------------------------------------------------- |
| 1        | Constant     | statement, one line of code        | No loops                                                                  |
| log(n)   | Logarithmic  | Divide and conquer (binary search) | Usually search algorithms are O(lg(n))                                    |
| n        | Linear       | Loop                               | for/while loops                                                           |
| n*log(n) | Linearithmic | Effective sorting algorithms       | it's also called Log linear                                               |
| n^2      | Quadratic    | Double nested loop                 | Every element in a collection needs to be compared to every other element |
| n^3      | Cubic        | Triple nested loop                 | Same but collection of 3                                                  |
| 2^n      | Exponential  | Complex full search                | Recursive algorithms that solve a problem of size n                       |
| n!       | Factorial    | Add a loop for every (n) element   | It's the worth!                                                           |

##### Sorting Algorithms
| Sorting Algorithms | Space complexity | Time complexity | Time complexity |
| ------------------ | ---------------- | --------------- | --------------- |
|                    | Worst case       | Best case       | Worst case      |
| Insertion Sort     | O(1)             | O(n)            | O(n^2)          |
| Selection Sort     | O(1)             | O(n^2)          | O(n^2)          |
| Bubble Sort        | O(1)             | O(n)            | O(n^2)          |
| Mergesort          | O(n)             | O(n log n)      | O(n log n)      |
| Quicksort          | O(log n)         | O(n log n)      | O(n^2)          |
| Heapsort           | O(1)             | O(n log n)      | O(n log n)      |

##### Common Data Structure Operations
| Worst Case→        | Access | Search | Insertion | Deletion | Space Complexity |
| ------------------ | ------ | ------ | --------- | -------- | ---------------- |
| Array              | O(1)   | O(n)   | O(n)      | O(n)     | O(n)             |
| Stack              | O(n)   | O(n)   | O(1)      | O(1)     | O(n)             |
| Queue              | O(n)   | O(n)   | O(1)      | O(1)     | O(n)             |
| Singly-Linked List | O(n)   | O(n)   | O(1)      | O(1)     | O(n)             |
| Doubly-Linked List | O(n)   | O(n)   | O(1)      | O(1)     | O(n)             |
| Hash Table         | N/A    | O(n)   | O(n)      | O(n)     | O(n)             |
##### Rule Book

**Rule 1:** Always worst Case
**Rule 2:** Drop the Constants
**Rule 3:** Different terms for inputs:
- Different inputs should have different variables: `O(a + b)`
- A and B arrays nested would be: `O(a * b)`
`+` for steps **in order**
`*` for **nested** steps
**Rule 4:** Drop Non-dominant terms
#### Space Complexity
##### What Causes Space Complexity?
We need to follow the same but this time thinking about space! if there's nothing of the list below, it's an O(1) otherwise we follow the same calculation thinking about What Causes Space Complexity? from the list above
- Variables
- Data Structures
- Function Call
- Allocations
#### Trade-offs between Time and Space complexity

> [!WARNING]
> These examples need to be verified.

Example 1: Tweets with a timestamp as an input:
- Store in a raw object?
	1. Time: O(n^2): We have to compare all
	2. Memory: O(1): We don't store anything
- Sort them first?
	1. Pre process time: O(lg(n)): To sort them
	2. Time: O(n): We just show them in order
	3. Memory: O(n): We need to store them sorted in an object.
Example 2: `.length` on a string
- C++
	- Needs to be calculated and it's an O(n), but doesn't take any extra space
- Javascript?
	- Is implemented as a simple look up: O(1) but it takes more space as this needs to be implemented

-----
# Section 5 – Data structures: Introduction

Data structure + Algorithms = Programs

Questions to be answered:
1. How to build a DataStructure?
2. How to use a DataStructure?


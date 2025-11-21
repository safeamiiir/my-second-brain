# Lesson 1 - Quantum Query algorithms

The query model of computation
- Duetsch's Algorithm (1985 paper)
- Duetsch's-Jozsa Algorithm
- Simon's Algorithm

Potential Advantages

Quantum computers might provide faster solutions to some computational problems.
Why classical on some problems slow? inherit computational difficulty
Other help
- Amount of computer memory required? Hmm yess but not that helpful.
- Amount of energy? Classical is not too much
- Amount of time? Yes! Faster computation

Shor's algorithm for factoring


Oracle/Blackbox -> describes input of the query model of computation.

Query gates

The phase kickback phenomenon
Interference

eigen value
eigen vector

Binary dot product.

Bernstein-Vazirani problem


Integer Factorisation



Good to remember vocabs:
- Turing Machine
- Boolean circuits
- Shed a great deal of light
- The all cancel out (با هم خط می‌خورن)

Glossary:
- Petry dish
- Oracle of Delphi
- highly contrived
- exponent
- superscript
- Modulo 2
- Gaussian elimination
- Null space
---
# Lesson 2 - Quantum algorithmic foundation


Integer Factorisation:
+Prime factorisation

computation: Mechanical transformation on strings of bits

input length -> size of the instance of the problem

Elementary operation: One involving a small fixed number of bits or qubits that can be performed quickly and easily: computing the end of two bits, or one step of a Turing machine

Each gate as being an elementary operation

Universal: good enough set of gates that we can make any unitary operation of out them

AND, OR, NOT, FANOUT -> A standard Boolean gate set -- Universal set for Boolean.

Circuit Size:
- Number of the elementary operation we need to perform.
- Sequential running time

Circuit Depth:
- Max num of gates encountered on any path from inp to out
- Number of the layer of gate- Parallel running time

Circuits don't grow -> Family of circuits

Cost for Integer addition:
(counting fanout gates as well)
half adder => 10 gates
full adder -> 2 * half adder + OR => 21 gates
SO for addition we need: 21(n-1) + 10 = 21n - 11

Asymptotic notation: Big-O notation

Polynomial
sub-exponential
Exponential

We don't know any sub-exponential for Integer factorisation!
number field sieve is the best for Integer Factorisation 2^O(n) --> it's still exponential
Shor's algorithm is with polynomial cost!

NP-Complete [[What problems are quantum computers good for?|problems]] are conjectured not to have sun-exponential cost?
We can't even prove that there aren't linear cost algorithms for NP-Complete problems

We can run classical computations on quantum computations.
for boolean we can do that in a **clean** manner if we run them as a subroutine inside a larger quantum computers.

Toffoli gates ~-> query gates for the AND function.
Toffoli gates could be implemented by: Hadamard, T, T dagger, Control-NOT gates.

We need workspace qubits but Classical Boolean circuits could be done in the same polynomial cost in a quantum computers

Glossary
- division
	- quotient
	- remainder
# Lesson 3 - Phase estimation and factoring

Spectral theorem

-> just for unitary matrices
-> Phase kickback helps to learn more about Eigen value
-> iterative phase estimation

Discrete Fourier transform: Linear mapping on vectors --being represented by matrix
+Fast Fourier transform
Quantum Fourier Transform (QFT) as a unitary operation

Best approximation always have the highest probability associated with them.
|
|-> what ever value of y/4 is closes to the true value of Theta

Try QFT for different sizes: 1 (Hadamard), 2, 4, 8 -> we learn when N is a power of 2:
- it's like a controlled-phase gate!
- it's recursive in nature.

In terms of complexity: Order-finding problem ≡ Phase-estimation



Glossary:
- Denominator, nominator
- Necessary and Sufficient (لازم و کافی)
- congruent, triple equal, ≡ Vs. equal, =


# Lesson 4 - Grover's algorithm

unstructured search
-> let's think about it as a query problem
- It's like searching for a particular phone number in a phone book
	Vs. searching for a name which is much easier presuming that the name had be alphabetised.
- It's not about searching through data
	Vs. searching for a solution for a complicated equation
- it's searching for a combination that opens a lock

There's an answer in O(2^n) for this


Glossary:
- Hereafter
- coeficient

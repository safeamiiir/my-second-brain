# Lesson 1 - Single systems
----

- Single system in isolation 

- Quantum information is an extension of classical information

classical information:
Quantum information:

Simplified description:
- Quantum states: Vectors
- Operations: *Unitary Matrices*
What can not be done by this? Model the effect of noise? 

General description:
- Quantum states: Density Matrices
- Operations: Density Matrices allow more general class of measurements and operations
Includes both simplified description and classical information

---

**Classical states**: Finite set + not empty. requires to be at least 2 classical states if the system is going to be useful at all for storing informations.


Column Vector
Row Vector
Probability Vector
Standard basis vector
Unit vectors

Deterministic operations
Probabilistic operations
Unitary Operations
Pauli Operations
Hadamard Operation
Phase Operation 

Bit flip
Phase flip

Stochastic Matrices
Unitary Matrices

Glossary
- Dirac
- Ket < |
- Bra | >
* Linear
* Assosiative (تراگذری)
* Closed
* Commutative (نامتقارن)
* matrix-vector Multiplication
* Matric multiplication
* conjugate transpose (ترانهادهٔ مزوج)
	* shown by dagger
* Composition
* Euclidean norm

# Lesson 2 - Multiple systems
----

Multiple systems can be considered as a compound system.

Classical state

n-tuple could be written in a string form (a, b, c) -> abc

Convention:
a. Cartesian products of classical state sets are ordered lexicographically.
b. Significance decreased from left to right.


X and Y are independence:

Pr((X,Y) = (a,b)) = Pr(X = a) Pr(Y = b)


Tensor product a default way to multiply two column vectors together. No Matrix multiplication because dimensions aren't right.

scalars "float freely" within tensor products.

In Simplified description: For a quantum state vector:
If it's not a product state --> it's an entangle state (lack of independence)

Bell states, which for Bell basis (Named after John bell)

Some quantum states example: `GHZ`, `W` states

swap operation
controlled-u operation
controlled-SWAP operation (Fredking operation/gate)
controlled-controlled-NOT operation(Toffoli operation/fate)

Glossary
- Respectively
- Independence (opposed to Correlation)
- Zero product property
- Tensor product
- bilinear
- multilinear
- analogas
- multiplicative
- subscript
- superscript?

#### Readmore

1. Significance decreased from left to right.?????? But it had been done differently
2. Read more on dependant Pr()
	![[IBM_lesson2_2819.png]]
3. Tensor product of matrices!


# Lesson 2 - Quantum circuits

Quantum protocols

Quantum circuit model

Inner products, orthonormality, projections

Limitations:
- ?
- No cloning
- Non-orthogonarmality

Wires -> Information
Gates -> Operations

Circuit are normally circular but here we mean Acyclic.
A circuit (In Quantum which actually is) -> Sequence of operations

Boolean circuit
Arithmetic circuit


Circuit: X --H--S--H--T--
Matric Multiplication: THSH
 X := |0> --> THSH |0>


Quantum circuit:
- Bottom to Top
- Left to Right

Classical bits can also be used but double dots

Once the qubits are measured, they're discarded and the classical measurement outcomes are carried forward.


![[IBM_lesson3_21704.png]]

Arbitrary unitary operations

Two unit vectors (with real number entries) Inner product -> Co-sign (cos) of the angle between them.

Inner product and Euclidean norm.
Inner product is linear in the second component.
Inner product is conjugate linear in the first component.
Inner product is Cauchy-Schwarz inequal.
Inner product is zero when they're orthogonal.

vectors being orthogonal: pointing not in opposite, but in different directions

Projective measurements

we can simply ignore global phases -> it's a generous-y in simplified description
relative phase difference

Hadamard gate being applied could show a difference on relative phase difference but not on global phase different

CNOT gate copies the standard basis state of the qubit.
CNOT gate doesn't clone some states like: plus state.

Cloning a probabilistic state is also impossible.
Cloning is a non-linear process.

perfect discriminate of two quantum state: some way to tell them apart without any chance of error.

if it is possible to do a perfect descimination -> they're orthogonal states

Glossary:
- Standard basis state:0, 1: 00, 01, 10, 11
- Inner products
- Unit Vector
- Conjugate symmetric
- Orthogonal set
- Orthonormal set
- Orthonormal basis
- perpendicular, right angle
- linearly independent
- Gram-Schmidt orthogonalisation process.
- Hermitian matrices
- global phase 
- process of discrimination

# Lesson 4 - Entanglement in action

- Teleportation
- Superdence coding
- CHSH game (inequality)

Entanglement: Non classical quantum correlation

e-bit -> unit of entanglement

resource -> one bit of shared randomness
a Private key, or as part of a private key

Share an e-bit meaning.

Teleportation is a protocol. allows a sender to transmit quantum information to a receiver; using only entanglement and classical communication to accomplish that transmission.


Teleportation: one Qbit using: e-bit + 2 classical bit -- transmission of classical quantum information
Superdense Coding: 2 classical bit using: e-bit 1 Qbit  -- transmission of classical information

Holevo's theorem

superdense coding is not having any practical application.

no local hidden variable theory

Best optimal is 85% in CHSH Game: seriousness inequality Bora Serison who first have proven it.
The 85% success rate is the **maximum allowed by quantum mechanics**, known as **Tsirelson’s bound**.

GHCH Game/experiment is an example of a Bell test
Players/detectors



Glossary
- denominator
- entanglement distillation
- nonlocal games 
- denominator (مخرج)
- 3 over 4
- deduce
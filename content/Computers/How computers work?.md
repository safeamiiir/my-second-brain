
### Memory
[Ref](https://www.youtube.com/watch?v=fpnE6UAfbtU)

**AND-OR Latch**
It "latches onto" a particular value and stays that way.
	- Writing: Putting data into memory
	- Reading: Getting the data out memory

![[and-or-latch.png]]

**Gated Latch**
WRITE ENABLE
	If 1 -> overwrites the DATA OUTPUT value
	If 0 -> nothing will change the DATA OUTPUT value

![[gated-latch.png]]

8 Latches side-by-side 8 bits of information --> A group of lathes operating like this is called **a register** --which holds a single number and the number of bits in a register is called its **width**.

Todays computers have a 64-bits wide registers.

**Problem:** Even if we use 1 wire for enable them, we still need n number of wires for the input and also n number of write for the output: `2 * n + 1` e.g. For a 256-bits width we need (2 * 256 + 1(enable) = 513)

![[memory-row.png]]

**Solution:** Grid: if ROW and COLUMN both are 1 the AND gate could turn the enable write on!

![[16-16-matrix.png]]
![[memory-grid.png]]

e.g. Then now for a 256-bits width we need (2 * 16(rows+columns) + 1 (data)+ 1(write enable) + 1(read enable) = 35)

Memory Address! defines the intersection

We store row addresses in a 4-bit number: 000(0) onto 1111 (16)

To convert from address into something and selects the right row or column, we use a **multiplexer**: 1 for row and 1 for column --> 8-bit then! 

This is for a 256-BIT memory!

We can put 8 * 256-BIT memory components next to each other and we can make an storage for an 8 bit number -- **A byte**.

![[RAM-A.png]]

Or we can think of it this way:

![[RAM-B.png]]

We can make larger and larger memories.

The point about RAM is that by this design we can have access to any address we want on the memory at anytime! meaning we have a Random Access Memory (RAM)

SRAM, DRAM, Flash Memory are Fundamentally similar to this but different in implementations.

### Multiplexer

A multiplexer is used to help us output the right memory address, we need tw 16:1 multiplexers to handle a 16\*16 memory grid.

![[multiplexer.webp | from: https://www.geeksforgeeks.org/digital-logic/multiplexers-in-digital-logic/]]

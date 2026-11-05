# Arithmetic Logic Unit
- The ALU is part of the computer that is responsible for processing arithmetic and logic operations.
- It is made up of two parts:
  - Arithmetic unit
  - Logic unit.

## Arithmetic Unit
The Different Operations include the following:

| S3 | S2 | S1 | S0 | Operation | Description |
|:--:|:--:|:--:|:--:|:---|:---|
| 0 | 0 | 0 | 0 | CAi = A + B | Add |
| 0 | 0 | 0 | 1 | CAi = A + B + 1 | Add with carry |
| 0 | 0 | 1 | 0 | CAi = A | Transfer A |
| 0 | 0 | 1 | 1 | CAi = A + 1 | Increment A |
| 0 | 1 | 0 | 0 | CAi = A + /B | Subtract with borrow (1’s complement) |
| 0 | 1 | 0 | 1 | CAi = A + /B + 1 | Subtract (2’s complement) |
| 0 | 1 | 1 | 0 | CAi = /A | Complement of A |
| 0 | 1 | 1 | 1 | CAi = /A + 1 | 2’s Complement of A |

## Logic Unit
The Different Operations include the following:

| S3 | S2 | S1 | S0 | Operation | Description |
|:--:|:--:|:--:|:--:|:---|:---|
| 1 | 0 | 0 | 0 | CLi = 0 | Reset |
| 1 | 0 | 0 | 1 | CLi = 1 | Set |
| 1 | 0 | 1 | 0 | CLi = A AND B | A AND B |
| 1 | 0 | 1 | 1 | CLi = A OR B | A OR B |
| 1 | 1 | 0 | 0 | CLi = A XOR B | A XOR B |
| 1 | 1 | 0 | 1 | CLi = A AND /B | Reset A bits selected by mask B |
| 1 | 1 | 1 | 0 | CLi = ashl A (Ai-1) | Arithmetic Shift Left (signed multiplication by 2) |
| 1 | 1 | 1 | 1 | CLi = ashr A (Ai+1) | Arithmetic Shift Right (signed division by 2) |

## Sub-Modules of the ALU
```
Lab3_top.bdf (Top-Level Entity)
├── state4bit.bdf
├── arithcircuit4bit.bdf
│   └── arithcircuit1bit.bdf
│       └── fulladder1bit.bdf
├── logiccircuit4bit.bdf
│   └── logiccircuit1bit.bdf
└── register4bit.bdf
```

## What I Learnt From this Project:

```
Building this ALU taught me that from a simple 1-Bit Full adder one can abstract the idea and build more complex circuits.
We are able to do all these micro operationsout of full adders and multiplexers.
The multiplexer simply routes the correct value to the full adder based on the select bits.
Another thing this project taught me is that these micro operations happen during one single clock pulse.
Overall was a fun project and I'm looking forward to learn how to implement more computer chip designs.

```

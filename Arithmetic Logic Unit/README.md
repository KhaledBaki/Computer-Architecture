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
# Hierarchy:
## Arithmetic & Logic Unit 4-Bit:
<img width="1563" height="761" alt="image" src="https://github.com/user-attachments/assets/591dac1a-3015-407f-9c6c-a272b47ba84d" />

## Logic Circuit 4-Bit:
<img width="738" height="861" alt="image" src="https://github.com/user-attachments/assets/342c8f0e-c754-4480-8f14-cfdef2ca61a6" />

## Logic Circuit 1-Bit:
<img width="1058" height="442" alt="image" src="https://github.com/user-attachments/assets/6fdfe28a-ad2a-4a6e-9612-f58565f8d00f" />

## Arithmetic Circuit 4-Bit:
<img width="723" height="822" alt="image" src="https://github.com/user-attachments/assets/eb5058b4-0826-46cb-9894-30bf85d025b7" />

## Arithmetic Circuit 1-Bit:
<img width="712" height="790" alt="image" src="https://github.com/user-attachments/assets/b4705bbc-5661-4737-8ce1-5f206611cda0" />

## Full Adder 1-Bit:
<img width="968" height="292" alt="image" src="https://github.com/user-attachments/assets/e6944505-dcae-4f07-a5ab-22ea472c639c" />

## State Circuit 4-Bit:
<img width="1160" height="497" alt="image" src="https://github.com/user-attachments/assets/93a83e07-d7f7-44ba-83d1-2123f53ba3ee" />

## Register 4-Bit:
<img width="1090" height="552" alt="image" src="https://github.com/user-attachments/assets/507a4843-dc5c-4097-a9c6-c6be5e0a4f80" />

## What I Learnt From this Project:

```
Building this ALU taught me that from a simple 1-Bit Full adder one can abstract the idea and build more complex circuits.
We are able to do all these micro operationsout of full adders and multiplexers.
The multiplexer simply routes the correct value to the full adder based on the select bits.
Another thing this project taught me is that these micro operations happen during one single clock pulse.
Overall was a fun project and I'm looking forward to learn how to implement more computer chip designs.

```

# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1280" height="1057" alt="image" src="https://github.com/user-attachments/assets/77752fc7-9138-4150-bd2d-c21a5f8a0b9b" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE

![mpmcadd1](https://github.com/user-attachments/assets/dcb4fe11-403f-404e-9f5c-74c10fbe65eb)
![mpmcadd01](https://github.com/user-attachments/assets/cdcdca96-7d93-4a8c-b5c9-5c87a5885575)


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1280" height="992" alt="image" src="https://github.com/user-attachments/assets/c7f95f2b-0373-4f71-b3c2-b8021a64d061" />

---


## OUTPUT SCREEN FROM MASM SOFTWARE

![mpmcsub1](https://github.com/user-attachments/assets/2eb441f4-2ebb-44cf-be13-3e8f2b92b8f1)
![mpmcsub01](https://github.com/user-attachments/assets/ceed2f03-f97f-46e5-a1d7-b5b528398d8a)


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1242" height="821" alt="image" src="https://github.com/user-attachments/assets/74b9301e-779e-493a-8edc-292146318407" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE

![mpmcmul001](https://github.com/user-attachments/assets/f1265782-6bc7-451e-8ae8-fe64a7668949)
![mpmcmul0001](https://github.com/user-attachments/assets/322979da-6512-43f4-b606-dd1620f38920)


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

<img width="1181" height="1167" alt="image" src="https://github.com/user-attachments/assets/104ef1e4-2863-4b07-95f1-f868449bc6cf" />

---
## OUTPUT FROM MASM SOFTWARE
![mpmcmul1](https://github.com/user-attachments/assets/ed41695e-0043-46ed-b263-9e32f0b07fbb)
![mpmcmul01](https://github.com/user-attachments/assets/7f8ba0bd-a4e9-48f4-926f-50628a730b9e)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

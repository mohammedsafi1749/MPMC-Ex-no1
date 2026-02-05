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
<img width="377" height="522" alt="image" src="https://github.com/user-attachments/assets/bd33a0c3-7a78-4c35-9c80-93dab8bae111" />


#### Program

```asm
CODE SEGMENT
ASSUME CS:CODE, DS:CODE
ORG 1000H
MOV CL,00H
MOV AX,1234H
MOV BX,1234H
ADD AX,BX
JNC L1
INC CL
L1:MOV SI,1200H
MOV [SI],AX
MOV [SI+2],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|      1200 : 12          |        1204 : 24         |
|      1201 : 34          |        1205 : 68         |  
|      1202 : 12          |        1206 : 00         |
|      1203 : 34          |                          |  

#### Manual Calculations

(Add your calculation here)

<img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/a7f1423e-0636-40f5-ad72-5a8a7361c238" />

---

## OUTPUT IMAGE FROM MASM SOFTWARE

<img width="646" height="431" alt="image" src="https://github.com/user-attachments/assets/404affba-0127-4ba5-8868-2d55807b8935" />

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
```asm
code segment
assume cs:code,ds:code
org 1000h
mov AX,1234h
mov BX,1234h
sub AX,BX
jnc down
inc CL
down:mov SI,1200h
mov [sI],AX
mov [SI+2],CL
mov ah,4ch
int 21H
code ends
end

```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

(Add your calculation here)

---
<img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/3f43ff55-243c-4abe-be14-3892eef1ab42" />


## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="637" height="424" alt="image" src="https://github.com/user-attachments/assets/d11df796-dea9-4ba7-8404-438f1b49f611" />


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

## FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
code segment
assume cs:code,ds:code
org 1000h
MOV DX,0000H
mov AX,1234h
mov BX,1234h
mul BX
mov si,1200h
mov [si],ax
mov [si+02h],dx
mov ah,4ch
int 21h
code ends
end

```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|                         |                          |

#### Manual Calculations

(Add your calculation here)

<img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/3227b79a-69b7-447d-915b-f085e97a73c3" />

---

## OUTPUT SCREEN FROM MASM SOFTWARE

<img width="645" height="427" alt="image" src="https://github.com/user-attachments/assets/4f56145f-cecb-4dd3-821f-4d32b3598705" />


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
ASSUME CS:CODE,DS:CODE
ORG 1000H
MOV DX,0000H
MOV AX,1234H
MOV BX,1234H
DIV BX
MOV SI,1200H
MOV [SI],AX
MOV [SI+©2H],DX
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

(Add your calculation here)
<img width="250" height="250" alt="image" src="https://github.com/user-attachments/assets/0462b7e3-3d65-4df3-9d34-ce0ede6964c9" />

---
## OUTPUT FROM MASM SOFTWARE

<img width="648" height="426" alt="image" src="https://github.com/user-attachments/assets/ee7678c1-5b36-4638-9e78-839d89711c14" />


## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.


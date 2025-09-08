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
|    1200 : 12            | 	   1204 : 24           |  
|    1201 : 34	           |      1205 : 68           |
|    1202 : 12	           |      1206 : 00           |
|    1203 : 34	           |      1207 : C4           |                          

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 01 39_09372a33](https://github.com/user-attachments/assets/66b930e4-2e0d-4cf2-9436-c142e304347c)

---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="638" height="423" alt="image" src="https://github.com/user-attachments/assets/81236424-d5af-4a31-be7c-2afff4c708bd" />

<img width="630" height="428" alt="Screenshot 2025-08-30 161216" src="https://github.com/user-attachments/assets/cff6b7f9-4f8c-4dd8-955f-2e17ee2be09e" />


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
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200 : 12	        |          1204 : 00       |
|       1201 : 34	        |          1205 : 00       |
|       1202 : 12	        |          1206 : 00       |
|       1203 : 34	        |          1207 : C4       |                                  

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 01 58_e200a013](https://github.com/user-attachments/assets/372ff327-da28-46dd-9d04-5a1a63080f5e)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="633" height="426" alt="image" src="https://github.com/user-attachments/assets/5e0549ef-d074-413f-a629-6cc4d0c07ffc" />

<img width="637" height="423" alt="Screenshot 2025-08-30 193837" src="https://github.com/user-attachments/assets/2c1da0bb-a04a-4a1c-bdb2-ed157f9edde3" />


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
|          1200 : 12      | 	    1204 : 44          |
|          1201 : 34      |       1205 : 51          |
|          1202 : 12	     |       1206 : 97          |
|          1203 : 34	     |       1207 : 0A          |                          

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 05 59_1eadf375](https://github.com/user-attachments/assets/b2c13020-4b29-405b-9b91-cbdd9e4603cc)


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="636" height="424" alt="image" src="https://github.com/user-attachments/assets/5f0df9ae-fe96-491c-99ea-f90f38755bf2" />

<img width="639" height="424" alt="Screenshot 2025-08-30 194958" src="https://github.com/user-attachments/assets/8495a12d-c97b-4bc3-8b19-489642461a01" />


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
|1200 : 12                |     1204 : 01            | 
|1201 : 34	              |     1205 : 00            |
|1202 : 12	              |     1206 : 00            | 
|1203 : 34	              |     1207 : 00            |                                

#### Manual Calculations
![WhatsApp Image 2025-08-30 at 16 06 26_4d9b1319](https://github.com/user-attachments/assets/be280d4a-951d-4c11-97fd-e48d1c9cf96f)

(Add your calculation here)

---
## OUTPUT FROM MASM SOFTWARE
<img width="642" height="423" alt="image" src="https://github.com/user-attachments/assets/f724de5b-78e3-4371-b0a9-e6f3e001c86d" />

<img width="635" height="418" alt="image" src="https://github.com/user-attachments/assets/4787f3ad-1c0d-4f12-8ef2-6662f588f32b" />

## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

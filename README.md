# FACTORIAL-OF-A-NUMBER
# FACTORIAL OF A NUMBER USING 8051 (Keil)

## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

---

## APPARATUS REQUIRED
- Personal computer with Keil software

---

## ALGORITHM
1. **Start**
2. **Input**: Read the number `n`.
3. **Initialize**:
   - Set factorial to `1`.
   - Set `i` to `1`.
4. **Loop**: While `i` is less than or equal to `n`:
   - Multiply factorial by `i`.
   - Increment `i` by `1`.
5. **Output**: Store or print the value of factorial.
6. **End**

---

## FLOWCHART
<img width="1199" height="1312" alt="image" src="https://github.com/user-attachments/assets/b7f95a4d-d80d-46f0-b270-9cbe0c128862" />



---

## PROGRAM
```asm
ORG 0000H

MOV DPTR,#4500H
MOVx A,@DPTR
MOV R0,A

MOV 30H,#01H    
MOV 31H,#00H    
LOOP:
MOV A,30H
MOV B,R0
MUL AB
MOV 32H,A        
MOV 33H,B       
MOV A,31H
MOV B,R0
MUL AB

ADD A,33H        
MOV 31H,A

MOV 30H,32H      

DJNZ R0,LOOP


MOV DPTR,#4501H
MOV A,30H
MOVX @DPTR,A

INC DPTR
MOV A,31H
MOVX @DPTR,A

HERE: SJMP HERE
END

```
OUTPUT

<img width="1907" height="1011" alt="Screenshot 2026-10-24 142547" src="https://github.com/user-attachments/assets/da1785a9-dabc-4e51-8bcb-e1255f77845c" />


RESULT

Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.

---

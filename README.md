
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program. 

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**

<img width="700" height="420" alt="image" src="https://github.com/user-attachments/assets/6b9c4665-fa07-44bd-943d-cc05669d2eb1" />

**MEMORY WINDOW:**

Before execution: D:0x40H:
<BR>
<BR>
<BR>
<img width="700" height="420" alt="image" src="https://github.com/user-attachments/assets/cb626d7f-ed92-471d-adac-19fdf7f8821c" />

After execution: D:0x40H:
<BR>
<BR>
<BR>
<img width="700" height="420" alt="image" src="https://github.com/user-attachments/assets/6b9c4665-fa07-44bd-943d-cc05669d2eb1" />


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**

<img width="700" height="420" alt="image" src="https://github.com/user-attachments/assets/50547314-8929-4db7-89ec-0fbfc9bcea6d" />

**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<BR>
<BR>
<BR>
<BR>
<img width="700" height="420" alt="image" src="https://github.com/user-attachments/assets/cb626d7f-ed92-471d-adac-19fdf7f8821c" />

After execution:
D:0x40H:
<BR>
<BR>
<BR>
<img width="700" height="420" alt="image" src="https://github.com/user-attachments/assets/50547314-8929-4db7-89ec-0fbfc9bcea6d" />

**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.


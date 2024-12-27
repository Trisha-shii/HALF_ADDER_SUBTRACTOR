# HALF_ADDER_SUBTRACTOR #

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder:**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor:**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor



**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

**Truthtable:**

![image](https://github.com/user-attachments/assets/a6eb520d-5e92-4fff-a342-eeec4e778087)

![image](https://github.com/user-attachments/assets/ebc25ced-e3de-4a99-ae3c-93bb14693305)

**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Trisha Priyadarshni Parida

RegisterNumber: 212224230293

*/

```i)HALF ADDER

module ha(a,b,sum,carry);
input a,b;
output sum,carry;
assign sum= (a ^ b);
assign carry= ( a & b);
endmodule

ii)HALF SUBTRACTOR

module hs(a,b,difference,borrow);
input a,b;
output difference,borrow;
assign difference= (a ^ b);
assign borrow= ( ~a & b);
endmodule
```

**RTL:**

<img width="697" alt="EXP 3 DE HA RTL" src="https://github.com/user-attachments/assets/20a046af-b279-4c16-b038-2f5f623e4ceb" />

<img width="628" alt="EXP 3 DE HS RTL" src="https://github.com/user-attachments/assets/82ddd95f-c241-43c5-95b0-14fb94a0afe1" />


**TIMING Waveform:**

<img width="960" alt="EXP 3 DE HA WF" src="https://github.com/user-attachments/assets/f4ce932a-0fe0-4bc1-9b4d-1e2ed7583ed3" />


<img width="959" alt="EXP 3 DE HS WF" src="https://github.com/user-attachments/assets/6be21860-02b8-46a2-b3e3-03c5f65f3897" />


**Result:**

Half-Adder-and-Half Subtractor-circuit implemented.


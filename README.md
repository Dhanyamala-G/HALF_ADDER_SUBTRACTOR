# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**
<br>
<img width="525" height="319" alt="image" src="https://github.com/user-attachments/assets/036586dc-fe43-4523-a2da-d398f08f93ff" />
<img width="477" height="354" alt="image" src="https://github.com/user-attachments/assets/6ee99dbc-7b14-44f3-858e-944bd0f6f41d" />


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```
module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor g1(sum,a,b);
and g2(carry,a,b);
endmodule
```
```
module exp3(a,b,diff,borrow);
input a,b;
output diff,borrow;
xor difference(diff,a,b);
assign borrow=(~a)&b;
endmodule
```

**RTL Schematic**
<img width="1694" height="716" alt="image" src="https://github.com/user-attachments/assets/ff2e7573-2075-4541-805f-c4a8d72f1a46" />

<img width="1687" height="768" alt="image" src="https://github.com/user-attachments/assets/bd9934fa-088d-4138-966d-f320bcd0aa52" />


**Output/TIMING Waveform**
<img width="1916" height="589" alt="image" src="https://github.com/user-attachments/assets/a759c93d-70db-436e-814a-32acee0d54fa" />

<img width="1917" height="374" alt="image" src="https://github.com/user-attachments/assets/1bfb1d6d-570c-4667-8db3-9330ad983c69" />


**Result:**
Thus implementation of Half adder and Half subtractor is completed and verified successfully using verilog programming.

# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**
**Full adder**
```
//full adder 
module ex04(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;

//internal nets
wire sl,cl,c2;

//Instantiate logic gate primitives
xor (sl,a,b);
and(cl,a,b);
xor(sum,sl,cin);
and(c2,sl,cin);
or(cout,c2,cl);

endmodule
```
**FULL SUBTRACTOR**
```
module ex04a (df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:Hari Priya.S RegisterNumber:212223220029
*/

**RTL Schematic**
FULL ADDER
![image](https://github.com/HARIPRIYASIVAKUMAR/FULL_ADDER_SUBTRACTOR/assets/147477684/cd3cb36a-0e9e-4411-aa3a-fa7cf3592c58)
FULL SUBTRACTOR
![image](https://github.com/HARIPRIYASIVAKUMAR/FULL_ADDER_SUBTRACTOR/assets/147477684/3600e88e-9536-4145-9cd2-0c98f579d383)


**Output Timing Waveform**
FULL ADDER
![image](https://github.com/HARIPRIYASIVAKUMAR/FULL_ADDER_SUBTRACTOR/assets/147477684/bc3cee9f-92fd-407e-bb3a-048124bc7853)
FULL SUBTRACTOR
![image](https://github.com/HARIPRIYASIVAKUMAR/FULL_ADDER_SUBTRACTOR/assets/147477684/e3b25c53-7bae-403a-870a-4d7169027b7e)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




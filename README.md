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

**Full Adder:**

![Screenshot 2025-04-15 111052](https://github.com/user-attachments/assets/fee5a37e-af32-44ed-b296-9e7b7556d6c8)

**Full Subtractor:** 

![Screenshot 2025-04-15 111106](https://github.com/user-attachments/assets/a178ebf5-511f-4835-863b-705d7059fb77)

**Procedure**

**Full Adder:**

1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit. 

3.The circuit consists of XOR, AND, and OR gates. 

4.Compile the design, verify its functionality through simulation. 

5.Implement the design on the target device and program it.

**Full Subtractor:** 

1.Follow the same steps as for the full adder.
 
2.Draw the full subtractor circuit using schematic design. 

3.The circuit includes XOR, AND, OR gates to perform subtraction. 

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**
```python
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: KISHORE.S
RegisterNumber: 212224230130
*/

//FULL ADDER//
module DE(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule

//FULL SUBRACTOR//
module DE(diff,carry,a,b,c);
input a,b,c;
output diff,carry;
xor(diff,a,b,c);
assign carry= (~a)&c | (~a)&b | (b&c);
endmodule

```

**RTL Schematic**

FULL ADDER:
![Screenshot 2025-04-15 102628](https://github.com/user-attachments/assets/71c48fec-200c-4a33-aa24-0fd6e63fef9c)

FULL SUBRACTOR:
![Screenshot 2025-04-15 104359](https://github.com/user-attachments/assets/2b4ad385-819d-4533-92c7-56474abab325)


**Output Timing Waveform**

FULL ADDER:
![Screenshot 2025-04-15 104037](https://github.com/user-attachments/assets/5062e2bc-9e02-417a-ae5f-230ff9700ca7)
FULL SUBRACTOR:
![Screenshot 2025-04-15 105131](https://github.com/user-attachments/assets/f9bc3381-7635-44a1-8735-6562fa7ce4b7)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




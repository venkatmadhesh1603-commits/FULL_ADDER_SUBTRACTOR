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
Truth Table for Full adder:
A	B	C	Sum	Carry
0	0	0	0	0
0	0	1	1	0
0	1	0	1	0
0	1	1	0	1
1	0	0	1	0
1	0	1	0	1
1	1	0	0	1
1	1	1	1	1

Truth Table for Full subractor:
A	B	B  Diff	Bout
0	0	0	0	0
0	0	1	1	1
0	1	0	1	1
0	1	1	0	1
1	0	0	1	0
1	0	1	0	0
1	1	0	0	0
1	1	1	1	1

**Procedure**
Full adder Procedure:
Take three inputs: A, B, and Carry-in (Cin).

Add the three inputs using logic gates.

Use XOR gates to get the Sum of the three bits.

Use AND and OR gates to find the Carry-out (Cout).

Sum shows the final bit, and Cout shows the carry generated.

Full subractor Procedure:
Take three inputs: A, B, and Borrow-in (Bin).

Subtract B and Bin from A using logic gates.

Use XOR gates to get the Difference.

Use AND and OR gates to get the Borrow-out (Bout).

Difference shows output bit, and Bout shows borrow needed.

**Program:**
```
module exp4(A,B,C,X,Y,Z,Sum,Carry,Diff,Bout);
input A,B,C,X,Y,Z;
output Sum,Carry,Diff,Bout;
xor g1(Sum,A,B,C);
assign Carry= (A&B)|(B&C)|(A&C);
xor g2(Diff,X,Y,Z);
assign Bout= (~X&Z)|(Y&Z)|(~X&Y);
endmodule

```

**RTL Schematic**
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9bc423b0-a61c-4004-8a08-45b2191656fa" />


**Output Timing Waveform**
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d7978395-5f4a-4edc-beeb-298e0814f9ae" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




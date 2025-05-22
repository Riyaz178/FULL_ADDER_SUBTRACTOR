## FULL ADDER SUBTRACTOR

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
Full adder
module levi(a,b,cin,sum,carry);
input a,b,cin;
output carry,sum;
wire w1,w2,w3,w4;
xor(w1,a,b);
assign sum=w1^cin;
and(w2,a,b);
and(w3,a,cin);
and(w4,b,cin);
assign carry=w2|w3|w4;
endmodule
full subtractor
module arm(a,b,bin,diff,bo);
input a,b,bin;
output bo,diff;
wire w1,w2,w3,w4;
xor(w1,a,b);
assign sum=w1^bin;
assign bo=(~a)&bin|(~a)&b|b&bin;
endmodule

**RTL Schematic**
Full adder

![WhatsApp Image 2025-04-24 at 20 21 59_053ab804](https://github.com/user-attachments/assets/c65f6cb1-0471-453f-90c9-38596c221609)
Full subtractor
![WhatsApp Image 2025-04-24 at 20 22 31_17d66a3b](https://github.com/user-attachments/assets/075e91d0-18cf-48a5-a0e8-4a7e840b7006)




**Output Timing Waveform**
Full adder
![436172995-f77ebd2d-fc3a-4c1a-bfc6-193f9627cbb2](https://github.com/user-attachments/assets/ec8e8540-88ae-49da-8507-f4e91535a7a8)
Full subtractor

![image](https://github.com/user-attachments/assets/d01f5093-8641-42de-8e1e-be76747a637a)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




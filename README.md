**EXP4:FULL ADDER AND SUBTRACTOR**

NAME: MUBARAK .R

REF NO : 24900694

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

1)FULL ADDER

![image](https://github.com/user-attachments/assets/92ac7f22-1659-4593-8be4-5121049a3360)


2)FULL SUBRACTOR

![image](https://github.com/user-attachments/assets/d332f58f-96d6-4f53-aa55-b78c14b4e7be)


**Procedure**

1. Type the program in Quartus software.

2. Compile and run the program.

3. Generate the RTL schematic and save the logic diagram.

4. Create nodes for inputs and outputs to generate the timing diagram.

5. For different input combinations generate the timing diagram.

**Program:**

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:


**1)FULL ADDER**


module fulladder(a,b,cin,sum,carry);

input a,b,cin;

output sum,carry;

assign sum=( (a ^ b)^cin);

assign carry= ( (a & b)| ( cin &(a ^ b )));

endmodule


**2)FULL SUBRACTOR**


module fs(a,b,bin,difference,borrow);

input a,b,bin;

output difference,borrow;

assign difference= ( (a ^ b)^bin);

assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));

endmodule


**RTL Schematic**

1)FULL ADDER

![screen shot of full adder](https://github.com/user-attachments/assets/f1c970dd-b2cf-49f4-891b-8932f53ccf31)


2)FULL SUBRACTOR

![screen shot of full subractor](https://github.com/user-attachments/assets/5dc0c99f-8c0a-43fc-8b5b-75693b413da6)


**Output Timing Waveform**

1)FULL ADDER

![wave form of full adder](https://github.com/user-attachments/assets/ffe82816-e05f-4fa0-8c20-547af099ef6d)


2)FULL SUBRACTOR

![waveform of full subractor](https://github.com/user-attachments/assets/41ada423-3864-4da5-b4e2-f4cad302d584)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.

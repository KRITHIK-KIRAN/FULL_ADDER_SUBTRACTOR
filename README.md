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

**Procedure**

Write the detailed procedure here.

Full Adder:

Program:
```
module fa1_df(sum, cout, a, b, cin);
    output sum;
    output cout;
    input a;
    input b;
    input cin;

	 wire w1,w2,w3;
	 assign w1=a^b;
	 assign w2=a&b;
	 assign w3=w1&cin;
	 assign sum=w1^cin;
	 assign cout=w2|w3;
endmodule
```

Rtl:
<img width="904" height="308" alt="image" src="https://github.com/user-attachments/assets/164344cd-50df-4694-a07f-2acdb80f965f" />

Output:
<img width="1034" height="574" alt="image" src="https://github.com/user-attachments/assets/77205060-ebec-4c99-a21d-0757a1757a78" />

Full Subtractor:

Program:
```
module fullsub(df, bo, a, b, bin);
    output df;
    output bo;
    input a;
    input b;
    input bin;
endmodule
```

Rtl:
<img width="1002" height="655" alt="image" src="https://github.com/user-attachments/assets/89517bfa-293b-4001-b15d-1a2bab23b56e" />

Outpu:
<img width="1027" height="574" alt="image" src="https://github.com/user-attachments/assets/f4fead91-0e55-48d0-a02e-78e9f0297e37" />




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




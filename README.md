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
Full Adder
![Screenshot 2024-12-07 215748](https://github.com/user-attachments/assets/9e3a17bb-3854-4def-800b-b89154fa38d4)

Full Subtractor
![Screenshot 2024-12-07 215757](https://github.com/user-attachments/assets/62dbb03b-64fe-4024-bd72-1901fa24b9e0)

**Procedure**
1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.


**Program:**
Full Adder

module fadd(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule 
Full Subtractor

module fsub(a, b, bin, diff, borrow);
input a, b, bin;
output diff, borrow;
wire w1, w2, w3, w4;
xor g1(diff, a, b, bin);
not g2(w1, a);          
and g3(w2, w1, bin);    
and g4(w3, w1, b);     
and g5(w4, b, bin);     
or g6(borrow, w2, w3, w4); 
endmodule
Developed by:Ravivarman vv
RegisterNumber:24006127


**RTL Schematic**
Full Adder
![Screenshot 2024-12-07 220117](https://github.com/user-attachments/assets/7294cb34-9f6e-47b4-a3b2-7690fc672b79)
Full Subtractor
![Screenshot 2024-12-07 220128](https://github.com/user-attachments/assets/39e89def-db08-43f7-84b1-cf0529da7b01)

**Output Timing Waveform**
Full Adder
![Screenshot 2024-12-07 220146](https://github.com/user-attachments/assets/05710c08-3717-4532-9e4a-ab4f10df0442)
Full Subtractor
![Screenshot 2024-12-07 220155](https://github.com/user-attachments/assets/eef5fb39-292f-4f6a-90ce-cbdc24abe7da)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




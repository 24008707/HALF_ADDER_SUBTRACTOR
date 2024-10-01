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

Figure -01 HALF ADDER

![HALF ADDER](https://github.com/user-attachments/assets/9d35f773-dd4b-4858-aaec-175bb8a5c448)

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

Figure -02 HALF Subtractor

![SUBRACTOR](https://github.com/user-attachments/assets/8300d9b3-ee63-494b-a41a-f70fd408328a)

**Truthtable

![tabular](https://github.com/user-attachments/assets/d945ac84-ffdc-491d-9021-0cb3c192c3a8)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Half_adder
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
 assign sum = a^b;
 assign carry = a & b;
endmodule

Half_subtractor
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule

Developed by: RegisterNumber:*/ VISAL R    24008707

**RTL Schematic**
![ciruit dia](https://github.com/user-attachments/assets/1cdcbb0b-31d8-408c-a576-a803a19b6671)

**Output/TIMING Waveform**
![output (2)](https://github.com/user-attachments/assets/d4a02121-5660-44d1-9150-78e9286962a1)
![output 2](https://github.com/user-attachments/assets/02f44016-e374-4b67-be21-387d06ae72d9)

**Result:**
To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming its are verifid

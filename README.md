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
![Half Adder Subtractor](https://github.com/CynthiaMehul/HALF_ADDER_SUBTRACTOR/assets/150319444/f6a16e31-c978-412c-bd71-086c7d1df268)

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: Cynthia Mehul RegisterNumber: 212223240020*/
```
module HALF_ADDSUB(a,b,sum,carry,D,Bo);
input a,b;
output sum,carry,D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
//TYPE HERE THE COMMAND FOR SUM GENERATION IN GATE LEVEL MODELLING
xor(sum,a,b);
//TYPE HERE THE COMMAND FOR CARRY GENERATION IN GATE LEVEL MODELLING
and(carry,a,b);
//Type logic for half subtractor difference D,Borrow Bo using gate level modelling
wire abar;
not(abar,a);
xor(D,a,b);
and(Bo,abar,b);
endmodule
```

**RTL Schematic:**
![exp3 output2](https://github.com/CynthiaMehul/HALF_ADDER_SUBTRACTOR/assets/150319444/9974c7c9-7293-4314-a1eb-aadc1ec361de)

**Waveform:**
![exp3 output1](https://github.com/CynthiaMehul/HALF_ADDER_SUBTRACTOR/assets/150319444/ad0edc83-470f-452b-8270-7c26f694ee3b)

**Result:**
Hence, Half-Adder and Half Subtractor circuit is implemented.

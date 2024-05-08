# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

# AIM:

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

# Equipments Required:

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

# Full Adder and Full Subtractor

## Full Adder

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

# Figure -1 FULL ADDER**

## Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

# Truthtable

## FULL-ADDER :

![324896908-b73708d8-ce3f-40da-b040-99d233112615](https://github.com/ameeshajeffi/FULL_ADDER_SUBTRACTOR/assets/150773598/3c562108-1d86-4d2f-9c36-b60ae87d1af8)

## FULL-SUBTRACTOR:

![324896946-02ffec74-0350-464a-b40b-cd0a0ed4c714](https://github.com/ameeshajeffi/FULL_ADDER_SUBTRACTOR/assets/150773598/e58474a2-be20-41bd-af1d-88a50b4bd5a5)

# Procedure

STEP-1 Open Quartus Prime software.

STEP-2 Create a new project and select the target FPGA device.

STEP-3 Design and implement the full adder/subtractor using Verilog or VHDL within a new HDL file.

STEP-4 Add the HDL file to the project and compile the design.

STEP-5 Program the FPGA with the compiled design to test the functionality of the full adder/subtractor.

# Program:
```
module fulladdsub(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
assign sum=a^b^c;
assign carry= a&b | a&c | b&c;
wire a0;
not (a0,a);
assign BO= b&c | a0&c | a0&b;
assign DIFF=a^b^c;
endmodule
```
# RTL Schematic:

![324897506-b96c91fd-7229-4032-a423-fff3456402c8](https://github.com/ameeshajeffi/FULL_ADDER_SUBTRACTOR/assets/150773598/f8858097-a861-4d6c-b264-5892196a137b)

# Output Timing Waveform

![324897236-7a0bd143-b720-44cd-a354-dd3ee537888a](https://github.com/ameeshajeffi/FULL_ADDER_SUBTRACTOR/assets/150773598/cc18c9b6-29c7-4305-91f3-b03261c50898)

# Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




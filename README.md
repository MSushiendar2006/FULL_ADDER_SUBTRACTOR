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

## Figure -1 FULL ADDER

## Full Subtractor

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin




## Procedure:

```
STEP-1 Open Quartus Prime software.
STEP-2 Create a new project and select the target FPGA device.
STEP-3 Design and implement the full adder/subtractor using Verilog or VHDL within a new HDL file.
STEP-4 Add the HDL file to the project and compile the design.
STEP-5 Program the FPGA with the compiled design to test the functionality of the full adder/subtractor.
```

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

## Truthtable:
### FULL-ADDER : 
![image](https://github.com/arbasil05/FULL_ADDER_SUBTRACTOR/assets/144218037/fe8a893e-7da2-49a7-b5f0-1fc2e4a1976f)
### FULL-SUBTRACTOR:
![image](https://github.com/arbasil05/FULL_ADDER_SUBTRACTOR/assets/144218037/532faf89-78bb-4299-b8ca-9a967622141a)


# RTL:
![image](https://github.com/arbasil05/FULL_ADDER_SUBTRACTOR/assets/144218037/776457b8-69fb-4627-87a1-4c58b479b2c9)


# Output:
![image](https://github.com/arbasil05/FULL_ADDER_SUBTRACTOR/assets/144218037/db43bff2-a490-4df7-8099-e8dfba237afa)



# Result:

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.


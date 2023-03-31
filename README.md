# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure
1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represent one for difference and the other for borrow.

5.End the verilog program using keyword endmodule.

## Program:
/*
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Preethi.A.A 
RegisterNumber:212222110035

Half subtractor:
module halfsubtractor(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference = (A^B);
assign Borrow = (~A&B);
endmodule

Full subtractor:
module fullsub(A,B,C,Difference,Borrow);
input A,B,C;
output Difference,Borrow;
assign Difference = (A^B^C);
assign Borrow = (~A&(B^C)|(B&C));
endmodule
```
*/

## Output:
##Logic gates:
Half subtractor:

![halfsub](https://user-images.githubusercontent.com/120115840/229187128-29dd3607-ce3d-4e7a-808b-7a05e3ccc7aa.png)

Full subtractor:

![fullsub](https://user-images.githubusercontent.com/120115840/229187267-7bbd0bf9-e747-4726-8243-a3c3c20667b7.png)

## Truthtable
Half subtractor:

![halfsub tt](https://user-images.githubusercontent.com/120115840/229187684-9df87cde-1022-44ea-9c7b-ab9da051b102.png)

Full subtractor:

![fullsubtt](https://user-images.githubusercontent.com/120115840/229187750-e2b05857-61c9-44fd-817b-9d28e08f6e81.png)

##  RTL realization
Half subtractor:

![halfsub logicgates](https://user-images.githubusercontent.com/120115840/229187989-215258bc-c8de-4301-85ef-b8b57ecb42c3.png)

Full subtractor:

![fullsub logic](https://user-images.githubusercontent.com/120115840/229188097-a3922fe0-2230-41b3-a173-4076371d43bf.png)

## Timing diagram
Half subtractor:

![halfsub waveform](https://user-images.githubusercontent.com/120115840/229188214-13caec9d-ba52-42ab-a3d3-5c90fe53e6e1.png)

Full subtractor:

![fullsub waveform](https://user-images.githubusercontent.com/120115840/229188321-7cf3a871-6b1c-45a3-943f-02d33a768724.png)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

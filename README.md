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
*Connect the supply (+5V) to the circuit.
*Switch ON the main switch.
*If the output is 1, then the led glows.
## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: DHARSHAN D
RegisterNumber:  23001663
1. Program to design a half subtractor:
module ex4(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=((~a)&b);
endmodule 
2. Program to design a full subtractor:
module ex41(a,b,bin,diff,borr);
input a,b,bin;
output diff,borr;
assign diff=a^b^bin;
assign borr=((~a)&b)|(b&bin)|((~a)&bin);
endmodule
```
## OUUTPUT:
## Truthtable:
## HALF SUBTRACTOR:
![image](https://github.com/dharshan7200/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/138850116/8c7c2108-82eb-4d03-a164-766a02b4e78e)
## FULL SUBTRACTOR:
![image](https://github.com/dharshan7200/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/138850116/1b8921ff-558d-44fe-bde0-4678d0391978)
## RTL realization:
## HALF SUBTRACTOR:
![image](https://github.com/dharshan7200/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/138850116/6c983604-445d-4648-890c-48740414f01e)
## FULL SUBTRACTOR:
![image](https://github.com/dharshan7200/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/138850116/a4f49bde-4083-4c14-b74f-2ce04c24e7ab)
## Timing diagram:
## HALF SUBTRACTOR:![image](https://github.com/dharshan7200/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/138850116/53f37e09-eb35-4e29-909e-25a3eeb72a0e)
## FULL SUBTRACTOR:![image](https://github.com/dharshan7200/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/138850116/cdfd6a13-e4af-4cd1-b9fa-8c82df0e8c21)
## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

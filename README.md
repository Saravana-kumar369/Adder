### Ex. No. 3
### Date:8.4.23
# Implementation of half adder and full adder circuit using Verilog HDL
## Aim :
To design and implement half adder and full adder circuit using Verilog HDL and verify its truth table.
## Components Required:
1.	Laptop with Quartus software and modelsim software.
## Theory:
Adders are digital circuits that carry out addition of numbers.
### 1.	Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.
#### Truth table
 ![image](https://github.com/rvinifa/Adder/assets/133735746/469bd63c-0a45-4d7a-a68a-b68bb36c637a)

Sum = A’B+AB’ = A  ![image](https://github.com/rvinifa/Adder/assets/133735746/aac88cdf-2255-4bff-971b-a3657a2c19e3)
     B
Carry=AB
#### Logic Diagram
 ![image](https://github.com/rvinifa/Adder/assets/133735746/c65758e5-f597-4204-8ab1-41575bd0c3e3)

### 2.	Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry. 
#### Truth table
  .![image](https://github.com/rvinifa/Adder/assets/133735746/f8301e61-a457-4c1b-97fd-1adcb039df01)

#### K-map Simplification
 ![image](https://github.com/rvinifa/Adder/assets/133735746/03a38bcf-2642-4391-8424-7011b94e6002)

Sum =A’B’Cin+A’BCin’+ABCin+AB’Cin’=A ![image](https://github.com/rvinifa/Adder/assets/133735746/d522a34d-a1e9-4d96-9b19-3cbc259cb7e2)
 B ![image](https://github.com/rvinifa/Adder/assets/133735746/f52fbe53-60e0-4c19-b728-7efb11d08248)
 Cin
Carry = AB + ACin+BCin
#### Logic Diagram
 ![image](https://github.com/rvinifa/Adder/assets/133735746/982f8574-d184-49fa-a66a-4201ea48c58d)

## Procedure:
1.	Type the program in Quartus software.
2.	Compile and run the program.
3.	Generate the RTL schematic and save the logic diagram.
4.	Create nodes for inputs and outputs to generate the timing diagram.
5.	For different input combinations, generate the timing diagram.


## Program:
### HALF ADDER
```
module Exp3a(a,b,sum,carry);
input a,b;
output sum,carry;
xor (sum,a,b);
and (carry,a,b);
endmodule
```
### FULL ADDER
```
module Exp3b(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor (sum,a,b,c);
wire x,y,z;
and (x,a,b);
and (y,b,c);
and (z,c,a);
or (carry,x,y,z);
endmodule
```

## RTL Schematic:
### HALF ADDER
![Screenshot (109)](https://github.com/Saravana-kumar369/Adder/assets/117925254/534ef671-a8db-48a8-9bc6-e1aaea2fbbb5)
### FULL ADDER
![Screenshot (113)](https://github.com/Saravana-kumar369/Adder/assets/117925254/e6da2976-6199-46d3-92f3-38e7f8f7c5d9)

## Timing Diagram:

### HALF ADDER
![Screenshot (110)](https://github.com/Saravana-kumar369/Adder/assets/117925254/bad6d768-efba-46a2-a8a8-375cebd72779)
### FULL ADDER
![Screenshot (114)](https://github.com/Saravana-kumar369/Adder/assets/117925254/093def7b-f2e7-465b-9e8a-7488c6d734f5)

## Result:
Thus the half adder and full adder circuits are designed and implemented and the truth tables are verified.

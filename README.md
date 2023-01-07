# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure

1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:
```
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: KANISHKAR M
RegisterNumber: 22007816 

using NAND:

module combo1(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=(~c & b & a);
assign q=(~d & c & ~a);
assign r=(c & ~b & a);
assign f=(~(~p & ~q & ~r));
endmodule

using NOR:
module combo2(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=( c & ~b & a);
assign q=( d & ~c & a);
assign r=( c & ~b & a);
assign f=((( p | q | r)));
endmodule

## RTL realization

## Output:

## RTL

using NAND:

![exp 4 rtl nand](https://user-images.githubusercontent.com/118886772/211156473-a9cc42a0-6b11-4256-94bd-7ca0533108a8.png)

using NOR:

![rtl exp 4 nor](https://user-images.githubusercontent.com/118886772/211156445-850c4f94-adf3-4f62-a605-f2172330fdd1.png)

## Timing Diagram

using NAND:

![time exp 4 nand](https://user-images.githubusercontent.com/118886772/211156458-d9c0dc06-11f4-4cdf-b18b-d85ded771917.png)

using NOR:

![time exp 4 nor](https://user-images.githubusercontent.com/118886772/211156453-946b1066-11fe-470c-ac72-a5be2f91597e.png)

##Truth Table

using NAND

![truth exp 4 nand](https://user-images.githubusercontent.com/118886772/211156514-f96704ec-0c95-466f-902e-9a306a45a718.png)

using NOR

![truth exp 4 nor](https://user-images.githubusercontent.com/118886772/211156522-0e181bff-572f-4956-b744-000d5d40380d.png)

## Result:

Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.

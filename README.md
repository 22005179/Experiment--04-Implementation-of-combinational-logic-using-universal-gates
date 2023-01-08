 AIM:
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

 Procedure
 Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programmi
COMBINATION 1

module combone(A,B,C,D,F

input A,B,C,D;

output F;

wire P,Q,R;

assign P=(~(~C & B & A));

assign Q=(~(~D & C & A));

assign R=(~(C & ~B & A));

assign F=~(P & Q & R);

endmodule

COMBINATION 2

module combtwo(A,B,C,D,F);

input A,B,C,D;

output F;

wire P,Q,R,S;

assign P = (C & ~B & A);

assign Q = (D & ~C & A);

assign R = (C & ~B & A);

assign S = (~(P | Q | R));

assign F = (~s);

endmodule


Developed by:K.ABINAYA 
RegisterNumber:22005179

COMBINATION 1

 RTL realization


![Screenshot (25)](https://user-images.githubusercontent.com/121557762/211180158-a893c7b1-963c-4351-8f28-e6071a9dddc9.png)


TIMING DIAGRAM



![Screenshot (26)](https://user-images.githubusercontent.com/121557762/211180224-6a8e5c8d-1269-432a-a3e2-3b4cadf55a6a.png)




TRUTH TABLE


![Screenshot (27)](https://user-images.githubusercontent.com/121557762/211180262-ca18992e-9621-4297-a195-e72a4ae786b8.png)



COMBINATION 2

RTL REALIZATION

![Screenshot (28)](https://user-images.githubusercontent.com/121557762/211180005-61133042-072a-4f7c-8f6b-37f4bc705c40.png)NATION 2



TIMING DIAGRAM 

![Screenshot (29)](https://user-images.githubusercontent.com/121557762/211180007-9fa0ea24-9d74-4e1c-98bb-65ebfe3038af.png)

TRUTH TABLE

![Screenshot (30)](https://user-images.githubusercontent.com/121557762/211180010-9deec638-70c6-4600-96a4-db6ea502dbb5.png)




Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.

## Name : Stephen raj.y
## Register No : 212223230217

# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.

##Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
#### Figure -01 HALF ADDER 
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCi

#### Figure -02 FULL ADDER 

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)



Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
module half_adder(A,B,C,S);
input A,B;
output S,C;
assign c=A&B;
assign S=A^B;
endmodule
module FullAdder(a,b,carryin,sum,carryout);
input a,b,carryin;
output sum,carryout;
wire x,p,q,r;
xor(x,b,carryin);
xor(sum,x,a);
and(p,a,b);
and(q,b,carryin);
and(r,a,carryin);
or(carryout,p,q,r);
endmodule
Output:
Logic symbol & Truth table:
## Truth Table:
## Half Adder:
![Screenshot 2023-12-29 142255](https://github.com/23002248/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151701774/dc1097e7-297a-4da3-8b2c-959cd68b1cdd)
## Full Adder:
:![Screenshot 2023-12-29 142341](https://github.com/23002248/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151701774/ed76b507-f262-4587-b6f7-9c6a76da07b8)

## RTL realization
## Half Adder:
![Screenshot 2023-12-29 141726](https://github.com/23002248/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151701774/edceb5e9-4c0d-44cc-8629-82ef0eec5b9b)
## Full Adder:
![Screenshot 2023-12-29 141845](https://github.com/23002248/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151701774/cef4dbed-275d-4d23-86c0-4eaeef5cd25d)

### TIMING DIAGRAM:
## Half Adder :
![Screenshot 2023-12-29 142006](https://github.com/23002248/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151701774/6f80e955-d704-4e44-9a56-057832577bd2)
## Full Adder:
![Screenshot 2023-12-29 142051](https://github.com/23002248/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151701774/7bf04267-67f7-4c97-8124-69ad22bc265a)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming.


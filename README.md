# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin


#### Figure -01 HALF ADDER 
 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -02 FULL ADDER 
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
```
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: AMRUTHA RAJSHEKER
RegisterNumber: 212222110003

Half Adder Program:

module HalfAdder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule

Full Adder Program:

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=((a^b)^c);
assign carry=((a&b)|(b&c)|(c&a));
endmodule
```
# Logic symbol & Truthtable
![image](https://user-images.githubusercontent.com/119475943/232210195-850d4088-6fc9-4669-a7b5-0887dca35006.png)


# RTL realization
HALF ADDER
![3](https://user-images.githubusercontent.com/119475943/232223825-69bc9dcd-ee1b-49b4-bcbc-3cdf641c7aaa.png)

FULL ADDER
![4](https://user-images.githubusercontent.com/119475943/232223825-69bc9dcd-ee1b-49b4-bcbc-3cdf641c7aaa.png)

### Output:
### RTL
### TIMING DIAGRAM
HALF ADDER
![image](https://user-images.githubusercontent.com/119475943/232223977-6e4685c3-e7b2-4852-a29d-1e529dc91427.png)

FULL ADDER
![image](https://user-images.githubusercontent.com/119475943/232223985-52346be5-0d6e-487e-bc9e-6a9121f3ffed.png)

### TRUTH TABLE 
![image](https://user-images.githubusercontent.com/119475943/232224025-871652f0-0782-4e24-9f70-623aca2e46ef.png)

### Result:
Thus the half adder and full adder are studied and the truth table for different logic gates are verified.


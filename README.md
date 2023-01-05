Developed by: ROHIT JAN D  
Reference number: 22005894  

## AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
* Hardware 
  - PCs, 
  - Cyclone II , 
  - USB flasher  
* Software  
  - Quartus prime  
Theory Adders are digital circuits that carry out addition of numbers.

## Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B  
Carry = AB

## Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin  
Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

### Figure -02 FULL ADDER 

## Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
## Program:  

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.  
```
HALF ADDER  

module HalfAdder(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule  

FULL ADDER  

module FullAdder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = ((a^b)^c);
assign carry = ((a&b)|(b&c)|(c&a));
endmodule  
```  
## LOGIC SYMBOL:  
<img width="145" height="145" alt="and-gate" src="https://user-images.githubusercontent.com/118707073/210394807-f0abebca-ed18-4300-9533-c8be717bf3d1.png">          <img width="145" height="145" alt="or-gate" src="https://user-images.githubusercontent.com/118707073/210394842-56ad9780-b0bf-4091-8330-58f7b0a9b1bb.png">          <img width="145" height="145" alt="xor-gate" src="https://user-images.githubusercontent.com/118707073/210394854-0f7bebd5-084e-42a4-b621-a96ba502d937.png">




# Output:  

## RTL Realization:  

- ### HALF ADDER:  
![Screenshot_20230103_052924](https://user-images.githubusercontent.com/118707073/210356210-d6d8ea30-5cf7-44c7-a334-688f8656dff6.png)
- ### FULL ADDER:  
![Screenshot_20230103_050235](https://user-images.githubusercontent.com/118707073/210356563-ef254816-8e38-42a5-b2a4-7e8eb00b63ee.png)

## TIMING DIAGRAM:  
- ### HALF ADDER:  
![Screenshot_20230105_052521](https://user-images.githubusercontent.com/118707073/210776790-0291d821-209d-4c7b-97e7-6ce9a609f2de.png)

- ### FULL ADDER:  
![Screenshot_20230105_053556](https://user-images.githubusercontent.com/118707073/210776909-29999c44-ebcb-4842-a2d5-35bb748ca1d5.png)

## TRUTH TABLE:  
- ### HALF ADDER:  
![WhatsApp Image 2023-01-03 at 21 21 18](https://user-images.githubusercontent.com/118707073/210396385-88c8d334-817f-438d-a83a-76ff5151a49a.jpg)


- ### FULL ADDER:  
![WhatsApp Image 2023-01-03 at 21 21 18](https://user-images.githubusercontent.com/118707073/210396429-e8b265c9-05a8-4cc8-b3ed-e540335a6e7d.jpg)


## Result:  
Thus the Implementation of Half Adder and Full Adder circuit are studied and the truth table for different logic gates are verified.

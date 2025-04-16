### Name: V Rakshita
### Reg no: 212224100049

# EXP 3 - HALF ADDER AND HALF SUBTRACTOR

## **AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

## **Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

## **Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

## **Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

## **Procedure**

1. Open Quartus and create a new project. Go to File -> New -> Verilog HDL File and type the program.

2. Compile and run the program.

3. Then go to Tools -> NetList Viewers -> RTL Viewer and generate the RTL schematic and save the logic diagram.

4. Then go to File -> New -> University program VWF. Create nodes for inputs and outputs to generate the timing diagram.

5. Give different input combinations and go to Run Functional Simulation to generate the timing diagram.


## **Program:**

```
module HALFADDERSUBTRACTOR(a,b,sum,carry,difference,bout);
input a,b;
output sum,carry,difference,bout;
assign sum = a ^ b;
assign carry = a & b;
assign difference = a ^ b;
assign bout = ~a & b;
endmodule
```

## **Truth Table and Logic Diagram:**

![Screenshot (244)](https://github.com/user-attachments/assets/42aba29b-2443-4091-aeb7-1d7d8e7cd8c1)

![Screenshot (236)](https://github.com/user-attachments/assets/64071c05-e733-4e44-a094-692b2ecc0da6)

## **Waveform:**
![Screenshot (237)](https://github.com/user-attachments/assets/759e80f8-d091-4f9f-b993-08afc3d14249)

## **Result:**
A half adder and half subtractor circuit has been designed and its truth table has been verified in Quartus using Verilog programming.

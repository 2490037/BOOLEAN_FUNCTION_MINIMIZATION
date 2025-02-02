### NAME : PRANAV S
### REG NO : 24900037
### EXPERIMENT 2 : IMPLEMENTATION OF BOOLEAN FUNCTION MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

Boolean Function Minimization is the process of reducing a Boolean expression to its simplest form without changing its functionality. This minimization reduces the number of gates and inputs required, optimizing circuit design.

Logic Gates: Fundamental building blocks like AND, OR, and NOT gates are used to implement Boolean expressions.
Karnaugh Map (K-map): A graphical technique for minimizing Boolean expressions by grouping terms based on commonalities.
The given Boolean functions can be minimized as follows:

F1 = A’B’C’D’ + AC’D’ + B’CD’ + A’BCD + BC’D
The terms can be simplified using K-map techniques to reduce the complexity of the circuit.
F2 = xy’z + x’y’z + w’xy + wx’y + wxy
Similar simplification can be done for this function to reduce the gate count.
The resulting minimized expressions are implemented using Verilog HDL and simulated on the Quartus Prime tool. The outputs can then be verified on an FPGA board (e.g., Cyclone II).

**Logic Diagram**

![de_ex02](https://github.com/user-attachments/assets/8db62afb-ea43-47ce-85af-50605d210908)


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

```
module boolean_function_minimization(a, b, c, d, w, x, y, z, f1, f2);
 input a, b, c, d, w, x, y, z;
 output f1, f2;
 wire x1, x2, x3, x4, x5, x6, x7, x8, x9, x10;
 assign x1 = (~a) & (~b) & (~c) & (~d);
 assign x2 = (a) & (~c) & (~d);
 assign x3 = (~b) & (c) & (~d);
 assign x4 = (~a) & (b) & (c) & (d);
 assign x5 = (b) & (~c) & (d);
 assign f1 = x1 | x2 | x3 | x4 | x5;
 assign x6 = (x) & (~y) & (z);
 assign x7 = (~x) & (~y) & (z);
 assign x8 = (~w) & (x) & (y);
 assign x9 = (w) & (~x) & (y);
 assign x10 = (w) & (x) & (y);
 assign f2 = x6 | x7 | x8 | x9 | x10;
 endmodule
```





**RTL realization**

![Screenshot (60)](https://github.com/user-attachments/assets/0f4f6ac7-9e7e-4aa4-8521-373c487d70c6)


**Timing Diagram**

![Screenshot (62)](https://github.com/user-attachments/assets/45b6ef16-0880-4422-8156-81cc4a71d095)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.


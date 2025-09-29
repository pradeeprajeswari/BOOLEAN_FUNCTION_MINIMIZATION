# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

## Developed by: MADHUMITHA R R
## RegisterNumber:212224240083*/
    module EXP_2_BOOLEAN_MIN(a,b,c,d,w,x,y,z,f1,f2);
    input a,b,c,d,w,x,y,z;
    output f1,f2;
    wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
    not(adash,a);
    not(bdash,b);
    not(cdash,c);
    not(ddash,d);
    and(p,bdash,ddash);
    and(q,adash,b,d);
    and(r,a,b,cdash);
    or(f1,p,q,r);
    not(ydash,y);
    and(s,ydash,z);
    and(t,y,x);
    and(u,w,y);
    endmodule

**RTL realization**

**Output:**

<img width="1091" height="936" alt="image" src="https://github.com/user-attachments/assets/20bb0224-1115-4206-af5f-eda730dc7eb7" />
**RTL**

**Timing Diagram**
<img width="1831" height="440" alt="image" src="https://github.com/user-attachments/assets/f891386c-ca89-4379-9ba3-bd3bf5220826" />


**Result:**
Thus,the program is verified.

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.


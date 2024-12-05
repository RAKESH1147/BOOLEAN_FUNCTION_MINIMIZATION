# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**


**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

      module booleanfunction(a,b,c,d,w,x,y,z,f1,f2);
      
      input a,b,c,d,w,x,y,z;
      
      output f1,f2;
      
      wire adash,bdash,cdash,ddash,ydash,p,q,r,s,t,u;
      
      not(adash,a);
      
      not(bdash,b);
      
      not(cdash,c);
      
      not(ddash,d);
      
      not(ydash,y);
      
      and(p,bdash,ddash);
      
      and(q,adash,b,d);
      
      and(r,a,b,cdash);
      
      or(f1,p,q,r);
      
      and(s,ydash,z);
      
      and(t,x,y);
      
      and(u,w,y);
      
      or(f2,s,t,u);
      
      endmodule

/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

**Developed by:RAKESH.K.S RegisterNumber:24006757**


**RTL REALIZATION**
![RTL OUTPUT2](https://github.com/user-attachments/assets/23c90f29-f2f0-41de-af53-6894e121241e)


**TIMING WAVEFORM**
![TIMING WAVEFORM 2](https://github.com/user-attachments/assets/f73c6d10-e294-4492-b070-c7d9899300f7)

**TRUTH TABLE**
![TRUTH TABLE 2](https://github.com/user-attachments/assets/43035bb6-4efc-4938-a801-c2f3258f54d9)


**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.


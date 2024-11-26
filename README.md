# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

![Screenshot 2024-11-26 101928](https://github.com/user-attachments/assets/a45cb19c-f5e7-40f7-b0d7-2dabaeaa3e13)


**Truthtable**

![Screenshot 2024-11-26 102020](https://github.com/user-attachments/assets/51d7dc16-a22e-455b-9166-ba6777d7ac20)


**Procedure**

1.Type the program in qartus software.     
2.Compile and run the program.    
3.Generate the RTL schematic and save the logic diagram.             
4.Create nodes for inputs and outputs to generate the timing diagram.       
5.For different input combination generate the timimg diagram.    

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

    module ex4(sum,cout,a,b,cin);
    output sum;
    output cout;   
    input a;   
    input b;   
    input cin;  
    wire s1,c1,c2;   
    xor(s1,a,b);
    and(c2,s1,cin);     
    or(cout,c2,c1);   
    endmodule   
    
    module exp4a(df, bo, a, b, bin);   
    output df;     
    output bo;    
    input a;    
    input b;    
    input bin;    
    wire w1,w2,w3 ;     
    assign w1-a^b;    
    assign w2=(-a&b);    
    assign w3=(-w1&bin);     
    assign df-w1 bin;      
    assign bo-w2/w3;    
    endmodule    
    
Developed by: Vasanth N   
RegisterNumber: 24000697
*/

**RTL Schematic  FULL-ADDER**

![Screenshot 2024-11-26 102132](https://github.com/user-attachments/assets/5a590aa0-b5cd-4bb5-b8ee-8afad684c328)



**FULL-SUBTRACTOR**


![Screenshot 2024-11-26 102227](https://github.com/user-attachments/assets/e09a70aa-d702-4dec-a523-4ece78716f5b)


**Output Timing Waveform FULL-ADDER**

![Screenshot 2024-11-26 102304](https://github.com/user-attachments/assets/ccd50e65-945f-4fc5-82b7-5bb3b9f88a08)


**FULL-SUBTRACTOR**

![Screenshot 2024-11-26 102440](https://github.com/user-attachments/assets/5c617246-beb0-4bc4-a0a2-a94f8c00f364)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.




# Experiment:04 Half Subtractor and Full subtractor
## Implementation of Half subtractor and Full subtractor circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure:
1. Open Quartus and create a new project by selecting "File" > "New Project Wizard."
2. Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
3. Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
4. Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
5. Open the newly created Verilog or VHDL file and write the code for your combinational logic.
6. To compile the project, click on "Processing" > "Start Compilation" in the menu.
7. Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
8. If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
9. Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".
10. Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
11. Give the Input Combinations according to the Truth Table amd then simulate the Output Waveform.

## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: SOMEASVAR R
RegisterNumber:  212221230103
```
## HALF SUBTRACTOR:
```
module exp4(a,b,difference,borrow);
input a,b;
output difference,borrow;
wire x;
xor (difference,a,b);
not (x,a);
and (borrow,x,b);
endmodule
```
## ADD SUBTRACTOR:
```
module exp4(a,b,difference,borrow);
input a,b;
output difference,borrow;
wire x;
xor (difference,a,b);
not (x,a);
and (borrow,x,b);
endmodule
```

## Output:

## Truthtable:
### HALF SUBTRACTOR:
![image](https://github.com/SOMEASVAR/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/93434149/8517260f-f424-482a-b069-72565a0839a6)

### FULL SUBTRACTOR:
![image](https://github.com/SOMEASVAR/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/93434149/f668bb60-a1d1-4e9d-a3aa-34bfbe1f36ab)


##  RTL realization:

### HALF SUBTRACTOR:
![image](https://github.com/SOMEASVAR/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/93434149/4d6def39-c8ee-4e5d-96ba-6c27e1b744e7)

### FULL SUBTRACTOR:
![image](https://github.com/SOMEASVAR/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/93434149/ecaa4c4e-12bc-47aa-8cbd-b5838a51dd99)

## Timing diagram:
### HALF SUBTRACTOR:
![image](https://github.com/SOMEASVAR/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/93434149/f5a5aef6-50e9-48e5-ae92-ba86b851c264)

### FULL SUBTRACTOR:
![image](https://github.com/SOMEASVAR/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/93434149/2bc08dde-f5f1-4afe-a201-a5af6952f73a)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.

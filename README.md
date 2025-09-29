# Lab 05 - Combinatorial Logic

In this lab, you’ve learned real world applications of digital logic, as well
as how to assemble your own Verilog modules. In addition, you’ve learned how
the constraints file maps your inputs and outputs to real pins on the FPGA.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Lab Questions
This lab helped us see how small logic circuits can be treated like building blocks and connected to make bigger systems. We practiced writing Verilog modules, then used a top-level file to pull them all together. We also learned how the constraints file is what actually links my design to the physical FPGA board, so the switches and LEDs work as expected. The main takeaway is that digital design is very modular—you can reuse pieces, connect them differently, and quickly build more complex systems.

### 1 - Explain the role of the Top Level file.
The top-level file is basically the “main” for the hardware design. It doesn’t run step by step like a program, but it wires everything together. In this lab, the top file connected Circuit A’s output into Circuit B and mapped switches and LEDs so we could test the design on the FPGA.

### 2 - Explain the function of the Constraints file.
The constraints file is what ties the Verilog code to the actual hardware. It tells Vivado which FPGA pins each switch, LED, or other I/O is connected to, and also sets the voltage standard. Without it, the FPGA wouldn’t know which physical components to use.

### 3 - Was the selection of Minterm and Maxterm correct for each circuit? What would you have chosen?
Yes, the choices were correct. Circuit A used Maxterms, which matched the way its truth table was set up, and Circuit B used Minterms, which was a better fit for its truth table. If I swapped them, the logic equations would be longer and more complicated, so the given choices were the best.

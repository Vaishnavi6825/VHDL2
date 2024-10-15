# VHDL2
A Half Adder is a basic digital circuit that performs the addition of two single-bit binary numbers, producing a sum and a carry.<br>
The two inputs are denoted as A and B, and the outputs are:  <br>
Sum: A ⊕ B (XOR of A and B) <br>
Carry: A ⋅ B (AND of A and B)<br>

`Aim:`

To design and implement a Half Adder using three different Verilog modeling styles: Dataflow, Behavioral, and Structural modeling. <br>
The goal is to verify the functionality of the Half Adder by simulating it and capturing the output waveforms.<br>

`Apparatus Required:`

-Xilinx Vivado or any Verilog-compatible IDE for simulation. <br>
-Computer with Verilog HDL installed.<br>

`Code Implementation:`

-Dataflow Model: <br>
In this model, the circuit is described using logical expressions. The dataflow model relies on assign statements to represent the logical flow of data.<br>

module half_adder_dataflow(input a, input b, output sum, output carry);<br>
  // XOR gate for sum<br>
  assign sum = a ^ b;<br>
  // AND gate for carry<br>
  assign carry = a & b;<br>
endmodule<br>

-Behavioral Model: <br>
The behavioral model uses an always block to describe the functionality of the Half Adder at an abstract level. It mimics how the circuit behaves without specifying exact hardware.

module half_adder_behavioral(input a, input b, output reg sum, output reg carry);<br>
  always @(*) begin<br>
    sum = a ^ b;    // XOR operation for sum<br>
    carry = a & b;  // AND operation for carry<br>
  end<br>
endmodule<br>

-Structural Model: <br>
The structural model is a low-level description where the design is expressed using basic logic gates (AND, XOR). This is closest to actual hardware representation.

module half_adder_structural(input a, input b, output sum, output carry);<br>
  xor(sum, a, b);<br>
  and(carry, a, b);<br>
endmodule<br>

![WhatsApp Image 2024-10-15 at 15 55 39_71944e19](https://github.com/user-attachments/assets/1bc52f5d-509f-4f1a-a0ad-85c7130137b0)

`Output Waveform:`

![WhatsApp Image 2024-10-15 at 15 49 24_c974fbe4](https://github.com/user-attachments/assets/10ef55a6-6431-4f3e-b908-763017861fe6)

`Result:`

The Half Adder was successfully designed and implemented using Dataflow, Behavioral, and Structural models in Verilog. <br>
The simulation results show correct functionality for each model, with the Sum and Carry matching the expected truth table values.<br>





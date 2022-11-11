# EE-2.301 : Introduction to Verilog

This module is basic introduction Verilog and System Verilog. It introduces the basic digital design and testbench concepts. It is specifically targeted towards fresh engineering graduates who have had exposure to undergraduate digital diesign but have never used Verilog or any other Hardware Description Language.

# Training and Exercise Material

- [**Lesson-1**]: Learning Material: https://www.chipverify.com/verilog/verilog-tutorial
  - The material covers the Verilog concepts comprehensively and provides example exercises or each topic. Make sure you execute every example in https://edaplayground.com . It is highly recommended to play around with the examples to get the maximum benefit out of the material. For example, if you are simulating a modulo-10 counter from the material, after successfully simulating it, try one or two different modulo counters to fully understand the concepts. [_Estimated Time: 24 hours_]

- [**Lesson-2**]: Prepare Verilog modules at behavioural level, gate primitive level and transistor primitive level for the primitive blocks given below and simulate for various inputs  `0, 1, X` and `Z`, observe and explain the outputs.
  - tristate Inverter,
  - 2-input NAND,
  - 2-input MUX,
  - D-Latch,
  - D-Flip-Flop,
  - Tristate Inverter with weak pull up
  
An example for an inverter is provided below:

```verilog
// example for an inverter
2
3 module inv_beh (output Y, input I);
4 assign Y = ~I;
5 endmodule
6
7 // available gate primitives in Verilog are:
8 // and, nand, or, nor, xor, nor, but, not, 
9 // bufif0, bufif1, notif0, notif1, 
10 // tran, trainif0, tranif1
11 module inv_gate (output Y, input I);
12 not(Y,I);
13 endmodule
14
15 // available transistor primitives in Verilog are:
16 // nmos, pmos, cmos
17 module inv_tran (output Y, input I);
18 pmos p1(Y,1,I);
19 nmos n1(Y,0,I);
20 endmodule
```

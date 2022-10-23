# Task 1 Logbook

## Creating environment

In lab 0, I install and create an linux environment in my windows laptop. Linux environment is more like a commend line operating system, which is user-unfriendly, but programmable. I installed a ubuntu terminal and it can run code under this virtual platform. I also installed verilator and gtkwave, which allows me to start my task in the little Vbuddy.

## Task 1, creating a counter

In task 1, I first created a counter using hardware description language (system verilog/.sv file). The module has three inputs and one 8-bit output. The counter counts when there is a rising clock edge, adding either 0 or 1 depending on enable value. If the reset value is high at rising clock edge, the counter will be reset to zero.

Then I also create a testbench file using C++ in VScode. The testbench file is a template for all other testbench files. In the file, a simulation is implemented. The program run 300 clock cycles, and the reset value is set to one every 15 cycles. The counter output is constantly monitered.

Then, by doing a short cut in a presetting shell script, the verilator inputs both counter.sv and counter_tb.cpp and output a Vcounter.mk file. The file is then convert to a excutable file called Vcounter through GNU tools.

Vcounter is a excutable file that can be used in gtkWave to generate a simulated waveform for each cycle. The program successfully generating a counting output in gtkWave.

![Result from gtkWave](https://github.com/shaopyshaozi/Lab1-Counter/blob/master/images/gtkWave.jpg)

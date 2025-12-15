# D_FlipFlop

AIM:

To implement D flipflop using verilog and validating their functionality using their functional tables

SOFTWARE REQUIRED:

Quartus prime

THEORY

D Flip-Flop

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.


This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

<img width="578" height="387" alt="image" src="https://github.com/user-attachments/assets/fe445075-eaf6-4134-af73-a6a8b6d6dd73" />

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


PROGRAM
```
module Data_flipflop (
    input  wire clk,   // Clock input
    input  wire rst,   // Reset input (active high)
    input  wire D,     // Data input
    output reg  Q      // Output
);

always @(posedge clk) begin
    if (rst)
        Q <= 1'b0;     // Reset output
    else
        Q <= D;        // Store D on rising edge of clock
end

endmodule
```
Register number:25017522
Name: Karthi V

RTL LOGIC FOR FLIPFLOPS:
[RTL Viewer.pdf](https://github.com/user-attachments/files/24171704/RTL.Viewer.pdf)


TIMING DIGRAMS FOR FLIP FLOPS:
[export (1).bmp](https://github.com/user-attachments/files/24171723/export.1.bmp)


RESULTS:
We got the successful output

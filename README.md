# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
![image](https://github.com/karthikeyanpachiyappan/D-FLIPDLOP-NEGEDGE/assets/155143878/c407edc7-62b4-41d9-8d03-f95f93aead71)


This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/karthikeyanpachiyappan/D-FLIPDLOP-NEGEDGE/assets/155143878/d8cbfacd-c325-484f-a9cb-10327ee9730c)


Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/karthikeyanpachiyappan/D-FLIPDLOP-NEGEDGE/assets/155143878/82e1c286-fdc3-4e53-939f-03d9c8d4285d)


Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Declare ports for the D flip-flop module, specifying inputs (D, CLK) and outputs (Q, Q_bar).

2.Write Verilog code to create the functionality of the D flip-flop, triggered by the rising edge of the clock signal (posedge CLK).

3.Develop a Verilog testbench to simulate how the D flip-flop responds to different input scenarios.

4.Set up the testbench to test various combinations of input signals (D, CLK) to cover all possible states.

5.Confirm that the D flip-flop's outputs (Q, Q_bar) behave as expected according to its functional table.

6.Ensure that the design doesn't encounter race conditions or undefined states by analyzing the timing and sequence of input changes.

**PROGRAM**
```
Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by: Karthikeyan P
RegisterNumber: 212223230102
```
```verilog
module DFLIPFLOPNEGEDGE(D,Clock,reset,Q);
input D,reset,Clock;
output reg Q;
always @ (negedge Clock)
if(!reset)
Q <= 0;
else
Q <= D;
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/karthikeyanpachiyappan/D-FLIPDLOP-NEGEDGE/assets/155143878/425fe0a8-043d-45bd-9a44-055e554f3987)



**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/karthikeyanpachiyappan/D-FLIPDLOP-NEGEDGE/assets/155143878/a1fcddba-8c7d-4c43-a5b3-b70b535de589)



**RESULTS**

Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables.

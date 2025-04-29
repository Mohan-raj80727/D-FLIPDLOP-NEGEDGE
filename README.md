# NAME : MOHANRAJ.S
# REG NO: 212224100036

# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1.Declare ports for the D flip-flop module, specifying inputs (D, CLK) and outputs (Q, Q_bar).

2.Write Verilog code to create the functionality of the D flip-flop, triggered by the rising edge of the clock signal (posedge CLK).

3.Develop a Verilog testbench to simulate how the D flip-flop responds to different input scenarios.

4.Set up the testbench to test various combinations of input signals (D, CLK) to cover all possible states.

5.Confirm that the D flip-flop's outputs (Q, Q_bar) behave as expected according to its functional table.

6.Ensure that the design doesn't encounter race conditions or undefined states by analyzing the timing and sequence of input changes.


**PROGRAM**
~~~C
module exp6(D,clk,Q,Qbar);
input D,clk;
output reg Q;
output reg Qbar;
initial Q=0;
initial Qbar=1;
always @(posedge clk)
begin
Q=D;
Qbar=~D;
end
endmodule
~~~
 Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by: SARAVANA KUMAR
RegisterNumber:24900200


**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/user-attachments/assets/34ec605e-bdfa-453b-b691-951d7eb19c41)


**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/user-attachments/assets/c404f53c-6643-4c8f-a1c6-51d8c6f6951f)


# RESULTS:
The d-flipflop are the output is verified

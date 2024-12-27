# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using Verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, the D latch operates with an enable signal. That means, the output of the D flip-flop is insensitive to the changes in the input, D except for the active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has a single input D and two outputs Qtt & Qtt’. The operation of the D flip-flop is similar to the D Latch. However, this flip-flop affects the outputs only when the positive transition of the clock signal is applied instead of active enable. The following table shows the state table of the D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, the D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of the clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

/* write all the steps invloved */

**PROGRAM**



developed by Swetha Nivasini B R





registration number 24900367





module d_ff_neg_edge (d, clk, rst, q);
  input d, clk, rst;
  output reg q;

  always @(negedge clk or posedge rst) begin
    if (rst)
      q <= 0; // Reset the flip-flop
    else
      q <= d; // D input is passed to Q on the negative clock edge
  end
endmodule






**RTL LOGIC FOR FLIPFLOPS**



![image](https://github.com/user-attachments/assets/a855e0eb-ea35-487e-bc86-17f22be0d0e5)



**TIMING DIAGRAMS FOR FLIP FLOPS**




![image](https://github.com/user-attachments/assets/a597079c-0965-4e89-a4ef-ee97bd64b07f)



**RESULTS**




implemented D flipflop using Verilog and validated their functionality using their functional tables

# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by: Sundareswaran K
 RegisterNumber:212225040439
*/
```
module EXP6(input clk, reset, output reg [3:0] q);
    always @(posedge clk or posedge reset)
        if (reset) q[0] <= 0; else q[0] <= ~q[0];

    always @(negedge q[0] or posedge reset)
        if (reset) q[1] <= 0; else q[1] <= ~q[1];

    always @(negedge q[1] or posedge reset)
        if (reset) q[2] <= 0; else q[2] <= ~q[2];

    always @(negedge q[2] or posedge reset)
        if (reset) q[3] <= 0; else q[3] <= ~q[3];
endmodule
```

**RTL LOGIC FOR 4 Bit Ripple Counter**
<img width="1015" height="353" alt="Screenshot 2026-05-28 234652" src="https://github.com/user-attachments/assets/de980edc-2aa9-4c2c-b34e-17cdc0bcc17b" />

**TIMING DIGRAMS FOR 4 Bit Ripple Counter**
<img width="1036" height="541" alt="Screenshot 2026-05-28 234705" src="https://github.com/user-attachments/assets/c04a3315-38cb-4450-b806-dcbcf7881943" />

**RESULTS**

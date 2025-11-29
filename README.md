### ENCODER 8TO3 DATAFLOW Modelling

**AIM:**

To implement  Encoder 8 To 3 in Dataflow Modelling using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:** Quartus prime

**THEORY**

**Encoder 8 To 3**

The 8 to 3 line Encoder is also known as Octal to Binary Encoder. In 8 to 3 line encoder, there is a total of eight inputs, i.e., D0, D1, D2, D3, D4, D5, D6, and D7 and three outputs, i.e., A0, A1, and A2. In 8-input lines, one input-line is set to true at a time to get the respective binary code in the output side. Below are the block diagram and the truth table of the 8 to 3 line encoder.

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/0bc242c1-eb9e-4c47-afe5-30428470efc3)

Figure 01  Block Diagram of Encoder 8 * 3

**Truth Table**

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/35496b14-ae6e-4cd1-9abd-d6736b576575)

The logical expression of the term A0, A1, and A2 are as follows:

A0 = D1 + D3 + D5 + D7

A1 = D2 + D3 + D6 + D7

A2 = D4 + D5 + D6 + D7

Logical circuit of the above expressions is given below:

![image](https://github.com/naavaneetha/ENCODER8TO3DATAFLOW/assets/154305477/95acaee6-c873-4c75-89eb-ef09fb158053)

Figure 02  Encoder 8 * 3

**Procedure**

1.Create a Verilog module with 2 inputs and 4 outputs.

2.Write dataflow logic using assign statements to convert 8-bit input into 3-bit output.

3.Ensure only one input is HIGH at a time.

4.Compile and simulate the design.

5.Verify output using the truth table.

**PROGRAM**
module encoder4to2 (
    input  wire [3:0] in,   // 4 input lines
    output reg  [1:0] out   // 2 output lines
);
    always @(*) begin
        case (in)
            4'b0001: out = 2'b00;
            4'b0010: out = 2'b01;
            4'b0100: out = 2'b10;
            4'b1000: out = 2'b11;
            default: out = 2'bxx;  // Invalid case
        endcase
    end
endmodule


Developed by:Mugilarasi E

RegisterNumber:25017644


**RTL LOGIC FOR Encoder 4 To 2 in Dataflow Modelling**
<img width="1920" height="1080" alt="Screenshot (60)" src="https://github.com/user-attachments/assets/f785731b-3b24-4ebb-ac0e-a39399b13351" />


**TIMING DIGRAMS FOR Encoder 4 To 2 in Dataflow Modelling**
<img width="1920" height="1080" alt="Screenshot (61)" src="https://github.com/user-attachments/assets/b36550f2-d10d-446f-a3e0-e0e6e270c4e7" />



**RESULTS**
Thus the encoder4to2 dataflow modelling using verilog and validating their functionality using their functional tables is implemented and verified.




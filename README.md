# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

1.Type the program in Quartus software.
2.Compile and run the program.
3.Generate the RTL schematic and save the logic diagram.
4.Create nodes for inputs and outputs to generate the timing diagram.
5.For different input combinations generate the timing diagram.


**PROGRAM**
```
/* Program for flipflops and verify its truth table in quartus using Verilog programming.
 
 module t_ff (t, clk, rst, q);
  input t, clk, rst;
  output reg q;

  always @(posedge clk or posedge rst) begin
    if (rst)
      q <= 0;          // Reset the flip-flop
    else if (t)
      q <= ~q;         // Toggle when T=1
    // else: q holds its value automatically
  end
```
endmodule

Developed by:Yuvasri V
RegisterNumber:25008890
*/

**RTL LOGIC FOR FLIPFLOPS**
<img width="938" height="816" alt="519881108-f5c1ea41-bdd1-44da-85cc-14af2a22352e" src="https://github.com/user-attachments/assets/8b0257d8-941d-4a76-bac3-4cf56c6ed437" />

**TIMING DIGRAMS FOR FLIP FLOPS**
<img width="1314" height="558" alt="519881158-f8b36c24-98a3-4bc0-8e0b-dc0bc505da0b" src="https://github.com/user-attachments/assets/1eec67ff-1754-41fb-a711-a81121da11fb" />


**RESULTS**
Thus, the T flipflop is implemented using and their operations are verified using Verilog programming.

# TITLE : DECADE SYNCHRONOUS UPCOUNTER WITH T-FLIP FLOP
## AIM
Design and simulate Decade Synchronous Upcounter with T flip flop using Verilog.

## EQUIPMENTS REQUIRED
1. Hardware – PCs, Cyclone II , USB flasher
2. Software – Quartus prime

## THEORY
#### Decade Counter: 
A decade counter counts ten different states and then reset to its initial states. 
A 4-bit decade synchronous counter can also be built using synchronous binary counters to produce a count sequence from 0 to 9. A standard binary counter can be converted to a decade (decimal 10) counter with the aid of some additional logic to implement the desired state sequence. After reaching the count of “1001”, the counter recycles back to “0000”. We now have a decade or Modulo-10 counter.

![Truth-table-of-Decade-counter](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/34c13164-49f2-459b-b3dd-2d1af36750b3)
#### T-Flip Flop:
In T flip flop, "T" defines the term "Toggle".We can construct the "T Flip Flop" by making changes in the "JK Flip Flop". The "T Flip Flop" has only one input, which is constructed by connecting the input of JK flip flop. This single input is called T.

![t ff truth](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/f5d3b7db-8e7d-44c5-9991-73a3991164f8)

### TRUTH TABLE
![decade truth](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/a3776f0a-e858-4dd8-bd33-66ffb6156f69)


### STATE DIGRAM
![State-Diagram-for-the-Decade-Counter](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/30345ea3-f721-4c53-825e-c02bdae6de96)

### LOGIC DIAGRAM
![decade logic](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/14842e6c-496c-4223-a4a4-9ccc637283db)

#### T- FLIP FLOP LOGIC DIAGRAM
![t-flip-flop logic](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/749522b2-5117-472d-8ee1-e950e4860979)

## NETLIST DIAGRAM
![simurtl](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/db8e9cdd-4d5d-4bd5-9041-6d89ea219df4)

## TIMING DIAGRAM
![simutime](https://github.com/Jenishajustin/Simulation-project--Digital-Electronics/assets/119405070/496172f4-da64-4f9f-be52-e7fe4674bf6d)

## PROGRAM
```
Program to simulate Decade synchronous upcounter with T- Flip Flop using Verilog.
NAME : JENISHA.J
REG.NO : 212222230056

module simuproj (clk,a);
input clk;
output reg[0:3]a;
always@(posedge clk)
begin
a[0]=((a[3]&a[0])|(a[1]&a[2]&a[3]))^a[0];
a[1]=(a[2]&a[3])^a[1];
a[2]=(a[3]&(~a[0]))^a[2];
a[3]=1^a[3];
end
endmodule
```
## RESULT
Thus the synchronous decade upcounter has been implemented in Quartus Prime and output is verified by using Verilog programming through its truth table.
## REFERENCE
https://www.electronics-tutorials.ws/counter/count_3.html

https://www.geeksforgeeks.org/counters-in-digital-logic/

https://www.codecubix.eu/electronics/synchronous-decade-counter/

https://www.javatpoint.com/t-flip-flop-in-digital-electronics

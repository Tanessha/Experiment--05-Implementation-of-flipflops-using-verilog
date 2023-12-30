## NAME: Tanessha Kannan
## REGISTER NUMBER: 23006086
## EXPT NO: 5- Implementation of flipflops using verilog programming.
## AIM: 
To implement all the flipflops using verilog and validating their functionality using their functional tables
## HARDWARE REQUIRED:  
PC, Cyclone II , USB flasher 
## SOFTWARE REQUIRED: 
Quartus prime
## THEORY:

### SR flip-flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/85d414da-2a2b-403a-9572-4be015e90c10)

This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of SR flip-flop.


![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/7a7c3361-83e4-4945-a5c8-d52102b9f5cd)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop. Present Inputs Present State Next State


![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/6cd6c306-c2dd-4a4e-ae12-fb15e3ff9c1a)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.


![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/3e6e3fe7-6651-4054-a120-8444f7e80956)


The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)

### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop. 

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/42723817-cf4f-4c22-8fde-8b8d28e5af79)

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/04be9c06-df16-4fcd-8f45-b09d0c962cb9)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/f3f3a552-63d8-46e0-ac97-3b8be9ef6680)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure. 

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/073e8ea3-11f5-4c7f-a116-626d0c83228e)

This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/2b43a9ab-09fd-479e-afa8-2ff6caf2523f)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/8295fe1a-bd51-4e13-9c7b-65385da9a73b)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/081db516-668a-44a1-8491-29c2a8ce9930)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/cc850c2a-d90e-4974-acbf-67af97cf521f)

This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/Tanessha/Experiment--05-Implementation-of-flipflops-using-verilog/assets/140876194/0082a7e9-c658-4878-96ec-e3e1dfb9182b)

From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

## Procedure
1.Create a New Project:

Open Quartus and create a new project by selecting "File" > "New Project Wizard."
Follow the wizard's instructions to set up your project, including specifying the project name, location, and target device (FPGA).
2.Create a New Design File:

Once the project is created, right-click on the project name in the Project Navigator and select "Add New File."
Choose "Verilog HDL File" or "VHDL File," depending on your chosen hardware description language.
3.Write the Combinational Logic Code:

Open the newly created Verilog or VHDL file and write the code for your combinational logic.
4.Compile the Project:
To compile the project, click on "Processing" > "Start Compilation" in the menu.
Quartus will analyze your code, synthesize it into a netlist, and perform optimizations based on your target FPGA device.
5.Analyze and Fix Errors:

If there are any errors or warnings during the compilation process, Quartus will display them in the Messages window.
Review and fix any issues in your code if necessary. View the RTL diagram.
6.Verification:

Click on "File" > "New" > "Verification/Debugging Files" > "University Program VWF".

Once Waveform is created Right Click on the Input/Output Panel > " Insert Node or Bus" > Click on Node Finder > Click On "List" > Select All.
## SR Flip-Flop
### PROGRAM:
module flipflops(S,R,clk,Q,Qbar);

input S,R,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=S|((~R)&Q);

Qbar=R|((~S)&(Qbar));

end

endmodule

## RTL REALIZATION:
![WhatsApp Image 2023-12-20 at 20 51 46_0243905f](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/62199ab4-4cd3-4fc8-b90c-05d94714239c)
## TRUTHTABLE:
![Screenshot 2023-12-20 210134](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/114ae702-3b48-4ef1-88d8-c56805bff757)
## OUTPUT WAVEFORM:
![WhatsApp Image 2023-12-20 at 20 51 47_09b12a69](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/364ab21f-1102-452c-886b-c261a54ba340)

## JK Flip-Flop
### PROGRAM:
module flipflops(J,K,clk,Q,Qbar);

input J,K,clk;

output reg Q;

output reg Qbar;

initial Q=0;

initial Qbar=1;

always @(posedge clk)

begin

Q=(J&(~Q))|((~K)&Q);

Qbar=((~J)&(Qbar))|K&(~Qbar);

end

endmodule

# RTL REALIZATION:
![WhatsApp Image 2023-12-20 at 20 52 22_d891bc7e](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/24b47dc7-cd5e-4828-8715-6475a175fb41)
## TRUTHTABLE:
![Screenshot 2023-12-20 211207](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/4b125e5e-b900-4589-8094-ba922575ecc0)
## Output Waveform:
![WhatsApp Image 2023-12-20 at 20 52 22_67c00636](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/9ea4f1dd-84fe-4169-8802-29062f57983c)

## T FLIPFLOP:
### PROGRAM:
module exp_5c(clk,T,q,qbar);

input clk,T;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin

q<=(T&~q)|(~T&q);

qbar<=~q;

end 

endmodule

## RTL REALIZATION:
![WhatsApp Image 2023-12-20 at 20 52 05_61a5a5ba](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/dab35cc8-87d1-474f-8955-9c8c8724a770)
## truthtable:
![image](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/b43c7e82-ac92-4c33-a21f-6a0b465906e5)
## WAVEFORM:
![WhatsApp Image 2023-12-20 at 20 52 05_8e6ca545](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/104519cf-9f8f-4425-a80d-ddd791872d8d)

## D flip flop:
### PROGRAM:
module exp_5d(d,clk,q,qbar);

input d,clk;

output q,qbar;

reg q,qbar;

always @(posedge clk)

begin 

q<=d;

qbar<=~q;

end 

endmodule

## RTL REALIZATION:
![WhatsApp Image 2023-12-20 at 20 52 35_af5bfd61](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/92e0d52a-cc75-4367-9585-5ca70e1e8dd1)
## TRUTH TABLE:
![image](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/98953d7a-6fba-4c01-a974-aee0ddc52274)
## WAVEFORM:
![WhatsApp Image 2023-12-20 at 20 52 35_d79a5a41](https://github.com/23011258/Experiment--05-Implementation-of-flipflops-using-verilog/assets/139842204/08641bde-ea79-4919-baae-9acc235aaaad)

## RESULTS
By this we have verified the truth table of JK, SR, D and T using verilog.

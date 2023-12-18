# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

 ![Screenshot 2023-12-18 204405](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/222a6ef8-2f43-4ebb-b992-77c399265279)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.

![Screenshot 2023-12-18 204412](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/a40907a8-1c59-450e-ae18-5d7b1d3d5e5b)

 

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State

![Screenshot 2023-12-18 204420](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/242ae440-fc17-4151-bc04-3c9758efcc4d)
 
By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

 ![Screenshot 2023-12-18 204432](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/154931f0-b75d-48cf-9a05-e1a5e4898b19)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state 

![Screenshot 2023-12-18 204723](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/c6b96d14-5fa3-456e-85f6-7b99396ff5cb)
table of D flip-flop.

 ![Screenshot 2023-12-18 204733](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/8e9b3237-df81-450a-88a3-981ca5b8351c)




Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

 ![Screenshot 2023-12-18 204747](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/665c3972-38a6-4b92-ae7d-d38df9ccae68)

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.

![Screenshot 2023-12-18 204915](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/63505092-6225-4527-8ce9-6db94eb991fb)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

 ![Screenshot 2023-12-18 204926](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/91e04757-5fbc-4917-b02f-47bc63b18dfb)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 ![download](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/c6e816db-fde5-41e1-a4f8-9f32c11b21c0)

 
 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

 ![Screenshot 2023-12-18 205209](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/06751c1a-4cec-4e36-a1af-6f7bc615cdbb)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.

![Screenshot 2023-12-18 205215](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/0fe08617-3ad3-4ed7-861a-ea6a0b539544)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State

![Screenshot 2023-12-18 205225](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/d01d25a8-e0f9-4a82-9baf-a99cecc090ab)

![images](https://github.com/Kathiresan-23013376/Experiment--05-Implementation-of-flipflops-using-verilog/assets/150008375/e9895ce4-d99a-4cd5-b989-dde61388f461)



From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Kathiresan-K
RegisterNumber: 23013376
*/






### RTL LOGIC FOR FLIPFLOPS 









### TIMING DIGRAMS FOR FLIP FLOPS 








### RESULTS 

# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure
1.Using nand gates and wires construct SR flipflop

2.Repeat same steps to construct J,K,D,T flip flops

3.Find RTL logic and timing diagram for all flipflop

4.End the program



### PROGRAM 
```
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: Dharanish MS
RegisterNumber:  23011819
```






# CODE:


## SR FLIP FLOP:

![Code](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/d9ddff60-4485-499d-abc9-079a07e591c5)



## D FLIP FLOP:

![code](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/e570a329-08f0-470f-adbf-f8b44eb07895)





## JK FLIP FLOP:

![code](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/14bda5c6-3dad-4083-a4ea-8c96a4a2826c)




## T FLIP FLOP:

![Code](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/41d1adf0-a5e0-4306-a1de-765b401fdd54)



# RTL DIAGRAM:



## SR FLIP FLOP:

![RTL](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/a8863068-6c1f-48b4-9c7f-e057b742de92)



## D FLIP FLOP:


![RTL](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/71f2925e-faf8-48f4-aa4c-037f8715eb86)



## JK FLIP FLOP:


![RTL](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/bc5afe51-c649-4252-9ad7-b39790bf37d1)



## T FLIP FLOP:

![RTL](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/375152e6-58bb-4b3a-a4f8-b30872e85758)



# TRUTH TABLE:



## SR FLIP FLOP:

![truth table](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/4bf5f26c-bdff-41e7-93eb-1f4960b9e751)



## D FLIP FLOP:


![truth table](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/8c5783ba-a9d1-4bac-b4ad-ff968b35d875)



## JK FLIP FLOP:


![truth table](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/48502ce3-96ef-4118-802f-2db13f8a0fb4)



## T FLIP FLOP:


![truth table](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/e7a1bb01-a8fc-4096-90ba-26fc686fb7c4)




# TIMING DIGRAMS :




## SR FLIP FLOP:

![Output](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/9bf1877f-94e4-40cb-aadb-f955899575d8)



## D FLIP FLOP:


![timing diagram](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/d0014f7f-5b64-4554-8451-3bf06ab620e6)



## JK FLIP FLOP:


![timing diagram](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/9b51429c-e3e7-490a-bac4-623051f53deb)



## T FLIP FLOP:


![Output](https://github.com/Harevasu/Experiment--05-Implementation-of-flipflops-using-verilog/assets/147985044/a4c24891-2513-42c4-922c-77017234cddd)






# RESULTS :


Thus, all the FLIP FLOPS are designed and the truth tables are verified using quartus software.

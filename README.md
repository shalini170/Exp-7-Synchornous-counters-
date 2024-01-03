# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

 
 

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure
/* write all the steps invloved */



### PROGRAM 
/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: shalini venkatesulu
RegisterNumber:23001992  
*/

##UP COUNTER

![Screenshot 2024-01-03 031932](https://github.com/shalini170/Exp-7-Synchornous-counters-/assets/151901983/de541b5f-f17d-4aa0-812f-7edfb61f724b)

##DOWN COUNTER

![Screenshot 2024-01-03 031938](https://github.com/shalini170/Exp-7-Synchornous-counters-/assets/151901983/3c5b813a-9521-4671-8fd8-53c6d30d7a3a)


##RTL

![Screenshot 2024-01-03 031953](https://github.com/shalini170/Exp-7-Synchornous-counters-/assets/151901983/8dda394c-f7e1-4758-b4fc-14d44e804b7b)



![Screenshot 2024-01-03 032001](https://github.com/shalini170/Exp-7-Synchornous-counters-/assets/151901983/31a62397-2632-4915-974a-ce3f81467842)


##OUTPUT

![Screenshot 2024-01-03 032016](https://github.com/shalini170/Exp-7-Synchornous-counters-/assets/151901983/a156b5d7-b0b1-4d4c-9c57-2e7514b7f84f)


![Screenshot 2024-01-03 032028](https://github.com/shalini170/Exp-7-Synchornous-counters-/assets/151901983/a1dc136b-06ad-4ed1-880f-1725b7c8cec5)

##RESULT



By this way we have verified the truth table of 4-bit upcounter using verilog








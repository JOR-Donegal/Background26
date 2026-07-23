# Logic and Memory

The first computer systems (e.g. ENIAC) required programmes to be hard wired, literally with jumper cables, dials and switches. A computer at the time looked like something out of a bad sci-fi movie!

From 1944 and the development of the EDIVAC computer, work began on holding computer programmes and data in electronics memory. In 1945 Jon Von Neumann proposed that a working computer system should consist of a processing unit or ALU, a control unit, and memory. We have looked at the ALU and at control in previous notes, let’s take a look at memory!
Firstly some terminology.

- A bit is a single binary digit and can be a one or a zero
- A nibble is a group of 4 bits
- A byte is a group of 8 bits
- A word is a group of 16 or more bits, we can have 32 bit words, 64 bit words etc.

In previous notes, we have built the bones of a simple 4 bit computer. Can we provide this computer with a small amount of 4-bit memory?

<figure>
<img src = "https://jor-donegal.github.io/Background26/images/fig19.jpg">
<figcaption>fig 19. A four bit register.</figcaption>
</figure>

In fact, the design is that of a 4 bit register. 

As previously, we will clock the circuit. When write is enabled, whatever is on the input bus will be copied to the registers. They can then be read at the output bus an unlimited number of times.

Once write enabled is switched off, any changes in the input bus will not be copied to the memory element. 

So now we have a single memory element, good to store a single nibble of data. How do we scale that up to make a useful quantity of memory?

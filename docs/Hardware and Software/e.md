# Digital Logic
In this section, I am going to build up gates into useful subsystems.

## The Set/Rest Latch
The first thing that we needed to do useful calculations with these gates was to have a way of storing numbers (remember, all numbers are represented in binary within the computer); this is the concept of _memory_. We need a circuit which can store a single bit of data; we call a circuit like this a _latch_. There are several types of latch available in TTL which were built into early computers (and are now integrated into much larger circuits).

<figure>
<img src = "https://jor-donegal.github.io/Background26/images/fig8.jpg">
<figcaption>Fig 8. SR Latch.</figcaption>
</figure>

One of these simple circuits was the _set-reset latch_ or _S-R Latch_. Very simple, if you raise the input S to a one, Q will set to 1 and ¯Q will reset to 0. If you raise the R input to 1, Q will reset to 0 and ¯Q will set to 1. Work your way through the circuit to confirm this!

One of the problem with this circuit is that if you raise S and R to 1 at the same time, the circuit acts in an unpredictable manner. Again, try working your way through the circuit to see.

Up to now, all the digital gates and circuits we have looked at have been deterministic, that means that for the inputs given, there is only one possible outcome. Once we start dealing with circuits which can store bits (memory) we need to understand the concept of _state_; a circuit can be in a particular state before we encounter it and the output of any action may depend on the state the circuit was in before we started.

## Clocks and Timing
In a real computer, most things are synchronised by a timing signal. Have a look at the circuit below where we introduce a timing signal, known as a _clock_. The AND gates block any inputs from either S or R until the clock signal is high. Now we can control when the set or reset command are sampled.

<figure>
<img src = "https://jor-donegal.github.io/Background26/images/fig9.jpg">
<figcaption>Fig 9. Clocked SR Latch.</figcaption>
</figure>


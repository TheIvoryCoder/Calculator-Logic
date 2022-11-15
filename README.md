# Calculator-Logic

Using arithmetic to make logic gates that can process basic input

NOTE: Any code below should be pasted into [Desmos Scientific Calculator](https://www.desmos.com/scientific) where you can see and edit it clearly.

For example, if you use a smart calculator that can store algebraic variables, then you could have two inputs: i_{1} and i_{2} (syntax for subtext in Desmos Scientific Calculator) then you can make logic gates. For example: 

AND gate 

i_{1}\cdot i_{2}

or a NOT gate

-\left(i_{1}-1\right)


Here is a list of all Logic Gates I have figured out so far:

----------------------------------------------------------------------------

**AND:**

i_{1}\cdot i_{2}

**NOT:**

-\left(i_{1}-1\right)

**NAND:**

-\left(i_{1}\cdot i_{2}-1\right)

**OR:**

-\left(\left(-\left(i_{1}-1\right)\cdot-\left(i_{2}-1\right)\right)-1\right)

**NOR:**

-\left(i_{1}-1\right)\cdot-\left(i_{2}-1\right)

**XOR:**

-\left(i_{1}\cdot i_{2}-1\right)\cdot-\left(-\left(i_{1}-1\right)\cdot-\left(i_{2}-1\right)-1\right)

----------------------------------------------------------------------------

And using these logic gates alone we can create a 2-BIT adder:

with 2 inputs and a carry:

i_{1}=0

i_{2}=0

c_{1}=0

And Two outputs. The SUM and the CARRY:

S=-\left(-\left(i_{1}\cdot i_{2}-1\right)\cdot-\left(-\left(i_{1}-1\right)\cdot-\left(i_{2}-1\right)-1\right)\cdot c-1\right)\cdot-\left(-\left(-\left(i_{1}\cdot i_{2}-1\right)\cdot-\left(-\left(i_{1}-1\right)\cdot-\left(i_{2}-1\right)-1\right)-1\right)\cdot-\left(c-1\right)-1\right)

C=-\left(\left(-\left(-\left(i_{1}\cdot i_{2}-1\right)\cdot-\left(-\left(i_{1}-1\right)\cdot-\left(i_{2}-1\right)-1\right)\cdot c-1\right)\cdot-\left(i_{1}\cdot i_{2}-1\right)\right)-1\right)

And the output is as follows:

![image](https://user-images.githubusercontent.com/94403790/201755159-7648150a-ae35-4d3d-824b-c3b4319ced1d.png)


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

a=0

b=0

c=0

And the code below returns a two-digit binary output:

\left(\left(ab-1\right)\left(\left(a-1\right)\left(b-1\right)-1\right)c-1\right)\left(\left(\left(ab-1\right)\left(\left(a-1\right)\left(b-1\right)-1\right)-1\right)\left(c-1\right)-1\right)-\left(\left(\left(ab-1\right)\left(\left(a-1\right)\left(b-1\right)-1\right)c-1\right)\left(ab-1\right)-1\right)\cdot10

Here is the truth table expected results

![image](https://user-images.githubusercontent.com/94403790/201755159-7648150a-ae35-4d3d-824b-c3b4319ced1d.png)

Using this we can then create a 4-bit adder:

a_{1}=0

a_{2}=0

a_{4}=0

a_{8}=0

b_{1}=0

b_{2}=0

b_{4}=0

b_{8}=0

c=0

S_{1}=\left(\left(a_{1}b_{1}-1\right)\left(\left(a_{1}-1\right)\left(b_{1}-1\right)-1\right)c-1\right)\left(\left(\left(a_{1}b_{1}-1\right)\left(\left(a_{1}-1\right)\left(b_{1}-1\right)-1\right)-1\right)\left(c-1\right)-1\right)

C_{1}=-\left(\left(\left(a_{1}b_{1}-1\right)\left(\left(a_{1}-1\right)\left(b_{1}-1\right)-1\right)c-1\right)\left(a_{1}b_{1}-1\right)-1\right)

S_{2}=\left(\left(a_{2}b_{2}-1\right)\left(\left(a_{2}-1\right)\left(b_{2}-1\right)-1\right)C_{1}-1\right)\left(\left(\left(a_{2}b_{2}-1\right)\left(\left(a_{2}-1\right)\left(b_{2}-1\right)-1\right)-1\right)\left(C_{1}-1\right)-1\right)

C_{2}=-\left(\left(\left(a_{2}b_{2}-1\right)\left(\left(a_{2}-1\right)\left(b_{2}-1\right)-1\right)C_{1}-1\right)\left(a_{2}b_{2}-1\right)-1\right)

S_{3}=\left(\left(a_{4}b_{4}-1\right)\left(\left(a_{4}-1\right)\left(b_{4}-1\right)-1\right)C_{2}-1\right)\left(\left(\left(a_{4}b_{4}-1\right)\left(\left(a_{4}-1\right)\left(b_{4}-1\right)-1\right)-1\right)\left(C_{2}-1\right)-1\right)

C_{3}=-\left(\left(\left(a_{4}b_{4}-1\right)\left(\left(a_{4}-1\right)\left(b_{4}-1\right)-1\right)C_{2}-1\right)\left(a_{4}b_{4}-1\right)-1\right)

S_{4}=\left(\left(a_{8}b_{8}-1\right)\left(\left(a_{8}-1\right)\left(b_{8}-1\right)-1\right)C_{3}-1\right)\left(\left(\left(a_{8}b_{8}-1\right)\left(\left(a_{8}-1\right)\left(b_{8}-1\right)-1\right)-1\right)\left(C_{3}-1\right)-1\right)

C_{4}=-\left(\left(\left(a_{8}b_{8}-1\right)\left(\left(a_{8}-1\right)\left(b_{8}-1\right)-1\right)C_{3}-1\right)\left(a_{8}b_{8}-1\right)-1\right)

O=S_{1}+S_{2}\cdot10+S_{3}\cdot100+S_{4}\cdot1000+C_{4}\cdot10000

The truth table for a 4 bit caclulator would have roughly 200 different possible combinations so instead i'll give an example:
lets say for imput a you put 1011
and for input b you put 1100
if you put that into an existing binary calculator (or worked it out yourself) you would get the answer: 10111
and this calculator will give the same output:
![image](https://user-images.githubusercontent.com/94403790/203427963-eb3231df-1e47-4227-b4f4-2e6189ea2e81.png)


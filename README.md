# Calculator-Logic
Using arithmetic to make logic gates that can process basic input
NOTE: Any code below should be pasted into [Desmos Scientific Calculator](https://www.desmos.com/scientific) where you can see and edit it clearly
For example, if you use a smart calculator that can store algebraic variables, then you could have two inputs: i_{1} and i_{2} (syntax for subtext in Desmos Scientific Calculator) then you can make logic gates. For example: AND gate \left(i_{1}\cdot i_{2}\right) or a NOT gate -\left(\left(i_{2}\right)-1\right)

Here is a list of all Logic Gates I have figured out so far:
AND:
\left(i_{1}\cdot i_{2}\right)
NOT:
-\left(\left(i_{2}\right)-1\right)
NAND:
-\left(\left(i_{1}\cdot i_{2}\right)-1\right)
OR:
-\left(\left(-\left(\left(i_{1}\right)-1\right)\cdot-\left(\left(i_{2}\right)-1\right)\right)-1\right)
NOR:
\left(-\left(\left(i_{1}\right)-1\right)\cdot-\left(\left(i_{2}\right)-1\right)\right)
XOR:
\left(-\left(\left(i_{1}\cdot i_{2}\right)-1\right)\cdot-\left(\left(\left(-\left(\left(i_{1}\right)-1\right)\cdot-\left(\left(i_{2}\right)-1\right)\right)\right)-1\right)\right)

And using these logic gates alone we can create a 2-BIT adder:

with 2 inputs and a carry:

i_{1}=0
i_{2}=0
c_{1}=0

And Two outputs. The SUM and the CARRY:

S=\left(-\left(\left(\left(-\left(\left(i_{1}\cdot i_{2}\right)-1\right)\cdot-\left(\left(\left(-\left(\left(i_{1}\right)-1\right)\cdot-\left(\left(i_{2}\right)-1\right)\right)\right)-1\right)\right)\cdot c_{1}\right)-1\right)\cdot-\left(\left(\left(-\left(\left(\left(-\left(\left(i_{1}\cdot i_{2}\right)-1\right)\cdot-\left(\left(\left(-\left(\left(i_{1}\right)-1\right)\cdot-\left(\left(i_{2}\right)-1\right)\right)\right)-1\right)\right)\right)-1\right)\cdot-\left(\left(c_{1}\right)-1\right)\right)\right)-1\right)\right)

C=-\left(\left(-\left(\left(\left(\left(-\left(\left(i_{1}\cdot i_{2}\right)-1\right)\cdot-\left(\left(\left(-\left(\left(i_{1}\right)-1\right)\cdot-\left(\left(i_{2}\right)-1\right)\right)\right)-1\right)\right)\cdot c_{1}\right)\right)-1\right)\cdot-\left(\left(\left(i_{1}\cdot i_{2}\right)\right)-1\right)\right)-1\right)

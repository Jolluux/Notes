* # Resistor in Series
	* Two elements connected at a single node are said to be in series
	* Series - connected circuit elements carry the same current.
	* ![[Pasted image 20250127093821.png]]
* # Resistors in Parallel
	* Two elements connected at both of their nodes are said to be in parallel.
	* Parallel-connected circuit elements have the same voltage across their terminals
	* ![[Pasted image 20250127093936.png]]
	* The parallel connection of the resistors mean that the voltage across each resistor must be the same. Hence, from Ohm's law
	* ![[Pasted image 20250127094022.png]]
* # Resistors in Series and Parallel Summary
	* ![[Pasted image 20250127094044.png]]
* # Example:
	* ![[Pasted image 20250127095209.png]]
	* ![[Pasted image 20250127095218.png]]
* # Useful Equation
	* 2 resistors in parallel equation$$\frac{1}{R_{eq}} = \frac{1}{R_1} + \frac{1}{R_2} = \frac{R_1+R_2}{R_1R_2} ; \space R_{eq} = \frac{R_1R_2}{R_1+R_2}$$
* # The Voltage Divider
	* The voltage-divider circuit, where two or more resistors in series with each other and a voltage source 
	* $i = \frac{v_s}{R_1 + R_2}$
	* $v_1=iR_1         v_s\frac{R_1}{R_1+R_2}$
	* $v_2=iR_2=v_s\frac{R_2}{R_1+R_2}$
* # The Current Divider
	* Two or more resistors in parallel with each other and a current source
	* $V = R_1i_1 = R_2i_2 = \frac{R_1R_2}{R_1 + R_2}i_s$
	* $i_1 = \frac{R_2}{R_1+R_2}i_s$
	* $i_2 = \frac{R_1}{R_1+R_2}i_s$
	* Notice that the resistor opposite of the one you want the current through is in the numerator (unlike the voltage divider)
* General Equations for Current-Divider/Voltage Divider
	* Voltage Divider Equation for more than 2 resistors in series
		* $v_j = iR_j = \frac{R_j}{R_{eq}}v$
	* Current Divider Equation for more than two resistors in parallel
		* $i_j=\frac{v}{R_j} = \frac{R_{eq}}{R_j}i$

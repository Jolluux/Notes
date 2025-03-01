# Patrick Lecture
* Road to Ohm's Law
	* 1791
		* Luigi Galvani proposes that muscles have an "animal electricity" from experiments with frog legs and a bimetallic probe
	* 1797
		* Alessandro Volta correctly interpreted Galvani's experimental results
		* The bimetallic probe was the source of electricity
		* Then invented the battery
	* 1825
		* Georg Ohm performed experiments using Volta's battery to help formulate V=IR
* Equivalent Circuits
	* Thevenin's Theorem(1883)
		* A complicated network of resistors and sources, when viewed from a port, can be simplified down to one voltage source and one resistor.
	* Norton's Theorem (1926)
		* A complicated network of resistors and sources when viewed from a port, can be simplified down to one current source and one resistor.
	* History
		* The voltage source equivalence theorem was first proposed by Hermann von Helmholtz in 1853 while studying the electrical nature of muscle.
		* Independently, Leon Thevenin, who was an engineer in the national Telegraph company in France, published the same theorem 30 years later.
		* Both built their equivalency theorem from Ohm's law and Kirchhoff's law
* Thevenin and Norton Equivalent Circuits
	* ![[Pasted image 20250210094908.png]]
* Thevenin Equivalent Circuits
	* (1) measure the open circuit voltage $V_{oc} = V_{Th}$
	* (2) measure the short-circuit current, $i_{sc}$
	* (3) then solve for $R_{Th}$
	* $$R_{Th} = \frac{V_{Th}}{i_{sc}}$$
	* ![[Pasted image 20250210095151.png]]
* Thevenin Equivalent Circuits with independent sources only![[Pasted image 20250210095431.png]]
* Thevenin Equivalent Circuits with dependent sources only![[Pasted image 20250210095518.png]]
* Thevenin Equivalent Circuits with independent and dependent sources![[Pasted image 20250210095549.png]]

# Thevenin and Norton Equivalents [19:15]
* At times in circuit analysis, we want to concentrate on what happens at a specific pair of terminals. For example, when we plug a toaster into an outlet, we are interested primarily in the voltage and current at the terminals of the toaster. We have little or no interest in the effect that connecting the toaster has on voltages or currents elsewhere in the circuit supplying the outlet. We can expand this interest in terminal behavior a set of appliances, each requiring a different amount of power, We then are interested in how the voltage and current delivered at the outlet change as we change appliances. In other words, we want to focus on the behavior of the circuit supplying the outlet, but only at the outlet terminals. Thevenin and Norton equivalents are circuit simplification techniques. These equivalent circuits retain no information about the internal behavior of the original circuit and focus only on terminal behavior. They are extremely valuable when analyzing complex circuits where one portion of the circuit is fixed, so it can be replaced by a simple Thevenin and Norton equivalent, and another portion of the circuit is changing. Although here we discuss them as they pertain to resistive circuits, Thevenin and Norton equivalent circuits may be used to represent *any circuit made up of **linear** elements*. 
* ![[Pasted image 20250212002118.png]]
* To represent the original circuit by its Thevenin equivalent, we must calculate the Thevenin voltage $V_{Th}$ and the Thevenin resistance $R_{Th}$ . First, we note that i f the load resistance is infinitely large, we have an open-circuit condition. The open-circuit voltage at the terminals a and b in the circuit shown above is $V_{Th}$ . By hypothesis, this must be the same as the open-circuit voltage at the terminals a and b in the original circuit. Therefore, to find the Thevenin voltage $V_{Th}$ , calculate the open circuit voltage in the original circuit. Reducing the load resistance to zero gives us a short-circuit condition.
* If we place a short circuit across the terminals a and b of the Thevenin equivalent circuit, the short-circuit current directed from a to b is $$i_{sc} = \frac{V_{Th}}{R_{Th}}$$
* By hypothesis, this short circuit current must be identical to the shirt circuit current that exists in a short circuit placed across the terminals a and b of the original network $$R_{Th} = \frac{V_{Th}}{i_{sc}}$$
* Thus, the Thevenin resistance is the ratio of the open-circuit voltage to the short-circuit current. Work through this example to see how to find the Thevenin equivalent of a circuit
* ![[Pasted image 20250212004039.png]]
	* To find the Thevenin equivalent of the circuit shown above, we first calculate the open-circuit voltage $v_{ab}$ . Note that when the terminals a, b are open, there is no current in the 4$\Omega$ resistor. Therefore the open circuit voltage $v_{ab}$ is identical to the voltage across the 3A current source, labeled $v_1$ . We find the voltage by solving a single KCL equation. Choosing the lower node as the reference node, we get $$\frac{v_1-25}{5} + \frac{v_1}{20}-3=0$$ Solving for $v_1$ yields$$v_1 = 32V = V_{Th}$$ Hence, the Thevenin voltage for the circuit is 32V.     
	* The next step is to place a short circuit across the terminals a and b and calculate the resulting short-circuit current. Below shows the circuit with the short in place. Note that the short-circuit current is in the direction of the open-circuit voltage drop across the terminals a and b. If the short-circuit current is in the direction of the open-circuit voltage rise across the terminals, a minus sign must be inserted into the equation. 
	* ![[Pasted image 20250212005506.png]]
	* The short circuit current $i_{sc}$ is found easily once $v_2$ is known. Therefore, the problem reduces to finding $v_2$ with the short in place. Again, if we use the lower node as the reference node, the KCL equation at the node labeled $v_2$ is $$\frac{v_2-25}{5} + \frac{v_2}{20} - 3 + \frac{v_2}{4}$$ Hence, the short-circuit current is $i_{sc}=\frac{16}{4} = 4A$ 
	* We now find the Thevenin resistance by substituting the numerical values for the Thevenin voltage, $V_{Th}$ , and short circuit current $i_{sc}$ into $$R_{Th} = \frac{V_{Th}}{i_{sc}} = 8\Omega$$ The picture below shows the Thevenin equivalent for the circuit shown above
	* 
	  ![[Pasted image 20250212005802.png]]
	* You should verify that, if a 24$\Omega$ resistor is connected across the terminals a and b for the entire circuit, the voltage across the resistor will be 24V and the current in the resistor will be 1A, as would be the case with the Thevenin circuit above. This same equivalence between the circuits holds for any resistor value connected between a and b.
* Example:
	* ![[Pasted image 20250212011618.png]]
	* ![[Pasted image 20250212011830.png]]![[Pasted image 20250212011835.png]]
	* ![[Pasted image 20250212011840.png]]
	* A resistor in parallel with a voltage source does not influence rest of the circuit 
	* ![[Pasted image 20250212012304.png]]
	* ![[Pasted image 20250212012308.png]]
	* too many photos
* A Norton equivalent circuit consists of an independent current source in parallel with the Norton equivalent resistance, as shown below. We can derive it directly from the original circuit by calculating the open-circuit voltage and the short-circuit current, just as we did for the Thevenin equivalent. The Norton current equals the short current at the terminals of interest and the Norton resistance is the ratio of the open circuit voltage to the short circuit current, so its identical to the Thevenin resistance $I_N=i_{sc}$ $$R_N=\frac{V_{oc}}{i_{sc}} = R_{Th}$$ If we already have a Thevenin equivalent circuit, we can derive the Norton equivalent circuit from it simply by making a source transformation
* ![[Pasted image 20250212013012.png]]
* Sometimes we can use source transformations to derive a Thevenin or Norton equivalent circuit. This technique works best when the network contains only independent sources. Dependent sources require us to retain the identity of the controlling voltages and/or currents, and this constraint usually prohibits simplification of the circuit by source transformations. 
* Example
	* Find the Norton equivalent of the circuit below by makng a series of source transformations.
	* ![[Pasted image 20250212013415.png]]
* Example with dependent sources
	* ![[Pasted image 20250212013548.png]]
	* The first step is to recognize that $i_x$ must be zero (Note the absence of the return path for $i_x$ to return to the LHS of the circuit). The Thevenin voltage is the voltage across the 25$\Omega$ resistor, since $i_x$ = 0 $$V_{Th} = v_{ab} = (-20i)(25) = -500i$$ The current $i$ is $$i = \frac{(5-3V)}{2k\Omega} =  \frac{(5-3V_{Th})}{2k\Omega} $$
	* In writing the equation for $i$, we recognize that the Thevenin voltage is identical to v. When we combine these two equations, we obtain $$V_{Th} = -5V$$ To calculate the short circuit current, we place a short circuit across a and b. When the terminals a and b are shorted together, the control voltage $v$ is reduced to zero. Therefore, with the short in place, the circuit shown above becomes the circuit shown below. With the short shunting the 25$\Omega$ resistor, all of the current from the dependent current source appears in the short, so as the voltage controlling the dependent voltage source has been reduced to zero, the current controlling the dependent current source is $$i = \frac{5}{2000} = 2.5mA$$ Combining these two equations yields a short circuit current of $$i_{sc} = -20(2.5) = -50mA$$ From $i_{sc}$ and $V_{Th}$ we get $R_{Th} = \frac{V_{Th}}{i_{sc}} = 200\Omega$

	* ![[Pasted image 20250212014146.png]]
# More on Thevenin Equivalents[19:25] 
* We can calculate the Thevenin resistance, $R_{Th}$ , directly from the circuit rather than calculating it as the ratio of the open circuit voltage to the short circuit current. If the circuit contains only independent sources and resistors, we can determine $R_{Th}$ by deactivating all independent sources and then calculating the resistance seen looking into the network at the designated terminal pair. A voltage source is deactivated by replacing it with a short circuit, while a current source is deactivated by replacing it with an open circuit. Below illustrates this direct method for determining $R_{Th}$ 
* ![[Pasted image 20250212122527.png]]
* Deactivating the independent sources simplifies the circuit to the one shwon below. The resistance seen looking int o the terminals a and b is denoted $R_{ab}$ which consists of the 4$\Omega$ resistor in series with the parllel combination of the 4 and 20$\Omega$ resistors. Thus, ![[Pasted image 20250212123012.png]]$$R_{ab} = R_{Th} = 4 + \frac{5 \times 20}{5 + 20} = 8\Omega$$ Note that deriving $R_{Th}$ directly from the circuit is much simpler than finding $R_{Th}$ from the equation from before.
 * If the circuit network contains dependent sources, as a direct method for finding the Thevenin resistance $R_{Th}$ is as follows. We first deactivate all independent sources, then apply a test voltage source or a test current source to the Thevenin terminals a and b. The Thevenin resistance equals the ratio of the voltage across the test source to the current delivered by the test source. We will solve an example which illustrates this alternative procedure for finding $R_{Th}$ using the same circuit as below. ![[Pasted image 20250212123336.png]]
 * Find the Thevenin resistance $R_{Th}$ for the circuit above using the test source method. 
	 * Begin by deactivating the independent voltage source and exciting the circuit from the terminal a and b with either a test voltage source or a test current source. If we apply a test voltage source, we will know the voltage of the dependent voltage source and hence the controlling current i. Therefore, we opt for the test voltage source. Below shows the circuit for computing the Thevenin resitance.
	 * The test voltage source is denoted $v_T$, and the current that it delivers to the circuit is labeled $i_T$. To find the Thevenin resistance, we solve the circuit for the ratio of the voltage to the current at the test source; that is, $R_{Th} = v_T / i_T$ $$i_T = \frac{v_T}{25}+20i$$$$i = \frac{-3v_T}{2000}$$
	 * We then substitute the expression for i into the equation for $i_T$ and solve the resulting equation for the ratio $\frac{i_T}{v_T}$: $$i_T = \frac{v_T}{25} - \frac{60v_T}{2000} = 1/100$$$$\frac{i_T}{v_T} = \frac{1}{25} - \frac{6}{200} = \frac{1}{100}$$$$R_{Th} = 100\Omega$$
* In a network containing only resistors and dependent sources, the Thevenin equivalent voltage $V_{Th} = 0$ and the Norton equivalent $I_N = 0$. It should be clear that if the circuit you start with has no independent sources, its equivalent circuit cannot have any independent sources either. Therefore, the Thevenin and Norton equivalents for a circuit with only dependent sources and resistors is a single equivalent resistance whose value must be determined using the test source method.  Next, this procedure will be illustrated below. 
* i've stopped caring to write.
* 
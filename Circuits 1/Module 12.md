# Superposition using Thevenin and Norton Equivalent for solving a circuit with a dependent source (17:17)
* A linear system obeys the principle of superposition, which states that whenever a linear system is excited, or driven, by more than one independent source of energy, the total response is the sum of the individual responses. An individual response is the result of an independent source acting alone. Because we are dealing with circuits made up of interconnected linear-circuit elements, we can apply the principle of superposition directly to the analysis of such circuits when they are driven by more than one independent energy source. At present, we restrict the discussion to simple resistive networks; however, the principle is applicable to any linear system. 
* Superposition is applied in both the analysis and design of circuits. In analyzing a complex circuit with multiple independent voltage and current sources, there are often fewer, simpler equations to solves when the effects of the independent sources are considered one at a time. Applying superposition can thus simplify circuit analysis. Be aware, though, that sometimes applying superposition actually complicates the analysis, producing more equations to solve than with an alternative method. Superposition is required only if the independent sources in a circuit are fundamentally different. 
* In the early chapters, all independent sources are dc sources, so superposition is not required. We introduce superposition here in anticipation of later chapters in which circuits will require it. Superposition is applied in design to synthesize a desired circuit response that could not be achieved in a circuit with a single source. If the desired circuit response can be written as a sum of two or more terms, the response can be realized by including one independent source for each term of the response. This approach to the design of circuits with complex responses allows a designer to consider several simple designs instead of one complex design. We demonstrate the superposition principle next in the example.
* Example
	* Use the superposition principle to find the branch currents in the circuit shown below. 
	* We begin by finding the branch currents resulting from the 120V voltage source. We denote those currents with a prime. Replacing the ideal current source with an open circuit deactivates it; Below shows this. The branch currents in this circuit are the result of only the voltage source. 
	* We can easily find the branch currents in the circuit below once we know the node voltage across the 3$\Omega$ resistor. Denoting this voltage $v_1$, we write $$\frac{v_1-120}{6}+\frac{v_1}{3}+\frac{v_1}{2+4} = 0$$![[Pasted image 20250216170524.png]]
	* from which,  $v_1 = 30V$
	* Now, we can write the expressions for the branch currents $i'_1-i'_4$ directly:
		* $i'_1=\frac{120-30}{6}=15A$
		* $i'_2=\frac{30}{3}=10A$
		* $i'_3=i'_4=\frac{30}{6}=5A$
	* To find  the component of the branch currents resulting from the current source, we deactivate the ideal voltage source and solve the circuit shown below. The double-prime notation for the currents indicates they are the components of the total current resulting from the ideal current source. We determine the branch currents in the circuit shown below by first solving for the node voltages across the 3 and 4$\Omega$ resistors, respectively. Below shows the two node voltages. The two KCL equations that describe the circuit are:
		* $\frac{v_3}{3}+\frac{v_3}{6}+\frac{v_3-v_4}{2}=0$
		* $\frac{v_3-v_4}{2}+\frac{v_4}{4}+12=0$
	* ![[Pasted image 20250216171233.png]]
	* Solving the simultaneous KCL equations for $v_3$ and $v_4$ , we get
		* $v_3 = -12V$
		* $v_4 = -24V$
	* Now we can write the branch currents $i''_1-i''_4$ directly in terms of the node voltages $v_3$ and $v_4$ :
		* $i''_1 = \frac{-v_3}{6}=\frac{12}{6} = 2A$
		* $i''_2 = \frac{v_3}{3}=\frac{-12}{3}=-4A$
		* $i''_3 = \frac{v_3-v_4}{2}=\frac{-12+24}{2}=6A$
		* $i''_4=\frac{v_4}{4}=\frac{-24}{4}=-6A$
	* To find the branch currents in the original circuit, that is, the currents $i_1, i_2, i_3, \text{and } i_4$ below, we simply add the single primed-currents to the double-primed currents:
		* $i_1=i'_1+i''_1=17A$
		* $i_2=i'_2+i''_2=6A$
		* $i_3=i'_3+i''_3=11A$
		* $i_4=i'_4+i''_4=-1A$
	* You should verify that the currents have the correct values for the branch currents in the circuit shown below
	* ![[Pasted image 20250216172631.png]]
* When applying superposition to linear circuits containing both independent and dependent sources, you must recognize that the dependent sources are never deactivated. This example applies superposition when a circuit contains both dependent and independent sources, which we will solve next. 
* Example:
	* ![[Pasted image 20250216172810.png]]
	* We begin this process by finding the component of $v_0$ resulting from the 10 V source. Below shows the circuit. With the 5A source deactivated, $v'_{\triangle}$ must equal ($-0.4v'_{\triangle}$)(10). Hence, $v'_{\triangle}$ ***must be zero***, the branch containing the two dependent sources is open $$v'_0 = \frac{20}{25}(10) = 8V$$![[Pasted image 20250216173148.png]]
	* When the 10V source is deactivates, the circuit reduces to the one shown below. We have added a reference node and the node designations a, b, and c to aid the discussion. KCL at these nodes gives:![[Pasted image 20250216173600.png]]
	* We now use $v_b$ to find the value of $v''_{\triangle}$. Thus, ![[Pasted image 20250216173727.png]]
* Chapter 4 Summary, just gonna watch
	* Node Voltage Method
		* Step 1: Identify the essential nodes by circling them on the circuit diagram
		* Step 2: Pick and label a reference node; then label the remaining essential node voltages
			* If a voltage source is the only component in a branch, connecting the reference node and another essential node, label the essential node with the value of the voltage source. 
			* If a voltage source is the only component in a branch connecting two nonreference essential nodes, create a supernode that includes the voltage source and the two nodes on either side.
		* Step 3: Write the following equations
			* A KCL for any supernodes
			* A KCL for any remaining essential nodes where the voltage is unknown. 
			* A constraint equation for each dependent source that defines the controlling variable for the dependent source in terms of node voltages. 
			* A constraint equation for each supernode that equated the difference between the two node voltages in the supernode to the voltage source in the supernode
		* Step 4: Solve the equations to find the node voltages
		* Step 5: Use the node voltage values to find any unknown voltages, currents, or powers. 
		* Step 6: Was this the best method? Always think both before you start a problem and after you have solved it. Ask yourself, did you use the most effective method to solve your problem, or were there simplifications that should have been considered first, prior to choosing your method and solving?
	* Mesh-Current Method
		* Step 1: Identify the meshes by drawing directed arrows inside each mesh (clockwise). 
		* Step 2: Label each mesh current
			* If a current source is in a single mesh, label the mesh current with the value of the current source.
			* If a current source is shared by two adjacent meshes, create a supermesh and temporarily eliminating the branch that contains the current source. 
		* Step 3: Write the following equations
			* A KVL equation for any supermeshes
			* A KVL equation for any remaining meshes where the current is unknown.
			* A constraint equation for each dependent source that defines the controlling variable for the dependent source in terms of the mesh currents.
			* A constraint equations for each supermesh that equates the difference between the two mesh currents in the supermesh to the current source eliminated to form the supermesh. 
		* Step 4: Solve the equations to find the mesh currents
		* Step 5: Use the mesh current values to find any unknown voltages, currents, or powers
		* Step 6: Was this the best method? Always think both before you start a problem and after you have solved it. Ask yourself, did you use the most effective method to solve your problem, or were there simplifications that should have been considered first, prior to choosing your method and solving?
* 
# Circuit with Dependent Source Simplification [5:26]
* ![[Pasted image 20250216181426.png]] 1V test voltage source, with current Is coming out. 
* ![[Pasted image 20250216181602.png]]
* ![[Pasted image 20250216181647.png]]
* V1 = 10i_delta, so Is = 1/8 A
* R_Th = V_t/I_t = 1/I_s = 8Ohms
# Circuit Analysis for Maximum Power Transfer [14:42]
* In general, in a circuit with no independent sources, there is no current or voltage anywhere in the circuit. Dependent sources do not have the capacity to generate power on their own, and they rely on the independent sources to generate power. Your $V_{Th}$ will automatically be 0V due to this.
* Find the maximum power delivered to the resistor $R_0$ ![[Pasted image 20250216182450.png]]
* $R_0 = R_{Th}$ for maximum power delivered to $R_o$
* Some source transformations and addition later, we get![[Pasted image 20250216184055.png]]
* So, $R_0$ needs to be 5k$\Omega$ for maximum power transfer. 
* $I_0 = \frac{4.372}{10}mA$
* $P_0=I_0^2(5k\Omega)$

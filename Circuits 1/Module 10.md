# Nodal and Mesh With Dependent Sources Example [18:56]
* If dependent sources are present, all the steps are identical except for additional equations due to the variables describing the dependent sources. 
* ![[Pasted image 20250207003247.png]]
* 5 nodes, 4 meshes
* Nodal Analysis: 
	* 4 non reference nodes
	* 1 supernode
	* 4 node voltages + i_x => 5 variables.
* Mesh Analysis:
	* 4 mesh currents
	* SuperMesh
	* Additional equation for i_x
	* 5 variables. 
* ![[Pasted image 20250207003603.png]]
* Nodal Analysis solving steps:
	* Supernode $V_3-V_4 = 10V$
	* $V_1 = 10$
	* KCL At The Supernode:
		* $\frac{V_4-V_1}{10} + \frac{V_3-V_2}{5} + \frac{V_3}{20} - 2 = 0$
	* KCL at V2
		* $\frac{V_2-V_1}{20}-2i_x+\frac{V_2-V_3}{5} = 0$
	* Dependent sources get the same respect as independent sources. 
	* $i_x$ must be written in terms of the node voltages ==> $i_x = \frac{V_3}{20}$
* Mesh Analysis Method
	* ![[Pasted image 20250207010038.png]]
	* $I_2 - I_1 = 2i_x$
	* KVL for supermesh (I1 and I2):
		* $20(I_1-I_4) +5(I_2-I_4) + 20(I_2-I_3) - 20 = 0$
	* $I_3 = -2A$
	* $10I_4-10+5(I_4-I_2) + 20(I_4-I_1) = 0$
	* $i_x = I_2-I_3$
# Source Transformations w/ Example [21:38]
* A voltage source in series with a resistor is equivalent to a current source in parallel with a resistor, connected to the same terminals.  
* I'm lazy will watch later

# Patrick Lecture
* Check the extra problems, lecture recordings, and yea. 
* Simplification Techniques
	* Series and Parallel reductions
	* Delta to Y transformations
	* Source transformation (the video i skipped)
	* Superposition (same video lol)
* As-Is analysis methods
	* KVL/KCL
	* Nodal Analysis
	* Mesh Analysis
	* Thevenin and Norton Equivalent Circuit (mon/wed. hw4. "hardest hw")
* Source Transformations
	* A source transformation allows a voltage source in series with a resistor to be replaced by a current source in parallel with the same resistor, or vice versa.
	* ![[Pasted image 20250207094302.png]]
	* ![[Pasted image 20250207094314.png]]
	* ![[Pasted image 20250207094337.png]]
* Superposition
	* Principle of superposition: whenever a *linear system* is driven by more than one independent source of energy, the total response (voltage and current) is the sum of the individual responses
		* ![[Pasted image 20250207095747.png]]
	* To Solve: Deactivate all but one independent source and use analysis technique to solve for desired current or voltage
	* To deactivate, 0A or 0V, open the circuits or short them. 
	* ![[Pasted image 20250207094438.png]]
	* ![[Pasted image 20250207094447.png]]
	* ![[Pasted image 20250207094455.png]]
	* superposition lowkey cracked
	* 
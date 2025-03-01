# Node Voltage Method 8-1 [9:37]
* Nodal Analysis
	* When no voltage sources are present.  
	* Steps:
		1. Identify all the nodes (N nodes).
		2. Assign one of the nodes as the reference node and a voltage to each of the remaining (N-1) non reference nodes.
		3. Work KCL at each of the non-reference nodes, in terms of node voltages ($V_1, V_2, \dots$)
		4. Solve the (N-1) linear equations (calc).
		5. Find the desired quantity. Power, Current, Voltage and such. 
# Example of Node Voltage Method [13:02]
* ![[Pasted image 20250204184408.png]]
* KCL at Node 1 = $I_{S3} + \frac{V_1-V_2}{R_1} = I_{S1} \dots (1)$      
* KCL at Node 2 = +$\frac{V_1-V_2}{R_1} + I_{S2} + I_{S3} = \frac{V_2}{R_2} + \frac{V_3}{R_3};\space \frac{V_2}{R_2} + \frac{V_3}{R_3} + \frac{V_2 - V_1}{R_1} = I_{S2} + I_{S3} (2)$ 
* ![[Pasted image 20250204185054.png]]
* Equation for that circuit$$\frac{V_A-V_B}{R_1}+\frac{V_A-V_C}{R_2} + \frac{V_A-V_D}{R_3} + \frac{V_A-V_E}{R_4}$$
* You can draw currents, and rewrite functions, but they will all be equivalent, so use KCL with currents leaving the node, since it'll be easier.
# Nodal Analysis Method with Numbers [5:53]
(lowkey the first 3 vids could've just been merged). 
* Ex. w/ #'s
* ![[Pasted image 20250204201715.png]]
* $\frac{V_1-V_2}{20} + \frac{V_1}{5} + 1 + 3 = 0 \dots (1)$
* $\frac{V_2}{10} + 2 + \frac{V_2 - V_1}{20} - 1 = 0 \dots (2)$
* Plug into systems of equations, get $V_1 \space \text{and} \space V_2$ 
# Nodal Example using Super-Node
* Voltage sources present. Two cases:
	1. When all the voltage sources share the reference node
	2. Some voltage sources do not share the reference node
* ![[Pasted image 20250204203254.png]]
	* $V_1 = 20V$ ... (obviously)
	* $V_2 = -30V$ 
	* KCL for Node 2 and node 4
	* $\frac{V_2 - V_1}{20} + 3 + \frac{V_2 - V_4}{30} = 0 \dots (1)$
	* $-5 + \frac{v_4-V-3}{10} + \frac{V_4 - V_2}{30} = 0 \dots (2)$ 
	* Solve those and get the answer :)
# Nodal Example using Super-Node
* When voltage sources do not share the reference node, we introduce the concept of **supernode!!!** A supernode consists of all the non-reference nodes interconnected to each other. 
* ![[Pasted image 20250204210518.png]]
* ^first 2 equations there 2 ^
* $\frac{V_2-V_1}{15} + \frac{V_2}{10} + \frac{V_3-V_4}{20} = 0 \space \dots (3)$
* We do KCl for node 2 and 3 as a supernode, because of the voltage source there. Thats the dotted circle
* $\frac{V_4-V_3}{20} + \frac{V_4}{20} = 2 \space ]dots (4)$
* Plug and play, bang u get the answer :)
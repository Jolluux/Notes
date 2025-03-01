# Mesh Analysis Intro [17:45]
* Mesh
	* A mesh is a closed loop with no other closed loops inside it. 
	* When no current sources are present 
	* ![[Pasted image 20250204220105.png]]
	1. Identify the meshes and assign a mesh current to each mesh by drawing a clockwise or counterclockwise arrow. The mesh currents are the variables to be determined, not the voltages. 
		* ![[Pasted image 20250204222643.png]]
	2. Write KVL around each mesh in terms of mesh currents.
	3. Solve the set of linear equations.
	4. Find the desired quantity.
	* Mesh 1
		* $V_{BC} = (I_1-I_2)*10$
		* $V_{CB} = (I_2-I_1)*10$
		* $V_{AB} = (I_1+I_4)*20$
		* $A \rightarrow B \rightarrow C \rightarrow A$ 
		* $20(I_1+I_4) + 10(I_1-I_2) - 10 = 0$ 
	* Mesh 2
		* $B \rightarrow D \rightarrow C' \rightarrow C \rightarrow B$ 
		* $15(I_2+I_4) -20 + 10(I_2-I_1) = 0$ 
	* Mesh 3
		* $-10 + 15I_3 = 0$
	* Mesh 4
		* $30I_4 + 20(I_1+I_4)+15(I_2+I_4) = 0$ 
# Mesh Analysis with Current Sources
* 2 cases
	1. Each current source belongs to a single mesh
	2. Some current sources are shared by two meshes. 
	*  ![[Pasted image 20250204231957.png]]
	* $40I_2 + 50(I_2-I_4) + 30(I_2-I_3)+10(I_2-I_1) = 0 \dots (1)$
	* $30(I_3-I)2) + 10(I_3-I_4) + 20(I_3-I_1) = 0 \dots (2)$
	* $50(I_4-I_2) - 10 + 10(I_4-I-3) = 0 \dots (3)$  
* Example:
	* ![[Pasted image 20250204233001.png]]
	* self explanatory, just need to know when to add and subtract a current/voltage source. 
# SUPERMESH 
* Same photo above, but supermeshed with 2 and 4! Do KVL on the supermesh. 
* ![[Pasted image 20250204233409.png]] I'm tired basically he just goes top to bottom including the supermesh up top. SUPERMESH is accounted for in each mesh that shares that source. 

# Patrick Lecture 2/5
* Node-Voltage Method Review
	* Solve for n-1 node voltages in the circuit
	* By writing KCL equations (as a function of nodal voltages, use Ohm's law) or voltage constraints for all nodes but reference nodes
	* Solve system of n-1 equations. 
	* ![[Pasted image 20250205093527.png]]
* The Mesh-Current Method (mesh analysis)
	* Solve for n mesh-currents in the circuit
	* By writing KVL equations (as a function of mesh currents, using Ohm's law) or current source constraints for all defined meshes. 
	* Solve system of n equations. 
	* A mesh is any loop that starts and ends at the same node and does not have any other loops in it. 
	* ![[Pasted image 20250205093655.png]]
	1. Identify all the meshes
	2. Label all mesh currents
		* *Note. A branch current is different than a mesh current*
	3. Write KVL equations for each mesh as a function of mesh currents
	4. Solve the system of equations for the mesh currents
	* ![[Pasted image 20250205093857.png]]
	* ![[Pasted image 20250205093913.png]]
	* ![[Pasted image 20250205093935.png]]
* Type 1 - Current source unique to one mesh
* Type 2 - Current source shared by 2 meshes
* Compared to 
	* Voltage source attached to ref. node
	* Voltage source not attached to ref.
* ![[Pasted image 20250205094039.png]]
* ![[Pasted image 20250205094046.png]]
* ![[Pasted image 20250205094124.png]]
* Summary
	1. Identify all meshes and label mesh currents
	2. Write KVL equations (as a function of mesh currents) for meshes or supermeshes
		* If you have current source /s, they will define the mesh current, no KVL in that mesh
	3. Solve the set of linear equations for all mesh currents
		1. Using substitution (if few) [supermesh]
		2. Using matrices on calculator (if many)



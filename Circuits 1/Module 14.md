# Operational Amplifier Introduction [4:33]
![[Pasted image 20250216190755.png]]
* What is an Operational Amplifier ("Op-Amp")
	* Integrated circuit capable of amplifying input voltages and currents. 
	* Applications 
		1. Mathematical operations
		2. Sensors
		3. Filters
		4. Voltage regulators
		5. Analog to Digital conversion (vice-versa)
* ![[Pasted image 20250216190946.png]]
* $(V^+-V^-)A=V_0$. Lets say +5V and -5V, so our output will not be greater than 5V. 
# Op-Amp Characteristics [8:08]
* ![[Pasted image 20250216195323.png]]
* $V_{out} = A(V^+-V^-); A=\infty$
* $\frac{V_{out}}{A} = V^+ - V^- = 0$
* First constraint of op-amp, V=0 across + and - terminals, so there's an infinite resistance at $R_i$ 
* ![[Pasted image 20250216195858.png]]
* Negative Feedback
	* $V_o = A(V^+-V^-)$
	* What happens if we increase $V_{in}?$
	* $V_n=V_p; i_n=i_p; v_p = v_{in}$
	* $V_o = A(V_in - V^-)$
* ![[Pasted image 20250216200050.png]]
* ![[Pasted image 20250216200124.png]]
* 
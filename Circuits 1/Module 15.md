# Inverting Operational Amplifier [11:23]
* ![[Pasted image 20250219145628.png]]
	* No feedback path, so this is an open-loop inverting op amp.
	* ![[Pasted image 20250219150524.png]]
* ![[Pasted image 20250219150543.png]]
	* ![[Pasted image 20250219151649.png]]
	* In the open loop gain, we reach saturation quickly for any significant input voltage. However, in the closed loop gain, it's dependent on the comparison of the feedback resistance and the series resistance.
* ![[Pasted image 20250219151812.png]]
	* Find $i_0$ assuming it's an ideal op amp.
	* Ideal op amp assumptions:
		* ![[Pasted image 20250219151847.png]]
	* finding i_0, since i_n is 0, all 0.5mA goes to the feedback resistor. 
	* solving steps? DO KCL AT NEGATIVE NODE.
	* ![[Pasted image 20250219152043.png]]
# Non-Inverting Op-Amp [11:04]
* ![[Pasted image 20250219152300.png]]
	* Notice how the voltage source is connected in series to the non inverting input.
	* Find the closed loop gain of the non-inverting op amp (A)
	* $V_0=A(V^+-V^-)$
	* $V^+=V^-$
	* $i_n=i_p$
	* $V^+ = V_g$ since it's the voltage in series at the non-inverting terminal. Infinity resistance inside op-amp, no voltage drop outside only inside.
	* $V^- = V_{out}(\frac{R_s}{R_s+R_f})$, since that's what's connected to there lol. 
	* $V_{out} = A(V_g)-A(V_{out}\frac{R_s}{R_s+R_f})$
	* since A is infinitely large, get rid of the 1+... cuz we can do that
	* ![[Pasted image 20250219153050.png]]
* ![[Pasted image 20250219153130.png]]
	* Find $V_0$ in terms of $V_s$
	* KCL AT INVERTING TERMINAL !!!!!!
	* ![[Pasted image 20250219153636.png]]
# Difference Op Amps [12:49]
* ![[Pasted image 20250219154131.png]]
	* Find closed loop gain $V_o$
	* use superposition
	*  ![[Pasted image 20250219170433.png]]
* ![[Pasted image 20250219170444.png]]
	* ![[Pasted image 20250219172042.png]]
# Summing Op Amp [12:49]
* ![[Pasted image 20250219172344.png]]
	* Find the closed loop gain $v_0$. 
	* ![[Pasted image 20250219173127.png]]
* ![[Pasted image 20250219173140.png]]
* 
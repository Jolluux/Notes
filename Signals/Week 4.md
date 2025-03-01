# Harley Vids
## Special Signals [9:38]
* NO MORE CONTINUOUS TIME SIGNALS !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!! Discrete signals over
* Impulse Function - Kronecker Delta Function
	* $\delta [n] = \begin{cases} 1 & when \space n=0 \\ 0 & when \space n\ne 0 \end{cases}$  
	* easy asf from the classwork. 
* Step Function
	* $u[n] = \begin{cases}  1 & when \space n \ge 0 \\ 0 & when \space n \lt 0 \end{cases}$
	* easy asf again
	* $u[n] = \sum_{m = 0}^{\infty}{\delta[n-m]}$
## Discrete-Time Systems [16:03]
* x[n] - input
* feeds into *system* H{x[n]}
* y[n] is our output
* Impulse Response (output)
	* Impulse = Input
	* h[n] : impulse response
	* $\delta[n] \rightarrow H(x[n]) \rightarrow y[n]=h[n]$ ignore parenthesis, latex curly braces
* System Function/Input-output Representation
	* $y[n] =$ H{$x[n]$} $= 3x[n-1]$
	* ![[Pasted image 20250205233246.png]]
* Step Response
	* $u[n] \rightarrow H \rightarrow y[n]$
	* 3 important elements of systems tend to be
		* summing
		* multiplying by a scalar
		* shifting or delaying
	* ![[Pasted image 20250205233600.png]]
	* Finite Impulse Response Property (FIR)
		* System is FIR if: $H${$\delta[n]$}$= h[n] = y[n]$ 
		* in the name, if it's only a couple values, it's finite
	* Infinity Impulse Response
		* the opposite, if the values go on forever
	* Causal/Noncausal
		* uses on past and present inputs
		* Causal when looking at previous inputs
		* Non/causal requires future values. 
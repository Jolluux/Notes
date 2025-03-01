# Linear and time-invariant Systems - Signals and Systems Unwrapped [14:49]

* LTI systems
	* Let $x[n] \rightarrow H \rightarrow H(x[n]) = y[n]$
	* $x[n] \rightarrow H \rightarrow \text{Delay N}$ must be equivalent to $x[n] \rightarrow \text{Delay n} \rightarrow H$ for a time-invariant system, aka both must return $y[n-N]$. 
	* Example 1:
		* $H(x[n]) = y[n] = nx[n]$
		* In order to make sure they're equivalent, we must first DELAY THE INPUT
		* $H(x[n-N]) = nx[n-N]$
		* $y[n-N] = (n-N)x[n-N]$ 
		* These are not equal, so they are not time invariant, or time varying.
	* Example 2:
		* $H(x[n]) = y[n] = 5x[n-2]$
		* $H(x[n-N]) = 5x[n-2-N]$
		* $y[n-N] = 5x[n-2-N]$
		* These are equal, so the system is time invariant. 
* Linearity
	* Let
		* $x_1[n] \rightarrow H \rightarrow H(x_1[n]) = y_1[n]$
		* $x_2[n] \rightarrow H \rightarrow H(x_2[n]) = y_2[n]$
	* ![[Pasted image 20250211000940.png]]
	* Example 1:
		* $H(x[n]) = |x[n]|^2 = y[n]$
		* $H(a_1x_1[n] + a_2x_2[n]) = |a_1x_1[n] + a_2x_2[n]|^2$
		* $a_1y[n] + a_2y[n] = a_1|x[n]|^2 + a_2|x[n]|^2$
		* Not equal, therefore not linear.
	* Example 2:
			* $H(x[n]) = 5x[n-2] = y[n]$
			* $H(a_1x_1[n] + a_2x_2[n]) = 5a_1x_1[n-2] + 5a_2x_2[n-2]$
			* $a_1y[n] + a_2y[n] = a_1(5x_1[n-2]) + a_2(5x_2[n-2])$
			* equivalent, therefore the system is linear.
			* This is linear, and time invariant, so LTI system. 

# Convolution [16:22]
* Linearity : $H(a_1x_1[n] + a_2x_2[n]) = a_1y_1[n] + a_2y_2[n]$
* Time-Invariance: $H(x[n-N]) = y[n-N]$
* Sifting Property to convolution
	* $x[n] = \sum_{m=-\infty}^{\infty}{x[m]\delta[n-m]}$  
	* $H(x[n]) = H(\sum_{m=-\infty}^{\infty}{x[m]\delta[n-m]})$ 
	* Linearity -> = $\sum_{m=-\infty}^{\infty}{x[m]H(\delta[n-m]}$ 
	* Time Invariance -> = $\sum_{m=-\infty}^{\infty}{x[m]h[n-m]}$ where h is the impulse response
	* This, is convolution! $y[n] = x[n]*h[n] = \sum_{m=-\infty}^{\infty}{x[m]h[n-m]}$ 
* Example:
	* $y[n] = \sum_{m=-\infty}^{\infty}{x[m]h[n-m]}$ , $x[n] = \delta[n]$
	* $= \sum_{m=-\infty}^{\infty}{\delta[m]h[n-m]}$ 
		* This is telling me that there is only one value where delta[n] is nonzero, when m = 0.
	* $= \sum_{m=-\infty}^{\infty}{\delta[m]h[n-0]}$
	* $= \sum_{m=-\infty}^{\infty}{\delta[m]h[n]}$
	* $= h[n]\sum_{m=-\infty}^{\infty}{\delta[m]}$ 
	* $= h[n]$
		* Impulse response is my output when my input is the delta function.
* Example:
	* $= \sum_{m=-\infty}^{\infty}{\delta[n]h[n-m]}$ , $x[n] = 15\delta[n-3]$
	* $= \sum_{m=-\infty}^{\infty}{15\delta[m-3]h[n-m]}$
	* Time invariance tells me that the new solution will be $h[n-3]$, linearity tells me to multiply it by 15.
	* $15\delta[n-3]*h[n] = 15h[n-3]$
	* n-3 is shifting the signal, the 15 is multiplying the system.
* Example:
	* $= \sum_{m=-\infty}^{\infty}{\delta[n]h[n-m]}$ , $x[n] = 2\delta[n-4] + 3\delta[n-5]$
	* $x[n] * h[n]$
	* $2h[n-4] + 3h[n-5]$
	* thats it !
	* ![[Pasted image 20250212184814.png]]
	* 
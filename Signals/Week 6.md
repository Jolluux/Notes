3# Frequency Response [11:50]
* Frequency Response
	* If the impulse response is the response of a system putting in an impulse (delta function)
	* Then, the frequency response is the response of a system when we input a single frequency.
	* This will be a function of that frequency, so $\hat{\omega}$ 
	* We assume $x[n] = e^{j\hat{\omega}n}$ 
	* When we input that one single sinusoid, we get out one single complex number that we multiply the sinusoid by.
	* ![[Pasted image 20250222162858.png]]
* So let's prove it
	* ![[Pasted image 20250222163048.png]]
* Example
	* $h[n] = \frac{1}{2}(\delta[n] + \delta[n-1])$
	* $y[n] = h[n] * e^{j\hat{\omega}n}$ 
	* $= \frac{1}{2}(e^{j\hat{\omega}n}+e^{j\hat{\omega}(n-1)})$ 
	* $= \frac{1}{2}(1 + e^{-j\hat{\omega}})e^{j\hat{\omega}n}$
	* $= H(e^{j\hat{\omega}})e^{j\hat{\omega}n}$ 
	* $H(e^{j\hat{\omega}}) = \frac{1}{2}(1+e^{-j\hat{\omega}})$
* Continued
	* ![[Pasted image 20250222163449.png]]
	*  ![[Pasted image 20250222165407.png]]
# Magnitude and Phase Response [13:31]
* Impulse response: delta function
* Frequency response: sinusoid/complex exponential
* ![[Pasted image 20250222172903.png]]
* Let's describe frequency responses
* Magnitude response
	* Lets take the frequency response and take the magnitude of it
* Phase response
	* Lets take the frequency response and take the phase of it
* Filters filter frequencies
* This gives us the tools to describe these frequencies
* Compute Magnitude/Phase
	*  ![[Pasted image 20250222174658.png]]
	* $-1=e^{j\pi}$
	*  ![[Pasted image 20250222175239.png]]
	* have to move pi to get those magnitude values, -pi vice versa. chills bro...
	* ![[Pasted image 20250222175754.png]]
* 
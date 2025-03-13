# Z-Transform [12:26]
* We've learned 2 ways to represent signals
	* time domain input x[n], output y[n], and impulse response h[n]
	* frequency domain input X(e^jw), output Y(e^jw), and frequency response H(e^jw)
* New third way, **z-transform domain*** 
	* X(z) input in z-transfer domain, Y(z) output, and Transfer Function H(z)
* The Z Transform
	* $$X(z) = \sum_{n=-\infty}^{\infty}{x[n]z^{-n}}$$Forward z-transformation$$x[n] = \frac{1}{2\pi j}\int_C{X(z)z^{n-1}dz}$$Inverse Z-Transform (synthesis equations). We will never do this, and we'll use tables for this.
* TO go from z-transform to dtft, say $z = e^{j\hat{\omega}}$
* More generally, $z = |z|e^{j\hat{\omega}}$ where we have the magnitude of z and phase of z
* When |z| = 1, we get the DTFT
* Example:
	* ![[Pasted image 20250311020631.png]]DTFT does not converge!
	* So, we can't use the DTFT, now let's use the z transform
	* ![[Pasted image 20250311020816.png]]
	* ![[Pasted image 20250311020912.png]]
	* ![[Pasted image 20250311020918.png]]
	* We've successfully done a z-transform, note the condition, it's called the "region of convergence"

# Pole-Zero Plot [10:50]
* ![[Pasted image 20250313090114.png]]
* The transfer function of a system can be shown as a pole/zero plot
* Transfer Function
	* $H(z) = \frac{\text{polynomial in z}}{\text{polynomial in z}} = \frac{y(z)}{x(z)}$ 
	* zeros: z when H(z) = 0
	* poles: z when H(z) = $\infty$
	* Example plot:![[Pasted image 20250313091224.png]]
* Example Pole-Zero Plot![[Pasted image 20250313091556.png]]
* 
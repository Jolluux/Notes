# Discrete Time Fourier Transform [14:58]
* ![[Pasted image 20250304004803.png]]
* Discrete Time Fourier Transform$$\left (\sum_{m=-\infty}^{\infty}{h[m]e^{-j\hat{\omega}m}}\right ) e^{j\hat{\omega}n} = H(e^{j\hat{\omega}})$$It takes the signal h[m] and transforms it to H(e^jw). Allows us to have time and frequency representations of our signals. "This is the frequencies that our signal is made up of."
* The DTFT:
	* Forward DTFT: $X(e^{j\hat{\omega}}) =  \sum_{m=-\infty}^{\infty}{x[m]e^{-j\hat{\omega}m}}$   (Analysis)
	* Inverse DTFT: $x[n] = \frac{1}{2\pi}\int_{2\pi}{X(e^{j\hat{\omega}})e^{+j\hat{\omega}n}d\hat{\omega}}$  (Synthesis)
* Example:
	* ![[Pasted image 20250304005722.png]]
	* Time: A$\delta$[n-N] <=>  Frequency: A$e^{-j\hat{\omega}N}$
	* ![[Pasted image 20250304010027.png]]
	* DTFT Table!! Best thing ever!!!
# DTFT Properties [19:54]
* ![[Pasted image 20250304010845.png]]
* This allows us to relate our convolution in the real domain to the frequency domain. Convolution property is that it's multiplication in the frequency domain. 
* Tables are given to us. 
* Shifting Property:
	* $x[n-N]  \leftarrow\rightarrow X(e^{j\hat{\omega}})e^{-j\hat{\omega}N}$
	* ![[Pasted image 20250304011242.png]]
* Time Reversal
	* $x[-n] = X(e^{-j\hat{\omega}})$
	* ![[Pasted image 20250304011330.png]]
* Example:
	* Class Activities did good. 
	* ![[Pasted image 20250304011502.png]]
* Good Convolution Example
	* ![[Pasted image 20250304011721.png]]
	* ![[Pasted image 20250304011838.png]]
	* ![[Pasted image 20250304011958.png]]
	* 
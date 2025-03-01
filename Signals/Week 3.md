# Fourier Series 2 [10:49]
* Synthesis: (k are the harmonics, $\omega_0$ is the fundamental freq.)$$x(t) = \sum_{k=-\infty}^{\infty}{C_ke^{+jk\omega_0t}}  $$
* Analysis: basically a search engine algo. Integrated over 1 period$$C_k=\frac{1}{T_0}\int_{T_0}{x(t)e^{-jk\omega_0t}\text dt}$$
* Orthogonality Property: $$\frac{1}{T_0}\int_{T_0}{e^{-j \left ( k -k_0 \right )\omega_0}\text dt} = \begin{cases} 
          0 & \text{if}\space k \ne k_0 \\
          1 & \text{if}\space k = k_0 \end{cases}  
$$
* All _truly_ periodic signals can be sum of sinusoids! 
* Example:
	* ![[Pasted image 20250128001823.png]]
	* ![[Pasted image 20250128001900.png]]
	* ![[Pasted image 20250128002000.png]]
	* ![[Pasted image 20250128002020.png]]

# Fourier Series 2 (Wong) [45:14]
* $x(t)$ periodic w/ $T_0$ 
* Fourier Synthesis: $x(t) = \sum_{k = -\infty}^{\infty}{a_ke^{j\frac{2\pi kt}{T_0}}\text dt}$ 0 
* Fourier Analysis: $a_k = \frac{1}{T_0}\int_0^{T_0}{x(t)e^{-j\frac{2\pi kt}{T_0}}\text{d} t}$  
* Examples: Square Wave w/ 50% duty cycle
	* ![[Pasted image 20250203160758.png]]
	* $x(t) = \begin{cases}1 \space \text {if }nT_0 \le t \lt n_oT + \frac{1}{2}T_0 \\0 \space \text{if } nT_0+\frac{1}{2}T_0 \le t \lt (n+1)T_0\end{cases}$
	* when k = 0: $a_k = \frac{1}{T_0}\int_0^{T_0}{x(t)e^{-j\frac{2\pi kt}{T_0}}\text{d} t}$ = 1/2. 
	* when k $\ne$ 0: $\frac{1}{T_0}\int_0^{\frac{T_0}{2}}{e^{-j\frac{2\pi k t}{T_0}}}$  (for a square wave since T_0/2-T_0 = 0)
	* ![[Pasted image 20250203202835.png]]
	* ![[Pasted image 20250203203011.png]] Because $cos(\pi k) = 0 \text{ when even and -1 when odd}$ 
	* Graphs:
	* ![[Pasted image 20250203212112.png]]
	* Conjugate Symmetry
	* ![[Pasted image 20250203212448.png]]
	* True if x(t) is real-valued.
	* There's the triangle wave example i'll see if it's useful. Also am not typing allat.
	* 
# Sampling Sinusoids [16:09]
* Cyclic Frequency: $f_0$ 
* Period: $T_0 = \frac{1}{f_0}$
* Angular Frequency: $\omega_0 = 2\pi f_0$ 
* Cyclic *Sampling* Frequency: $f_s$
* *Sampling* Period: $T_s = \frac{1}{f_s}$
* Angular *Sampling* Frequency: $\omega_s=2\pi f_s$
* ![[Pasted image 20250129213011.png]]
* $x(t) = Acos(\omega_0t + \phi)$
* $x(nT_s) = x\left [ n \right ]  = Acos(\omega_0(nT_s) + \phi)  = Acos(\omega_0 T_s n + \phi)$
* $\omega_0 T_s = \frac{\omega_0}{f_s} = \hat{\omega_0} = \frac{\pi}{8}$ 
* $T_0 = 8; f_0 = \frac{1}{8}; \omega_0 = \frac{\pi}{4}$ 
* Normalized Cyclic Freq: $\hat{f_0} = \frac{f_0}{f_s}$
* Normalized Angular Frequency: $\hat{\omega_0} = \frac{\omega_0}{f_s} = \frac{2\pi f_0}{f_s}$
* Normalized Period: $\hat{T_0} = T_sf_s = \frac{T_0}{T_s}$
* ![[Pasted image 20250129214217.png]]
* ![[Pasted image 20250129215325.png]]

# Sampling Sinusoids 1 [51:32]
* How fast should we sample a sinusoid so that we perfectly get back sinusoid from samples? 
* ![[Pasted image 20250203215706.png]](values from the Harley vid above).
* $y_l(t) = Acos((\omega_0t + 2\pi lf_s)t + \phi$ 
* $y[n] = y(nT_s) = Acos((\omega_0+2\pi lf_s)nT_s + \phi)$ 
* $= Acos(\hat{\omega_0}n+2\pi ln + \phi)$ 
* principal alias - lowest freq among all aliases of x(t)
* $l$ is an integer 
* ![[Pasted image 20250203233104.png]]
* graphing them (lightwork i think)
# Sampling Sinusoids 2 [33:41]
* If $f_s \gt 2f_0 \rightarrow$ principal alias = x(t); oversampling
* If $f_s \lt 2f_0 \rightarrow \ne x(t)$ ; undersampling
* If $f_s = 2f_0 \rightarrow$ IDK
* If $f_s \gt f_0$ pick principal alias. 
* $2f_0$ = Nyquist freq. rate. 
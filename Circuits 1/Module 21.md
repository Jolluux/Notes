# Second Order Diff EQ, Parallel RLC 1st Order Integrating Amplifier [15:34]
* To find the natural response of the circuit shown in the figure below, we begin by deriving the differential equation that the voltage v satisfies. We choose to find the voltage because it is the same for each component. Once we know the voltage, we can find every branch current by using the current-voltage relationship for the branch component. We write the differential equation for the voltage using KCL to sum the currents leaving the top node, where each current is expressed as a function of the unknown voltage v:$$\frac{v}{R}+\left( \frac{1}{L} \int_0^t{vd\tau+I_0}\right) + C\frac{dv}{dt} = 0$$![[Pasted image 20250307140624.png]]
* We eliminate the integral in the KCL equation by differentiating once with respect to t, and because I0 is a constant, we get $$\frac{1}{R}\frac{dv}{dt} + \left(\frac{v}{L}\right)+C\frac{d^2v}{dt^2} = 0
  $$We now divide the equation by the capacitance C and arrange the derivatives in descending order.$$\frac{d^2v}{dt^2} + \left(\frac1{RC}\frac{dv}{dt}\right)\frac v{LC} = 0$$This equation is an ordinary second order diff eq with the constant coefficients because it describes a circuit with both an inductor and a capacitor. Therefore, we also call RLC circuits second-order circuits.
* We can't solve this equation like the past ones by separating the variables and integrating, so instead we assume v=Ae^(st), where A and s are unknown constants.
* Diff eq stuff
* ![[Pasted image 20250307141842.png]]
* ![[Pasted image 20250307141913.png]]
* ![[Pasted image 20250307142058.png]]
* ![[Pasted image 20250307142117.png]]
* ![[Pasted image 20250307142212.png]]
# Parallel RLC Overdamped Response [21:52]
* In this section, we find the natural response for each of the three types of damping; over, under, and critically. As we have already seen, the values of s1 and s2 determine the type of damping. We need to find values for the two coefficients A1 and A2 so that we can completely characterize the natural response $v = A_1s_1e^{s_1t}+A_2s_2e^{s_2t}$. This requires two equations based on the following observations:
	* The initial value of the voltage in the equation must be the same as the initial value of voltage in the circuit.
	* The initial value of the first derivative of the voltage in the equation must be the same as the initial value of the first derivative of the voltage in the circuit.
* As we will see, the natural response equations, as well as the equations for evaluating the unknown coefficients, are slightly different for each of the three types of damping. This is why the first task that presents itself when finding the natural response is to determine whether the response is over, under, or critically damped.
* ***When Overdamped*** $$v = A_1e^{s_1t}+A_2e^{s_2t}$$where s1 and s2 are the roots of the characteristic equation. The constants A1 and A2 are determined by the initial conditions, specifically from the values of v(0+) and dv(0+)/dt which in turn are determined from the initial voltage on the capacitor, v0, and the initial current on the inductor, I0.
* To determine the values of A1 and A2, we need two independent equations. The first equation sets the initial value from the equation to equal the initial value of v in the circuit, which is the initial voltage for the capacitor, v0, resulting is ![[Pasted image 20250307143429.png]]
* The second equation sets the initial value of dv/dt from the equations equal to the initial value of dv/dt in the circuit $$\frac{dv(0^+)}{dt} = s_1A_1+s_2A_2$$But how do we find the initial value of dv/dt frmo the circuit? Remember that dv/dt appears in the equation relating voltage and current for a capacitor $i_c = C\frac{dv}{dt}$. We can solve the capacitor equation for dv/dt and find it's initial value in terms of the initial current in the capacitor: $\frac{dv(0^+)}{dt} = \frac{i_c(0^+)}{C}$ ![[Pasted image 20250307143750.png]]
* Now we use KCL to find the initial current in the capacitor. We know that the sum of the three branch currents at t=0+ must be zero. The initial current in the resistive branch is the inital voltage v0 divided by the resistance, the initial current in the inductive branch is I0. Using the reference system, we obtain![[Pasted image 20250307143935.png]]
* The method for finding the voltage for the parallel RLC circuit below is as follows
	* Determine the initial values of v0 and I0, by analyzing the parallel RLC circuit for t < 0
	* Determine the values of the neper frequency, alpha, and the resonant radian frequency, omega, using the values of R,L, and C and the equations in the table.
	* Compare alpha^2 and omega^2. If alpha^2 > omega^2, the response is overdamped: $v(t) = A_1e^{s_1t}+A_2e^{s_2t}$
	* 
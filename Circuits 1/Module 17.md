# Response of First Order RL/RC [4:18]
* In this chapter, we focus on circuits that consist only of sources, resistors, and either (but not both) inductors or capacitors. We call these circuits RL and RC circuits. In chapter 6, we saw that inductors and capacitors can store energy. We analyze RL and RC circuits to determine the currents and voltages that arise when energy is either released or acquired by an inductor or capacitor in response to an abrupt change in a dc voltage or current source. 
* We divide our analysis of RL and RC circuits into three phases.
* First phase: Find the currents and voltages that arise when stored energy in an inductor or capacitor is suddenly released to a resistive network. This happens when the inductor or capacitor is abruptly disconnected from its dc source. Thus, we can reduce the circuit to one of the two equivalent forms shown below. These currents and voltages characterize the natural response of the circuit because the nature of the circuit itself, not external sources of excitation, determines the behavior. ![[Pasted image 20250228121758.png]]
* Second Phase: Find the currents and voltages tht arise when energy is being acquired by an inductor or capacitor when a dc voltage or current source is suddenly applied. This response is called the **step response**
* Third phase: Develop a general method for finding the response of RL and RC circuits to any abrupt change in a dc voltage or current source. A general method exists because the process for finding both the natural and step responses is the same. 
* ![[Pasted image 20250228122352.png]]
* RL and RC circuits are known as first-order circuits because their voltages and currents are described by first order differential equations. No matter how complex a circuit may appear, if it can be reduced to a Thevenin or Nortion equivalent connected to the terminals of an equivalent inductor or capacitor, it is a first order circuit. If the original circuit has two or more inductors or capacitors, they must be interconnected so that they can be replaced by a single equivalent element. After introducing the techniques for analyzing the natural and step responses for first-order circuits, we will discuss three special cases:
	* Sequential switching (circuits in which switching occurs at two or more instants in time)
	* Circuits with an unbounded response
	* The integrating amplifier circuit (containing an op-amp)
	* 
# The Natural Response of RL Circuits [24:19]
* We can describe the natural response of an RL circuit using the circuit below. We assume that the independent current source generates a constant current Is and that the switch has been in a closed position for a "long time. " We define the phrase *a long time* more accurately later in this section. For now it means that all currents and voltages have reached a constant value. Thus only constant, or dc, currents exist in the circuit just before the switch opens, and the voltage across the inductor is zero (Ldi/dt = 0). Therefore, before the stored energy is released
	* The inductor behaves like a short circuit
	* The entire source current Is appear in the inductive branch
	* There is no current in either R0 or R
* ![[Pasted image 20250228122956.png]]
* To find the natural response, we find the voltage and current at the terminals of the resistor R after the switch has been opened--that is, after thee source and its parallel resistor R0 have been disconnected and the inductor begins releasing energy. If we let t = 0 denote the instant when the switch is opened, we find v(t) and i(t) for t >= 0. For t >= 0, the circuit shown below reduces to the one to the right![[Pasted image 20250228124213.png]]
* To find i(t), we write an expression involving r, R, and L for the circuit below using KVL. Summing the voltages around the enclosed loop where we used the passive sign convention. The equation below is a first order ordinary differential equation because it involves the ordinary derivative of the unknown di/dt and the highest order derivative appearing in the equation is 1 $$L\frac{di}{dt} + Ri = 0$$ We can go one step further in describing this equation. The coefficients in the equation, R and L, are constants; that is, they are not functions of either the dependent variable, i, or the independent variable, t. Thus, the equation can also be described as an ordinary differential equation with constant coefficients. 
* To solve the equation, we divide by L, move the term involving i to the right hand side, and then multiply both sides by a differential time dt. The result is $$\frac{di}{dt}dt = -\frac{R}{L}i\space dt$$Next, we recognize the left-hand side of this equation simplified to a differential change in the current i, that is, di. We now divide through by i, getting $$\frac{di}{i} = -\frac{R}{L}dt$$We obtain an explicit expression for i as a function of t by integrating both sides. Using x and y as variables of integration yields $$\int_{i(t_0)}^{i(t)}\frac{dx}{x} = -\frac{R}{L}\int_0^tdy$$ where i(t0) is the current at time t0 and i(t) is the current at time t. Here, t0 = 0, therefore carrying out the indicated integration gives $$\ln\left(\frac{i(t)}{i(0)}\right) = -\frac{R}{L}t$$ Based on the definition of the natural log, we can solve for the current to get $$i(t) = i(0)e^{-(\frac{R}{L})t}$$
* Recall in chapter 6 that the inductor current cannot change instantaneously. Therefore, in the first instant after the switch has been opened, the current in the inductor remains unchanged. If $0^-$ is the time just prior to switching and $0^+$ is the right immediately following switching, then $$i(0^-) = I_0e^{-(\frac{R}{L})t}, t \ge 0$$
* The figure below shows the response, where the current has an initial value I0 and decreases exponentially toward zero as t increases. Note that the expression for i(t) includes the term $e^{-(\frac{R}{L})t}$ . The coefficient of t-- namely, R/L -- determines the rate at which the current approaches zero. 
* ![[Pasted image 20250302220726.png]]
* The reciprocal of this coefficient is the **time constant** of the circuit denoted $\tau = \frac{L}{R}$. Using the time constant, we write the expression for the natural response of an RL circuit as $$i(t) = i(0)e^{-(\frac{1}{ \tau})}$$
* Now we have a step-by-step method for finding the natural response of an RL circuit.
	1. Determine the initial current I0 in the inductor. This usually involves analyzing the circuit for t < 0
	2. Calculate the time constant tau. To do this, you need to find the equivalent resistance attached to the inductor for t >= 0.
	3. Write the equation for the inductor current for t >= 0 by substituting values for the inital current and the time constant into the equation above.
	4. Calculate any other quantities of interest, such as resistor current and voltage, using resistive circuit analysis techniques
* ![[Pasted image 20250302221151.png]]
* Example images.
	* ![[Pasted image 20250302221226.png]]
	* ![[Pasted image 20250302221254.png]]
	* ![[Pasted image 20250302221315.png]]
	* ![[Pasted image 20250302221349.png]]
	* ![[Pasted image 20250302221413.png]]
	* ![[Pasted image 20250302221433.png]]
	* ![[Pasted image 20250302221444.png]]
	* ![[Pasted image 20250302222143.png]]
	* The time constant is an important parameter for first order circuits. You can express the time elapsed after switching as an integer multiple of tau. For example, one time constant after the inductor begins releasing its stored energy to the resistor, the current has been reduced to e^-1, or approximately 37% of its initial value. The table below gives the value of e^-t/tau for integer multiples of tau from 1 to 10. Note that the current is less than 1% of its initial value when the elapsed time exceeds five time constants . So, five time constants after switching has occurred, the currents and voltages have essentially reached their vinal values. After switching,  the changes to the currents and voltages are momentary events and represent the **transient response** of the circuit.![[Pasted image 20250302222552.png]]
	* By contrast, the phrase *a long time* implies that give or more time constants have elapsed, for first order circuits. The response that exists a long time after witching is called the **steady-state response**. The phrase *a long time* then also means the time it takes the circuit to reach its steady state value. The time constant also represents the time required for the current to reach its final value if the current continues to change at its initial rate. To illustrate, we evaluate di/dt at 0^+ and assume that the current continues to change at this rate: $\frac{di}{dt}(0^+)=-\frac{I_0}{\tau}e^{-\frac{0^+}{\tau}} = \frac{-I_0}{\tau}$ 
	* Now,  if i starts at I0 and decreases at a constant rate of I0/tau amperes per second, the expression for i becomes: $i = I_0 - \frac{I_0}{\tau}t$
	* This expression indicates that i would reach its final value of zero in tau seconds. The figure below shows how this graphic interpretation can be used to estimate a circuits tie constant from a plot of its natural response. Such a plot could be generated on an oscilloscope measuring output current. Drawing the tangent intersects the time axis gives the value of tau. This allows you to determine the time constant of a circuit even if you don't know its component values. Up to this point, we have dealt with circuits having a single inductor. But the techniques presented apply to circuits with multiple inductors if the inductors can be combined into a single equivalent inductor.
	* ![[Pasted image 20250302223214.png]]
# The Natural Response of RC Circuits [20:56] 
* The form of an RC circuit's natural response is analogous to that of an RL circuit. Consequently, we don't treat the RC circuit in as much detail as we did the RL circuit. We develop the natural response of an RC circuit using the circuit shown below. Begin by assuming that the switch ahs been in position a for a long time, allowing the loop containing the dc voltage source Vg, the resistor R1, and the capacitor C to reach a steady-state condition. Recall from Chapter 6 that a capacitor behaves as an open circuit in the presence of a constant voltage, so the source voltage appears across the capacitor terminals. We will discuss how the capacitor voltage builds to the steady=state value of the dc voltage source. Here it is important to remember that when the switch is moved from position a to position b 9t = 0), the voltage on the capacitor is Vg. Because there can be no instantaneous change in the voltage at the terminals of a capacitor, the problem reduces to solving the circuit shown below. 
* ![[Pasted image 20250302223645.png]] the voltage source is Vg
* We can easily find the voltage v(t) by writing a KCL equation. Using the lower node between R and C as the reference node and summing the currents away from the upper node between R and C gives $$C\frac{dv}{dt} + \frac{v}{R} = 0$$ Comparing this equation with the RL one, you should see that the mathematical techniques used to find i(t) in the RL circuit can be used to find v(t) in the RC circuit. $$v(t) = v(0)e^{-\frac{t}{RC}}, t \ge 0$$As we have already noted, the initial voltage on the capacitor equals the voltage source Vg, or $$v(0^-)=v(0)=v(0^+)=v_g=v_0$$where v0 denotes the initial voltage on the capacitor. The time constant for the RC circuit equals the product of the resistance and capacitance: $\tau = RC$. Therefore, the general expression for the voltage becomes $$v(t) = V_0e^{\frac{-t}{\tau}}$$which indicates that the natural response of an RC circuit is an exponential decay of the initial voltage. The time constant RC governs the rate of decay. The figures below show the plot of the equation adn graphic interpretation of the time constant
* ![[Pasted image 20250303011323.png]]
* Now we have a step by step method for finding the natural response of an RC circuit
	1. Determine the initial voltage, V0, in the capacitor. This usually involves analyzing the circuit for t < 0
	2. Calculate the time constant, tau. To do this, you need to find the equivalent resistance attached to the capacitor for t >= 0
	3. Write the equation for the capacitor voltage for t >= 0 by substituting values for the initial voltage and time constant
	4. Calculate any other quantities of interest, such as resistor current and voltage, using resistive circuit analysis techniques.
* ![[Pasted image 20250303011544.png]]
* ![[Pasted image 20250303011646.png]]
* Example
	* ![[Pasted image 20250303011713.png]]
	* ![[Pasted image 20250303011741.png]]
	* ![[Pasted image 20250303011827.png]]
	* ![[Pasted image 20250303011914.png]]
	* ![[Pasted image 20250303011956.png]]
	* ![[Pasted image 20250303012008.png]]
	* ![[Pasted image 20250303012808.png]]
	* 
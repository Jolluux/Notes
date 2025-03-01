


# The Inductor - Current and Voltage Characteristics [11:19]
* An inductor is an electrical component that opposes any change in electrical current. It is composed of a coil of wire wound around a supporting core whose material can be magnetic or non magnetic. The behavior of inductors is based on the phenomena associated with the magnetic fields. The source of the magnetic field is charge in motion, or current. If the current is varying with time, the magnetic field is varying with time. A time-varying magnetic filed induces a voltage in any conductor linked by the field. The circuit parameter of **inductance** relates to the induced voltage to the current.
* The figure below shows an inductor represented graphically as a coiled wire. Its inductance is symbolized by the letter L, and is measured in henrys H. Assigning the reference direction of the current in the direction of the voltage drop across the terminals of the inductor, as shown below, and using the passive sign convention yields where v is measured in volts, L in henrys, i in amperes, and t in seconds. If the current reference is in the direction of the voltage rise $$v = L\frac{di}{dt}$$ is writted with a minus sign. 
* ![[Pasted image 20250227110810.png]]
* Note from this equation that the voltage across the terminals of an inductor is proportional to the time rate of change of the current in the inductor. We can make two important observations here. First, if the current is constant, the voltage across the ideal inductor is zero. Thus, the inductor behaves as a short circuit in the presence of a constant, or dc, current. Second, current cannot change instantaneously in an inductor; that is, the current cannot change by a finite amount in zero time. The equation tells us that this change would require an infinite voltage, and infinite voltages are not possible. For example, when someone opens the switch on an inductive circuit in an actual system, the current initially continues to flow in the air across the switch, a phenomenon called *arcing*. The arc across the switch prevents the current from dropping to zero instantaneously. 
* Example
	* Determining te Voltage, Given the current, at the Terminals of an inductor. The independent current source in the circuit shown below generates zero current for t < 0, and the pulse $10te^{-5t}A$ for t > 0
		* Sketch the current waveform
		* At what instant of time is the current at maximum?
		* Express the voltage across the terminals of the 100mH inductor as a function of time
		* Sketch the voltage waveform
		* Are the voltage and the current at a maximum at the same time?
		* At what instant of time does the voltage change polarity?
		* Is there ever an instantaneous change in voltage across the inductor? if so, at what time?
		* ![[Pasted image 20250227111440.png]]
		* ![[Pasted image 20250227112637.png]]
		* ![[Pasted image 20250227112844.png]]
		* ![[Pasted image 20250227112850.png]]
* Current in an Inductor in Terms of the Voltage Across the Inductor
	* The equation above expresses the voltage across the terminals of an inductor as a function of the current in the inductor. Now we express the current as a function of the voltage. To find i as a function of v, start by multiplying both sides of the above equation by a differential time dt: $vdt = L\left(\frac{di}{dt}\right)dt$. Multiplying the rate at which i varies with t by a differential change in time generates a differential change in i, so the expression simplifies to $vdt = Ldi$. We next integrate both sides of the simplified expression. For convenience we interchange the two sides of the equation and write $L\int_{i(t_0)}^{i(t)}dx = \int_0^tvd\tau$ . Note that we use x and $\tau$ as the variables of integration, so i and t become limits on the integrals. then, divide both sides of the integral equation by L and solve for the inductor current to get $$i(t) = \frac{1}{L}\int_0^tvd\tau+i(t_0)$$ where i(t_0) is the value of the inductor current at the time when we initiate the integration, namely t0. in many practical applications, t0 is zero and the equation replaces it with i(0).
* Example again
	* Determining the current, given the voltage, at the terminals of an inductor.
	* The voltage pulse applied to the 100mH inductor shown below is 0 for t > 0 and is given by the expression $v(t)=20te^{-10t}V$
	* For t>0, also assume i = 0 for t$\le$ 0.
	* Sketch the voltage as a function of time
	* Find the inductor current as a function of time
	* Sketch the current as a function of time. 
	* ![[Pasted image 20250227114339.png]]
	* ![[Pasted image 20250227114605.png]]
	* ![[Pasted image 20250227114732.png]]
# The Inductor - Power and Energy [23:19]
* The power and energy relationships for an inductor can be derived directly from the current and voltage relationships. If the current reference is in the direction of the voltage drop across the terminals of the inductor, the power is $p=vi$. Remember that pwoer is in watts, voltage is in volts, and current is in amperes. If we express the inductor voltage as a function of the inductor current, the expression for the inductor power becomes $$p=Li\frac{di}{dt}$$ We can also express the current in terms of the voltage:$$p=v\left[ \frac{1}{L}\int_0^t vd\tau + i(t_0)\right]$$
* We can use the equation below to find the energy stored in the inductor. Power is the time rate of expending energy, so $$P=\frac{dw}{dt} = Li\frac{di}{dt}$$ Multiplying both sides by a differential time gives the differential relationship $$dw = Li\space di$$Integrate both sides of the differential relationship, recognizing that the reference for zero energy corresponds to zero current in the inductor. Thus $$\text{Power in an Inductor}; \space p=Li\frac{di}{dt}$$$$\text{Energy in an Inductor}; \space w=\frac{1}{2}Li^2$$
* ![[Pasted image 20250227143327.png]]
* ![[Pasted image 20250227143451.png]]
* ![[Pasted image 20250227143527.png]]
* ![[Pasted image 20250227143553.png]]
* ![[Pasted image 20250227143645.png]]
* ![[Pasted image 20250227143745.png]]
* ![[Pasted image 20250227143807.png]]
* ![[Pasted image 20250227145357.png]]
# The Capacitor - Voltage and Current Characteristics [9:34]
* A capacitor is an electrical component consisting of two conductors separated by an insulator or dielectric material. The capacitor is the only device other than a battery that can store electric charge. The behavior of capacitors is based on phenomena associated with electric fields. The source of the electric field is separation of charge, or voltage. If the voltage is varying with time, the electric field is varying with time. A time-varying electric field produces a displacement current in the space occupied by the field. the circuit parameter of capacitance related the displacement current to the voltage, where the displacement current is equal to the conduction current at the terminals of the capacitor. C - Farads.
* The capacitors symbol reminds us that the capacitance occurs whenever electrical conductors are separated by a dielectric, or insulating, material. This condition implies that electric charge is not transported through the capacitor. Although applying a voltage to the terminals of the capacitor cannot move a charge through the dielectric, it can displace a charge within the dielectric. As the voltage varies with time, the displacement of charge also caries with time, causing what is known as the **displacement current**. The displacement current is indistinguishable from the conduction current at the capacitor's terminals. The current is proportional to the rate at which the voltage across the capacitor varies with time, so $$i=C\frac{dv}{dt}$$
* i is measured in amperes, C in farads, v in volts, and t in seconds. The current reference is in the direction of the voltage drop across the capacitor. Using the passive sign convention, we write the equation above with a positive sign. If the current reference is in the direction of the voltage rise, the equation is then written with a minus sign. 
* Two important observations follow from the equation. If the voltage across the terminals is constant, the capacitor current is zero because a conduction current cannot be established in the dielectric material of the capacitor. Only a time-varying voltage can produce a displacement current. Thus, a capacitor behaves as an open circuit in the presence of a constant voltage. Second, voltage cannot change instantaneously across the terminals of a capacitor. The equation indicates that such a change would probably produce infinite current, a physical impossibility. 
* The equation gives the capacitor current as a function of the capacitor voltage. To express the voltage as a function of the current, we multiply both sides of the equation by a differential time dt and then integrate the resulting differentials: $$i\space dt = C \space dv or \int_{v(t_0)}^{v(t)}dx = \frac{1}{C}\int_{t_0}^td\tau$$
* Carrying out the integration of the left-hand side of the second equation rearranging gives $$v(t) = \frac{1}{C}\int_{t_0}^tid\tau + v(t_0)$$
* We can easily derive power and energy relationships for the capacitor. From the definition of power $$p = vi = Cv\frac{dv}{dt}$$ or $$p = i\left[ \frac{1}{C}\int_{t_0}^tid\tau + v(t_0) \right]$$ combining the definition of energy with above gives $$dw=Cvdv$$ from which you integrate and get$$w=\frac{1}{2}Cv^2; \space p = Cv\frac{dv}{dt}$$ In deriving the equations, the reference for zero energy corresponds to zero voltage. 
* Example
	* ![[Pasted image 20250227152930.png]]
	* ![[Pasted image 20250227152950.png]]'![[Pasted image 20250227152958.png]]
	* ![[Pasted image 20250227153024.png]]
	* ![[Pasted image 20250227153100.png]]
# The Capacitor - Power and Energy Characteristics [18:08] 
* ![[Pasted image 20250227153527.png]]
* ![[Pasted image 20250227153708.png]]
* ![[Pasted image 20250227154006.png]]
* ![[Pasted image 20250227154018.png]]
* ![[Pasted image 20250227154041.png]]
* ![[Pasted image 20250227154103.png]]
* ![[Pasted image 20250227154218.png]]![[Pasted image 20250227154249.png]]
* ![[Pasted image 20250227155807.png]]
# The Inductor - Series & Parallel [15:49]
* ![[Pasted image 20250227160032.png]]
* ![[Pasted image 20250227160223.png]]
* ![[Pasted image 20250227160747.png]]
# The Capacitor - Series and Parallel
* ![[Pasted image 20250228104142.png]]
* ![[Pasted image 20250228104200.png]]
* ![[Pasted image 20250228104232.png]]
* ![[Pasted image 20250228105711.png]]
* 
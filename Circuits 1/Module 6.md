# Patrick Lecture
## Recap of Voltage & Current Division
* ![[Pasted image 20250129093818.png]]
* ![[Pasted image 20250129093824.png]]
* ## Currently and Voltage Measurement
	* An ammeter is an instrument designed to measure current; it is placed in series with the circuit element whose current is being measured.
	* A voltmeter is an instrument designed to measure voltage; it is placed in parallel with the element whose voltage is being measured.
* ## Nonideal Ammeters and Voltmeters
	* Analog Meters
	* Digital Meters (Ideal)
	* Real meters add resistance to the system. Digital meters are more accurate than analog (add less resistance).
* ## D'Arsonval Movement Meters
	* Physical function discussed in Lecture Videos (watch after class)
	* ![[Pasted image 20250129094106.png]]
		* Ammeter is placed in series with element whose current is being measured
		* Voltmeter is placed in parallel with the element whose voltage is being measured.
	* ### Example:
		* ![[Pasted image 20250129094154.png]]
		* ![[Pasted image 20250129094211.png]]
* ## The Wheatstone Bridge Circuit
	* ![[Pasted image 20250129095538.png]]
	* $R_1 \text{and } R_2 \text{are known fixed resistors.}$
	* $R_3 \text{ is a variable resistor}$
	* $R_x$ is an unknown resistance
	* $R_x$ could be:
		* a resistive strain gauge
		* a thermistor (temp sensitive resistor)
		* a resistive photocell
	* A Wheatstone bridge is vey sensitive to small changed in resistance
	* ### How to find $R_X$ 
		* ![[Pasted image 20250129095800.png]]
		* $R_x = \frac{R_2}{R_1}R_3$ 
* ## Class Problem
	* 

# Measuring Voltage & Current [3:41]
* Working with actual circuits often requires making voltage and current measurements. The next two sections explore several common devices used to make these measurements. The devices are relatively simple to analyze and offer practical examples of the current-divider and voltage-divider configurations. We begin by looking at ammeters and voltmeters.
	* An ammeter is an instrument designed to measure current; it is placed in series with the circuit element whose current is being measured
	* A voltmeter is an instrument designed to measure voltage; it is placed in parallel with the element whose voltage is being measured.
* Ideal ammeters and voltmeters have no effect on the circuit variable they are designed to measure. That is, an ideal ammeter has an equivalent resistance of 0 $\Omega$  and functions as a short circuit in series with the element whose current is being measured. AN ideal voltmeter has an infinite equivalent resistance $\left ( \infty \Omega \right )$ and functions as an open circuit in parallel with the element whose voltage is being measured.

# The D'Arsonval Analog Meter
* Analog meters
	* based on the D'Arsonval meter movement, which includes a dial readout pointer as shown in the photo below. The D'Arsonval meter movement consists of a movable coil placed in the field of a permanent magnet. When current flows in the coil, it creates a torque on the coil, causing it to rotate and move a pointer across a calibrated scale. By design, the deflection of the pointer is directly proportionally to the current in the movable coil. The coil is characterized by both a voltage rating and a current rating. For example, one commercially available meter movement is rated at 50 mV and 1 mA. This means that when the coil is carrying 1 mA, the voltage drop across the coil is 50 mV and the pointer is deflected to its full-scale position. 
	* ![[Pasted image 20250129111925.png]]
	* An analog ammeter consists of a D'Arsonval movement in parallel with a resistor, as shown below. The parallel resistor limits the amount of current in the movement's by shunting some of it through RA. In contrast, an analog voltmeter consists of a D'Arsonval movement in series with a resistor, as shown below. Here, the resistor limits the voltage drop across the meter's coil. In both meters, the added resistor determines the full-scale reading of the meter movement. 
	* ![[Pasted image 20250129112243.png]]
	* From these descriptions we ese that an analog meter is non ideal; both a the added resistor and the meter movement introduce resistance in the circuit where the meter is attached, In fact, any instrument used to make physical measurements extracts energy from the system while making measurements.  The more energy distracted by the instruments, the more severely the measurement is disturbed. The equivalent resistance of a real ammeter is not zero, so it adds resistance to the circuit in series with the element whose current is being read. The equivalent resistance of a real voltmeter is not infinite, so it adds resistance to the circuit in parallel with the element whose voltage is being read. 
* Example with Ammeter
	* ![[Pasted image 20250129114507.png]]
	* ![[Pasted image 20250129180623.png]]
	* ![[Pasted image 20250129180711.png]]
	* ![[Pasted image 20250129180759.png]]
* Example with Voltmeter:
	* ![[Pasted image 20250129181227.png]]
	* ![[Pasted image 20250129181338.png]]
	* ![[Pasted image 20250129182848.png]]
	* Part D is 5k$\Omega$ 
* Digital Meters
	* measure the continuous voltage or current signal at discrete points in time, called the sampling times. The signal is thus converted from an analog signal, which is continuous in time. A more detailed explanation of the workings of digital meters is beyond the scope of this text and course. However, you are likely to see and use digital meters in lab settings because they offer several advantages over analog meters. They introduce less resistance into the circuit to which they are connected (though they are still non ideal), are easier to connect, and take more precise measurements owing to the nature of their readout mechanism. 
# Volt meter. Amp meter 6-3 [11:38]
* Measuring Resistance - The Wheatstone Bridge
	* While many different circuit configurations are used to measure resistance, here we will focus on just one, the Wheatstone bridge. The Wheatstone bridge, circuit is used to precisely measure resistances of medium values, that is, in the range of 1 $\Omega$ to 1 $\text{M}\Omega$ . In commercial models of the Wheatstone bridge, accuracies on the order of $\pm 0.1\%$ are possible. The bridge circuit, shown blow, consists of four resistors, a DC voltage source, and a detector. the resistance of one of the four resistors can be varied, which is indicated by the arrow through $R_3$ . The DC voltage source is usually a battery, which is indicated by the battery symbol for the voltage source v below. The detector is generally a D'Arsonval movement in the microamp range and is called a *galvanometer.* Below, $R_1$ , $R_2$ , and $R_3$ are known resistors and $R_x$ is unknown. 
	* ![[Pasted image 20250129210329.png]]
	* To find the value of $R_x$ we adjust the variable resistor $R_3$ until there is no current in the galvanometer. We then calculate that the unknown resistor from the simple expression$$R_x = \frac{R_2}{R_1}R_3$$ We derive this equation by applying Kirchhoff's law to the bridge circuit. We redraw the bridge circuit as below to show the branch currents in the bridge. When $i_g$ is zero, we say the bridge is balanced. At node **a**, Kirchhoff's current law requires that $i_3 = i_1$, while at node **b**, KCL requires $i_2 = i_x$. 
	* ![[Pasted image 20250129210832.png]]
	* We did the rest in class, along with the practice problem.
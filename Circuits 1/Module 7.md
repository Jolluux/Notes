# D-Y and Y-D Transformations [5:55]
* Delta-to-Wye (Pi-to-Tee) Equivalent Circuits
	* Look again at the Wheatstone bridge, if we replace the galvanometer with it's equivalent resistance $R_m$ , we get the circuit shown below. Because this circuit does not have any series-connected or parallel-connected resistors, we cannot simplify it using the simple series or parallel equivalent circuits introduced earlier in this chapter. BUt the five interconnected resistors can be reduced to a single equivalent resistor using a delta-to-wye ($\Delta - \text{to} - Y$) or pi-to-tee ($\pi - \text{to} - T$) equivalent circuit. 
	* ![[Pasted image 20250130230028.png]]
		* **1** $\Delta$ and Y structures are present in a variety of useful circuits, not just resistive networks. Hence the $\Delta$ and Y transformation is a helpful tool in circuit analysis.
*  The resistors $R_1, R_2, \text{and} \space R_m \left ( \text{or} \space R_3, R_m, \text{and} \space R_x \right )$ in the circuit shown below form a **delta** ($\Delta$) **interconnection** because the interconnection looks like the Greek letter Delta $\Delta$ . It is also called a **pi interconnection** because the $\Delta$ can be reshaped like the Greek letter $\pi$ without disturbing the electrical equivalence of the two configurations, as shown below.
	* ![[Pasted image 20250130230952.png]]
* The resistors $R_1, R_m, \text{and} \space R_3 \left ( \text{or} \space R_2, R_m, \text{and} \space R_x \right )$ in the circuit shown below form a **wye (Y) interconnection** because the interconnection can be shaped to look like the letter Y. The Y configuration is also called a **tee (T) interconnection** because the Y structure can be reshaped into a T structure without disturbing the electrical equivalence of the two structures, as shown below. 
	* ![[Pasted image 20250130231248.png]]
* The figure below illustrates the $\Delta - \text{to} - Y$ (or $\pi - \text{to} - T$) equivalent circuit transformation. but we cannot transform the $\Delta$ interconnection into the Y interconnection simply by changing the shape of the interconnections. Saying the $\Delta$-connected circuit is equivalent to the Y-connected circuit means that the $\Delta$ configuration can be replaced with a Y-configuration without changing the terminal behavior. Thus, if each circuit is placed in a black box, we can't tell whether the box contains a set of $\Delta$- connected resistors or a set of Y-connected resistors by making external measurements. 
* This condition is true only if the resistance between corresponding terminal pairs is the same fore ach box. For example, the resistance between terminals a and b must be the same whether we use the $\Delta$-connected set or the Y-connected set. For each pair of terminals in the Y-connected circuit, compute the equivalent resistance using only series simplification. The three equivalent resistance equations are:
	* $$R_{ab} = \frac{R_c \left ( R_a + R_b\right )}{R_a + R_b + R_c} = R_1 + R_2$$
	* $$R_{bc} = \frac{R_a \left ( R_b + R_c \right )}{R_a + R_b + R_c} = R_2 + R_3$$
	* $$R_{ca} = \frac{R_b \left ( R_c + R_a \right )}{R_a + R_b + R_c} = R_1 + R_3$$
	* ![[Pasted image 20250130233326.png]]
* Straight forward algebraic manipulation of the equations above gives the values for the Y-connected resistors in terms of the $\Delta$-connected resistors. Use these equations when transforming three $\Delta$-connected resistors into an equivalent Y connection.
	* $$R_1 = \frac{R_bR_c}{R_a + R_b + R_c}$$
	* $$R_2 = \frac{R_cR_a}{R_a + R_b + R_c}$$
	* $$R_3 = \frac{R_aR_b}{R_a + R_b + R_c}$$
* Reversing the $\Delta - \text{to} - Y$ transformation also is possible, so we can start with a Y structure and replace it with an equivalent $\Delta$ structure. The expressions for the three $\Delta$-connected resistors as functions of the three Y-connected resistors are
	* $$R_a = \frac{R_1R_2+R_2R_3+R_3R_1}{R_1}$$
	* $$R_b = \frac{R_1R_2+R_2R_3+R_3R_1}{R_2}$$
	* $$R_c = \frac{R_1R_2+R_2R_3+R_3R_1}{R_3}$$
# Application of D-Y and Y-D transformations [13:14]
* Example 1:
	* ![[Pasted image 20250130235454.png]]
	* ![[Pasted image 20250130235803.png]]
* Example 2 (Pearson):
	* ![[Pasted image 20250131000201.png]]
	* ![[Pasted image 20250131000311.png]]
# Special Cases (Power) of D-Y and Y-D transformations [5:12]
* We will now set $R_a = R_b = R_c$ && $R_1 = R_2 = R_3$. This is known as a **balanced system.** 
	* $$R_{ab} = \frac{R_c \left ( R_a + R_b\right )}{R_a + R_b + R_c} = R_1 + R_2$$
	* $$R_{bc} = \frac{R_a \left ( R_b + R_c \right )}{R_a + R_b + R_c} = R_2 + R_3$$
	* $$R_{ca} = \frac{R_b \left ( R_c + R_a \right )}{R_a + R_b + R_c} = R_1 + R_3$$
* When there is a balanced system:00
	* $$R_{ab} = \frac{2{R_\Delta}^2}{3R_{\Delta}} = 2R_Y$$
	* $$3R_Y = \frac{{R_{\Delta}}^2}{R_{\Delta}} \Longrightarrow R_y = \frac{R_{\Delta}}{3}$$
	* $$R_Y = \frac{{R_{\Delta}}^2}{3R_{\Delta}} \Longrightarrow R_Y = \frac{R_{\Delta}}{3}$$

# Lecture 1/31
* Most is repeated, there is this tho
* ![[Pasted image 20250131093831.png]]
* Voltage Division:
	* $V_1 = \frac{V_s + R_{eq}}{R_a + R_{eq}}$
	* 






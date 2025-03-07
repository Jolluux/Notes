# The Ideal Diode [8:25]
* ![[Pasted image 20250305081141.png]]
*  ![[Pasted image 20250305081722.png]]
* i > 0, v = 0, short
* i = 0, v < 0, open
* ![[Pasted image 20250305081802.png]]
# The Diode DC Component [16:15]
* Offset Diode Model
* ![[Pasted image 20250305082025.png]]
*  ![[Pasted image 20250305082629.png]]
* ![[Pasted image 20250305083011.png]]
* Vd = 0
* ![[Pasted image 20250305083231.png]]
* ![[Pasted image 20250305083505.png]]
* The process of taking the negative half of the sin wave out is half-wave rectification
* V_DC = Vp / pi
* ![[Pasted image 20250305083734.png]]
# The Diode - Ripple [4:57]
* Ripple: $v_{rip}(t) = v_0(t)-v_{DC}$
* Reduce the ripple : R_D || C
* Changes the wave form to discharge slower per time constant. Makes it stay above the V_DC of Vp/pi. "Filters" out the AC component, lowpass filter.
* R_D * C must be greater than the period *by a lot* 
* ![[Pasted image 20250305084456.png]
# The Diode Rectifier, Full-Wave Rectification [14:37]
* Bridge rectifies, 4 diodes
* ![[Pasted image 20250305090309.png]]
* 0 <= t <= T/2, Vs > 0, i > 0; D1 and D4 closed, D2 and D3 open. Vs(t) = V_0(t)
*  T/2 < = t <= T, Vs <= 0, i' > 0
	* i' because it flows from the negative terminal
* D3 and D2 are closed, D1 and D4 are open. V_0(t) = -V_s(t) >= 0
* ![[Pasted image 20250305091235.png]]
* ![[Pasted image 20250305091250.png]]
* 
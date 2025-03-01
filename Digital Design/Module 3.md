# VHDL :0
- What is an entity?
	- An entity description declares inputs and outputs of the circuit being described
	- An entity contains a port, which defines the interface for the module. The port has the list of inputs and outputs, which are called signals
	- In VHDL, there are **variables** and there are **signals**, which get synthesized to different things.
	- Viewed from outside, entity is a "Black Box", structure/behavior is hidden, only inputs and outputs are visible
- Structure vs Behavior
	- Defining an entity through structure is just connecting different components together rather than writing functions/equations/conditionals/etc. to have behavior
	- Defining an entity through behavior is writing actual equations and logic and so on to define the entity's behavior

## Entity - Definition
```vhdl
library ieee; -- library to be used
use ieee.std_logic_1164.all; -- which part of library

entity two_gate is -- name of entity
-- keyword "port" defines the interface
port( x1, x2 : in std_logic; -- two input signals, x1 and x2
	  y : out std_logic); -- one output signal, y 
	  -- std_logic = datatype of signal, a single bit (with extra stuff)
end two_gate; -- end entity
```

The behavior of an entity is described in the **architecture**. The architecture has a unique name, signals and components can be internally declared, and is assigned to a unique entity.
One entity can have multiple architectures.

## Architecture - Definition
```vhdl
-- two_gate_nand = architecture name, two_gate = entity name
architecture two_gate_nand of two_gate is
-- internal signal declaration would go here
begin -- start behavioral/structural definition
	y <= not (x1 and x2); -- y = x1 nand x2
end two_gate_nand; -- end architecture
```

## XOR Entity
```vhdl
library.ieee;
Use ieee.std_logic_1164.all;

ENTITY xor_gate IS
PORT(
	x1, x2 : IN std_logic;
	y      : OUT std_logic
); END xor_gate;

ARCHITECTURE behavioral OF xor_gate IS
BEGIN

y <= x1 XOR x2;

END
```

Signal Assignment: `y <= x1`
Boolean Operators
```vhdl
and, or, nand, nor, xor, xnor
```
Random Boolean statements can be specified in VHDL with parentheses. 

## Assignments and Statements
Signal assignment: `y <= x1`
Boolean operators available: `and, or, nand, nor, xor, xnor`. Parenthesis can be used between expressions to enforce precedence.

**Concurrent statements**: All concurrent statements execute at the same time. Anything outside a process is a concurrent statement. 

**Sequential statements**: Sequential statements can only be used within a process. Sequential statements execute depending on their sequence.

A process itself is a concurrent statement (executes alongside other statements), and everything inside a process is sequential.

VHDL describes parallel processes. All signal assignments take place simultaneously.
For example,
```vhdl
A <= B;
C <= A;
-- Because signal assignments take place simultaneously, C will always take on the previous value of A rather than the value of B.
```

A signal defines a connection in hardware. It can also be used to connect components within an entity. A signal has a datatype, which is the set of possible values and operations on those values
```vhdl
signal signal1[,signal2, signal3, ...] : signal_type;
```
Declaration can be done in package, port declaration of an entity, and in other places.

Internal signals can be used within an architecture to simply logic. 
```vhdl
entity position is
port(a : in std_logic_vector(2 downto 0);
	b : out std_logic_vector(0 to 2));
end position;

architecture behv of position is:
signal signal1, signal2 : std_logic; -- internal signal
signal signal3 : std_logic_vector(4 downto 0); -- another internal signal

begin
signal1 <= a(0) and b(2);
b(0) <= signal1 xor a(1);
...
```

## REMEMBER VHDL IS A DESCRIPTION LANGUAGE YOU ARE DEFINING A CIRCUIT NOT VARIABLES SO IN THIS EXAMPLE

```vhdl
architecture structural of example is
signal int_sig : std_logic;
begin
int_sig <= (b or c);
g <= c and (int_sig and (not(a and b)));
...
```
`g` is **not** defined because we are defining a circuit, so when inputs get received they will propagate like normal.

## Variables
A variable defines a memory location, it can be used to store values. A variable has a datatype similar to a signal. Variable declaration:
```vhdl
variable var1[, var2, var3, ...] : var_type;
```
Variable declaration can be done **exclusively** in a process. Variable assignment is performed with the symbol `:=`, ex. `a := '0'`.

## Datatypes
Datatypes define a set of values a signal or variable can take, along with operations on those values. Predefined datatypes:
- bit (std_logic): '0', '1'
- bit vector (std_logic_vector): "0001", "101010"
- integer: 10, 23
- character: "a"
- string: "aodsfaodhfisadhf"

## Other stuff
- Standard logic IEEE1164
	- Declaration in package \_standard_logic\_1164
	- Possible values: 'U' not initialized, 'X' unknown, '0' logic 0, '1' logic 1, 'Z' high impedence, 'W' unknown weak signal, 
- Logic vectors
	- Single signals can be grouped into a vector: std_logic -> std_logic_vector
	- Define them through std_logic_vector(2 downto 0) for decreasing index from MSB to LSB, std_logic_vector(0 to 2) for increasing index from MSB to LSB.
- Logic vector assignment:
	- By position (assigning each index)
	- Concatenation: `vector <= A & B & C;`
	- Aggregates: `vector <= (A, B, C, D);`
	- By index: `vector <= (3 => '1', 1 downto 0 => '1', 2 => '0')`
	- Others: `vector <= (3 => '1', 1 => '0', others => '0')`
		- Can set everything to zero with `vector <= (others => '0')`
- Operators:
	- Logic operators
		- AND, OR, NAND, NOR, XOR (Equal Precedence)
		- NOT (higher precedence)
	- comparison
		- <, <=, =, >=, >, /=
	- Arithmetic operators
		- +, -, *, /, `**`(exponent), abs, mod, rem,
- Concurrent Assignment Statements
	- Simple Assignment
		- signal name <= expression
		- Example 2:

```vhdl
SIGNAL X,Y : STD_LOGIC_VECTOR(3 downto 0);
SIGNAL Sum : std_logic_vector(4 downto 0);
SIGNAL Cin : std_logic;
Sum = ('0' + X) + ('0' + Y) + Cin
```
* Assigning Signal Values Using Others
```vhdl
SIGNAL S : std_logic_vector(4 downto 0);
S <= "00000"
S <= (others => '0')
```
* Selected Signal Assignment
```vhdl
SIGNAL x1, x2, Sel, f : std_logic;
WITH Sel SELECT
	f <= x1 when '0'
	x2 when others;
```
* Conditional Signal Assignment
```vhdl
[label:]
signal_name <= expression WHEN logic_expression ELSE {expression WHEN logic expression ELSE} expression;
-- Example
f <= '1' WHEN x1 = x2 ELSE '0';
```
* Process - Parallel Statements
	* Process Execution:
		* Selection (module) in the architecture execute in parallel
		* Processes communicate with other components using signals
		* A process has a sensitivity list. That is the list of all the signals that activate the process when their value change (event).
```vhdl
-- Inside an Architecture
BEGIN
[label:] PROCESS (x1, x2, ...)
-- Sensitivity list: driven signals activate the process on change. Analog to:,, wait and see if x1 or x2 has change" (alternative, internal wait statement)
BEGIN
	parallel Area; 
-- Behavior is evalued in parallel! Different to variables in traditional Programming language. 
END PROCESS [label:] --process name optional
END
```
* Processes are accompanied by a **sensitivity list**. All inputs to the logic inside the process MUST be listed in the sensitivity list.
* When a signal listen in the sensitivity list changes, the process will restart and the values computer by the logic will change. If an input to the logic is not listed in the sensitivity list (parameters), this change may not occur, resulting in an incorrect output.
Example:
```vhdl
Entity 'Or' is
	port(
	A, B : in bit;
	   Z : out bit
	);
architecture bh of 'Or' is
begin
--process declaration
or_func:process(A,B)
	begin
		if (A = '1' or B = '1') then
			Z <= '1';
		else
			Z <= '0';
		end if;
	end process;
end bh;
```
Control- Flow
```vhdl
-- IF-Else
if condition then
	sequential instructions
end if;
if condition then
	instructions
elsif condition 
	instrucitons
else
	instructions
end if;
```
```vhdl
--Case
case object is
	when value 1 => instructions
	when value 2 => instructions
	when 3 to 10 => instructions
	...
	when value n => instructions
	when others => instructions
```
```vhdl
-- For Loops
[loop label:]
for variable_name in range LOOP
	statement;
	{statement;}
end loop [loop label];

[loop label:]
while variable_name IN range loop
	statement;
	{statement;}
end loop [loop label];
```

* Synchronous Circuits
	* outputs are correct with the value of the clock
	* Clock: special signal with alternating 1 and 0 values
	* Clock Cycle: Distance between two edges
	* Edges can be positive or negative
		* falling edge = negative
		* rising edge = positive
```vhdl
((clock event) AND (clock = '1')) -- rising edge
((clock event) AND (clock = '0')) -- falling edge
```
* Hierarchy
	* Components (modules, submodules) are instantiated in a high level (top level) design to build more complex structures
	* Example: full adder
		* instantiation of 2 half adders and 1 XOR-Gate (check slides I ain't writing allat)
more vhdl later

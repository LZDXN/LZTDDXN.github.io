This chapter focus on heat, temperature and concepts related to those.
- Heat is defined as thermal energy transmitted from one to another.
- Thermal energy exist due to the random motion of an object's molecules.
- An object doesn't contain heat, heat is energy in transit.
- Temperature, is a measure of an object's internal thermal energy

### Heat Transfer
There are three principal modes by which energy can be transferred:
- Conduction: Transfer by a solid (usually metal), for example, when you order a cup of hot coffee, the heat from coffee to solid cup, from the cup to you hand. 
- Convection: Happens in gas and liquid. Usually the higher temperature gas or liquid flows up, lower temperature flows down. This example can be seen during the process of heating water. (If earth science, magma convection)
- Radiation: Through light. For example radiant energy from the sun's fusion reactions.

Heat conducts from one point to another only if there is a temperature difference ($\Delta T$) The rate at which heat is transferred is given by $$H = \frac{Q}{\Delta{t}}=\frac{kA\Delta{T}}{L}$$
- Q: Energy transferred to a system by heating
- t: Time
- k: Coefficient of thermal conductivity of an object
- A: Area
- T: Temperature
- L: Thickness

### The Kinetic Theory of Gases
- Atoms or molecules in gas move freely and rapidly
- A confined gas exerts a fore on the walls of its container
- Pressure $P$ increases when the gas molecules move faster in a zipped container.

### The Ideal Gas Law
The most important equation through the whole Thermal energy unit: $$PV = nRT$$ This can also be applied in AP Chemistry
- n: The number of moles of gas
- R: Universal gas constant (8.31 J/mol*K)
- This equation can also be written as $PV = Nk_BT$, which $k_B$ is Boltzmann's constant ($k_B = 1.38 \times 10^{-23}$J/K)

### The Laws of the Thermodynamics
This study of the energy transfers involving work and heat, and the resulting changes in internal energy, temperature, volume and pressure is called **Thermodynamics**
#### The Zeroth Law of Thermodynamics
>If Objects 1 and 2 are in thermal equilibrium with Object 3, then Objects 1 and 2 are in thermal equilibrium each other.
#### The First Law of Thermodynamics
>Energy (in the form of heat) is neither created nor destroyed in any thermodynamic system.

From those laws above, we can see every equations are base on those conditions. 
The questions are usually based on an insulated container filled with an ideal gas rests on a heat reservoir.
![[thermow=pv.png]]
The state of gas is given one its pressure, volume and temperature are known. Also we study the changes in variable when work are done in this system. Thus we can use the ***P-V*** **diagram** to see how the system is affected as it moves from one state to another.
![[pv_diagram.png]]
From Physics 1 we know that the work is calculated by the equation $W = -Fd$, since $F = PA$, we have $W = -PAd$. In addition, we know that the Volume of container is calculated by $V = Ad$, which lead the equation we have: $$W = -P\Delta V$$
- Textbooks differ about the circumstances under which work in thermodynamics is defined to be + or -
- But for the Exam AP Physics 2, the work in thermodynamics is *positive* when the work is being done *on the system*. So,
	- When $\Delta V$ is negative, energy is being *added* to the system by $W = -P\Delta V$ and W is *positive*.
	- Also, when the system in doing work *on surroundings* the work is *negative*, energy is leaving the system.
	- The Area $aV_aV_bb$ is work

Experiments have shown that the value of Q+W is not path dependent; it depends only on the initial and the final state of the system.  This property is called the system's **internal energy**, denoted $U$. The equation we have $$\Delta U = Q \space + \space W$$ $\Delta U$ depends only on the temperature change. (If $\Delta V$ is zero, $W = 0$ and $U = 0$)
By the definition of Ideal Gas Law, we can also have those different situations:
![[thermal.png]]
==Don't confuse *isothermal* with *adiabatic*==
- Isothermal: 等温线, when temperature remains constant
- Isobaric: 等压线
- Isochoric: 等容线
- Adiabatic: 绝热的, when $Q = 0$

==It is possible for $U$ to remain unchanged even if $Q$ is not 0==

Here come my favorite one:
#### The Second Law of Thermodynamics
##### Entropy (S)
- Measurement of disorder
- Higher entropy, more chaotic
- Lower entropy, less chaotic
- From Solid -> Liquid/Gas, or Liquid -> Gas, $\Delta S$ is *positive*
- On the other hand, Gas -> Liquid/Solid, or Liquid -> Solid, $\Delta S$ is *negative*

The essence of one form of the Second Law of Thermodynamics:
>The total amount of disorder -- the total entropy -- of a system plus its surroundings will never decrease.

so,
>The $\Delta S$ is always *positive* in the universe, unless there is any multi-universe.

### Heat Engines
This part describes the efficiency of converting work to heat. A device that uses heat to produce useful work is called a **heat engine**.
- All engines function to convert heat into work by exchanging energy from a reservoir at higher temperature to reservoirs of lower temperature.
- in the exam we look at the cyclic engines only, so the system returns to its original state at the end of each cycle, so $\Delta U = 0$.
	- Heat absorbed from high-temperature source is denoted $Q_H$ (H for hot)
	- Heat discharged into the low-temperature reservoir is denoted $Q_C$ (C for cold)
	- $Q_H$ is positive, $Q_C$ is negative
	- Net heat: $|W| = Q_{net}  = Q_H + Q_C$ usually we write $Q_{net}$ as $Q_H-|Q_C|$ to show $Q_{net}$ is less than $Q_H$

Based on one of the forms of **The Second Law of Thermodynamics**:
>For any cyclic heat engine, some exhaust heat is always produced. It's impossible to completely convert heat into useful work.

![[heatengine.png]]

##### Efficiency of heat engines
The efficiency of heat engines is given by the fractional ratio between the total work done and the orginal amount of heat added:
Efficiency = $$\frac{W}{Q_1}=1-\frac{Q_2}{Q_1}=1-\frac{T_2}{T_1}$$
Where the $T_1 > T_2$ and both temperatures are in Kelvins.

---
Back to Index [[Physics 2 Study Notes]]

Last unit [[Fluid]] Next unit [[Electric Force, Field, and Potential]]
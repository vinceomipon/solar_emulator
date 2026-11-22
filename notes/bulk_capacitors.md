Bulk Capacitors are local reservoir of of electrical charge to smooth motor current variation

Connected in parallel w/ power supply

&#x09;Provides safety net of current

&#x09;Flattens ripple current and transients on supply due to inrush current



\*\*General Guideline for choosing bulk capacitors\*\*

&#x09;At least 1 to 4uF of capacitiance for each Watt if motor power.

&#x09;	Ex. 10A w/ 12V = 120W Power, so choose bulk capacitor b/w 120 to		480 uF capacitor



Another guideline



1/2\*C\_bulk\*(delta\*V)^2 > 1/2 L \* I^2



Where L and I are the inductance and current of motor



In my case:

2A motor with 12V supply means 24W Power

So bulk capacitance is 24 uF to 96 uF capacitor



Factors when choosing Bulk Capacitor Sizing



* Highest current required by motor system
* Power supply type, capacitance, and ability to source current
* Amount of inductance b/w power supply and motor system
* Method of operation, continuous, PWM (pulse width modulation)
* Type of motor and its characteristics
* Motor startup and braking methods



Electrolyic capacitors

&#x09;High ESR = Equivalent Series Resistance

&#x09;	thus HIGH power loss

&#x09;Used in bulk capacitors only to bypass high power motor drive systems

Ceramic capacitors

&#x09;Low ESR



In a realistic motor system. Inductance b/w power supply and motor driver.

&#x09;This limits rate of current changing from power supply.



If bulk capacitance is too small, system responds to excessive current demands/dumps from motor w/ change in motor supply voltage.

&#x09;An adequate bulk capacitor will handle large variations in current w/ fast responses, thus stabilizing the motor supply voltage





place bulk capacitors as close as possible to elements that are supplying current

&#x09;Like motor driver



Voltage rating of bulk capacitor

&#x09;Has highr ating with voltage of system

Voltage margin

&#x09;Range above/below nominal voltage of system which can operate temporarily w/o permanent damage

&#x09;Specifc to motor system not driving



Power supply in motor systems

&#x09;Voltage will fluctuate depending upon torque applied by motor

&#x09;This requires more current and since V = IR, voltage will change relative to current

&#x09;when Motor stops spinning without being applied a voltage, current is generated since motor acts like a generator,

&#x09;This will cause the power supply to spike above normal operating voltage

&#x09;This can be compared to how motors will act as wind turbines, generating current



Motor braking

&#x09;Coastings

&#x09;	FETS off, current recirculates through body diodes. Generates large amount of voltage in power supply

&#x09;Resisitve braking

&#x09;	Current dissipates as heat across resistor

&#x09;FET braking

&#x09;	current go through FETs by shorting the motor



Rule of thumb for voltage margin of a motor system:

* Power Supply, Recommended voltage margin

  * <100W, +- 20%
  * 100W-1kW, +- 50%
  * >1kW, +- 100%



Guideline calculation assuming ideal capacitors

* C\_BULK > Delta\*I\_motor x T\_PWM/Delta\*V\_supply

  * &#x20;Delta\*I\_motor
  * Expected variation in motor current, i.e. i\_max - i\_min
  * T\_PWM is PWM period which is reciprocal of PWM frequency
  * Delta\*V\_supply is allowable variation in motor supply voltage

But real world its actually

* C\_BULK > K \* Delta\*I\_motor \* T\_PWM / Delta\_V\_supply
* K is scale factor to account for ESR typical capacitors based on lab measurements??

  * Typical value of 3 is practical??



Ringing that is occurring during PWM switching is due to parasitic inductance

* Specifically the parasitic inductance of the loop

The higher the gate loop inductance the higher the gate resistance needs to damp ringing overshoot during PWM switching


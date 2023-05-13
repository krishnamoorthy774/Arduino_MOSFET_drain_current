# Arduino_MOSFET_drain_current

Arduino-Based Drain Current Measurement and Analysis of MOSFETs for Electronics Applications.

Introduction:
In this project, we apply a variable voltage to the MOSFET's gate terminal, use an Arduino to calculate the drain current of the MOSFET, and plot the results.
Components:
Arduino UNO, Potentiometer, Resistor ( 33Ω ), Breadboard, MOSFET ( IRFZ44N ).
Circuit Diagram:
 
Methodology:
As shown in the circuit diagram, we connect the circuit. We use a potentiometer to control the voltage flowing through the MOSFET's Gate terminal, and the Arduino's Analogue Pin ( A0 ) to measure the gate voltage. The drain terminal of the MOSFET is connected to a load resistance of 33Ω, and we use the Arduino's analogue input pin ( A3 ) to measure the voltage drop across the load resistance ( Vr ). Using the equation,
Ir=Vr/33
we can then determine the current flowing through the circuit. The gate voltage regulates the resistance ( Rds ) in the MOSFET's channel, which is located between the drain and source. Since the load resistance and the MOSFET are connected in series, we can calculate Rds .
Rds=(5/Ir)-33
And if we know Rds, we can determine the current through the drain ( Id ) ,
Id=5/Rds
assuming the voltage across MOSFET's drain and source is 5 Volts . Because the resistance of the channel between the drain and source ( Rds ) is only influenced by the gate voltage ( Vg ).
In this circuit we primarily do not measure the drain current. Instead, we measure the current across the circuit and calculate the drain current assuming the voltage across the MOSFET drain and source is 5 Volts .
Result:

GATE VOLTAGE (Vg)	DRAIN CURRENT (Id)
0.00	0.00
0.10	0.00
0.19	0.00
0.28	0.00
0.37	0.00
0.40	0.00
0.47	0.00
0.61	0.00
0.53	0.00
0.61	0.00
0.73	0.00
0.85	0.00
0.92	0.00
1.05	0.00
1.10	0.00
1.17	0.00
1.22	0.00
1.27	0.00
1.33	0.00
1.39	0.00
1.51	0.00
1.61	0.00
1.74	0.01
1.90	0.05
2.05	0.20
2.15	0.66
2.27	2.43
2.39	3.22
2.54	3.54
2.62	3.63
2.72	3.72
2.84	3.72
3.00	3.72
3.20	3.72
3.26	3.72
3.38	3.72
3.50	3.72
3.68	3.72
3.78	3.72
3.87	3.72
3.96	3.72
3.97	3.72
4.12	3.72
4.25	3.72
4.38	3.72
4.54	3.72
4.69	3.72
4.80	3.72
4.95	3.72


 
Conclusion:
Using Arduino, we were able to successfully plot the MOSFET's drain current ( Id ) for a range of gate voltages ( Vg ). The graph above demonstrates that current begins to flow when the gate voltage reaches the MOSFET's threshold voltage ( Vth ), which is 2 Volts . This project addresses the need for a physical circuit that verifies the physical reality of the results of mathematical simulations, despite the fact that it is easily simulatable using software like MATLAB.

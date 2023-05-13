# Arduino_MOSFET_drain_current

Arduino-Based Drain Current Measurement and Analysis of MOSFETs for Electronics Applications.

Introduction:
In this project, we apply a variable voltage to the MOSFET's gate terminal, use an Arduino to calculate the drain current of the MOSFET, and plot the results.
Components:
Arduino UNO, Potentiometer, Resistor ( 33Ω ), Breadboard, MOSFET ( IRFZ44N ).
Circuit Diagram:
 ![Arduino_MOSFET_drain_current](https://github.com/krishnamoorthy774/Arduino_MOSFET_drain_current/assets/133330566/219d03b2-1add-4dd5-b637-171b45f4f78b)

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

Gate Voltage= 0.00 | Drain Current= 0.00
Gate Voltage= 0.10 | Drain Current= 0.00
Gate Voltage= 0.19 | Drain Current= 0.00
Gate Voltage= 0.28 | Drain Current= 0.00
Gate Voltage= 0.37 | Drain Current= 0.00
Gate Voltage= 0.40 | Drain Current= 0.00
Gate Voltage= 0.47 | Drain Current= 0.00
Gate Voltage= 0.53 | Drain Current= 0.00
Gate Voltage= 0.61 | Drain Current= 0.00
Gate Voltage= 0.73 | Drain Current= 0.00
Gate Voltage= 0.85 | Drain Current= 0.00
Gate Voltage= 0.92 | Drain Current= 0.00
Gate Voltage= 1.05 | Drain Current= 0.00
Gate Voltage= 1.10 | Drain Current= 0.00
Gate Voltage= 1.17 | Drain Current= 0.00
Gate Voltage= 1.22 | Drain Current= 0.00
Gate Voltage= 1.27 | Drain Current= 0.00
Gate Voltage= 1.33 | Drain Current= 0.00
Gate Voltage= 1.39 | Drain Current= 0.00
Gate Voltage= 1.51 | Drain Current= 0.00
Gate Voltage= 1.61 | Drain Current= 0.00
Gate Voltage= 1.74 | Drain Current= 0.01
Gate Voltage= 1.90 | Drain Current= 0.05
Gate Voltage= 2.05 | Drain Current= 0.20
Gate Voltage= 2.15 | Drain Current= 0.66
Gate Voltage= 2.27 | Drain Current= 2.43
Gate Voltage= 2.39 | Drain Current= 3.22
Gate Voltage= 2.54 | Drain Current= 3.54
Gate Voltage= 2.62 | Drain Current= 3.63
Gate Voltage= 2.72 | Drain Current= 3.63
Gate Voltage= 2.84 | Drain Current= 3.72
Gate Voltage= 3.00 | Drain Current= 3.72
Gate Voltage= 3.20 | Drain Current= 3.72
Gate Voltage= 3.26 | Drain Current= 3.72
Gate Voltage= 3.38 | Drain Current= 3.72
Gate Voltage= 3.50 | Drain Current= 3.72
Gate Voltage= 3.64 | Drain Current= 3.72
Gate Voltage= 3.78 | Drain Current= 3.72
Gate Voltage= 3.87 | Drain Current= 3.72
Gate Voltage= 3.96 | Drain Current= 3.72
Gate Voltage= 3.96 | Drain Current= 3.82
Gate Voltage= 3.97 | Drain Current= 3.72
Gate Voltage= 4.12 | Drain Current= 3.72
Gate Voltage= 4.25 | Drain Current= 3.72
Gate Voltage= 4.38 | Drain Current= 3.72
Gate Voltage= 4.54 | Drain Current= 3.72
Gate Voltage= 4.69 | Drain Current= 3.72
Gate Voltage= 4.80 | Drain Current= 3.72
Gate Voltage= 4.95 | Drain Current= 3.72
Gate Voltage= 4.95 | Drain Current= 3.72
Gate Voltage= 4.95 | Drain Current= 3.72
Gate Voltage= 4.95 | Drain Current= 3.72
Gate Voltage= 4.94 | Drain Current= 3.72
Gate Voltage= 4.95 | Drain Current= 3.72
Gate Voltage= 4.95 | Drain Current= 3.72
Gate Voltage= 4.95 | Drain Current= 3.72

![Arduino_MOSFET_drain_current_graph](https://github.com/krishnamoorthy774/Arduino_MOSFET_drain_current/assets/133330566/0f9dfa47-8ecc-407d-8ebf-fbea606ef040)

Conclusion:
Using Arduino, we were able to successfully plot the MOSFET's drain current ( Id ) for a range of gate voltages ( Vg ). The graph above demonstrates that current begins to flow when the gate voltage reaches the MOSFET's threshold voltage ( Vth ), which is 2 Volts . This project addresses the need for a physical circuit that verifies the physical reality of the results of mathematical simulations, despite the fact that it is easily simulatable using software like MATLAB.

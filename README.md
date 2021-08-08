# DC-to-DC Ćuk-Convertor
The Ćuk converter is a type of buck-boost converter with zero-ripple current. Ćuk converter can be seen as a combination of boost converter and buck converter, having one switching device and a mutual capacitor, to couple the energy.

Similar to the buck-boost converter with inverting topology, the output voltage of non-isolated ćuk converter is typically inverted, with lower or higher values with respect to the input voltage. Usually in DC converters, the inductor is used as a main energy-storage component. In ćuk converter, the main energy-storage component is the capacitor.

<p align="center">
  <img src="https://github.com/rimshasaeed/Cuk-Convertor/blob/main/images/dc-dc%20cuk%20convertor.jpg" width="60%"/>
</p>

### Operting Principle
A non-isolated Ćuk converter comprises two inductors, two capacitors, a switch (usually a transistor), and a diode. Its schematic can be seen in the above figure. It is an inverting converter, so the output voltage is negative with respect to the input voltage.

The capacitor C is used to transfer energy. It is connected alternately to the input and to the output of the converter via the commutation of the transistor and the diode. The two inductors L<sub>1</sub> and L<sub>2</sub> are used to convert respectively the input voltage source (V<sub>g</sub>) and the output voltage source (V<sub>o</sub>)into current sources. This conversion is necessary because if the capacitor were connected directly to the voltage source, the current would be limited only by the parasitic resistance, resulting in high energy loss. For a short time-interval, inductor can be considered as a current source as it maintains a constant current. Charging a capacitor with a current source (i.e., the inductor) prevents resistive current limiting and its associated energy loss. MOSFET conduction states follows the sequence given below.
- On-state: The current through the inductor L<sub>1</sub> increases linearly and the diode blocks.
- Off-state: Since the current through the inductor L<sub>1</sub> cannot abruptly change the diode must carry the current so it commutates and begins conducting. Energy is transferred from the inductor L<sub>1</sub> to the middle capacitor C<sub>2</sub> resulting in a decreasing inductor current.
- On-state: The current through the inductor L<sub>1</sub> again increases linearly and the diode blocks. The middle capacitor discharges and supplies the RC load through the inductor L<sub>2</sub>. The induced voltage across the resistor 𝑅𝑅 has the opposite polarity of the input voltage.

### Applications
Ćuk converter finds its applications in:
- voltage regulation for the Dc application systems,
- hybrid solar-wind energy system as a regulator where input voltage depends on speed of wind and sun,
- battery-powered systems, and
- high voltage, negative polarity output voltage, and low standby continuous current applications.

### Device Significance
As with other converters (buck converter, boost converter, buck–boost converter) the Ćuk converter can either operate in continuous or discontinuous current mode. However, unlike these converters, it can also operate in discontinuous voltage mode (i.e., the state when the voltage across the capacitor drops to zero during the commutation cycle).
The Ćuk converter can be incorporated to yield either voltage step-up or step-down, thus making it a top choice for a wide range of voltage requirements. Also, it uses a capacitor as the key energy storage component whereas most of the other power converters employ inductors for that purpose.
The ćuk converter conduction losses can be effectively reduced by reducing the usage of components and their operating ranges. Also, the switching losses can be reduced by soft switching techniques.

## Design Specifications
| Parameters | Specifications |
| --- | --- |
| Output voltage ripple| ≤1% of the output voltage |
| Inductors current ripple| ≤10% of the load current |
| Conversion efficiency| >80% |
| Load resistance| 8Ω−12Ω |
| Signal source| Triangular voltage source |
| Feedback device to control duty cycle| Comparator |
| MOSFET driver IC| UCC37322D |

## Designed Schematic
<p align="center">
  <img src="https://github.com/rimshasaeed/Cuk-Convertor/blob/main/images/schematic.jpg" width="60%"/>
</p>

## Results
### Input and Output Voltages
<p align="center">
  <img src="https://github.com/rimshasaeed/Cuk-Convertor/blob/main/images/Vin%20Vout.jpg" width="60%"/>
</p>

### RC filter and PID output
<p align="center">
  <img src="https://github.com/rimshasaeed/Cuk-Convertor/blob/main/images/V_filter%20V_PID.jpg" width="60%"/>
</p>

### Triangular pulse input
<p align="center">
  <img src="https://github.com/rimshasaeed/Cuk-Convertor/blob/main/images/V_triangular.jpg" width="60%"/>
</p>

### Comparator output
<p align="center">
  <img src="https://github.com/rimshasaeed/Cuk-Convertor/blob/main/images/V_comparator.jpg" width="60%"/>
</p>

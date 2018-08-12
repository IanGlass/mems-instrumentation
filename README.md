# MEMS-Instrumentation
16 channel instrumentation circuit designed with emphasis on high precision, low-noise sampling of low sensitivity MEMS sensors in Wheatstone bridge configuration. The circuit does not digitize results and requires an external ADC, such as the NI 6009 DAQ.


## Specifications
* CMRR: 124 dB
* Input Voltage Range: 4.5 V to 5.5 V
* Gain: 1x, 10x, 100x, or 1,000x
* Channels: 16
* Sensor Drive Voltage: +- 1.25 V

## Single Channel

The circuit needs an external DAQ to quantize samples and has two gain select digital lines designated 'A0' and 'A1' to select 1x, 10x, 100x or 1000x, refer to the PGA204 doc for bit patterns. Anti-aliasing is implemented for signals below 500 Hz and needs to be changed for higher sample rates. Each channel contains a 4x1 header to accommodate a 'stub tester' for differential sensing.

<p align="center">
<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/Amplifier-Schematic.jpg" width="900">
</p>

## Stub Tester

The sensor is mounted in a 'stub tester' and need to be balanced with surface mount resistors. Each sensor element is configured in a voltage divider topology to create a Wheatstone bridge. 'Balancing' means to add resistors such that the two out voltage divider voltages are equal and the differential voltage is zero. This is done to give the largest measurement range through the operational amplifier, as the output will saturate close to VCC.

<p align="center">
<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/Standard-Bridge-Schematic.jpg" width="900">
</p>

## Complete Circuit

The circuit has 16 PGA204 amplifier channels and can handle 16 sensors concurrently.  On-board V regulators supply +- 1.25 V and are switched with 'Cont1' and 'Cont2' for +ve and -ve supply voltages respectively. This means sensor supply voltage can be modulated if needed. Boards are 6-layered with internal GND, VCC+, VCC- and VExcite power and ground planes. The voltage regulators can be replaced to provide a higher drive voltages as required.

<p align="center">
<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/Stub-Tester-Schematic.jpg" width="900">
</p>
<p align="center">
<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/MEMS-Instrumentation.JPG" width="500">
</p>

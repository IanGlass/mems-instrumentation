# MEMS-Instrumentation
Instrumentation for high precision, low-noise sampling of low sensitivity MEMS sensors in Wheatstone bridge configuration. Altium schematics and PCB files are included along with a BoM.

The sensor is mounted in a 'stub tester' and need to be balanced with surface mount resistors, where the circuit can handle 16 sensors concurrently. The circuit needs an external DAQ to quantize samples and has two gain select digital lines designated 'A0' and 'A1' to select 1x, 10x, 100x or 1000x. Anti-aliasing is implemented for signals below 500 Hz and needs to be changed for higher sample rates. On-board V regulators supply +- 1.25 V and are switched with 'Cont1' and 'Cont2'.

CMRR: 124 dB
Input Voltage Range: 4.5 V to 5.5 V
Gain: 1x 10x 100x 1,000x
Channels: 16
Sensor Drive Voltage: 1.25 V


<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/Amplifier_Schematic.jpg" width="360"> <img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/Stub_Tester_Schematic.jpg" width="360"> 
<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/MEMS_Instrumentation.JPG" width="360">

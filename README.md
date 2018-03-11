# MEMS-Instrumentation
Instrumentation for high precision, low-noise sampling of low sensitivity MEMS sensors in Wheatstone bridge configuration. Altium schematics and PCB files are included along with a BoM.

The sensor is mounted in the stub tester and need to be balanced with surface mount resistors and can handle 16 sensors concurrently. The circuit needs an external DAQ to quantize samples and has two gain select digital lines designated 'A0' and 'A1' to select 1x, 10x, 100x or 1000x. Anti-aliasing is implemented for signals below 500 Hz and needs to be changed for higher sample rates. CMRR of 124 dB.


<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/Amplifier_Schematic.jpg" width="360"> <img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/Stub_Tester_Schematic.jpg" width="360"> 
<img src="https://github.com/IanGlass/MEMS-Instrumentation/blob/master/MEMS_Instrumentation.JPG" width="360">

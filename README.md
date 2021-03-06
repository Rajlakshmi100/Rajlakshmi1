# DESIGNING OF A 10-BIT POTENTIOMETRIC DAC
This repository offers the designing of a 10 Bit Potentiometric Digital to Analog converter with 3.3V Analog voltage and 1 off-chip external reference using the sky130 technology.

# INTRODUCTION 
An n bit DAC:
 An N-Bit DAC takes an input of N-Bit digital word and converts the digital input signal into analog output signal in the form of voltage or current. It is a digital analog convertor device. According to the Nyquist-Shannon sampling theorem , any sampled data can be reconstructed perfectly with bandwidth and  Nyquist criteria.  A N-bit DAC takes an input of N-bitdigital word and converts the digital input-ouput signal in the form of signal or current. The number of possible different ouput levels which DAC can generate is known as resolution of the DAC convertor. 
The digital signal is represented with binary codes combination of bits 0 and 1.
Here’s an example of N-Bit Potentiometric DAC shown in the figure below:
![circuit (1)](https://user-images.githubusercontent.com/91679375/135673322-c367c782-b1f4-4fba-9e8d-72d02e1fe73f.png)


Opensource Tools used:
e-sim: A solution developed by FOSSEE, IIT Bombay for circuit design, simulation, analysis and PCB. The technology is based on free/libre and open source software like KiCad, Ngspice, GHDL etc. Earlier, it was known as Oscad/FreeEDA. It offers reasonable and affordable price to customers mostly educational institutes and SMEs as an alternative to high priced software like Xpedition/OrCAD/HSPICE. Jio, VI and Airtel also offer the ability to convert physical sim to e sim for the devices the support it. 

Ngspice: It is mixed- mode, mixed-level circuit simulator for electrical and electronic circuits. It is an open source spice simulator offering various models for active, passive analog and digital elements. Ngspice is based on three open-source free-software packages. Spice3f5, Xspice and Cider1b1: SPICE is the origin of all electronic circuit simulators, its advanced versions are now widely used in the electronics community. The best free circuit simulations software for windows 10 are LT Spice, Ngspice, CircuitLab, CircuitLogix, EasyEDA.

SkyWater Pdk: The SkyWater Open Source PDK is a collaboration between Google and SkyWater Technology Foundry to provide a fully open source Process Design Kit and related resources, which can be used to create manufacturable designs at SkyWater’s facility.

Installations:
e-sim:  https://static.fossee.in/esim/installation-files/Install_eSim_on_Windows.pdf   
https://github.com/FOSSEE/eSim/blob/master/INSTALL   

Ngspice: http: //ngspice.sourceforge.net/download.html 

Skywater Pdk: 
( Refer to: ) https://www.layouteditor.org/schematiceditor/libraries/skywater    

Switch:
The schematics for a swutch circuit and a 2 bit DAC were designed in e-sim. The analog input voltage was 3.3V, the vdd and vref was set to 3.3V and a series of 4 resistors were used.
Shcematic of the switch circuit is shown below:
 ![Screenshot (12)](https://user-images.githubusercontent.com/91679375/135672697-33897019-f4a0-418d-babf-bbe0e4f2a3ac.png)
  

The initial transient solution of the switch is shown below:
 ![nggffvd](https://user-images.githubusercontent.com/91679375/135674345-a40dcc18-8e65-4e7d-bcbb-2eb0c8dbd85a.jpeg)



Resultant Transient analysis is shown below:
 ![image](https://user-images.githubusercontent.com/91679375/135674499-61d94e94-7916-4ae6-9f90-96fa39e1ba07.png)

2-Bit DAC:
Below shown 2-Bit DAC Circuit was implemented using 3 switch instances on e-sim.
 ![Screenshot (15)](https://user-images.githubusercontent.com/91679375/135674719-f275f7c7-12bc-425c-a6c9-8e6213222043.png)

Initial transient solution of the 2-bit DAC circuit by using ngspice:
 ![image](https://user-images.githubusercontent.com/91679375/135674807-f509fedf-9ab5-4783-872b-a8221034df61.png)


	
Resultant transient analysis is shown below:
 
![image](https://user-images.githubusercontent.com/91679375/135674872-e37a97cb-a676-477a-a084-3dc9dab0b87f.png)




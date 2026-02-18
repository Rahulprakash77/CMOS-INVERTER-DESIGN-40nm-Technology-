# CMOS-INVERTER-DESIGN-40nm-
The CMOS inverter is the fundamental building block of digital ICs. It serves as the basis for constructing more complex logic gates and circuits.


## IMPORTANCE OF CMOS INVERTER IN DIGITAL DESIGN

1. **Basic Logic Element:** CMOS inverters are the basic building blocks of digital logic circuits. They enable the creation of more complex logic gates and circuits by combining multiple inverters.

2. **Logical Operations:** Inverters perform the NOT operation, a fundamental logical function. They are crucial for implementing logical operations such as AND, OR, and XOR, forming the basis of digital computations.

3. **Voltage Level Shifting:** CMOS inverters are used for voltage level shifting in digital circuits, enabling smooth communication between different logic families or voltage domains.

4. **Signal Restoration:** In digital systems, CMOS inverters can be used to regenerate and restore digital signals, helping to mitigate signal degradation and noise effects.

5. **Clock Signal Generation:** Inverters are used in clock signal generation and distribution, ensuring synchronized timing across digital circuits.

6. **Low Power Consumption:** CMOS inverters consume minimal power due to their inherent design, making them vital for energy-efficient digital systems.

## IMPORTANCE OF CMOS INVERTER IN ANALOG DESIGN

1. **Voltage Amplification:** CMOS inverters can be used as voltage amplifiers in analog circuits, amplifying weak input signals while maintaining a linear response.

2. **Voltage-to-Current Conversion:** CMOS inverters are used to convert voltage signals into current signals, a common requirement in analog design.

3. **Buffering and Isolation:** In analog design, CMOS inverters are employed as buffers and isolators to prevent signal distortion and ensure proper impedance matching.

4. **Biasing and Level Shifting:** Inverters are used for biasing and level shifting in analog circuits, aiding in setting operating points and signal ranges.

5. **Oscillator and Filter Design:** CMOS inverters are integral to designing oscillators and filters in analog circuits, helping generate stable oscillations and filter signals.

6. **Mixed-Signal Integration:** In mixed-signal circuits, CMOS inverters enable seamless integration of digital and analog components, bridging the gap between these two domains.

In both digital and analog design, CMOS inverters serve as versatile components that underpin a wide range of circuit functionalities. Their low power consumption, robustness, and flexibility make them indispensable tools for modern electronic circuit design.

#### Software of Use: Cadence Virtuoso





## Theory ( know about Inverter)
A simple inverter inverts the logically high input to low output and vice versa. It is of immense significance in clock generation, generation of delays, memories to store the data, improving the circuit's noise immunity, and much more. It is a simple two transistor device. For input 0, PMOS turns ON, and NMOS stays OFF. This charges the output capacitance, thus making output logic HIGH. Whereas for input 1, PMOS is OFF, and NMOS is ON. The charged capacitance now discharges, making output logic LOW. On a periodic application of pulse, an inverted pulse is obtained at the output. The in-depth analysis of the output on logic 0 to 1 at the input is summed up by its Voltage Transfer Characteristics (VTC).

![image](https://github.com/user-attachments/assets/6536dafe-d8a7-4307-96b0-57857fb546b5)



## What is CMOS Inverter?

CMOS inverter definition is a device that is used to generate logic functions is known as CMOS inverter and is the essential component in all integrated circuits. A CMOS inverter is a MOSFET (metal oxide semiconductor field effect transistor), composed of a metal gate that lies on top of oxygen’s insulating layer on top of a semiconductor. These inverters are used in most electronic devices which are accountable for generating data n small circuits.

![cmos](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/6c2dc6a6-cc44-43f4-a1b9-54401752d7b9)


## CMOS Inverter Schematic Diagram

The logic element like an inverter reverses the applied input signal. In digital logic circuits, binary arithmetic & switching or logic function’s mathematical manipulation are best performed through the symbols 0 & 1. The CMOS inverter truth table is shown above. If the input logic is zero (0) then the output will be high (1) whereas, if the input logic is one (1), then the output will be low (0).

![CMOS-Inverter-Circuit](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/3604d303-3762-4a75-964f-e26f110329f1)

## Inverter Dynamic Characteristics

The CMOS inverter dynamic characteristics are shown below. So, some of the following formal definitions of different parameters are discussed below. Here, all the percentage (%) values are the steady-state values

![Dynamic-Characteristics-of-CMOS-Inverter](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/987134c6-beae-4ee9-a833-bb57e0db2df3)

Rise Time or tr: Rise time is the time used to increase the signal from 10% to 90%.
Fall Time or tf: Fall time is the time used to drop the signal from 90% to 10%
Edge Rate or trf : It is (tr + tf )/2.

The propagation delay from high to low or tpHL: The time used to drop from VOH – 50%.
The propagation delay from low to high or tpLH: The time used to increase from 50%- VOL.
Propagation Delay or tp: It is (tpHL + tpLH)/2.

Contamination Delay or tcd: It is the smallest time from the 50% input crossing to the 50% output crossing

## My Work on CMOS Inverter 

1. [DC Response (VTC Curve)](#1-dc-response-vtc-curve)  
2. [Transient Response Without Load Capacitor (Propagation Delay)](#2-transient-response-without-load-capacitor-propagation-delay)  
3. [Effect of W/L on Transfer Characteristics](#3-effect-of-wl-on-transfer-characteristics)  
4. [DC Current with Varying Wp (Width of PMOS)](#4-dc-current-with-varying-wp-width-of-pmos)  
5. [Transient Response With Load Capacitor (Propagation Delay)](#5-transient-response-with-load-capacitor-propagation-delay)  
6. [Static and Dynamic Power Calculation from Simulation](#6-static-and-dynamic-power-calculation-from-simulation)  
7. [Effect of W/L on Power Consumption](#7-effect-of-wl-on-power-consumption)  
8. [Layout](#8-layout)


I used the gpdk 40nm library in Cadence virtuoso, conducting transient and DC analysis on the inverter. I calculated parameters such as power consumption, rise time, and propagation delay for the inverter.
Fun part was analysing the effect of W/L ratio, Power supply and fanout on these parameters. Some of the notable conclusions are:

![InverterSchematic](https://github.com/user-attachments/assets/1515d431-682a-454e-b42d-b92f0ac238ba)



### 1. DC Response (VTC Curve)
The DC response of an inverter characterizes its static behavior by plotting the output voltage against the input voltage, resulting in the Voltage Transfer Characteristic (VTC) curve, which defines key parameters such as the switching threshold, noise margins, and gain. Alongside the VTC curve, the drain current (Id) versus input voltage graph provides insights into the operating regions of the transistors (cutoff, linear, and saturation) during switching, enabling a comprehensive understanding of the inverter's performance.

![dc output](https://github.com/user-attachments/assets/eb19b4fc-d56b-43ec-8721-6f92a25a686e)


### 2. Transient Response Without Load Capacitor (Propagation Delay)
The transient response of an inverter analyzes its output behavior over time during input transitions, highlighting dynamic performance. The propagation delay, measured as the average of rise and fall delays, determines the inverter's speed and timing efficiency.

![Trans ckt](https://github.com/user-attachments/assets/6bc1b62c-151d-444b-908f-373a9f040e36)


Input Pulse voltage specification - 0 to 1 volt , Time period = 20ns , Rise Time and Fall Time = 50ps

#### CASE-1:  Propagation Delay for Wp=120nm Wn=120nm (keep length = 40nm)

![rise and fall time](https://github.com/user-attachments/assets/73b2a3a5-17f7-4c64-8ff1-d915936e9208)


The propagation delay from high to low or tpHL: 6.099 ps
The propagation delay from low to high or tpLH: 11.868 ps
**Propagation delay = 8.98 psec**

#### CASE-2:  Propagation Delay for Wp=240nm Wn=120nm (keep length = 40nm)

![rise and fall time (1)](https://github.com/user-attachments/assets/3500d8ab-1289-4d84-ba79-dab7685b4754)


The propagation delay from high to low or tpHL: 7.56 ps
The propagation delay from low to high or tpLH: 8.979 ps
**Propagation delay = 8.272 psec**


### 3. Effect of W/L on Transfer Characteristics
The impact of changing the W/L ratio...
![variable_Wp DC response](https://github.com/user-attachments/assets/e5b8a28a-3933-42b4-9f33-b37042ef469a)


### 4. DC Current with Varying Wp (Width of PMOS)
Analyzing the current behavior...
![variable_Wp current responce](https://github.com/user-attachments/assets/7d15e9b5-d120-42bb-842d-210505fbf301)

### 5. Transient Response With Load Capacitor (Propagation Delay)
The transient response of an inverter analyzes its output behavior over time during input transitions, highlighting dynamic performance. The propagation delay, measured as the average of rise and fall delays, determines the inverter's speed and timing efficiency. 
**CL = 10fF**
![PowerAnalysis ckt](https://github.com/user-attachments/assets/83608948-8783-412a-886c-814eb09f7128)


Input Pulse voltage specification - 0 to 1 volt , Time period = 20ns , Rise Time and Fall Time = 50ps

#### CASE-1:  Propagation Delay for Wp=120nm Wn=120nm (keep length = 40nm)

![Inverter1-1_trans2](https://github.com/user-attachments/assets/2f7bacb5-28ac-404f-bb74-0083bbef98d5)

The propagation delay from high to low or tpHL: 84.9 ps
The propagation delay from low to high or tpLH: 165.6 ps
**Propagation delay = 125 psec**

#### CASE-2:  Propagation Delay for Wp=240nm Wn=120nm (keep length = 40nm)

![Inverter2-1_trans2](https://github.com/user-attachments/assets/12358079-224d-4223-9d32-263a0f98d4c2)


The propagation delay from high to low or tpHL: 85.4 ps
The propagation delay from low to high or tpLH: 96.3 ps
**Propagation delay = 90.8 psec**

### 6. Static and Dynamic Power Calculation from Simulation
**Vdd = 1.1 volt , Cl = 10fF , Time period = 20ns , Frequency = 50 MHz**

#### CASE-1: For Wp(Width of Pmos) = 120nm , Wn(Width of Nmos) = 120nm  length = 40nm 


𝗗𝗬𝗡𝗔𝗠𝗜𝗖 𝗣𝗢𝗪𝗘𝗥 = 750nW  ( 𝗦𝘄𝗶𝘁𝗰𝗵𝗶𝗻𝗴 𝗣𝗼𝘄𝗲𝗿 = 610 𝗻𝗪 , 
               𝗦𝗵𝗼𝗿𝘁 𝗖𝗶𝗿𝗰𝘂𝗶𝘁 𝗣𝗼𝘄𝗲𝗿 = 140 n𝗪 }

𝗦𝗧𝗔𝗧𝗜𝗖 𝗣𝗢𝗪𝗘𝗥  (𝗟𝗲𝗮𝗸𝗮𝗴𝗲 𝗣𝗼𝘄𝗲𝗿 = 𝟬.𝟭𝟭𝟯 𝗻𝗪 ) 

𝗧𝗼𝘁𝗮𝗹 𝗣𝗼𝘄𝗲𝗿 = 751n𝗪


#### CASE-2: For Wp(Width of Pmos) = 240nm , Wn(Width of Nmos) = 120nm  length = 40nm 

𝗗𝗬𝗡𝗔𝗠𝗜𝗖 𝗣𝗢𝗪𝗘𝗥 = 880nW  ( 𝗦𝘄𝗶𝘁𝗰𝗵𝗶𝗻𝗴 𝗣𝗼𝘄𝗲𝗿 = 620 𝗻𝗪 , 
               𝗦𝗵𝗼𝗿𝘁 𝗖𝗶𝗿𝗰𝘂𝗶𝘁 𝗣𝗼𝘄𝗲𝗿 = 260 n𝗪 }

𝗦𝗧𝗔𝗧𝗜𝗖 𝗣𝗢𝗪𝗘𝗥  (𝗟𝗲𝗮𝗸𝗮𝗴𝗲 𝗣𝗼𝘄𝗲𝗿 = 𝟬.𝟰𝟮𝟬 𝗻𝗪 ) 

𝗧𝗼𝘁𝗮𝗹 𝗣𝗼𝘄𝗲𝗿 = 881 n𝗪


### 7. Effect of W/L on Power Consumption

![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/ef8dd65e-c751-416d-b72a-f348a65d5be8)

### 8. Layout
The layout diagram for the CMOS inverter design...

![image](https://github.com/Rahulprakash77/CMOS-INVERTER-DESIGN-/assets/130161648/5a15f023-bfce-48c4-8c33-c29c1a9c713e)



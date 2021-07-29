---
layout: post
title: Electronics Notes, IoT, DIY, Hobby
categories: notes electronics
last_modified_at: 2021-07-27 23:26:15
---



Notes about IOT, Electronics etc.

## Volts Amps Ohms Watts Hours

**Voltage (V) Volts** - pressure of water, or how fast the electrons are moving. volt can be measured in parallel, stays same.

**Current (I) Amps** - amount of water, or number of electrons moving. Amps can be measured in series, stays same. The current through the load depends on the load and not on the supply. 2A supply means it can support load upto 2A, means it has enough electrons to move current upto 2A, however, the current drawn from supply in a circuit depends on the resistance in it, it **does not depend on the supply**. Higher resistance is less electrons flowing thru, hence less Amps.

**Resistor (R) Ohm** - can be added in series to resist current (drops volts), so that bulb doesn't blow. bands tell ohms. 

$$ V = I.R , Ohm's Law $$

**Power (P) Watts** - Power or rate of energy transfer or used.

$$ P = V.I = \frac{V^2}{R} = I^2.R $$

**Que** - Caculate resitance required to power less volt component (LED) from high volt battery. You need:
- fwd_voltage = electronic component = LED = 3.2 volts
- source_volt = battery used / supply = 9v
- amps = component amps = amps of LED = 24mA

R = V / I , here find V remaining to be consumed by R, Amps remains same in series.

R = (source_volt - fwd_volt) / Amps

R = (9-3.2) / 0.024 = 240 ohms

- This resistor should be added in series to LED. Here, as in series, resistor is taking some volt and led is taking some volt.

**Flow in circuit** 
- current only flows when there is potential difference, 
- current is drawn only when there is space for electrons to move, or the cricuit conducts. 
- we can only change volts of source, but current drawn depends on load. we cannot provide high current.
- current is amount of electrons flowing, depends inversely on resistance in circuit.
- volts is pressure or how fast electrons are flowing.
- a load, say LED, can only allow few electrons to move through (current) and at some pressure/pace (volts). if we increase volts, it will burn.
- low resistance will allow more current to flow, hence more watts. 
- high resistance allows less current to flow, in series it drops volts, or reduces pressure.
- in parallel current gets multiple routes to move, hence overall current increases and resistance drops.
- in series, resistances offer more restrictions hence less current and more resistance,
- Hence
  - Series, I is same, V is different
  - Parallel, I is diff, V is same.
- **Example:** A bulb, has resistance, this defines its volts and watts, say, 4V 1W for bike meter and 4v 20W for headlight. Volt can vary and hence Current and Watts will: 
  - 4V 1W => 16ohm (fixed), draws 0.25A
  - now connect this to 12V source
  - 12V 16ohm => draws 0.75A, becomes 9W.
  - this is why the bulb blows when connected to high volts.

**Amp Hours** - measures battery capacity, as in steady current flowing through one hour. 150Ah, inverter battery will give 15A for 10hours. A typical car battery with 12 volts rating has a capacity of 48 Ah. It means that when fully charged, the battery can deliver one amp for 48 hours, two amps for 24 hours and so on.



## Components

**LEDs** - bulb, usually added with resister. This give resistance to circuit.

**Multimeter** - measures volts, amps and resistance. Continuity, NPN and PNP, for AC and DC. When measuring AMPs do switch red com.

**Bread board** - can be used for prototyping.

**Schematics** is blueprint of a circuit.

**Potentiomenter** is var resistor, or regulator.

**Capacitors** - store chaege and act like battery 
- unit is (F) Farads, and Volts it can handle. 
- Prevents sudden start of motor, bulb, helps protect jerk in movements.
- ceramic have no polarity.

**Diodes**, current in one direction, valve
- forward bias and reverse bias.
- They take volts from the circuit, cylinderical with silver strip, negative.
- Has volts drop, eg, 1.1v drop reduces volt by it. It eats volts in one direction.
- acts as protection for led which can accept current in one directions only.
- 1N4148 diode can be used upto 4V, single diode
- 1N4007 rectifier diode, used <1000V. Most used.

**Complete circuit**:
- resistor to reduce volts
- capacitor to fade out led, in parallel
- diode to prevent polarity

**Relays** 
- electronic switch, has electromagnet. another circuit makes switch operate. retangular box. its slow, so transistor was created.
- Types:
  - Electromechanical relay - has 5 terminals, 2 of electromagnet, 1 common and 1 Normally Open, 1 Normally Closed
  - solid state relay

- Relay Oscillator:
  - allows on-off loop, blinking light
  - add capacitor in parallel
  - make electromagnet go on and cut itself
  - changing capacitor size will change frequency of on and off.

**Transistor**
- is base + cylindrical shaped. 
- has 3 legs - base, collector and emmitter. Small +ve current in base completes the circuit. 
- used for switching or amplifying.
- Types:
  - **BJT** - bipolar juction transistor - 2 types 
    - NPN - emmiter out, +ve signal in base
    - PNP - emitter in, -ve signal in base
  - **MOSFET**
    - used to switch or amplify voltages in circuits.
    - 3terminals, gate, drain and source.
    - IRFZ24N - it blocks current until some volts is applied on gate. the more the volts on gate, more current it allows. 
    - A09N03N - MOsfet
- eg, to supply small current we add high resistor in series, this can be photo resistor to make day/night switch.
- models, 
  - NPN - BC547, 2N3904
  - PNP - BC557, 2N3906
- **2N2222** is a common NPN bipolar junction transistor (BJT) used for general purpose low-power amplifying or switching applications. It is designed for low to medium current, low power, medium voltage, and can operate at moderately high frequency.

**Integrated Cuircuits (IC):**
- it has more than 1 circuit inside, can have componets like resistor, transistor or capacitor. called chip. 
- save time, money, energy, space.
- types
  - Analogue/lienar IC - signal on gives cont output. eg, 7805, 555, LM386N
  - Digital IC - no continuous output, but O/P is based on Logic Gates. eg, 7404 NOT Gate,  7408 AND Gate IC. 
  - Mixed IC -  .eg, ADC 0804, Analog to digital converter IC.
- Forms - DIP, SMD, TO-220, eg, 
  - ATMEGA328P - Programmabel IC
  - ESP8266 - wifi programmable
- **555 timer** IC is common, 
  - contains more than 20 transistors + more components. 
  - 8 pins, 8 is +ve, 1 -ve, 3 output. 
  - it has combination of logic to switch on and off.
  - max load 200mA. if we power component more than this load the use mosfet.
- Voltage regulator IC
  - used to control voltage, eg, give different volts to diff components.
  - Types:
    - Linear volt regualtor - can only down volts, wasted volts as hear, to be used with heat sink. eg, 7805 - 5V, 7809 - 9V
    - Switching volts regulator - wastes less energy, can down n up volts. eg, LM2678, LM2577. 


**Transformer**
- step down - 220v to 12v, mobile charger
- step up - inverter -

**Bridge Rectifier**:
- Converts AC to DC

**Tips/Concepts**:
- Didode in parallel prevent volt volt reply on connct and disconnect.
- Capacitor in parallel prevent jerk and high volts reply. Reduces plasma.
- add 1kohm resistor in series to prevent damage by current.

**MicroControllers**:
- can be programmed to change current of output pins
- Arduino, tiny computer on IC. 
- AtTiny85

**Logic Gates:**
- XOR chip is IC with 14 pins for eg.

**Binary** is number to base 2:
- 8 bit computer can handle number till 8 bits.
- binary half adder is used to add two numbers.
- adders can be built using gates, AND XOR etc. which are ICs having pins.
- We can extrnd this to have full binday adder and subtractor to add 8 bits numbers.


**PCB** - Printed Circut Board are circuits on mdf board with sigle or multi layer copper connections. Surface Mount Components SMC are electronic components soldered on top of PCB. Through Hole Components THC are passed through hole and soldered on back of plate. Pick-and-Place machine use SMT - surface mount technology to place SMD surface mount devices on PCBs, JUKI is the company. Altium is US based.


**RF Communication** module - nRF24L01 -  Rs 60. for drones. can be used for transmission and receiver. single chip radio transceiver for the world wide 2.4 - 2.5 GHz ISM band.


**Gyro and Accelero** - MPU-6050 is  6-axis, cost 50. Micro Electro-mechanical system (MEMS),  It helps us to measure velocity, orientation, acceleration, displacement and other motion like features, also measure temp, -40 to 85


**Bluetooth** - HC-06 is slave bluetooth module.


**Veroboard** is used for prototypying before pcb, its like breadboard.


**Magnetic Sensor** - A3144 - detects magnet when close


**Touch Switch** - TTP223 , rs. 20. - is a PCB with A/B modes.



## Small Projects and Devices

**Arduino** boards having microporcessor. single board computer. uno for begineers, nano for breadboard. Kit has related components. It is open source microcontroller. It comes original and compatible copies. Arduino nano is 125 each and can be used as processing unit.


**Electric Motor Speed Controller**
- using 555 timer IC - IP 4.5v-16v, OP <200mA. pin1 ground, pin8 +ve. 
- Motor, 12V, 1.5A. It needs more current, so we use mosfet  to power 12v motor and use signal from 555.
- Mosfet - IRFZ24N - <17A, <55V - uses small current in gate pin1 to output more current from drain pin2. Source pin3 is ground. No current in gate, no flow of current. More volt in gate, more volts from drain.- Current to gate is given by 555 pin3. This volt is on/off pulse. this gives average volts and called Pulse Width Modulation.
- Add 1k ohm resistor in series b/w 555pin3 and mosfetpin1 to prevent 555 in case mosfet malfunctions and allows 12v to flow. Also add 1k ohm resistor in parallel to discharge this current. Need Explaination.
- When motor is turned off, it produces high volts to clear magnetic field, to prevent this add flyback diode 1N4007. parallel.
- ref - https://www.youtube.com/watch?v=UPTU6nYSaMo


**5V Regulator design**
- Input is 9-12V with fluctuation, but output is constant 5v.
- use an IC LM7805, takes in random 9-12v outs 5v. 
- add capacitor in 0.22uF cap, in parallel to smooth drops
- add 0.1uF ceramic cap, to smooth noise.
- 10uf elector cap, and 0.1uF ceramic cap in OP to smooth out flow.
- add diode in IP to prevent polarity fault. schottky diode has less drop so add it.


**DTH - Free Dish - Settop Box**
- SMPS - 2658A1.PCB - 200 rs - converts 220v to 5v DC


**Fan Resistor 220v B1 R-783**
- SE 104j2A - capacitor, 100V 2A
- BT124 600E - Thyristors - TRIACs


**diac triac light dimmer circuit**
- triac - bt136
- ref - https://www.youtube.com/watch?v=C1qGVaGgGOo


**Step-down buck converters**
- reduces volts without wasting energy.


**Malaysian Baloon**
- 6v, 40mA - working.


**Trimmer** 
- resistor - 100ohm 5%

Todo:
- Add remote to symphony cooler
- Add mobile controlled Motor starter and water level monitor
  - Solar tank level monitor, wifi/rf to send signals.
  - Relay to start motor.

---

**References**:
- [Learn Beginner Electronics YouTube](https://www.youtube.com/playlist?list=PLah6faXAgguOeMUIxS22ZU4w5nDvCl5gs)
- Multimeter Manual - https://www.petervis.com/meters/dt830d/dt830d-how-to-use-instructions.html
- https://quadstore.in/
- Water plants auto - https://www.electromaker.io/blog/article/elecrow-smart-plant-watering-system-using-arduino-uno-review-and-tutorial



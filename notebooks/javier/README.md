# Javier Martinez
# Table of Contents

### 1/27/2022
Meeting and work in the project approval and submit it.
### 1/28/2022
CAD assignment
### 2/8/2022
Work in the Project proposal
### 2/9/2022
Research on how to implement the machine learning model
### 2/12/2022
Research on hot to put the model in the microcontroller
### 2/14/2022
Meeting to discuss the Design Document

Work on the design document
### 2/18/2022
Fix Proposal errors, rewrite some parts and added changes to the design document.

Research on voltage regulators, denoise capacitors, the use of diodes to prevent reverse polarity and how to prevent. Create a document with all the information.
### 2/19/2022
Research on components.

Design Power supply circuit schematic and start choosing some components.
### 2/22/2022
Design Document Review.
### 2/23/2022
Soldering Assignment.
### 2/27/2022
LED circuit schematic, mosfet current analysis, button debouncing system circuit schematic.

Change voltage regulators and power supply circuit because 5 V are needed for the LED circuit.

Choosing some components (Mosfet, resistors, capacitors, voltage regulators).

### 3/5/2022
Microcontroller schematic circuit: Add external pin connectors and do the connections needed. Choose pin connectors
### 3/6/2022
Finish the schematic
### 3/7/2022
Change voltage regulators because there were not in the stock market and do the footprints assignment to each element.
### 3/8/2022
Layout:

Do all the component placement and connections.

PCB check and order the PCB version 1.
### 3/9/2022
Teamwork Evaluation
### 3/18/2022
List of components to order
### 3/22/2022
Find some components that are needed such as the battery, pin connectors, resistors…
### 3/23/2022
Research about the buzzer. How to use a buzzer with a stm32 microcontroller. Design the schematic and find the components.
### 3/26/2022
Do the buzzer connections and organize the new PCB design.
### 3/29/2022
Do the schematics and PCB layout of the LED connection with Pratheek.
### 3/30/2022
Work on the individual progress report.

I realize that the battery may not work and tried to find a new solution.
### 4/02/2022
Decide the best option for the battery
### 4/06/2022
Pratheek and I went to the lab to start soldering and testing the PCB.
We started with the power subsystem to verify the desired voltages.

First, we soldered all the the power subsystem and when we provided power to the PCB, the regulators got hot and we may have burned them.
We checked again that the connections were good and that the components were well soldered. But we could not find the problem.

## 4/07/2022
After some troubleshooting we resolved some of the problems with the connections to the battery and the connections to the switch.
We then unit tested both of the voltage regulators.
We first only added the 5 V regulator to the PCB and powered it on, this resulted in the desired behaviour. We were able to drop 6.4 V to 5 V.

However, when we added the 3.3V regulator we experienced the same problem as before, both regulators got too hot, we were able to turn off the circuit to prevent the regulators from getting damaged.
We checked using the multimeter and there aren't any shorts in the circuit which tells us that this isn't a soldering problem.

Finally, we have realized that the problem is in the 3.3 V LDO footprint. We designed the PCB layout for an LDO but when we placed the order they were out of stock. We ordered another LDO with the same features and same package but it did not have the same pin values.

We ordered a new LDO that works with our PCB. Tomorrow, I will check the voltages using the LDO we had but making external connections to connect the pins correctly.



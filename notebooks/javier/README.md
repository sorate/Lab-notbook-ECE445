# Javier Martinez
# Table of Contents

### 1/27/2022
Meeting and work in the project approval and submit it.
We have thought of a small device that can be kept on a table at home. The device is intended for visually impaired or blind people, therefore, it needs a LED to illuminate the tray where the bill is deposited, easy access to change the battery and ease of placing the bill.
### 1/28/2022
CAD assignment: 
Learned how to make schematics and PCB layout of a PCB.
### 2/8/2022
Work in the Project proposal.
### 2/9/2022
Finished and submitted the project proposal.

Research on how to implement the machine learning model. 
### 2/12/2022
Research on how can we use the model in the microcontroller.
We could use TensorFLow.TensorFlow is a python library that allows easy manipulation and convolution for tensors that are used in the neural network 
### 2/14/2022
Meeting to discuss the Design Document

Work on the design document
### 2/18/2022
Fix Proposal errors, rewrite some parts and added changes to the design document.

Research on voltage regulators, denoise capacitors and the use of diodes to prevent reverse polarity. Create a document with all the information.
### 2/19/2022
Keep working on the Power Supply circuit. First approach: Use 5 V battery and 3.3 V for the microcontroller, LED, buzzer and camera.

Research on the components we need to know how to design the circuits.
### 2/21/2022
Continue research on the circuit schematics for our components.
I realized we needed a MOSFET for the LED and Buzzer circuit. As the maximum output current of the microcontroller 20 mA is smaller than the current that need the LED and the Buzzer.
### 2/22/2022
Design Document Review.
### 2/23/2022
Soldering Assignment. Learn soldering some surface-mount and through-hole components to the PCB, how to assemble an enclosure with panel-mount parts, and learn some basics of programming a bare AVR chip.
### 2/27/2022
LED circuit schematic, mosfet current analysis, button debouncing system circuit schematic.

Change voltage regulators and power supply circuit because 5 V is needed for the LED and buzzer circuits.

Choosing some components (Mosfets, resistors, capacitors and voltage regulators).

### 3/5/2022
Microcontroller schematic circuit: Add external pin connectors and do the connections needed.

Design the schematics using external pin connectors in case some connections fail we still have access to our microcontroller. We use 2 10 pin header connectors to output the 5 V, 3.3 V, ground and several pins of the microcontroller.
### 3/6/2022
Finish the schematic
### 3/7/2022
Change voltage regulators because there were not in the stock market. Change the schematics of the voltage regulator that drops the voltage from 6 V to 5 V as the new voltage regulator has a different footprint. 
Do the footprints assignment to each element (resistors, capacitors, voltage regulators...). 
Almost all the footprints were in the CAD libraries except for the microcontroller and LED. Import LED and microcontroller footprints. Change some pins names and assignations of the microcontroller as the one I found was similar but not equal to the one we are using.
### 3/8/2022
Layout:

Do all the component placement and connections.
Pass the PCB check of PCBway and order the PCB version 1.
### 3/9/2022
Teamwork Evaluation
### 3/18/2022
Create a list of all the components to order.
### 3/22/2022
Find the battery we are going to use. 
### 3/23/2022
As we coudn't finished the buzzer schematic circuit for the PCB version 1 order.
Research about the types of buzzers. How to use a buzzer with a stm32 microcontroller. Design the schematic and find the components.
I finally used a very similar schematic as the one used for the LED. We have used a MOSFET as a switch and it helps to provide the desired current to the buzzer.
### 3/26/2022
Do the buzzer schematic and organize the new PCB design.
### 3/28/2022
Do the schematics and PCB layout of the second PCB. This PCB has the surface mount LED and a 2 pin connector.
Pass the PCBs check of PCBway and order the PCB version 2 and the PCB for the LED.
### 3/30/2022
Work on the individual progress report.

I realize that the battery may not work and tried to find a new solution.
### 4/02/2022
Decide the best option for the battery. After some research of batteries with a higher voltage than 5 V we are using a 6 V.
We are using 4 1.5 V alkaline batteries in series to provide the 6 V desired to our device.
### 4/06/2022
Pratheek and I went to the lab to start soldering and testing the PCB.
We started with the power subsystem to verify the desired voltages.

The schottky diode we ordered to prevent the reverse voltage did not have the same footprint as the one we have in the PCB so we started testing making a short but being carefull with the battery polarity. I searched a new shottky diode with the footprint  we have in our PCB.

First, we soldered all the the power subsystem and when we provided power to the PCB, the regulators got hot and we may have burned them.
We checked again using the multimeter that the connections were good and that the components were well soldered. But we could not find the problem.

### 4/07/2022
After some troubleshooting we resolved some of the problems with the connections to the battery and the connections to the switch.
We then unit tested both of the voltage regulators.
We first only added the 5 V regulator to the PCB and powered it on, this resulted in the desired behaviour. We were able to drop 6.4 V to 5 V.

However, when we added the 3.3V regulator we experienced the same problem as before, both regulators got too hot, we were able to turn off the circuit to prevent the regulators from getting damaged.
We checked using the multimeter and there aren't any shorts in the circuit which tells us that this isn't a soldering problem.

Finally, we have realized that the problem is in the 3.3 V LDO footprint. We designed the PCB layout for an LDO but when we placed the order they were out of stock. We ordered another LDO with the same features and same package but it did not have the same pin values.

We ordered a new LDO that works with our PCB and the new shottky diode as well as other spare components. Tomorrow, I will check the voltages using the LDO we had but making external connections to connect the pins correctly.
### 4/08/2022
I went to the lab to make the external connections os the 3.3 V voltage regulator to check that the voltages were as desired. 

When I was making the external connections I broke some wires on the PCB but I was still able to make the connections. I checked using a multimeter that the connections of all the nodes were good and I also checked their voltages. The voltage on the microcontroller pins is 3.3 V so all the power subsystem is working properly.

I also soldered and checked that the button and LED circuit are working properly. 
To check if the button works I used a multimeter. First I checked all the connections were good and then I check that when it is not pressed the multimeter shows 3.298 V in the microcontroller input pin and when it is pressed shows almost 0 V.

To check the LED circuit as we didn't have the microcontroller soldered yet, I had to put 3.3 V on the microcontroller pin with an external connection. Also as we didn't have the LED PCB I made a connection as I could (soldering wires to the LED) and checked that the circuit also works correctly. However, the connections were not very good so the LED connection was not very stable.
### 4/11/2022
We received the new LDO so I went to the lab to test it.
I had to unsolder some of the components I had and solder them on a new PCB because some connections were broken the day before.

As I was soldering the components I checked that the connections and voltages were the desired ones.
In addition I made new connections for the LED and I could check that it always works as expected. So know we just need to soldered the microcontroller to test its pins and wait for the second PCB order to test the buzzer circuit and solder everything again.
### 4/13/2022
We received the second PCB ordering. I went to the lab to solder everything in our final PCB.
I did the same process as the previous days and soldered all the PCB components except the microcontroller. I checked that the voltages and connections were good with the multimeter.The only difference is that I was also able to verify that the buzzer circuit works. For this I made an external connection to put 3.3 V on the microcontroller pin. So now we have a fully operating PCB. We just need to solder the microcontroller and try to program it.

Also Pratheek and I went to talk to the machine shop to tell them about the design we had in mind so they start building the physical project.

### 4/14/2022
I went with Pratheek to the lab and we soldered the microcontroller and 2 missing pin connectors. Using the multimeter we test that the connections were good.
### 4/17/2022
We were able to flash the microcontroller. So all the PCB works. We have a fully operational PCB. 
### 4/18/2022
We received the physical device from the machine shop.
### 4/19/2022
Mock demo with the TA. I realized we should make some changes to the pysical designed.
The LED PCB is located vertically so the LED is not iluminating the tray and we can have a plastic corner to help the user placing the bill on the tray.
### 4/21/2022
As the 20th was not the person of the machine shop who is making our device I went today to explain the changes we need for our design. 

Tilt the LED to illuminate the tray where the bill is deposited. Add a plastic corner on the tray so that the user knows where to place the bill. In this way we reduce the number of orientations of the bill and the bill is always placed in the same place getting the camera to focus well on the bill.
### 4/26/2022

### 4/27/2022
Final Demonstration
### 4/28/2022
Worked on the slides for the Mock Presentation. Decide who is going to explain each part.
### 4/29/2022
Finished the slides for the Mock presentation and did the Mock presentation.
### 5/01/2022
Corrected some errors we had in the Mock presentation. Added some new slides for the final presentation. Wrote down the contents I will say in the final presentation.
### 5/02/2022
Finished the slides for the final presentation and practiced what I was going to say. Did the final presentation. 
### 5/04/2022
Wrote down the final paper and submitted it.
### 5/05/2022
Lab checkout. Fini

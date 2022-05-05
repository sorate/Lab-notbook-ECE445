# Pratheek Worklog

# Table of Contents
1. [01/31/2022](#initial)
2. [02/11/2022](#machine)
3. [02/15/2022](#begin)
4. [02/20/2022](#camera)
5. [02/25/2022](#soldering)
6. [03/01/2022](#PCB_review)


## 01/31/2022 - Bought the highest memory microcontroller I could find

After some initial conversation I realized that we should secure a microcontroller for the rest of the project.

STM32G0B1KET6 was selected, this is an M0+ core microcontroller with 512 Kb of flash and
148 Kb of ram. This is the highest memory microcontroller that wasn't out of stock so getting this one was important.


## 02/11/2022 - Had initial Conversation with Machine Shop <a name = "machine"></a>

Talked with Greg from the machine shop about possible ideas for a product to help the blind.
We sent over the initial idea for the design below which illustrates how we want the bill
to be below the camera in order to make capture even easier.

He discussed the ability of having a variable mounted camera and that could help us with testing the device
and finding the optimal focal length of the camera.



## 02/15/2022 - Researching Ways to Load models onto Microcontrollers <a name = "begin"></a>

Beginning research on ways to load CNN for image classification onto a microcontroller. Initial model building is beginning now so that memory requirements can be considered when the microcontroller is finally ordered.

Image processing will also need to be thought of because all images fed into the model need to be the same size to reduce variance.

## 02/20/2022 - Starting Research on different types of cameras and cameras that work with simple communication interfaces <a name = "camera"></a>

https://www.amazon.com/ov7670-fifo/s?k=ov7670+fifo

Might be a possible camera but it doesn't have the best resolution and pixel accuracy. We need relatively high pixel accuracy in order for the model to predict things correctly.


## 02/25/2022 - Finishing Up Soldering Assignment <a name = "soldering"></a>

The Soldering assignment should give some insight into the types of parts we should use for the actual PCB design

For this assignment I have learned about the standard sizes of components like resistors, capacitors, and diodes.
I have also learned that soldering microcontrollers is hard so the final design should not use a microcontroller with a lot of small pins.

Connectors are important to have figured out as this project is going to have a lot of things off board like the camera, led, user interface buttons, and the battery.


## 03/01/2022 - Needing to finalize PCB review <a name = "PCB_review"></a>

We didn't end up going to the actual PCB review we have simply set up a meeting with Jeff.

I will be working with Javier with working on the actual footprints for the PCB as well as routing.

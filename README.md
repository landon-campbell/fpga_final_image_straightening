# FPGA Final Project of 3D Image Straightening

Automated Image Straightening FPGA Final Project

Overview
Our goal is to use a camera to record live feed, pull individual images from the feed, and return a 2-D flattened image. Meaning, if the camera is above a piece of paper at an angle, the return image would be a perfectly proportional piece of paper with its surface parallel to the screen. We plan to do this using a hardware accelerated image “deskewer” in relation to straightening an object.

Our Motivation
Although this may initially seem easy or useless, it is quite the opposite. We are not rotating this image but flattening it in the third dimension. Accounting for the proper proportionality will require significant image processing, and likely some trigonometry. 
We wish to create this process so we can implement it by taking an image of an object(s) with a ruler in the image and flattening the image to be used in created a CNC Router-made foam insert for the object. CNC Foam inserts are commonly made for professional DSLR cases, FPV Quadcopters, high-end tools, and many other expensive and fragile technologies. 

Outline of Project
a)	Find or build upon an existing high level program to deskew an image. From current research, we have found examples that deskew based off text found in an image, but not based off the edges of an object. 
b)	Create an IP block using HLS from the high level language implementation of the deskew. Then, connect the IP block on the FPGA board (presumable the De0-Nano-SoC) and run the program using hardware acceleration on the board. The board should return the image deskewed (straight, and proportional). 
c)	We hope to connect the board to the network and return the deskewed image to a connected device over the network. To do this, we may utilize jupyter notebooks to both implement the hardware accelerated code as well as return the image to an accessible location on a separate device.

Expected Outcome
We expect to have a functioning image deskewer from running the accelerated program on the De0-Nano-SoC board. When scanning the image it should register the edges of an object in the frame, and reshape it to be in a flat orientation, with maintained dimensions.

Expected Challenges
The precise difficulty of this project is unknown to us at the moment, but we can already foresee many challenging topics. Some of such include:
-Accounting for the proper proportionality will require significant image processing, and likely some trigonometry.
-Taking an image’s data and properly handling it in the FPGA board using a high-level synthesis software.
-Somehow returning the flattened image data from the FPGA board back a laptop, either using a cable or via wireless network.


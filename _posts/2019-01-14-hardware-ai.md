---
layout:     post
title:      Hardware AI ready
date:       2019-01-14 18:24:00
summary:    Find hardware AI solutions
categories: AI
thumbnail:  cogs
tags:
 - AI
 - Hardware
 - Deep neural networks
 - Embedded system
 - DNN
 - CNN
---

I have been looking for that development board that can give me that speedup for CNNs that everyone wants in their
embedded devices.  

Raspberry Pis are cool but let's face it, they suck if you try to run a NN in it. One this you can do is to attach 
[Neural compute sticks](https://software.intel.com/es-es/neural-compute-stick) to it but that kind of sucks for two reasons:  
First, computing power on RPI is not that good and secondly, RPI uses USB2.0 and neural compute sticks can use USB3.0 protocol
so you make use of a higher bandwidth with another board.
  
If I had to choose a board I would definitely go to ODROID. Depending of your budget and what do you want to go with 
you board, you can choose between the [ODroid XU4](https://www.hardkernel.com/shop/odroid-xu4/) or 
[ODroid H2](https://www.hardkernel.com/shop/odroid-h2/)

But I want to get something that already have the power inside. I want to release THE POWER from the heart of the SoC.
So there it goes, the magical list of development boards with some sort of Neural accelerator:

### [Chamaleon96 Cyclone V FPGA](https://www.96boards.org/product/chameleon96/)  
Packing an Intel Cyclone V FPGA this can be some useful thing although you shouldn't expect a huge computing power
compared to other boards.

__Around 110€ is not a great deal compared to others.__

### [HiKey 970](https://www.96boards.org/product/hikey970/)  
This bad boy is the first HiSilicon SoC with a NPU on it so you can enjoy some AI power up in the box.
* ARM-Cortex A73 + ARM-Cortex A53
* 6Gb RAM
* MALI G72 GPU
* Bluetooth + GPS + WiFi
* NPU which can achieve 1.94TFLOPS/s (HP 16-bit)
  
__It cost around 300€ so it is not cheap BUT here you have some hardware focus on AI.__

### [Sophon Edge](https://www.96boards.org/product/sophon-edge/)  
This is said to be a development board designed for deep learning. It comes with a TPU that delivers 2TOPS/s (SP 8-bit). 

__You can find it at 120$__

### [Rock960](https://www.96boards.ai/products/rock960/)
They announced the new RK3399Pro processor which features the same pinout as the RK3399 but with an NPU that can deliver
up to 2.4 TOPS/s.  
The Rock960 development board should include this processor but in the webpage there's no link that states that change yet.


### [Nvidia Jetson Xavier](https://developer.nvidia.com/embedded/buy/jetson-agx-xavier-devkit)
Not for everyone's pocket. This is one of the most powerful embedded platforms and it comes with a cost...
If you are developer it will cost you 1300€ although you won't find anything more powerful at this size. 
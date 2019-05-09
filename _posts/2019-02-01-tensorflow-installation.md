---
layout:     post
title:      Tensorflow from sources for Android and embedded deployment 
date:       2019-02-01 20:00:00
summary:    Step-by-step installation of tensorflow for Android and embedded devices deployment
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

My main goal with this tutorial is to write down the steps I take to install tensorflow in a way I
can reconfigure it easily in the future when I break my SO again.  

This is going to be quite straightforward in the beginning if you have already built Tensorflow from 
sources before.  The point with this tutorial is to find the small differences that are going to be helpful
to use tensorflow for C++ deployment and also Android development and deployment. Probably in the future
I will write another post explaining how to create a project for C++ or Android but right now I just want 
to get a working version that I can easily load with C++ and Android.

First of all, follow the instructions you can find in [here](https://www.tensorflow.org/install/source) to 
build Tensorflow from sources.  
Once you have tensorflow running for Python you will be able to train models and run them easily in Python, but
our goal here is to run models in C++ and Android. For that we have to compile tensorflow as a C++ library so we
can link against it to run our program.

This command is really useful if you want to know which intrinsics are enabled in your CPU for better performance ([Thanks](https://stackoverflow.com/questions/49094597/illegal-instruction-core-dumped-after-running-import-tensorflow)):
```grep flags -m1 /proc/cpuinfo | cut -d ":" -f 2 | tr '[:upper:]' '[:lower:]' | { read FLAGS; OPT="-march=native"; for flag in $FLAGS; do case "$flag" in "sse4_1" | "sse4_2" | "ssse3" | "fma" | "cx16" | "popcnt" | "avx" | "avx2") OPT+=" --copt=-m$flag";; esac; done; MODOPT=${OPT//_/\.}; echo "$MODOPT"; }```
---

References:
[How to configure Tensorflow](https://medium.com/@fanzongshaoxing/use-tensorflow-c-api-with-opencv3-bacb83ca5683)

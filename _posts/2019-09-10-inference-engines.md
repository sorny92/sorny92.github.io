---
layout:     post
title:      DNN Inference Engines for embedded systems 
date:       2019-10-09 09:36:00
summary:    List of DNN inference engines for embedded devices. Specially, Android devices but not only.
categories: AI
thumbnail:  cogs
tags:
 - AI
 - Hardware
 - Deep neural networks
 - Embedded system
 - DNN
 - Inference engine
 - Android
---

One of the most annoying things one can try to do nowadays in deep learning is to deploy in embedded devices.
If you have a linux device it is kind of easy because you can just use the default inference engine that comes with your
favourite framework AKA tensorflow, pytorch, whatever the fuck you want.

BUT, WHAT ABOUT THE DAMN PHONES AND ARM BASED SYSTEMS?!
Here it comes a non-curated list of frameworks because I just found them in internet and I did not bother to do a comparison, yet.

List of inference engines:
* TF-Lite: https://www.tensorflow.org/lite
    * Created by Google based on tensorflow
    * Optimized for Android devices although I think it can run in non Android devices?
* TVM: https://tvm.ai/
    * Seems to be faster than TF-Lite. Do I know if it is true? Nope
* MNN: https://github.com/alibaba/MNN
    * Alibaba's inference engine
    * Superdupper tiny (400kb in Android)
    * Compatible with iOS and Android but also to other embedded devices
    * Based on Alibaba, its way faster than TF-Lite
    * Can make use of CPU and GPU with focus on mainstream GPU as the Adreno and Mali series.
    * Several backends as OpenCL, Vulkan and OpenGL
    * Am I selling to you this one? Because it seems superdope
* ncnn: https://github.com/Tencent/ncnn
    * Tencent the other Chinese owner of the future world. ALL HAIL TENCENT. 
    * It has a nice icon in the repo
    * Has loads of info to cross-compile the library
    * Should be tested to know more information
    
Do you have any idea of another inference engine? Let me know! PLSSSSS!
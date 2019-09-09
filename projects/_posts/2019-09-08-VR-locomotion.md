---
# Posts need to have the `post` layout
layout: post

# The title of your post
title: VR Locomotion Paradigms
image: assets/img/VRimg.jpg
# This description is used to preview the page on search engines, social media, etc.
description: >
    A proof of concept for different locomotion in the Oculus Go Virtual Reality device. The main take away from this project is the connectiong of a prototype bluetooth device. This development makes it possible to create custom-made peripherals for users based on needs, frailty or disability.


# (Optional) Link to an image that represents your blog post.

# You can hide the description and/or image from the output
# (only visible to search engines) by setting:
# hide_description: false
# hide_image: false

# (Optional) Each post can have zero or more categories, and zero or more tags.
# The difference is that categories will be part of the URL, while tags will not.
# E.g. the URL of this post is <site.baseurl>/hydejack/2017/11/23/example-content/
categories: [Arduino, prototype, dev, VR]
tags: [VR, Oculus]
# If you want a category or tag to have its own page,
# check out `_featured_categories` and `_featured_tags` respectively.
---

#  VR Locomotion Demo
## VR movement with the Oculus Go
> This project shows the development of locomotion methods with the Virtual Reality [VR] Head Mounted Display [HMD].

## Project overview
### Required for project 
#### HMD

- The current HMD used is the [Oculus Go](https://www.oculus.com/go/)
    - This is a mobile based system (no external PC connection needed though a mobile phone is required for set up)
    - Completely wireless use
    - Android Based
    - ~ $200 USD
    - Light weight and fairly comfortable to wear on face
    - One controller for menu navigation included
        - Controller has a touch-pad, trigger, and other buttons

        ![Oculus Go]({{ "assets/img/vr_gait_img/oculus_go_super_look.gif" | absolute_url }})
    
#### Bluetooth Peripheral
- [Adafruit Feather NRF52](https://learn.adafruit.com/bluefruit-nrf52-feather-learning-guide?view=all)
- [1 Small FSR](https://www.adafruit.com/product/166?gclid=Cj0KCQjwj_XpBRCCARIsAItJiuTcrXpMGNeuTHYRj1z0Lm8RHtkYdx6qYQlsoPKe9_s6JMVDyEAw94IaAk0qEALw_wcB)
- [Analog Joystick module](https://www.adafruit.com/product/512?gclid=CjwKCAjwzdLrBRBiEiwAEHrAYmUsQVV8naf0vDMFiv1VPabeRbG70Zir_onQ3j0o6PJl6fBpTTy3EBoCWCYQAvD_BwE)

#### Software Required
- [Unity 2018.3.3f1](https://unity.com/)
- [Android Studio](https://developer.android.com/studio)
- [Arduino IDE](https://www.arduino.cc/en/main/software)

### Aims of Project
- Goal of the project is to create a VR environment to demonstrate and test different VR locomotion technique. 
- Creation of Bluetooth peripheral device to make different locomotion possible
- Analysis of feasibility for aging and frail to use locomotion

## Background
The main idea behind creating VR experience is to immerse the user in an environment where they can feel and react as if they would in the physical world. This immersion and feeling is often termed as "presence". Research is being done to look into the use of VR and cognitive health in the elderly[^fn1] [^fn2]. In order to create presence, the VR environment must respond to actions much like reality. This can make locomotion difficult as there are different constraints that impede what the user might want to do with what is possible based on the VR limitations. If the locomotion paradigm are improved they may even be able to assess constructs that would be difficult to observe in reality due to deficits or frailty. [^fn3] 

Some VR Limitations:
- All VR is not "room-scale" where you are able to walk around 1 to 1 with the VR experience.
- VR is not body tracking every muscle or movement of the user, usually only one to two connection points (ie. touch controllers)
- At any point the user is able to pull off the HMD to leave the VR experience

Taking these limitation into account the creation of an experience to mimic the locomotion in reality was challenging, but the addition of peripheral sensors help to access construct otherwise unattainable. 

## Methods of locomotion [^fn4]
- Controller or Joystick
    - Using the touch-pad or an external joystick to move the player in VR space
- Point and Teleport
    - The player uses a pointer to select the location they want to move-to in VR space
- Walking-in-place
    - With the addition of a sensor on the foot the user is able to mimic the act of walking to move around in VR-space
    
The goal was to access the user mimic walking. A typical VR game would use the touch-pad or teleportation for the user to move in the world.

I made a simple demonstration as proof of concept in Unity 3D. The task is a simple move to a way-point, then turn around and return to the start.

![Walking path]({{ "assets/img/vr_gait_img/walk_over.jpg" | absolute_url }})

Initially this was completed with the touch-pad on the Oculus Go. After reading previous works about VR research with aging individuals; I realized there were many studies that used mouse[^fn5] and joysticks [^fn6]. Using the touch-pad on the controller for the Oculus Go requires minute thumb movements. But the use of a joystick would allow greater control with more gross motor movements. So I was able to connect a AdaFruit NRF52 micro-controller module to the HMD. (A more in detail right-up of this procedure will be in a github repository). With the connected micro-controller I realized I was not longer limited to the conventional movement methods of games and starting looking toward other locomotion methods to get at different constructs. Recently I constructed a [step tracking device](https://ttruty.github.io/projects/arduino/prototype/dev/2019-07-29-Step-tracking/)

![foot2]({{ "assets/img/sst/foot1.jpg" | absolute_url }})

 I translated the device from saving raw data on an SD card to transfer that step data over BLE bluetooth to be used in Unity 3D. While this method does work it still needs refinement. I tested the concept sitting in a chair, mimicking the act of walking.

> **CLICK ON IMAGE BELOW TO VIEW VIDEO**

[![Alt text](https://img.youtube.com/vi/wGFj-F2yMsI/0.jpg)](https://www.youtube.com/watch?v=wGFj-F2yMsI)

## Discussion

While "VR Rigs" do exist that give the user a feeling of immersion in VR locomotion.

![Walking path]({{ "assets/img/vr_gait_img/vrWalkRig.jpg" | absolute_url }})

These are expensive, bulky and complicated to use. Set-ups like this have been used in previous studies with aging individuals[^fn7] This current project has shown that basic immersion control can be attained with a ~$30 micro-controller and a mobile HMD. This opens the door for future research to develop simple controls and task in the VR space that can be utilized by research studies and commercial products alike. The VR paradigm of locomotion no longer is limited to what is included in the HMD box, but can be expanded to any sensor that is able to be connected to a micro-controller. These advances can be used to make a portable, robust system to study aging individuals in the field. 

## Future Work

Using the findings of VR locomotion to create a VR experiences to observe memory, decision making, mobility measures and the connections between those constructs. 
- User locomotion will be adaptable to user preferences for comfort.
- These tasks might be unsafe to do in the "real world"
- Examples: 
    - CROSSING STREET: Measure the task of crossing a street with heavy traffic. (possible tracked computed scores: time to cross street, missed opportunities, count of "look-both-ways", restarts due to "hit by car", close calls)  
    - SUPERMARKET: Measure the task a trip to the grocery store. (possible tracked computed scores: amounts of times looking at list, missed item on list, time to navigate store, attention tasks)
- User movement and environment parameters can be changed to test different setting and user control.



[^fn1]: García-Betances RI, Arredondo Waldmeyer MT, Fico G and Cabrera-Umpiérrez MF. A succinct overview of virtual reality technology use in Alzheimer’s disease.Frontiers in Aging Neuroscience. 2015;80(7):1-8

[^fn2]: García-Betances RI, Arredondo Waldmeyer MT, Fico G and Cabrera-Umpiérrez MF. A succinct overview of virtual reality technology use in Alzheimer’s disease.Frontiers in Aging Neuroscience. 2015;80(7):1-8

[^fn3]: Laura A Cushman, Karen Stein, Charles J Duffy. Detecting navigational deficits in cognitive aging and Alzheimer disease using virtual reality. Neurology. 2008 Sep 16;71(12):888-95. doi: 10.1212/01.wnl.0000326262.67613.fe


[^fn4]: Costas Boletsis. The New Era of Virtual Reality Locomotion: A Systematic Literature Review of Techniques and a Proposed Typology. In: Multimodal Technologies and Interact; 2017. DOI: 10.3390/mti1040024

[^fn5]: Manera V, Chapoulie E, Bourgeois J, Guerchouche R. A Feasibility Study with Image-Based Rendered Virtual Reality in Patients with Mild Cognitive Impairment and Dementia. PloS ONE. 2016;(Mci):1-15. doi:10.1371/journal.pone.0151487

[^fn6]: Blackman T, Calderon C, Flynn D, et al. Developing a Virtual Reality–Based Methodology for People with Dementia: A Feasibility Study. CyberPsychology and Behaviors. 2003;6(6):591-611

[^fn7]: Glen M. Doniger, Michal Schnaider Beeri, Alex Bahar-Fuchs, et al. Virtual reality-based cognitive-motor training for middle-aged adults at high Alzheimer's disease risk: A randomized controlled trial. Alzheimer’s & Dementia: Translational Research & Clinical Interventions 4 (2018) 118-129 Published online 2018 Mar 27. doi: 10.1016/j.trci.2018.02.005


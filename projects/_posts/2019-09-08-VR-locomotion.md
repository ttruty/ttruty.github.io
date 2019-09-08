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
        - Controller had a touchpad
        - Accelerometer
    
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

## Background
The main idea behind creating VR experience is to immerse the user in an environment where they can feel and react as if they would in the physical world. This immersion and feeling is often termed as "presence".[^fn1] In order to create presence, the VR environment must respond to actions much like reality. This can make locomotion difficult as there are different constraints that impede what the user might want to do with what is possible based on the VR limitations. 
- All VR is not "room-scale" where you are able to walk around 1 to 1 with the VR experience.
- VR is not body tracking every muscle or movement of the user, usually only one to two connection points (ie. touch controllers)
- At any point the user is able to pull off the HMD to leave the VR experience

Taking these limitation into account the creation of an experience to mimic the locomotion in reality was challenging, but the addition of peripheral sensors help to access construct otherwise unattainable. 

## Methods of locomotion [^fn2]
- Controller or Joystick
    - Using the touchpad or an external joystick to move the player in VR space
- Point and Teleport
    - The player uses a pointer to select the location they want to move-to in VR space
- Walking-in-place
    - With the addition of a sensor on the foot the user is able to mimic the act of walking to move around in VR-space



The goal was to access the user mimic walking. A typical VR game would use the touchpad or teleportation for the user to move in the world.

I made a simple demonstration as proof of concept in Unity 3D. The task is a simple move to a waypoint, then turn around and return to the start.

![foot2]({{ "assets/img/vr_gait_img/walk_over.jpg" | absolute_url }})

Initially this was completed with the touchpad on the Oculus Go. After reading previous works about VR research with aging individuals; I realized there were many studies that used mouse[^fn3] and joysticks [^fn4]. Using the touchpad on the controller for the Oculus Go requires minute thumb movements. But the use of a joystick would allow greater control with more gross motor movements. So I was able to connect a AdaFruit NRF52 micro-controller module to the HMD. (A more in detail right-up of this procedure will be on a github repository)

[^fn1]: García-Betances RI, Arredondo Waldmeyer MT, Fico G and Cabrera-Umpiérrez MF. A succinct overview of virtual reality technology use in Alzheimer’s disease.Frontiers in Aging Neuroscience. 2015;80(7):1-8

[^fn2]: Costas Boletsis. The New Era of Virtual Reality Locomotion: A Systematic Literature Review of Techniques and a Proposed Typology. In: Multimodal Technologies and Interact; 2017. DOI: 10.3390/mti1040024

[^fn3]: Manera V, Chapoulie E, Bourgeois J, Guerchouche R. A Feasibility Study with Image-Based Rendered Virtual Reality in Patients with Mild Cognitive Impairment and Dementia. PloS ONE. 2016;(Mci):1-15. doi:10.1371/journal.pone.0151487

[^fn4]: Blackman T, Calderon C, Flynn D, et al. Developing a Virtual Reality–Based Methodology for People with Dementia: A Feasibility Study. CyberPsychology and Behaviors. 2003;6(6):591-611


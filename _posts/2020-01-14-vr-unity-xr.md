---
layout: post
author: Tim Truty
title: VR development with Unity XR manager
date: 2020-01-14
thumbnail: /assets/img/vr-unity-xr-post/Unity_Technologies_logo.png
category: VR
summary: Simple demo project to show the use of the XR interaction manager for Unity with the Oculus Go
---

# Unity XR interaction

## Addition to Unity 2019.3!

As an addition starting in unity 2019.3 Unity released a preview package to integrating XR/VR management and interactions natively. Read about it at the [Unity Blog here](https://blogs.unity3d.com/2019/12/17/xr-interaction-toolkit-preview-package-is-here/)

### Click Image to view youtube sample of XR Interaction

[![](http://img.youtube.com/vi/9jHPecg3EJE/0.jpg)](http://www.youtube.com/watch?v=9jHPecg3EJE "XR Interaction")

- This is the initial demo project for use of the interaction tools of the XR toolkit
- Locomotion is through teleporting with a snap turn method
- All interaction uses the XR toolkit framework, so it will be able to build on any VR device with the button mapping automatically adjusting.

## Interaction Demos

- Teleporting
    - Area (all of floor is able to be be teleport location)
    - Target (a single target area to teleport to)
- Turns with Primary 2D axis
    - On Oculus Go, this is the thumb pad
- Grab Interaction
    - Can grab/throw objects
- UI Raycaster interaction
    - Interact with buttons or scroll views
- Socket interactions
    - door opens with correct game object is connected to socket


## The World

- Build with [ Unity Snaps Sci-fi free asset](https://assetstore.unity.com/packages/3d/environments/sci-fi/snaps-prototype-sci-fi-industrial-136759) from asset store.

### This project will continue to be developed to make a working escape room vertical slice. Stay Tuned for more updates

Github for project can be found: [here](https://github.com/ttruty/VR-EscapeRoom-VS)
---
# Posts need to have the `post` layout
layout: post

# The title of your post
title: VR development with Unity XR manager
image: assets/img/vr-unity-xr-post/Unity_Technologies_logo.png
# This description is used to preview the page on search engines, social media, etc.
description: >
    Simple demo project to show the use of the XR interaction manager for Unity with the Oculus Go


# (Optional) Link to an image that represents your blog post.

# You can hide the description and/or image from the output
# (only visible to search engines) by setting:
# hide_description: false
# hide_image: false

# (Optional) Each post can have zero or more categories, and zero or more tags.
# The difference is that categories will be part of the URL, while tags will not.
# E.g. the URL of this post is <site.baseurl>/hydejack/2017/11/23/example-content/
categories: [VRdev]
tags: [Vr, dev]
# If you want a category or tag to have its own page,
# check out `_featured_categories` and `_featured_tags` respectively.
---

# Unity XR interaction

## Addition to Unity 2019.3!

As an addition starting in unity 2019.3 Unity released a preview package to integrating XR/VR management and interactions natively. Read about it at the [Unity Blog here](https://blogs.unity3d.com/2019/12/17/xr-interaction-toolkit-preview-package-is-here/)

### Click Image to view youtube sample of XR Interaction

[![](http://img.youtube.com/vi/BZ8uPCwh034/0.jpg)](http://www.youtube.com/watch?v=BZ8uPCwh034 "XR Interaction")

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
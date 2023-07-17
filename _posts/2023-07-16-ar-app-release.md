---
layout: post
author: Tim Truty
title: Building and Deploying an AR App- A Journey of Learning and Accomplishment
date: 2023-07-16
thumbnail: /assets/img/thread-headz/title.png
category: Tech
summary: Woo Hoo - A post that is within a week of a previous post. I did it! Ok, so this is going to be a post about building and deploying an AR app. The app may not be groundbreaking, but it holds a special place in my heart. It marks one of the first Unity projects I completed from start to finish. While I've dabbled in creating games and experiences before (some of which you can find on this blog), this project stands as a fully realized endeavor. I dedicated countless nights and weekends to bring it to life. The app allows users to scan their faces using their smartphones and superimposes an emoji over their heads, saving it as a GIF. Join me as I delve into the process of building and deploying this app, along with the valuable lessons I learned along the way.
---

# The State of VR/AR/XR in Medical and Research: Revolutionizing Healthcare (MAYBE)
Title: Building and Deploying an AR App: A Journey of Learning and Accomplishment

*Date: July 16, 2023*

## Introduction

Woo Hoo - A post that is within a week of a previous post. I did it! Ok, so this is going to be a post about building and deploying an AR app. The app may not be groundbreaking, but it holds a special place in my heart. It marks one of the first Unity projects I completed from start to finish. While I've dabbled in creating games and experiences before (some of which you can find on this blog), this project stands as a fully realized endeavor. I dedicated countless (well i can count. It was probably like 4 or 5 weekends and some of the weeknight in between) nights and weekends to bring it to life. The app allows users to scan their faces using their smartphones and superimposes an emoji over their heads, the user can then spin for a random emoji or choose a specific emoji saving it as a GIF. Then the user can share it on their favorite apps. Join me as I delve into the process of building and deploying this app, along with the valuable lessons I learned along the way.

## Section 1: The Genesis of the Project

So I have dabbled quite a bit with Unity and wanted to begin messing around with the augmenter reality integration and its potential for creating interactive experiences. After brainstorming some ideas I decided on a simple experience for random emojis and generating gifs. The app enables users to add expressive emojis to their own faces in real-time. This playful yet engaging concept captured my imagination, and I was eager to turn it into reality. I honestly though it would take me less time, but I am pleased that I was able to pull off something that actually works.

## Section 2: The Building Blocks: Unity and AR Foundation

To bring my AR app to life, I turned to Unity, a powerful and versatile game development engine. Unity provided the perfect foundation for my project, allowing me to combine 3D models, animations, and AR functionalities seamlessly. With Unity's AR Foundation package, I gained access to a range of features that streamlined the development process, including face tracking, light estimation, and object placement.

![thread headz app pic 1]({{ "/assets/img/thread-headz/cap1.png" | absolute_url }})

## Section 3: Development Process

Building an AR app requires careful planning and execution. In this section, I'll take you through the step-by-step process I followed to create my app. There is some difficulty in AR development, as it takes a lot of code and deploying on a device to test. Note: It looks like there are options to [test from the Unity editor](https://assetstore.unity.com/packages/tools/utilities/ar-foundation-remote-2-0-201106). But for $150 I'll just keep deploying to my phone for now. Maybe there will be a sale.

![thread headz app pic 1]({{ "/assets/img/thread-headz/cap2.png" | absolute_url }})

### 3.1 Conceptualizing the User Experience

Before diving into coding, I took the time to define the user experience (UX) of my app. I sketched out the main screens and interactions, envisioning how users would interact with the AR elements and navigate through the app's features. This initial planning phase helped me clarify my goals and ensured a smooth development process.

### 3.2 Implementing Face Tracking and Emoji Overlay

One of the core features of my app was the ability to track users' faces and overlay emojis in real-time. Unity's AR Foundation made this possible with its built-in face tracking capabilities. I utilized the AR Face Manager component to detect and track facial features, and then used the obtained data to precisely position and animate the chosen emoji over the user's head. This integration of AR technology and expressive visuals brought the app to life.

![thread headz app pic 3]({{ "/assets/img/thread-headz/cap3.png" | absolute_url }})

### 3.3 Creating GIF Generation and Saving Functionality

To provide users with a way to preserve and share their augmented experiences, I incorporated GIF generation and saving functionality. This was a lot harder than I expected. There was not any simple plug and play to gif recording so I had to code up a way to capture each frame within some parameters and write those captured frames to a gif. I then implemented a save and share feature that allowed users to store their creations locally or share them with friends and family.

## Section 4: Deploying to the App Store

Completing the development phase was only the first step. In this section, I'll share the process I followed to deploy my AR app to the app store, making it accessible to a wider audience. I deployed on Android Play Store. Which is fairly straight forward.

### 4.1 Testing and Bug Fixing

Before submitting my app for review, I conducted rigorous testing to ensure a smooth and bug-free experience. I enlisted the help of beta testers to identify any issues, glitches, or performance bottlenecks. Their feedback was invaluable, and I iteratively improved the app based on their suggestions.

![thread headz app pic 5]({{ "/assets/img/thread-headz/cap5.png" | absolute_url }})


### 4.2 App Store Guidelines and Submission

To ensure compliance with the app store guidelines, I carefully reviewed the requirements set by the platform. I made the necessary adjustments, such as incorporating age restrictions and privacy policies, to meet the guidelines' standards. With everything in order, I submitted my app for review, eagerly anticipating its availability to the public.

## Section 5: Lessons Learned and Future Directions

Building and deploying my AR app was a significant learning experience. In this section, I'll share some of the key lessons I gleaned throughout the process and discuss potential future directions for the project.

## 5.1 The Power of Persistence

Throughout the development journey, I encountered numerous challenges and setbacks. With lots of testing and iteration I was able to make a fun engaging app.

### 5.2 User Feedback and Iteration

The feedback I received from users and beta testers proved instrumental in refining the app's functionality and user experience. Actively listening to users' suggestions and addressing their pain points allowed me to iterate and enhance the app's features, ensuring it met the needs and expectations of its intended audience.

### 5.3 Expanding Features and Enhancements

While my AR app is a fully realized project, there's always room for growth. In the future, I plan to expand its features, incorporating additional AR interactions, more expressive emojis, and social sharing capabilities. The journey doesn't end with deployment; it continues with continuous improvement and innovation.

![thread headz app pic 4]({{ "/assets/img/thread-headz/cap4.png" | absolute_url }})


## Conclusion

Building and deploying an AR app was an exhilarating and rewarding experience. Now the task is trying to get installs. I gues this is why there is normally a team involved. I am not a business person, I just like making that thing. We even if no one downloads it I am still happy I finished something. If you find this post and want to try out the app you can find it [here](https://play.google.com/store/apps/details?id=com.ButtonMasherBrew.HeadDirection&hl=en_US&gl=US).

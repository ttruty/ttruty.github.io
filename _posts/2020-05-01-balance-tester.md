---
layout: post
author: Tim Truty
title: Creation of balance testing hardware and application
date: 2020-05-1
thumbnail: /assets/img/balance-proj/out-of-balance.jpg
category: Tech
summary: Demo project to show homemade hardware and Android application to test balance in a simple fun game.
---

# Balance Tester

This project shows a demo of a simple home made balance game, the hardware and the software can be made and adapted easily from available parts and open source software. The goal is that anyone can build a simple, fun balance game. This project is aimed towards aging individuals who have balance problems. The game might be able to help train balance and reduce the risks of falls at home.

<hr />

<h3>Sample Video of Android Balance Game</h3>

<iframe width="560" height="315" src="https://www.youtube.com/embed/-CGvL4zsEN4?rel=0&amp;controls=0&amp;showinfo=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen=""></iframe>

<hr />

## Build the hardware.

The balance testing hardware has few parts for each foot to make it cheap and easy to assemble. The parts cost around $30 for each foot.

1. 1- Arduino BleuFruit Micro-controller from [Adafruit](https://www.adafruit.com/product/3406)
2. 2- Force Sensitive Resistors(FSR)[from Adafruit](https://www.adafruit.com/product/1075)
 - A few 10k resistors 
 - Wires and a battery


![hardware diagram]({{ "/assets/img/balance-proj/diagram.png" | absolute_url }})

The balance is measured using the FSR and foot pressure applied. The micro-controller reads variable resistance from the FSR based on the force applied to it. You can read more [here](https://learn.adafruit.com/force-sensitive-resistor-fsr/using-an-fsr)

![hardware]({{ "/assets/img/balance-proj/hardware1.jpg" | absolute_url}})

The BleuFruit Feather device has a bluetooth chip embedded on the device, this is how the each foots balance signal is sent to the phone. This project went through a few iterations. The first used a single sensor and board, using 2 micro-controlled allows the feet to be able to move freely and The FSRs can be expanded under foot.

![hardware]({{ "/assets/img/balance-proj/hardware2.jpg" | absolute_url }})

![hardware]({{ "/assets/img/balance-proj/hardware3.jpg" | absolute_url }})



### The Android Game

- The android game was built using Unity
- The Bluetooth readings of the FSR on the device are sent over bluetooth to the phone.
- The reticle is moved based on some simple algorithm
- Future work will include a leader board and costume player balance dots.

### This project is open source and the source code will be made available on github

Github for project can be found: [here](https://github.com/ttruty)
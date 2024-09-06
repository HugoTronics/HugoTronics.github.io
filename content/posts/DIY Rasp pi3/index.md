---
title: "Android Auto Crankshaft Project: DIY Installation with Raspberry Pi 3"
date: 2024-09-06T15:54:41+02:00
draft: false
tags: [Raspberry Pi, DIY Projects, Car Technology]
summary: "Transform your car with a DIY Android Auto system using Raspberry Pi 3. Discover how to create a functional, aesthetic setup without breaking the bank."
---

## Android Auto Crankshaft Project: My DIY Installation with Raspberry Pi 3

Hey everyone! Today, I’m sharing how I turned my Raspberry Pi 3 into an Android Auto system for my car. The idea was to create a practical, aesthetic, and affordable device without altering my vehicle’s original interior. After some research and a bit of tinkering, I managed to install a touchscreen and a 3D-printed mount without spending a fortune. Here’s a step-by-step guide, from choosing the hardware to setting up the software.

## Equipment and Where to Find It at Low Cost

For this project, I started by finding a used Raspberry Pi 3 on Leboncoin for about 25 euros. This mini-computer is perfect for this kind of setup with its Wi-Fi, Bluetooth capabilities, and USB ports. Next, I found the official 7-inch Raspberry Pi touchscreen for 35 euros. This screen is ideal for in-car use: it easily connects via a ribbon cable to the Pi’s DSI port and is powered directly through the GPIO pins, minimizing cable clutter.

I also chose a 16 GB microSD card to store the operating system, though an 8 GB card would suffice. To handle audio and voice commands, I added a USB sound card (5 euros) and an external microphone (5 euros). A 3.5 mm jack cable connects the Raspberry Pi’s audio to the car stereo’s AUX input, allowing sound to play directly through the car’s speakers.

For power, a micro-USB cable connects to a 12V/USB adapter plugged into the cigarette lighter, ensuring a stable power supply to the Raspberry Pi.

## Installing the Android Auto System with Crankshaft

Once all the hardware was gathered, it was time to turn the Raspberry Pi into an Android Auto system. I chose Crankshaft, a distribution specifically designed for Raspberry Pi that transforms it into an Android Auto interface as soon as it boots up.

I downloaded Crankshaft from their official site and used Balena Etcher to flash the image onto the Raspberry Pi’s microSD card. This software is straightforward and effective: simply select the downloaded image and flash it directly onto the microSD card. After inserting the card into the Raspberry Pi, Crankshaft automatically starts and configures the system to recognize the phone when connected.

## Crankshaft Options and Configuration

Crankshaft offers several options to customize your Android Auto experience. Besides the wired connection, you can set up Bluetooth and Wi-Fi connections. To enable wireless connectivity, I had to put my phone in developer mode. To do this, go to Settings, select "About Phone," and tap the build number multiple times to activate developer mode. Then, I enabled USB debugging, allowing the phone to communicate with Crankshaft.

Bluetooth pairing was easily done via Crankshaft’s web interface. By using Bluetooth and Wi-Fi together, I minimized cables in the cabin, although this setup limits internet access via the phone.

## Creating a Custom Mount with 3D Printing

To neatly install the Raspberry Pi and the screen in the car, I decided to create a custom mount using 3D printing. I found some basic models online, which I modified in SolidWorks. This CAD software allows importing STL files and adapting them to my needs. After opening the files, I converted them to solid models to add specific cutouts for cable routing and reinforcements for mounting.

I printed the parts using the Form 2 from Formlabs, an SLA printer that uses a laser to solidify liquid resin layer by layer. I chose Tough 1500 resin, which combines impact resistance with some flexibility, making it perfect for environments subject to vibrations like a car.

Once the parts were printed, I cleaned them in an isopropyl alcohol bath to remove residual resin before curing them in a UV oven at 70 degrees Celsius for 60 minutes. Finally, a coat of black paint was applied for an aesthetic finish that blends seamlessly into the car.

## Installation in the Car: Practical and Non-Invasive

For the car installation, I wanted to avoid any permanent modifications. I used self-adhesive Velcro strips to attach the mount to the dashboard, allowing me to position the screen and Raspberry Pi without drilling or permanent adhesives. This keeps the interior clean and offers an easily removable solution if I want to modify the setup or change vehicles in the future.

The cables (audio jack, microphone, micro-USB, and USB-C for the phone) were bundled with cable ties and secured along the cabin edges with Velcro mounts. This keeps the cables organized and discreet without compromising the dashboard’s aesthetics.

## Inspiration and Improvement Ideas

While exploring YouTube, I discovered that other enthusiasts have created even more advanced installations, incorporating rear cameras and other accessories to enhance their driving experience. These modifications are often more complex, requiring permanent adjustments to the vehicle, but they showcase the potential of a DIY Android Auto project. If you’re ready to take it further, I encourage you to check out their videos for inspiration.

**YouTube Channels to Explore:**

- Everlanders
- DB Tech

## Conclusion: An Accessible and Customizable Project

Transforming a Raspberry Pi into an Android Auto system is an accessible, flexible DIY solution perfectly suited for tinkerers looking to modernize their vehicles without making permanent modifications. With Crankshaft, 3D printing, and a bit of creativity, I successfully designed a custom system discreetly integrated into my car. This project is perfect for those wanting to personalize their driving experience without compromise. For the more ambitious, the advanced setups seen on YouTube can provide ideas to take things even further. So, get started, adapt, and enhance your vehicle your way!

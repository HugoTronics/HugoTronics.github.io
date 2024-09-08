---
title: "Android Auto Project: DIY Installation with Raspberry Pi 3"
date: 2024-09-06T15:54:41+02:00
draft: false
tags: [Raspberry Pi, DIY Projects, Car Technology]
summary: "Transform your car with a DIY Android Auto system using Raspberry Pi 3. Discover how to create a functional, aesthetic setup without breaking the bank."
---

## Android Auto Project: My DIY Installation with Raspberry Pi 3

Hey everyone! Today, I’m sharing how I turned my Raspberry Pi 3 into an Android Auto system for my car. The idea was to create a practical, aesthetic, and affordable device without altering my vehicle’s original interior. After some research and a bit of tinkering, I managed to install a touchscreen and a 3D-printed mount without spending a fortune. Here’s a step-by-step guide, from choosing the hardware to setting up the software.

![IMG20240907150234](https://github.com/user-attachments/assets/eaa6a23e-b19c-45e8-80bc-20582b076a78 "The complete setup of the Raspberry Pi 3 with the 7-inch touchscreen installed in the car.")

## Equipment and Where to Find It at Low Cost

For this project, I started by finding a used Raspberry Pi 3 on Leboncoin for about 25 euros. This mini-computer is perfect for this kind of setup with its Wi-Fi, Bluetooth capabilities, and USB ports. Next, I found the official 7-inch Raspberry Pi touchscreen for 35 euros. This screen is ideal for in-car use: it easily connects via a ribbon cable to the Pi’s DSI port and is powered directly through the GPIO pins, minimizing cable clutter.

![IMG20240906172803](https://github.com/user-attachments/assets/adeaaff3-56bd-412d-bbef-f73dd5c86751 "The Raspberry Pi 3 and the official 7-inch touchscreen ready for installation.")

The 7-inch touchscreen connects to the Raspberry Pi 3 via the DSI ribbon cable for video output. Power for the screen is supplied directly through the GPIO pins: 5V and GND pins provide the necessary voltage, reducing cable clutter.

![rasp   screen wire](https://github.com/user-attachments/assets/db506eb6-637c-4c97-a688-9c1a31fec28f "The image shows the 7-inch touchscreen connected to the Raspberry Pi 3 via the DSI ribbon cable. Power is supplied to the screen through the GPIO pins, with the 5V and GND pins visible")

I also chose a 16 GB microSD card to store the operating system, though an 8 GB card would suffice. To handle audio and voice commands, I added a USB sound card (5 euros) and an external microphone (5 euros). A 3.5 mm jack cable connects the Raspberry Pi’s audio to the car stereo’s AUX input, allowing sound to play directly through the car’s speakers.

![IMG20240906182355](https://github.com/user-attachments/assets/23e17178-5b97-40c2-8508-00ed7e371c93 "The audio setup with the USB sound card and external microphone.")

For power, a micro-USB cable connects to a 12V/USB adapter plugged into the cigarette lighter, ensuring a stable power supply to the Raspberry Pi.

## Installing the Android Auto System with Crankshaft

Once all the hardware was gathered, it was time to turn the Raspberry Pi into an Android Auto system. I chose Crankshaft, a distribution specifically designed for Raspberry Pi that transforms it into an Android Auto interface as soon as it boots up.

I downloaded Crankshaft from their [official site](https://getcrankshaft.com/) and used [Balena Etcher](https://www.balena.io/etcher/) to flash the image onto the Raspberry Pi’s microSD card. This software is straightforward and effective: simply select the downloaded image and flash it directly onto the microSD card. After inserting the card into the Raspberry Pi, Crankshaft automatically starts and configures the system to recognize the phone when connected.
![balena etcher   crankshaft](https://github.com/user-attachments/assets/62fb005e-b42c-4571-8244-2efabd5d81e6 "Download Crankshaft and Etcher")

![SD FLASH](https://github.com/user-attachments/assets/16ab3fd6-6311-4707-9c74-d464419fcb41 "Installing Crankshaft on the Raspberry Pi using Balena Etcher, a straightforward process that quickly sets up the system for Android Auto.")


## Crankshaft Options and Configuration

Crankshaft offers a range of settings to personalize your Android Auto experience. Audio settings include equalizer adjustments and sound balancing, allowing you to fine-tune the audio output to suit your car’s speakers. Display settings let you adjust brightness manually or automatically, ensuring optimal visibility in varying light conditions, and a sleep mode conserves power by turning off the display after inactivity.

![IMG20240906175435](https://github.com/user-attachments/assets/d8c68cc2-2e87-4ed0-9078-235354678d76 "The Crankshaft settings interface, showing various configuration options such as Bluetooth and Wi-Fi connectivity to enhance the Android Auto experience.")

For connectivity, Crankshaft supports both Bluetooth and Wi-Fi, enabling wireless pairing with your smartphone. This reduces cable clutter and allows for seamless connectivity, although setting up Bluetooth and Wi-Fi requires configuring your phone in developer mode and enabling USB debugging.

## Creating a Custom Mount with 3D Printing

To neatly install the Raspberry Pi and the screen in the car, I decided to create a custom mount using 3D printing. I found some basic models online, which I modified in SolidWorks. This CAD software allows importing STL files and adapting them to my needs. After opening the files, I converted them to solid models to add specific cutouts for cable routing and reinforcements for mounting.

![body case ](https://github.com/user-attachments/assets/226f40fc-8e6a-45d1-b6d8-26c6801e77fe "3D model of the custom mount designed in SolidWorks, showing the detailed adjustments made to fit the car’s dashboard and accommodate the necessary components.")

I printed the parts using the Form 2 from Formlabs, an SLA printer that uses a laser to solidify liquid resin layer by layer. I chose Tough 1500 resin, which combines impact resistance with some flexibility, making it perfect for environments subject to vibrations like a car.

![impression 3D 1](https://github.com/user-attachments/assets/6d9f3550-7fb1-4420-b6e9-ec7d47a477c5 "The finished 3D printed mount components, ready for assembly and installation in the car.")
![printing setup](https://github.com/user-attachments/assets/915dea97-944c-4915-b444-acef204d672a "3D printing setup")

Once the parts were printed, I cleaned them in an isopropyl alcohol bath to remove residual resin before curing them in a UV oven at 70 degrees Celsius for 60 minutes. Finally, a coat of black paint was applied for an aesthetic finish that blends seamlessly into the car.

![IMG20240906171529](https://github.com/user-attachments/assets/d2b32edd-2227-4417-a376-4e02459df19a "3D-printed parts with fresh black paint drying")

## Installation in the Car: Practical and Non-Invasive

For the car installation, I wanted to avoid any permanent modifications. I used self-adhesive Velcro strips to attach the mount to the dashboard, allowing me to position the screen and Raspberry Pi without drilling or permanent adhesives. This keeps the interior clean and offers an easily removable solution if I want to modify the setup or change vehicles in the future.

![IMG20240907150234](https://github.com/user-attachments/assets/40645e32-f762-47ab-bb62-4b276706bae1 "The final installation of the Raspberry Pi and touchscreen in the car")

The cables (audio jack, microphone, micro-USB, and USB-C for the phone) were bundled with cable ties and secured along the cabin edges with Velcro mounts. This keeps the cables organized and discreet without compromising the dashboard’s aesthetics.

## Inspiration and Improvement Ideas

While exploring YouTube, I discovered that other enthusiasts have created even more advanced installations, incorporating rear cameras and other accessories to enhance their driving experience. These modifications are often more complex, requiring permanent adjustments to the vehicle, but they showcase the potential of a DIY Android Auto project. If you’re ready to take it further, I encourage you to check out their videos for inspiration.

**YouTube Channels to Explore:**

- [Everlanders](https://www.youtube.com/c/Everlanders)
- [DB Tech](https://www.youtube.com/channel/UCVy16RS5eEDh8anP8j94G2A)

## Conclusion: An Accessible and Customizable Project

Transforming a Raspberry Pi into an Android Auto system is an accessible, flexible DIY solution perfectly suited for tinkerers looking to modernize their vehicles without making permanent modifications. With Crankshaft, 3D printing, and a bit of creativity, I successfully designed a custom system discreetly integrated into my car. This project is perfect for those wanting to personalize their driving experience without compromise. For the more ambitious, the advanced setups seen on YouTube can provide ideas to take things even further. So, get started, adapt, and enhance your vehicle your way!

## Useful Links

- [Crankshaft Official Site](https://getcrankshaft.com/)
- [Balena Etcher](https://www.balena.io/etcher/)
- [Everlanders YouTube Channel](https://www.youtube.com/c/Everlanders)
- [DB Tech YouTube Channel](https://www.youtube.com/channel/UCVy16RS5eEDh8anP8j94G2A)

---
title: "DIY: Building a High-Performance Wi-Fi Patch Antenna to Boost Your Connection"
date: 2024-11-17T15:54:41+02:00
draft: false
tags: [Patch Antenna, Wi-Fi, DIY, CST Simulation, CNC, 3D Printing]
summary: "Learn how to design, fabricate, and test a Wi-Fi patch antenna to significantly improve the signal quality of a card without an antenna."
series: ["Wi-Fi Antenna Projects"]
series_order: 1
---

{{< alert cardColor="#6a89cc" icon="circle-info" iconColor="white" textColor="white">}}
This project explores the complete process of creating a Wi-Fi patch antenna to improve the network connection of a PC by focusing on simulation, fabrication, and real-world testing.
{{< /alert >}}

## Introduction: Why Build a Wi-Fi Patch Antenna?

Have you ever repurposed a Wi-Fi card without an antenna and noticed unstable or slow connections? That’s exactly what motivated me to start this project.

To resolve this issue, I decided to design a DIY patch antenna specifically tuned to the **2.4 GHz** band. A patch antenna is compact, easy to fabricate, and provides good directivity—perfect for improving the network performance of a desktop PC.

In this project, I will cover:
1. Designing the antenna using classical calculations and **CST Studio** simulations.
2. Fabricating the antenna with a **CNC LPKF** machine and designing a protective box using **SolidWorks**.
3. Testing network performance to measure improvements with and without the antenna.

The goal is to create an affordable and efficient solution while exploring possibilities for future enhancements, such as dual-band coverage.

## Step 1: Design and Dimension Calculations

### Why a Patch Antenna?
A patch antenna consists of three main components:
1. A **metallic patch** that radiates the signal.
2. A **dielectric substrate** (FR4 in this case) that separates the patch from the ground plane.
3. A **ground plane** that directs the radiation.

![double antenna](https://github.com/user-attachments/assets/4f27e270-db87-4794-860c-d75a7bf3b09e "comparison of a Wikipedia patch antenna image (left) and a custom-built patch antenna designed and fabricated by me (right)")

This design is ideal for Wi-Fi because it provides:
- Good adaptation to a specific frequency (here **2.4 GHz**).
- Moderate directivity for targeting the area around your router.
- A compact structure, suitable for limited spaces.

### Dimension Calculations
The patch and feed line dimensions are calculated based on the target frequency (\(f_r = 2.4 GHz\)) and the substrate properties (\(\epsilon_r = 4.4\)). Key steps include:
1. **Patch width (\(W\))**:
   \[
   W = \frac{c}{2f_r\sqrt{\epsilon_r}}
   \]
   where \(c\) is the speed of light.
2. **Effective length (\(L_{eff}\))**: Adjusted to account for fringing effects.
3. **Microstrip line**: Tuned for a 50-ohm impedance to minimize energy losses.

Using an online calculator (**Everything RF**), the optimized dimensions are:
- Patch width: **38 mm**.
- Patch length: **30.8 mm**.
- Microstrip line width: **3.1 mm**.
- Feed point: **7.7 mm**.

![patch antenna 2.4 ghz](https://github.com/user-attachments/assets/3ad1b21b-a733-4528-9923-a2f6367d259b "calculated patch dimensions used for the design")

## Step 2: Simulation with CST Studio

### Why Use CST Studio?
I used **CST Studio Suite**, a powerful electromagnetic simulation tool, to validate the antenna’s performance before fabrication. This software enables:
- Virtual testing of the design to avoid costly errors.
- Analysis of key parameters like **S11** and **VSWR**.
- Visualization of radiation patterns and efficiency in the target frequency range.

### Key Parameters
- **S11 (Reflection Coefficient)**: Measures the power reflected by the antenna. A value below **-10 dB** ensures over 90% of the power is transmitted, critical for good adaptation.
- **VSWR (Standing Wave Ratio)**: Indicates how efficiently power is transmitted. A VSWR close to **1** is ideal; a value below **2** is acceptable for Wi-Fi applications.

### Simulation Results
- **S11**: Minima at **-12 dB** at 2.4 GHz, confirming proper adaptation.
- **VSWR**: Stable at **1.9**, sufficient for effective transmission.
- **Radiation patterns**: Moderate directivity with a **45° coverage angle**, ideal for domestic use.

## Step 3: Antenna Fabrication

### Etching the Patch
With validated dimensions, I etched the antenna on an **FR4 substrate** using a **CNC LPKF** machine. The DXF file generated in CST Studio was imported directly into the CNC software, ensuring precise fabrication.

### Designing the Protective Box
To protect the antenna and facilitate installation, I designed a box in **SolidWorks** and printed it in **PETG** using a **Bambu Lab 3D printer**. PETG is durable and resistant to temperature variations, making it ideal for this application.

## Step 4: Real-World Testing

### Testing with a VNA
A **vector network analyzer (VNA)** was used to evaluate the antenna’s performance:
- **S11**: Measured at **-12 dB** at 2.4 GHz, indicating proper adaptation.
- **VSWR**: Measured at **1.9**, confirming efficient power transmission.

### Network Testing with Acrylic Suite
To assess the antenna’s impact on network performance, I tested the connection before and after installing the antenna:
- **Without antenna**: RSSI of **-74 dBm**, unstable signal, limited to 144 Mbps.
- **With antenna**: RSSI improved to **-49 dBm**, stable connection, increased speed to 542 Mbps.

These results demonstrate that the antenna significantly improves both stability and speed.

## Step 5: Limitations and Future Improvements

The current monopolar design is limited to the **2.4 GHz** band, which is sufficient for basic Wi-Fi but does not cover the advantages of the **5 GHz** band. A future version could integrate dual-band coverage and utilize the two ports on the Wi-Fi card for **MIMO**, enhancing both stability and speed.

## Conclusion

This project demonstrates that building a high-performance Wi-Fi antenna at a low cost is entirely feasible.

Using modern tools like **CST Studio**, a **CNC**, and a **3D printer**, this patch antenna has significantly improved network quality. With future adjustments, it could be adapted for dual-band or IoT applications, making it even more versatile.

If you have questions or suggestions, feel free to share them in the comments! 😊

## Tools and References

### Tools Used
- **Software**: CST Studio, SolidWorks, Acrylic Suite.
- **Equipment**: CNC LPKF, Bambu Lab 3D printer (PETG), Vector Network Analyzer (VNA).

### References
- **Patch Antenna Calculator**: [Everything RF](https://www.everythingrf.com/tools/microstrip-patch-antenna-calculator).
- **CST Studio Guides**: Official documentation.
- **Theoretical Resources**: Articles from [ResearchGate](https://www.researchgate.net) and [IEEE Xplore](https://ieeexplore.ieee.org).

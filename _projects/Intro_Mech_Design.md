---
layout: project
title: Intro to Mechanical Design Project
description:
image: "assets/images/slf_clipart.png"
---


<!--
#/assets/images/function-graph.png


Compile to PDF (example):
  pandoc O3_ClientOutline_example_submission.md -o O3_ClientOutline.pdf


fontsize: 11pt
geometry: margin=1in
papersize: letter
pagestyle: empty
header-includes:
  - \pagenumbering{gobble}
-->

* Table of Contents
{:toc}

---

# Client Pitch

**Team:** No Fly Zone 
**Client(s):** Cornell CALS Extension / E&J Gallo Winery / National Grape 

## Problem statement

The spotted lantern fly (SLF) is an invasive species in North America. Economic losses to the grape industry in Finger Lakes alone is estimated to reach $1.5 million in the first year of infestation, and double annually. Infested grapevines use 38% less water due to lower sap flow rates, leading to lower quality product. The SLFs also remain on grapevines during the harvesting process, contaminating the grapes and further decreasing yields. Currently, SLF removal is only done at harvest and product processing.

## Impact

Passive SLF population control during the growing season will lower total vine damage, and limit the contamination levels for future SLF removal efforts during harvesting.

## Proposed direction: "The Lure"

**What it is**: A device hung from a trellis; SLFs are first attracted, and then contained.

**Minimum viable product / proof-of-concept**: A plastic bottle filled with wintergreen oil. A rubber valve would replace the cap and act as a one-way entrance.

**Potential long term product**: A dual-attraction system of wintergreen oil and a 60hz speaker. A helical wall will rotate and guide SLFs down into a replaceable containment chamber.

### Key risks / unknowns

- Cost: Targeting every grapevine would require many lures, what does this add too and and how much is too much?
- Efficacy: Testing how well lures attract is difficult in the classroom.
- Maintenance: How to balance required manual labor and lure effectiveness.

## Questions for the client

1. What financial investment would be available for the full-scale use of this product?
2. How much labor would be available for maintaining this product?
3. What level of attachment between a lure and the trellis is required to maintain integrity throughout the growing and harvesting seasons?

## References

- [Reference 1](https://academic.oup.com/jipm/article/16/1/2/7964417?searchresult=1&login=true#521897831)
- [Reference 2](https://www.sciencedirect.com/science/article/pii/S0167880924004390)
- [Reference 3](https://academic.oup.com/jipm/article/16/1/2/7964417)
- [Reference 4](https://academic.oup.com/jee/article/115/6/2116/6777183)

# Functional Prototype

## Purpose

The purpose of creating a functional prototype is to evaluate the feasibility of our design, to discover if there are major flaws in the design during the assembly process, to evaluate the ease of assembly, and to evaluate the strengths and weaknesses of our design. If our prototype is able to be assembled, this will show that our design accounts for all the real world physical constraints in the assembly process.

## Assembly process

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/cross_section.png' | relative_url }}" alt="Cross section">
  <figcaption><em>Cross section of the assembly</em></figcaption>
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/pieces_1.jpg' | relative_url }}" alt="Parts">
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/pieces_2.jpg' | relative_url }}" alt="Parts">
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/pieces_3.jpg' | relative_url }}" alt="Parts">
  <figcaption><em>The individual components of the assembly</em></figcaption>
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/circuit.jpg' | relative_url }}" alt="The circuit">
  <figcaption><em>The circuit used to control the motor</em></figcaption>
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/assembled.jpg' | relative_url }}" alt="The assembled prototype">
  <figcaption><em>The assembled prototype</em></figcaption>
</figure>


## Testing

We designed 3 tests to evaluate the ability of the motor to spin the rotating trap, which is the key element of our design which traps the spotted lanternflies.

### 1. Degree of rotation

- How you tested it: Turning on the motor and spinning the rotor mechanism by hand, to make sure the top pieces and shaft are aligned, and to make sure that no interference between parts occurs during rotation.
- What happened: The alignment is good and there is no interference. The trap can rotate by 360 degrees. The component, however, does not slide down fully due to the tape we used.
- What design changes may be needed as a result: We connected the shaft to the motor with tape. The tape displaced where the components sat, and in the future we are going to glue the shaft to the motor.

### 2. Minimum voltage on the motor for motion (with the rotor attached)

- How you tested it: Attach the rotor to the motor, and measure the minimum voltage required for continuous motion and to start it.
- What happened: For continuous motion, 1.74 V is required. To start rotation, 2.47 V is required.
- What design changes may be needed as a result: This will inform how the arduino is programmed and confirms that our current battery setup (6V max) is sufficient.

### 3. Minimum rotating speed

- How you tested it: With the shaft and rotor components attached to the motor, measure the minimum sustained speed of the motor.
- What happened: The minimum speed of the motor is 45 rpm.
- What design changes may be needed as a result: We may buy a stepper motor since it can deliver slow, controlled rotation.

## Outcome

Overall, the assembly process showed that the tolerances on individual pieces of the 3D printed components were very good, and that they were within the capacity of the RPL to print. It also showed that our design was feasible, and we were able to achieve rotation and show that our design was easy to assemble. We also decided to replace our current motor with a stepper motor, in order to achieve a slower, more controlled rotational motion that is not possible with the motor we currently have.

# Client Report

No Fly Zone 

"Clearing the skies since 2026"

Constance Argenson, Kate Collard, James Montague, Olivia Polsky, Joshua Tchou

## Context and Problem Statement:
The spotted lantern fly (Lycorma delicatula), also known as SLFs, is an invasive species spreading prolifically throughout North America. The SLFs remain on grapevines during the harvesting process, contaminating the grapes and further decreasing yields. There is currently no efficient way to remove the SLF without damaging the grapevine, and that isn't labor-intensive. As a result, these insects continue to feed on vines and remain present during harvest, contributing to reduced yield. This product aims to reduce the population density of the SLFs, a vine-level removal process, without causing physical damage to the grapevines and minimizes labor requirements.

## Final Prototype and Application:
Our team designed and developed a trellis-mounted device that attracts and removes spotted lanternflies directly from grapevines using a combination of sensory lures and motorized capture (fig 1). The device operates in 2 stages, first the attraction of the SLF followed by the capture. Wintergreen oil, a known SLF attractant, will be placed in the opening of the device to lure the SLF's into the device. Once inside, the geometry of the enclosure guides them to the second chamber, where a geared DC motor drives a rotating, toothed mechanism that physically directs the SLFs into an isolated, removable collection chamber (fig 2). This motorized system ensures continuous movement to prevent escape while minimizing power requirements. The device is designed to operate continuously during the growing season. Lastly, the system is externally mounted and avoids direct contact with the grapes, meaning it removes SLFs without causing damage to the grapevines.

## Conclusion and Recommendation:
Our design was built with the idea of scalability. While our prototype works effectively, adjustments would have to be made if it were to be implemented on a larger scale. A large reason why we chose an arduino instead of a simpler microcontroller was the ability to add more features in the future. To monitor battery and functionality of multiple devices across the vineyard, a control panel could be used to display and communicate with the arduinos so that the client would only need to service devices that are in need of it, instead of individually checking them. 
Another solution to implement into our design could be solar panels. Since batteries must be replaced, it is inefficient to install hundreds of these prototypes across a vineyard. Having rechargeable batteries powered by solar panels allows the client to leave the traps for much longer periods. 
Another factor to consider is the oil we use. While using wintergreen oil is effective for smaller scale projects, having to replace the oil every few days so the scent does not fade is an additional labour cost. If we instead had a speaker powered by the solar panels emitting a 60 Hertz frequency (a frequency that has been shown to attract SLFs), we could replace the need for wintergreen oil entirely. 
We could also potentially reduce the size to make it more cost effective and lighter, making the device more practical for large-scale deployment. Specifically, we could test a different design shape rather than a cylinder with a hood. Another solution could be to move the motor to a different section of the design, allowing for space optimization in the body of the design. By refining the geometry and minimizing unnecessary material, the system could become more compact and easier to install across vineyard trellises. Reducing weight would also decrease structural strain and simplify mounting, while lowering material usage would directly reduce production costs. 
Given our resources and the scope of the class, most of the functional testing has already been completed. Our device met all our success criteria, operating efficiently and allowing model SLFs to be captured. To have a stronger pitch, tests in a controlled environment with actual SLFs should be conducted to quantify attraction to our device.

## Testing and Results:
The first success criterion was to create a small, lightweight product, setting a target of 1 kg mass and 1 L volume. A small, lightweight product makes installation and transportation of the device easier. The second success criterion was to have a product with a single, intuitive on/off switch, to make the transition to using this product as seamless as possible. The third success criterion was being able to operate continuously for 24 hours without running out of power. Ideally, with a solar power source, this means that the product should be able to operate indefinitely on solar power. Due to time constraints, we evaluated this success criterion with battery power. Testing the mechanical operation of the rotor, the function of the motor, and the battery demonstrated the feasibility of our design and manufacturing process. We were able to 3D print most parts and use a 4xAA battery pack to power our device, resulting in a small, lightweight, energy-efficient device.

## Prototype and Testing Details:
Our prototype consisted of two main subsystems: A mechanical trapping mechanism and an electronics assembly, housed within a 3D structure. The structural housing is composed of multiple 3D printed components including a shielded canopy top, a cylindrical main body, and a removable screw in the collection chamber. Within the collection chamber is a wintergreen oil soaked sponge to lure the SLFs into the device. The trapping mechanism uses a rotating disk(rotor) and a fixed disk(stator) whose intersecting slots funnel the SLFs downwards without crushing them as the rotor spins. The rotor is driven by a DC motor connected to a drive shaft, controlled through an NPN transistor by an Arduino and operated by a side switch. An LED light indicates when the motor is active. A flyback diode protects the motor, and all components are communally grounded. The electronics and battery packs are housed within the main body beneath the trapping mechanism, and the collection chamber screws into the bottom for easy removal and emptying. 
Referenced below are the steps for assembly:

## Assembly instructions:
Glue the 2 top shade pieces together.
Assemble the circuit according to the diagram.
Insert the small stator pieces into the stator. Slide the stator and its spacing ring onto the shaft.
Press fit the shaft into the rotor piece.
Solder the shaft into the motor's shaft, then place the motor into its housing.
Slide the current assembled pieces (motor, stator, rotor, spacer ring) into the housing. Insert the circuitry, battery, and wintergreen oil sponge into the housing beneath the other pieces, along with the big spacer ring.


Fit the storage container lid into the bottom of the housing, making sure the tubes align with the holes.
Screw the storage container into the bottom of the housing.
Place the main component on top into position and attach string at the top to hang

As we were focused on scalability, we wanted our 3D printed components to be interchangeable and assembled with full clearance and space for other components. The first test we did was to make sure that all gate components could rotate 360 degrees as intended without friction, to evaluate the feasibility of making most parts out of 3D printed plastic. After assembling the prototype, we rotated the trap 360 degrees to confirm it spun smoothly (only slight power losses and friction), confirming our main mechanical component of our device to be operational. Because we can 3D print most components, our prototype is able to be lightweight, which is directly related to our first success criterion.
The second test was testing the minimum voltage on the motor to start and maintain rotation, which was 2.47 V and 1.74 V respectively. This was within the capability of our 6V battery pack, and meant that we could keep the battery as is. We wanted to use as lightweight and compact a battery pack as possible, which relates to our first success criterion. Additionally, the batteries we chose for longevity (4x AA), and after current calculations, can last approximately six days (fulfilling our third success criterion of lasting for 24 hours).
Lastly, we tested the minimum rotating speed, which informed us on the choice of motor. The minimum rotating speed without stopping due to friction was 45 rpm, which was too fast for a spinning fly trap, and it could scare the lanternflies away. We decided to replace the motor with a different one that was able to rotate more slowly at 20 rpm and also required less power, which makes for smoother and more controlled operation.

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/cross_section.png' | relative_url }}" alt="Cross section">
  <figcaption><em>Fig 1: Cross-sectional diagram of the lure-and-trap prototype, showing key components including the shielding, SLF entryway, Arduino-driven rotating trap disk, quarantine tubes that keep bugs away from the motor, and the removable screw-in collection chamber.</em></figcaption>
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/final_report_fig2.png' | relative_url }}" alt="Top-down view">
  <figcaption><em>Fig 2: Top-down view of the rotating gate mechanism, showing the direction of rotation that forces spotted lanternflies down into the collection tubes.</em></figcaption>
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/final_report_fig3.png' | relative_url }}" alt="Wiring diagram">
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/final_report_fig4.png' | relative_url }}" alt="Electrical schematic">
  <figcaption><em>Figs 3 & 4: Electrical schematic and Arduino writing diagram for the motor control system, controlled by a slide switch and powered by 4x AA batteries</em></figcaption>
</figure>

<figure style="text-align: center;">
  <img src="{{ '/assets/images/odp/final_report_fig5.jpg' | relative_url }}" alt="Final prototype">
  <figcaption><em>Fig 5: Final Prototype</em></figcaption>
</figure>

## References

### Bill of Materials:
[Link to full spreadsheet](https://docs.google.com/spreadsheets/d/16uwDL93W0Ph_2rDUHpTFeSXxPhX5ICIhDJ4LlQW6VzM/edit?usp=sharing)

| Item name | Price | Quantity |
| :---: | :---: | :---: |
| Drive shaft | $1.15 | 1 |
| Casing (RPL) | $19.32 | 1 |
| Rotor Disc 1 (RPL) | $1.93 | 1 |
| Stator Disc (RPL) | $2.85 | 1 |
| Rotors (RPL) | $0.31 | 1 |
| Stators (RPL) | $0.31 | 1 |
| Component 11 (RPL) | $0.90 | 1 |
| Component 12 (RPL) | $3.43 | 1 |
| Component 13 (RPL) | $4.34 | 1 |
| Component 14 (RPL) | $5.66 | 1 |
| Component 16 (RPL) | $6.74 | 1 |
| Component 18 (RPL) | $0.88 | 1 |
| Geared DC Motor 6V | $8.29 | 1 |
| Arduino Uno R3 | $27.60 | 1 |
| NPN Transistor (BJT) | $8.99 | 1 |
| Battery (VL, 4xAA) | Provided | 1 |
| Battery (Vs, 1x9V) | $6.46 | 1 |
| Resistor Variety Pack | $4.99 | 1 |
| Wires and heat shrink tubing | $11.99 | 1 |
| Female/Male Header Crimps | $9.69 | 1 |
| Slide Switch | $4.99 | 1 |
| Wintergreen oil | $7.99 | 1 |
| Sponge | $2.99 | 1 |
| Green LED | $5.99 | 1 |
| 9V barrel jack | $3.97 | 1 |
| Diode | $4.03 | 1 |

Total $155.79

### Citations:
Pinto, Allan F, et al. “Assessing the Potential Economic Impacts of Spotted Lanternfly (Hemiptera: Fulgoridae) Infestations on Grape Production in New York State.” Journal of Integrated Pest Management, vol. 16, no. 1, 1 Jan. 2025, academic.oup.com/jipm/article/16/1/2/7964417, https://doi.org/10.1093/jipm/pmae039. Accessed 16 Feb. 2025.

“Spotted Lanternfly Reveals a Potential Weakness.” Usda.gov, 10 Jan. 2025, www.usda.gov/about-usda/news/blog/spotted-lanternfly-reveals-potential-weakness.

Williams, Larry E. “MODELLING WATER USE of GRAPEVINE.” HortScience, vol. 28, no. 5, May 1993, pp. 489g489, https://doi.org/10.21273/hortsci.28.5.489g. Accessed 6 May 2026.



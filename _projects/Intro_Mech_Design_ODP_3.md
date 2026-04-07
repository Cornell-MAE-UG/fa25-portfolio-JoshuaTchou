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

- https://academic.oup.com/jipm/article/16/1/2/7964417?searchresult=1&login=true#521897831
- https://www.sciencedirect.com/science/article/pii/S0167880924004390
- https://academic.oup.com/jipm/article/16/1/2/7964417
- https://academic.oup.com/jee/article/115/6/2116/6777183

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

We designed 3 tests to evaluate the key feature of our design, which was the rotation of the rotor which serves as a rotating trap.

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
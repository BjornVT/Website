---
title: "Loadcells"
date: 2023-01-22T12:11:23+01:00
url: /loadcells/
tags:
    - Loadcells
draft: false

thumbnail: "images/2023/loadcell.png"
lead: "Loadcells - How to use them" # Lead text
comments: true # Enable Disqus comments for specific page
# authorbox: false # Enable authorbox for specific page
pager: true # Enable pager navigation (prev/next) for specific page
toc: false # Enable Table of Contents for specific page
mathjax: true # Enable MathJax for specific page
sidebar: "right" # Enable sidebar (on the right side) per page
widgets: # Enable sidebar widgets in given order per page
  - "search"
  - "recent"
  - "taglist"
---

A load cell is a type of transducer that is used to convert a force into an electrical signal. It is essentially a type of force sensor that can measure weight or force applied to it. Load cells are commonly used in industrial settings such as weighing scales, and in research and testing to measure force, weight, and pressure. They are typically made from materials such as steel, aluminum, or silicon and can be found in various forms such as beam, platform, and cylindrical. The electrical signal output by the load cell can be read by an electronic device such as a digital scale, which can then display the weight or force measurement.

## Calculation
Before calculating the force applied to the loadcell we need some characteristics of the loadcell. These can be found in the datasheet of the loadcell or on the calibration document.
* Sensitivity of the loadcell. This is usually in mV/V. This is what voltage the loadcell will return at max capacity when he has an excitation voltage of 1V.
* The maximum capacity of the loadcell. This can be in kg, Pounds, Newton. The result will be in the same unit as this parameter.

### Formula
$$F = \frac{Vm \times Max}{S \times Vs}$$
**With:**

* **F**: The measured force on the loadcell.
* **Vm**: The measured voltage from the loadcell (V).
* **Max**: The maximum capacity of the loadcell (kg).
* **S**: The sensitivirty of the loadcell (mV/V).
* **Vs**: Excitation voltage of the loadcell (V).

### Example 1
An ADC is measuring 4.97mV from a loadcell with 3.012mV/V sensitivity and a max load of 200kg. The excitation voltage of the loadcell is 3.3V. If we plug in these values in the formula above:
$$\frac{0.00497V \times 200kg}{0.003012\frac{V}{V} * 3.3V} = 100kg$$

### Example 2
An ADC is measuring 27mV from a loadcell with 3mV/V sensitivity and a max load of 100 pounds. The excitation voltage of the loadcell is 10V. If we plug in these values in the formula above:
$$\frac{0.027V \times 100 lbs}{0.003\frac{V}{V} * 10V} = 90 lbs$$
---
layout: project
type: project
image: images/micromouse.jpg
title: Saleen Series 6
permalink: projects/SaleenSeries6
# All dates must be YYYY-MM-DD format!
date: 2016-07-29
labels:
  - Cars
  - CAD
  - Fabrication
summary: Installation of a discontinued supercharger on a 2007 Mustang GT.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>

Saleen produced its series 6 supercharger for the 05-10 mustang gt's which were equipped with a 4.6 liter engine with 3 valves per cylinder. The series 6 supercharger was discontinued in mid-2011 with the introduction of the 5.0 liter 4 valves per cylinder engine that replaced the old 4.6. In March of 2016, a series 6 was being auctioned during a car show at a local dealership which I was in attendance. I bid and won the auction, but found out that none of the other components needed for installation were included with the purchase, nor did the dealership have it. After speaking to Saleen and other authorized dealers, I found that the series 6 was discontinued for some time and that the necessary components to install would be near impossible to find. Thus began the 2 month long project.

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

Here is some code that illustrates how we read values from the line sensors:

```js
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

You can learn more at the [UH Micromouse Website](http://www-ee.eng.hawaii.edu/~mmouse/about.html).


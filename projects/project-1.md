---
layout: project
type: project
image: images/micromouse.jpg
title: Micromouse
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2016-07-01
labels:
  - Cars
  - fabrication
  - CAD
summary:Installation of a discontinued supercharger on a 2007 Mustang GT.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>

Saleen produced its series 6 supercharger for the 05-10 mustang gt's which were equuipped with a 4.6 litre engine with 3 valves per cylinder. The series 6 supercharger was discontinued in mid-2011 with the introduction of the 5.0 litre 4 valves per cylinder engine that replaced the old 4.6. In March of 2016, a series 6 was being auctioned during a carshow at a local dealership which I was in attendance. I bid and won the auction, but found out that none of the other components needed for installation were included with the purchase, nor did the dealership have it. After speaking to Saleen and other authorized dealers, i found that the series 6 was discontiued for some time and that the necessary components to install would be near impossible to find. Thus began the 2 month long project.

For this project, I designed the needed components and with the help of Universal Engineering, was able to develop one-off components to continue installation. For various other components, readily available parts for varying other vehicles were repurposed for this project. I wired in a new fuse box which housed the relays to control an electric water pump, low speed radiator fan and high speed radaitor fan to aid in cooling. I routed battery cables through the passenger compartment to relocate the battery to the rear of the vehicle. I then designed a cooling loop for the supercharger that utilized the space that was previously occupied by the battery. Once the Series 6 was installed. I installed a more robust fuel system to provide enough fuel when the supercharger starts porviding possitive pressure in the combustion chambers. I retuned the engine with the help of an Engine tuning specialist from South America. The Mustang was then brought to a dynomometer which measures the power output at the rear wheels of a vehicle. 427 horsepower and 387 foot pounds of torque was measured, an increase of 42% for horsepower and 21% for torque from before the start of the project.  

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

This is currently an ongoing project of mine, always finding ways to increase the output of the engine, improve the handling of the vehicle, or going back to improve things as I myself improve my skills. 




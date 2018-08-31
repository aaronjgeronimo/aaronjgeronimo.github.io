---
layout: project
type: project
image: images/micromouse.jpg
title: Saleen Series 6
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2015-07-01
labels:
  - Cars
  - CAD
  - Fabrication
summary: Installation of a discontinued supercharger on a 2007 Mustang GT.

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, I designed the needed components and with the help of Universal Engineering, was able to develop one-off components to continue installation. For various other components, readily available parts for varying other vehicles were repurposed for this project. I retuned the engine with the help of an Engine tuning specialist from South America. The Mustang was then brought to a dynomometer which measures the power output at the rear wheels of a vehicle. 427 horsepower and 387 foot pounds of torque was measured, an increase of 42% for horsepower and 21% for torque from before the start of the project.  

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



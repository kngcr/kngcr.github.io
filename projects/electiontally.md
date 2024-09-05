---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "ElectionTally"
date: 2023-11-19
published: true
labels:
  - Calculations
  - Individual Project
  - C++
summary: "I programmed an election results calculator that takes five candidates and their number of votes for an ICS 212 homework assignment."

---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

ElectionTally was the first C++ homework assignment in ICS 212. The objective was to write a C++ program that allows the user to input five candidate surnames and their number of votes, then return all names and votes in a specific format along with the percentages of votes received by each candidate and the name of the election winner.

Here is some code that illustrates how we read values from the line sensors:

```cpp
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

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).

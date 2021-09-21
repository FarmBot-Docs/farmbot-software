---
title: "Kinematic Equations"
slug: "kinematic-equations"
description: "Equations relating linear speeds to motor speeds"
---

* toc
{:toc}


The equations on this page are affected by the following specs of your FarmBot hardware:

|                    |                    |
|--------------------|--------------------|
|**Motor Resolution**|200 steps/revolution|
|**Pulley Size**     |20 teeth/revolution |
|**Belt Pitch**      |2mm/tooth           |
|**Leadscrew Lead**  |8mm/revolution      |

# Convert motor speed into linear speed

## Belt-driven axes (X and Y)

**Linear Speed** = **Motor Speed** / **Motor Resolution** x **Pulley Size** x **Belt Pitch**

For an example Motor Speed of 500 steps/second on the stock belt-driven (X and Y) axes, the equation works out to:

**Linear Speed (mm/second)** = 500 / 200 x 20 x 2 = **100 mm/s**

## Leadscrew-driven axes (Z)

**Linear Speed** = **Motor Speed** / **Motor Resolution** x **Leadscrew Lead**

For an example Motor Speed of 500 steps/second on the stock leadscrew-driven (Z) axis, the equation works out to:

**Linear Speed (mm/second)** = 500 / 200 x 8 = **20 mm/s**


# Calculate steps per mm

## Belt-driven axes (X and Y)

**Steps per mm** = **Motor Resolution** / **Pulley Size** / **Belt Pitch**

For the stock belt-driven (X and Y) axes, the equation works out to:

**Steps per mm** = 200 / 20 / 2 = **5 steps/mm**

## Leadscrew-driven axes (Z)

**Linear Distance** = **Motor Resolution** / **Leadscrew Lead**

For the stock leadscrew-driven (Z) axis, the equations works out to:

**Steps per mm** = 200 / 8 = **25 steps/mm**
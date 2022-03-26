---
title: 'Hobby project: Hollow Shaft "Turret"'
date: 2022-03-26
permalink: /posts/2022/03/26/code/
tags:
  - hobby
  - turret
---

Hollow Shaft "Turrent" is a 3D printed, motorized mechanism for tracking in 2 or 3 axis. 
The *hollow shaft* refers to the mechanical design of rotation, such that it takes 
into account cable management. For instance, lets have a camera mounted on single 
axis, that is connected to PC via cable. If the camera rotates 360 degrees around its axis
then the cable is tangled around the mechanism providing the rotation. The more the camera 
turns around, the more cable is wound around the mechanism.

To address the problem of cable management on rotating mechanisms with multiple-axis, it is 
ideal to come with a solutions, than prevents a cable winding around the parts of the 
mechanism all together. One such solution is to have a **hollow shaft** through which the 
cable runs, such that there is *nothing* that the cable needs to revolve around in the 
first place (except its own axis).

To explain the name fully, the word "turret" refers to the rotation capability, and I hope to come
up with some cool acronym later, such as:

`T`inkerer's   \n
`U`niversal   \n
`R`otating   \n
`R`obot   \n
(with)   \n
`E`ffective   \n
`T`echnique for cable managenemnt   \n
  

*P.S. You are very welcome to contribute to this project with better acronym.*

## Progress
- [x]  decide of-the-shelf parts to settle on dimensions
- [x]  get mechanical parts (6810 bearings and M3 screws)
- [x]  design the first prototype of the "wheel"
- [x]  3D print the "wheel"
- [ ]  design the base-plate which holds everything together
- [ ]  design multi-axis mechanism 
- [ ]  3D print everything from correct material
- [ ]  pick proper NEMA17 stepper motors (with proper torque)
- [ ]  get timing pulley and timing belt (preferably 10mm wide)
- [ ]  get stepper motor drivers (based on TMC2209)
- [ ]  get arduino with CNC shield 


## "Napkin" inception of hollow shaft

The idea started as a sleepless night, when my mind was racing for a simple solution to age-old question. 
What to do with cables when things rotate? The below image is an inception of hollow shaft mechanism, which 
would be robust yet simple to manufacture using a 3D printer, with minimum of of-the-shelf parts. 
![turret_cross_section](/images/blog/hobby_turret/turret_cross_section_drawing.jpg)

## Assumptions about first prototype
Next step is to agree od dimensions and requirements, such as the hollow shaft width and necessary of-the-shelf parts.
 I have settled on 2 things: 

1. Allow myself to visit a local bearing shop and find a standardized bearing (as opposed to bushings in the "Napkin" inception)
2. Use NEMA17 stepper motors, since they are lighter and cheaper than NEMA24 and still pack a punch

The visit yielded a **bearing 6810**, a deep grove radial bearing. As I remember from my achelor studies, 
these bearings can take a radial torque and radial pressure without any problem. The dimensions of the bearings are below:

![6810_dimensions](/images/blog/hobby_turret/6810_dimensions.jpg)
D = 65 [mm]  \n
d = 50 [mm]  \n
B = 7 [mm]

The NEMA17 is a ctually a family of stepper motors, but this one seems particularly well built for the task in hand,
the **NEMA17 42CM08** shown below, has torque of 0.8 [Nm] and can be controlled with 1.5 [A] (max 2.5 [A]), which is 
exactly what the TMC2209 can handle without any problems. 

![NEMA17_42CM08](/images/blog/hobby_turret/NEMA17_42CM08.png)


## First prototype
With the basic of-the-shelf parts selected, I have installed SolveSpace and started to work on the hollow shaft gear, that 
will be driven by the stepper motor.

![solvespace_wheel_v4](/images/blog/hobby_turret/turret_wheel_v4.png)

And this is the prototype printed from **TPU** with 0.2 [mm] layer height with 50 [%] infill. 

![solvespace_wheel_v4](/images/blog/hobby_turret/3d_print_wheel_v4.jpeg)







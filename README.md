# Unreal Finding Project

**Unreal Finding Project** is my second VR project that I've built from scratch.
The player need find 'THE RED BALLOON' within the room and throw at a fire, to take a fire out.
the fire will be randomly generate and the time is limited!!!
becareful of the fake balloon! looking for the red one only!!
try to control the fire as long as possible.

#### Controllers
- B for turn menu on / off
- A for click / turn menu on
- right/left grip to grab object
- release to drop
- push Right Thumb Stick to turn on 'teleport prediction'
- move thumb stick around to select the direction and press to teleport
- look up for the menu
- START
- EXIT
- RESUME
- RESTART
#### Locomotion system
- I've chose the 'projectile locomotion' since the room space is really small, it'll be easier to control 
the teleport distance
- and it's much easier to move around the virtual, while you just sitting in real world!
- limited teleport area by measure the hit surface normal
- allow to choose which direction by rotate thumbstick

## Details
#### The Design
- FPS is limited at 90 (89-90fps in VR mode) (120-130fps in normal)
- GTX 980, i7-4790K 4.00 GHz, RAM 32GB
<img src="https://github.com/bestspang/unrealFindingProject/blob/master/ss01.jpg" width="300"/>
<img src="https://github.com/bestspang/unrealFindingProject/blob/master/ss02.jpg" width="300"/>
<img src="https://github.com/bestspang/unrealFindingProject/blob/master/ss03.jpg" width="300"/>

- balloon getting bigger before explode (animation!!)
- the fire will be remove after get overlap by RED BALLOON
- The menu is moveing refer to your head
- just stand at the spawn point and you'll be able to reach for all the plates
- able to restart
- custom whileloop for game mechanic
- most of BP store in player Pawn

#### Timing system (timer)
- Basically you start with a fixed amount of time (60secs) per round (one fire per round)
- after you take a fire out, you'll get +2 secs
- if you take out fire before round end you'll get unlimited extra fire. (+2secs per each)
- each round time reduce by 5 (60-5 = 55 and so on)
- the game will end when fire reach 5
- the score is the number of fire you had take out
- 1 score per fire

#### Lightings
- MSAA + Forward shading
- no Bloom
- no Auto explosure
- no Motion Blur

#### 3rd Party assets
- Sound and the room that come with the given package
- p_confentti from first lesson
- a_balloonPop sound
- udacity hand

## more details
- Unreal Engine 4.15.3
- built for Oculus Rift
- 2 hand supported (2 motion controller)
- only right hand can teleport for now
- both can grab

## what to improve
- can't release two object from both hand at the same time
- not fully release object


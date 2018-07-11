## Unreal VR Project

**Unreal VR Project** is VR ARCHVIZ template project that I've built from scratch.
the goal is to build a very simple and understandable template, 
for Architectural visualization purposes based on BLUEPRINTs, UNREAL.

#### Controllers

- 'Grab' for turn menu on / off
- 'Menu button' for click / turn menu on
- 'right/left grip' to grab object
- 'release' to drop
- 'Touch pad' to turn on 'teleport prediction'
- move around the Touch pad to select the direction and press to teleport
- look up for the menu

#### Locomotion system

- 'projectile locomotion' since the room space is really small, it'll be easier to control 
the teleport distance
- and it's much easier to move around the virtual, while you just sitting in real world!
- limited teleport area by measure the hit surface normal
- allow to choose which direction by rotate thumbstick

## Updates

### Version 0.02

```
- UE 4.19.2 supported!
- add basic VR blueprint 'Vive' and PS
- edit input mapping for 'Vive'
- prepare for hand spawn
- add BP_MotionController
- change to support for 'Vive'

```
### Version 0.01

```
- UE 4.15.3 supported
- 2 hand supported (2 motion controller)
- built for 'Oculus Rift'
- only right hand can be teleport
- both hands can grab

```

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

#### TO DO

- teleport map
- call map
- spawn Controller instead of attach it to Pawn.
- fix grab system
- fix can't release two object from both hand at the same time
- fix not fully release object

## Documentation

Documentation is available at [fennect.com](https://fennect.com/).

## License

**VRfennect** is published under [Apache License 2.0](https://github.com/bestspang/VR4Arch/blob/master/LICENSE).



ShockWave_LWRP
-------------------------------------
[Asset Store Link](http://u3d.as/8jm)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!-- TOC -->

- [ShockWave_LWRP](#shockwavelwrp)
- [Table of Contents](#table-of-contents)
- [Contact](#contact)
- [Description Features](#description-features)
- [Terms of Use](#terms-of-use)
- [Requirements](#requirements)
- [Overview/Setup](#overviewsetup)
- [ShockWave_WS](#shockwavews)
    - [SetUp](#setup)
    - [ShockWave.prefab](#shockwaveprefab)
- [ShockWave_PP](#shockwavepp)
    - [SetUp](#setup-1)

<!-- /TOC -->


## Contact  

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.info/contact](http://justingarza.info/contact/)

## Description Features

an Awesome ShockWave Effect!

* Easily customizable effect. Size, Color, * Speed, etc.
* Unity Free friendly.
* Fully commented C# code.
* Awesome demos!


## Terms of Use

You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

## Requirements
* Lightweight Render Pipeline (5.10.0)
* Shader Graph (5.10.0)
* Post Processing (2.1.6)

![Imgur](https://i.imgur.com/VAjPArs.png)


## Overview/Setup 

There are two parts to this asset.
* ShockWave_WS 
    * ShockWave in WorldSpace
* ShockWave_PP
    * ShockWave as a Post-Processing Effect

Examples:  
**ShockWave_WS**  
![Imgur](https://i.imgur.com/c2EZ0gZ.gif)

**ShockWave_PP**  
![Imgur](https://i.imgur.com/Ys10Ex8.gif)

## ShockWave_WS

### SetUp  
this is my setup for the LWRP assets
![Imgur](https://i.imgur.com/7HnoTto.png)

### ShockWave.prefab  
the ShockWave.prefab is a pretty standard Quad with a Special Script attached to it that allows the material to be animate.

The *Anim variables are the main ones you want to change to adjust for your liking.  

![Imgur](https://i.imgur.com/RUxuR4p.png)

And this little Slider helps to you preview it in edit mode!  

![Imgur](https://i.imgur.com/vCkhPiN.gif)

## ShockWave_PP

### SetUp

for this we'll need to add a few components to the camera.
* Post Processing Layer
* Post Processing Volume

And Also we'll need to Change the 
* Layer (both in the object and in Post Processing Layer)
* Is Global should be True
* Assign the ShockWave_PPP
* Add the ShockWave Effect
  

![Imgur](https://i.imgur.com/ZPFgCT1.png)


### ShockWaveCreator.prefab

the *Anim variables are the mains ones you'll use to customize this effect.

![Imgur](https://i.imgur.com/yOiKSLb.png)
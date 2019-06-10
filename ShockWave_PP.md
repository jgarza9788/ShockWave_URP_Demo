

ShockWave_PP
-------------------------------------
[Asset Store Link](http://u3d.as/1xYk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

# Table of Contents

<!--TOC-->
* [ShockWave_PP](#shockwave_pp)
* [Table of Contents](#table-of-contents)
* [Contact](#contact)
	* [Terms of Use](#terms-of-use)
* [Description Features](#description-features)
* [ShockWave_PP](#shockwave_pp)
	* [SetUp](#setup)
	* [ShockWaveCreator.prefab](#shockwavecreator.prefab)
	* [Demo](#demo)

<!--TOC-->

# Contact  

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [justingarza.info/contact](http://justingarza.info/contact/)

## Terms of Use

You are free to add this asset to any game you’d like
However:  
please put my name in the credits, or in the special thanks section. :)  
please do not re-distribute.  

# Description Features

Creates an Awesome ShockWave Effect!

* ShockWave_PP
    * This creates a shockwave in screen space using the Unity Post Processing Method.
    * Easily customize effect
        * Size
        * Color
        * Distortion
        * Speed


# ShockWave_PP

## SetUp

for this we'll need to add a few components to the camera.
* Post Processing Layer
* Post Processing Volume

And Also we'll need to Change the 
* Layer (both in the object and in Post Processing Layer)
* Is Global should be True
* Assign the ShockWave_PPP
* Add the ShockWave Effect
  

![Imgur](https://i.imgur.com/ZPFgCT1.png)


## ShockWaveCreator.prefab

the *Anim variables are the mains ones you'll use to customize this effect.

![Imgur](https://i.imgur.com/yOiKSLb.png)


## Demo
the demo is named **Demo_ShockWave_PP**.unity.  
just click around the demo to use it.  

here is a list of the main scripts used in the demo

**ShockWaveCreator.cs**  
This script will set global variables with in ShockWave_PPM(hidden).shader.  



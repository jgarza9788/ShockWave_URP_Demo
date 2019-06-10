

ShockWave_PPWS
-------------------------------------
[Asset Store Link](http://u3d.as/1xYk)  
© 2017 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
* [ShockWave_PPWS](#shockwave_ppws)
	* [Table of Contents](#table-of-contents)
	* [Contact](#contact)
	* [Terms of Use](#terms-of-use)
	* [Description Features](#description-features)
* [ShockWave_PPWS](#shockwave_ppws)
	* [SetUp](#setup)
	* [ShockWave.prefab](#shockwave.prefab)
	* [Demo](#demo)

<!--TOC-->


## Contact  

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

## Description Features

Creates an Awesome ShockWave Effect!

* ShockWave_PPWS
    * This creates a shockwave in world space using the Unity Post Processing Method.
    * Easily customize effect
        * Size
        * Distortion
        * Speed

note: i have not got color to work with this version...yet.


# ShockWave_PPWS

## SetUp

for this we'll need to add a few components to the camera.
* Post Processing Layer
* Post Processing Volume

And Also we'll need to Change the 
* Layer (both in the object and in Post Processing Layer)
* Is Global should be True
* Assign the ShockWave_PPWS
* Add the ShockWave Effect
  

![Imgur](https://i.imgur.com/q0B0jh0.png)


## ShockWave.prefab  
the ShockWave.prefab is a pretty standard Quad with a Special Script attached to it that allows the material to be animate.

The *Anim variables are the main ones you want to change to adjust for your liking.  

![Imgur](https://i.imgur.com/LknbcCK.png)

And this little Slider helps to you preview it in edit mode!  

![Imgur](https://i.imgur.com/J4P4ZkA.gif)


> Note: ShockWave_Sphere.prefab is the same shader being used on a sphere, and it looks pretty cool

## Demo
the demo is named **Demo_ShockWave_PPWS**.unity.  
just click around the demo to use it.  

here is a list of the main scripts used in the demo

**ShootOnClick.cs**  
generates a sphere projectile

**GenerateShockWave.cs**  
creates a ShockWave (from prefab)

**DestroyAfter.cs**  
destroys the projectile after 5 seconds

**ShockWaveWSEffect.cs**  
This animates the ShockWave and removes it



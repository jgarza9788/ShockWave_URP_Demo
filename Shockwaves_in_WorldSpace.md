Shockwaves_in_WorldSpace.md
---


## Table of Contents

<!--TOC-->
* [Shockwaves_in_WorldSpace.md](#shockwaves_in_worldspace.md)
	* [Table of Contents](#table-of-contents)
	* [Overview](#overview)
	* [Set Up](#set-up)
	* [prefabs](#prefabs)
		* [shockwave.prefab](#shockwave.prefab)
			* [ShockWaveAnim.cs](#shockwaveanim.cs)
			* [shockwave.shadergraph](#shockwave.shadergraph)
	* [other scripts](#other-scripts)
		* [GenerateShockWave.cs](#generateshockwave.cs)
		* [ShootOnClick.cs](#shootonclick.cs)
		* [DestroyAfter.cs](#destroyafter.cs)
	* [Videos](#videos)
	* [FAQs](#faqs)
		* [the ShockWave is grey!](#the-shockwave-is-grey!)
			* [example](#example)
			* [solution](#solution)
		* [I can see the edge of the Quad!](#i-can-see-the-edge-of-the-quad!)
			* [example1](#example1)
			* [solution](#solution)
			* [example2](#example2)
			* [solution](#solution)
		* [the Shockwave doesn't show the sprite (or transparent objects)](#the-shockwave-doesn't-show-the-sprite-(or-transparent-objects))
			* [solution](#solution)

<!--TOC-->

## Overview 
These are effects that render on a quad and distorts what's behind them. 

## Set Up

Use the URP_Asset  
it's in ***\ShockWave_URP\Assets\URP**

note: this will do several things.

1. Allow us to use _CameraOpaqueTexture
   * we are distorting this texture to make the effect

![Imgur](https://i.imgur.com/HgPbaSNm.png)  
[link](https://i.imgur.com/HgPbaSN.png)

## prefabs

### shockwave.prefab

this is the main prefab to generdate the effect.

#### ShockWaveAnim.cs

this will animate the settings in the shader.

* Material
  * the material we will copy from
* Shader
  * the shader we will use
* Speed
  * how fast it will play back
* T
  * the current time
* Radius Anim
  * the animation curve for the radius
* Wavesize Anim
  * the animation curve for the wavesize
* Amplitude Anim
  * the animation curve for the amplitude
* Color Anim
  * the color over time during the animation
* Sat Anim
  * the animation curve for the color's saturation
* Render Texture  
  * this is the render texture that will be used within the shader
  * if this is blank an opaque texture will be used...  
    *  thus sprites and transparent objects will not show
* Destory When Done
  * weather the object will be destroyed when done
* Time Preview_In Edit Mode Only
  * slide this during edit more to see the animation

#### shockwave.shadergraph

this is the shader that causes the effect.

![Imgur](https://imgur.com/zlutoFPm.png)  
[link](https://imgur.com/zlutoFP.png)

>Note:  
if useRenderTexture is true, the render texture will be used.  
if false, the script will use an opaque texture.  
--  
the opaque render texture will not show transparent objects or sprites.  



## other scripts

### GenerateShockWave.cs

this will instantiate the shockwave based on where the projectile hits.

### ShootOnClick.cs

shoots the projectile

### DestroyAfter.cs

destroys an object after X time.

## Videos

[Demo1](https://www.youtube.com/watch?v=lg5CAIxP-ww)  
[Demo2](https://www.youtube.com/watch?v=Z_wAd-TFDAY)


## FAQs

### the ShockWave is grey!

#### example

![Image](https://i.imgur.com/erOB8dim.png)   
[link](https://i.imgur.com/erOB8di.png)


#### solution

change the settings of one of the camera(s) so that it creates a CameraOpaqueTexture (see below).  
note there is also an option in the camera object called "Opaque Texture" (make sure this is on).  

![Imgur](https://i.imgur.com/vk3a1D7m.png)  
[link](https://i.imgur.com/vk3a1D7.png)


### I can see the edge of the Quad!

#### example1
![Image](https://imgur.com/0RgVJMwm.png)  
[link](https://imgur.com/0RgVJMw.png)

#### solution
this is caused by the Render Texture having a different aspect ratio then the screen.  
please see the createRT.cs, this will create a render texture at start up.

#### example2
![Image](https://imgur.com/B3PA9rim.png)  
[link](https://imgur.com/B3PA9ri.png)

#### solution
if two shockwaves overlap, they will not take each other into account.  
and you'll see the small glitch above.


### the Shockwave doesn't show the sprite (or transparent objects)

#### solution  
if no render texture is given to the shader it might be using the _CameraOpaqueTexture.  
Which will not have in it.  
you can set up a secondary camera, and render out to a render texture.  
and pass the render texture into the shader.  
and make sure the option is set to true.  
see Demo_Basic.unity (a scene)
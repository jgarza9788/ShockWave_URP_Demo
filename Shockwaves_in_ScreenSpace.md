Shockwaves_in_ScreenSpace.md
---


## Table of Contents

<!--TOC-->
* [Shockwaves_in_ScreenSpace.md](#shockwaves_in_screenspace.md)
	* [Table of Contents](#table-of-contents)
	* [Overview](#overview)
	* [Set Up](#set-up)
			* [shockwave_ss_v1.3.shadergraph](#shockwave_ss_v1.3.shadergraph)
	* [other scripts](#other-scripts)
		* [ShockWaveSS_Manager.cs](#shockwavess_manager.cs)
		* [CreateShockWave_OnClick.cs](#createshockwave_onclick.cs)
	* [FAQs](#faqs)

<!--TOC-->

## Overview 
These are effects that render right under the UI.

## Set Up

**big thanks to Cyanilux, for creating the blit pluging**  
[video demo](https://www.youtube.com/watch?v=mCpRxFP2J1c)

Use the URP_Asset  
it's in ***\ShockWave_URP\Assets\URP**

this URP has already been set up to allow for 5 shockwaves

![Image](https://imgur.com/ulKJsvom.png)  
[link](https://imgur.com/ulKJsvo)


#### shockwave_ss_v1.3.shadergraph

this is the shader that we will blit to the screen to make the screen effect.  
this is used in the ShockWave_SS#.mat files.

note: multiple materials need to be used so that the shockwaves can have different values.


## other scripts

### ShockWaveSS_Manager.cs  

this will manage our shockwave materials.  
and pass in values to animate them.


### CreateShockWave_OnClick.cs

on click this takes the point on the screen and passes it to the ShockWaveSS_Manager.cs,  
thus producing the shockwave.

## FAQs
i don't know what errors could happen with this.
i'll fill this in later, if/when people have issues using this.

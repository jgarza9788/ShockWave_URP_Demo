Shockwave_URP
---

<a href="https://www.youtube.com/watch?v=lg5CAIxP-ww" style="background-color: red; border-radius: 12px; color: white; padding: 6px 12px">
youtube.com
</a>

---

[Asset Store Link](http://u3d.as/1xYk)  

© 2020 Justin Garza

PLEASE LEAVE A REVIEW OR RATE THE PACKAGE IF YOU FIND IT USEFUL!
Enjoy! :)

## Table of Contents

<!--TOC-->
- [Shockwave\_URP](#shockwave_urp)
- [Table of Contents](#table-of-contents)
- [Contact](#contact)
- [Description Features](#description-features)
- [Set Up](#set-up)
- [prefabs](#prefabs)
  - [shockwave.prefab](#shockwaveprefab)
    - [ShockWaveAnim.cs](#shockwaveanimcs)
    - [shockwave.shadergraph](#shockwaveshadergraph)
- [if false, the script will use an opaque texture.](#if-false-the-script-will-use-an-opaque-texture)
- [other scripts](#other-scripts)
  - [createRT.cs](#creatertcs)
  - [GenerateShockWave.cs](#generateshockwavecs)
  - [ShootOnClick.cs](#shootonclickcs)
  - [DestroyAfter.cs](#destroyaftercs)
- [Videos](#videos)
- [Terms of Use](#terms-of-use)
- [FAQs](#faqs)
  - [the ShockWave is grey!](#the-shockwave-is-grey)
    - [example](#example)
    - [solution](#solution)

<!--TOC-->

## Contact

Questions, suggestions, help needed?  
Contact me at:  
Email: jgarza9788@gmail.com  
Cell: 1-818-251-0647  
Contact Info: [jgarza9788 - UnityPortfolio](https://github.com/jgarza9788/UnityPortfolio)  

## Description Features

Easily customize the animation's

* speed
* radius
* wavesize (thickness)
* amplitude (distortion amount)
* color

## Set Up

Use the URP_Asset  
it's in ***\ShockWave_URP\Assets\URP**

note: this will do several things.

1. Allow us to use _CameraOpaqueTexture
   * we are distorting this texture to make the effect

![Imgur](https://i.imgur.com/HgPbaSN.png)

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
* renderTexture_assetpath
  * this is the path were the RenderTexture can be loaded from 
    * make blank if you don't plan to use a Render Texture
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

![Imgur](https://imgur.com/zlutoFP.png)

>Note:  
if useRenderTexture is true, the render texture will be used.  
if false, the script will use an opaque texture.  
--  
the opaque render texture will not show transparent objects or sprites.  



## other scripts

### createRT.cs  
creates a RenderTexture and adds it to the Camera.
the RenderTexture will be created based on the current screensize.


### GenerateShockWave.cs

this will instantiate the shockwave based on where the projectile hits.

### ShootOnClick.cs

shoots the projectile

### DestroyAfter.cs

destroys an object after X time.

## Videos

[Demo1](https://www.youtube.com/watch?v=lg5CAIxP-ww)
[Demo2](https://www.youtube.com/watch?v=Z_wAd-TFDAY)

## Terms of Use

Required:
please follow [Unity's EULA](https://unity3d.com/legal/as_terms) 

Suggestion/Optional:
please put my name in the credits, or in the special thanks section. :)  



## FAQs

### the ShockWave is grey!

#### example

![Image](https://i.imgur.com/erOB8di.png)

#### solution

change the settings of one of the camera(s) so that it creates a CameraOpaqueTexture (see below)

![Imgur](https://i.imgur.com/vk3a1D7.png)



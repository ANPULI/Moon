---
layout: post
title:  "Computer Graphics Projects"
date:   2019-12-17
excerpt: "A list of projects done in CSCI-UA 480"
tag:
- computer graphics
- webgl
- vr
comments: true
project: true
feature: https://user-images.githubusercontent.com/26131764/71408444-39275a00-2679-11ea-950f-f28ea7eaa948.png

---

This is the list of projects I've done when learning Computer Graphics with Professor Ken Perlin.

- [Final Project: Go](#final-project-go)
- [Wave](#wave)
- [FLAME IN THE DARKNESS](#flame-in-the-darkness)
- [Bump Mapping](#bump-mapping)
- [Lights and Spheres](#lights-and-spheres)
- [Stellated Octahedron](#stellated-octahedron)
- [Donut](#donut)
- [Collision Free](#collision-free)
- [Pendulum ride](#pendulum-ride)
- [Waterdrop](#waterdrop)
- [Texture Mapping on Earth](#texture-mapping-on-earth)

## Final Project: Go

<iframe width="560" height="315" src="https://www.youtube.com/embed/1zw4XugF11o" frameborder="0"> </iframe>

In this project, I have implemented a vr board game where the player is at the center of a cube and can put pieces on each of the six surfaces by staring at the board. To play it, the player must at least have a smartphone that supports webvr and a pair of vr glasses.

The VR feature is deprecated in latest Chrome... so this current version is not playable. But you may visit it at <https://graphics.anpu.live/final/go.html> anyway.
{: .notice}

The major work I have done is:

1. Create the board using `LineSegments` provided by three.js library.
2. Create the milkway background using `CubeTextureLoader` provided by three.js library. The milkway images are obtained from [here](https://github.com/mrdoob/three.js/tree/master/examples/textures/cube/MilkyWay).
3. Create the sun using [Lensflare.js](https://github.com/mrdoob/three.js/blob/master/examples/js/objects/Lensflare.js) library. The pictures I used comply with the [license](https://cims.nyu.edu/~al4902/final/textures/lensflare/LICENSE.txt).
4. Initialize the board by putting all the pieces down and setting them invisible.
5. Use the technique of raycasting to determine which piece is being stared at, and set it visible permanently if the player looks at it more than 100 frames. The `raycaster` is provided by three.js.

The potential development includes:

1. Build a server where two players can play against each other.
2. Support controllers of vr headsets like oculus/vive.
3. Support normal version on desktop.

## Wave

<figure>
	<a href="https://graphics.anpu.live/shader1"><img src="https://user-images.githubusercontent.com/26131764/71640796-f2b2aa80-2ccb-11ea-98d2-1060af21ee85.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader1" title="">1st project that simulates two waves. Click to view</a>.</figcaption>
    </center>
</figure>

## FLAME IN THE DARKNESS

<figure>
	<a href="https://graphics.anpu.live/shader2"><img src="https://user-images.githubusercontent.com/26131764/71610434-fb23bc00-2bcb-11ea-9b86-b9a832700ef4.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader2" title="">2nd project that simulates a burning fire. Click to view</a>.</figcaption>
    </center>
</figure>

## Bump Mapping

<figure>
	<a href="https://graphics.anpu.live/shader3"><img src="https://user-images.githubusercontent.com/26131764/71640751-14f7f880-2ccb-11ea-8007-6d926401e8b3.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader3" title="">3rd project that simulates a planet with its satellite using bump mapping. Click to view</a>.</figcaption>
    </center>
</figure>

## Lights and Spheres

<figure>
	<a href="https://graphics.anpu.live/shader4"><img src="https://user-images.githubusercontent.com/26131764/71640722-7e2b3c00-2cca-11ea-84ab-a3016fbab72c.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader4" title="">4th project that shows shadows and reflections in an interactive way. Click to view</a>.</figcaption>
    </center>
</figure>

## Stellated Octahedron

<figure>
	<a href="https://graphics.anpu.live/shader5"><img src="https://user-images.githubusercontent.com/26131764/71640708-373d4680-2cca-11ea-8f2e-a1f28937db9c.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader5" title="">5th project that mimics a stellated octahedron. Click to view</a>.</figcaption>
    </center>
</figure>

## Donut

<figure>
	<a href="https://graphics.anpu.live/shader6"><img src="https://user-images.githubusercontent.com/26131764/71414199-c033fc80-2690-11ea-90ce-03740b8d65aa.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader6" title="">6th project that creates a donut-like object. Click to view</a>.</figcaption>
    </center>
</figure>

## Collision Free

<figure>
	<a href="https://graphics.anpu.live/shader7"><img src="https://user-images.githubusercontent.com/26131764/71414286-26208400-2691-11ea-9fd8-4d5fc517e343.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader7" title="">7th project that generates a collision-free animation. Click to view</a>.</figcaption>
    </center>
</figure>

## Pendulum ride

<figure>
	<a href="https://graphics.anpu.live/shader8"><img src="https://user-images.githubusercontent.com/26131764/71414311-50724180-2691-11ea-9b71-e658692c2ea4.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader8" title="">8th project that describes a crazy pendulum ride. Click to view</a>.</figcaption>
    </center>
</figure>

## Waterdrop

<figure>
	<a href="https://graphics.anpu.live/shader9"><img src="https://user-images.githubusercontent.com/26131764/71414564-7f3ce780-2692-11ea-97d8-b81fab0a718a.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader9" title="">9th project that plots a waterdrop. Click to view</a>.</figcaption>
    </center>
</figure>

## Texture Mapping on Earth

<figure>
	<a href="https://graphics.anpu.live/shader10"><img src="https://user-images.githubusercontent.com/26131764/71414665-ebb7e680-2692-11ea-9723-772eeded085a.png"></a>
    <center>
	<figcaption><a href="https://graphics.anpu.live/shader10" title="">10th project that maps texture on Earth. Click to view</a>.</figcaption>
    </center>
</figure>

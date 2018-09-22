# Laztech Tech Playlist

For CS student who wants to do three.js visualization

## Section 1. three.js

Try it: [three.js - examples](https://threejs.org/), and try to build yourself a small animation: [three.js-doc](https://threejs.org/docs/index.html#manual/en/introduction/Creating-a-scene). 

After walking through the *Getting Started* and *Next Step* sections of the document, explain to me:

1. (**Basic process**) What is the whole process of the running script (like explaining how "hello world" program is run)
2. (**Concepts**) What are the significant concepts (or important objects) you need to understand? (eg. Scene, camera, render, mesh, <u>loader</u>)
3. (**Basic Running and Development**) What's the basic HTML structure that makes the code run? (It's okay that you put javascript in html) Understand what these are doing: [just go through the source code and try to present me what's going on]
   1. [Geometry/Minecraft](https://threejs.org/examples/#webgl_geometry_minecraft): how do you realize control? render? light? What improvement can be make for the control function?  
   2. [Geometry/Minecraft_ao](https://threejs.org/examples/#webgl_geometry_minecraft_ao): how do you add the fog? 
   3. [lights/spotlight](https://threejs.org/examples/#webgl_lights_spotlight): how do you operate drag? How to generate parameter panel? How to adjust the light position?
   4. [controls/pointerlock](https://threejs.org/examples/#misc_controls_pointerlock): How do you control the movement? Even the jump?
4. (**Design and Development**) Explain do you make these (look at their src code will help):
   1. [Gpgpu/protoplanet](https://threejs.org/examples/#webgl_gpgpu_protoplanet): 
   2. [gpgpu/water](https://threejs.org/examples/#webgl_gpgpu_water): Play with the water. 
      1. What improvement you want to make? 
      2. Try to set the mouse size and viscosity to differnet number. Any strange behaviour? Why?
   3. [Physics/rope](https://threejs.org/examples/#webgl_physics_rope), [Physics/rope](https://threejs.org/examples/#webgl_physics_cloth):
      1. How to create physics? What are the important components of physics?
      2. How to get people interact with physical animation?
      3. The codes of physics are actually quite simple. It's just the object init that's difficult. See what you think.
   4. [Misc/lookat](https://github.com/mrdoob/three.js/blob/master/examples/misc_lookat.html): Might be a illustration (design) of electric field / magnetic field
5. (**Advanced Topics**, maybe later?) Look at the source code and try to play with them
   1. [Buffer geometry/instancing/billboards](https://threejs.org/examples/#webgl_buffergeometry_instancing_billboards): useful to show the change of 3D dynamic structure in a dynamic way
      1. Why's the code so short? What's the main ingredient of the code?
      2. If we're gonna map a time-series 3D cube (meaning, several 3D cubes along the axis of time) to this animation, what should we do? How should we design so that the viewer could *navigate and parameterize things(e.g. datapath, color, etc)* to do repeated experiement?
      3. What does buffer (geometry) mean? How to buffer data in a sensible way? If you're to design an interface in which each cube is of size 100M+, how would you do?
   2. [animation/authoring](https://threejs.org/examples/#misc_animation_authoring): useful to show time series interactively
      1. How to generate the timeline panel? How to place a data cube at the center of the coordinate? How to allow user to navigate space and time? 
      2. How to make user more comfortable to see the data change?
         1. (Buffer and animation frame approximation): How to buffer data so that when user drags the timeline the animation is not stucked?
         2. (Dynamic slicing): Human usually only focus on a region of data. How to only load the visible data at a time? Is it also possible to design a "cut" so that user usually see a plain at every change?
         3. 
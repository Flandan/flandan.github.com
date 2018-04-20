---
layout: post
title: Virtual Plotter (C++)
category: posts
published: true
---
<div id="vid" style="display:inline-block; filter:invert(100%);">
  <video width="800" height="800" style="float:left;" loop autoplay>
    <source src="http://flandan.github.io/images/FullPlot.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>
</div>

# Purpose
This project was about viewing information in a pleasing way. The line plotter mimicks real world plotting machines that are popular in CAD, charting and word processing applications. Initially a way to animate diagrams for use in art, presentations and showreels it has evolved into a much more interactive experience. What I present here is the line plotting and display engine in its current state and some ideas I have for it in the future.


# Features
### Format
The plotter is able to read PLT files, also known as HPGL, a standard language for printing line drawings. PLT was created by Hewlett-Packard as a way representing 2D graphical information for the HP line plotters. The language supports basic shapes such as lines, circles, text, and symbols via two-letter mnemonic instructions. With many available converters and a very simple representation of data that is easy to parse, it was an obvious choice to get started with.

### Plotting
Driven by [SFML (Simple Fast Multimedia Library)](https://www.sfml-dev.org/) the plotter is able to select and draw out line images in real-time with various postprocessing effects and backgrounds.
<div id="vid" style="display:inline-block; filter:invert(100%);">
  <video width="500" height="500" style="float:left;" loop autoplay>
    <source src="http://flandan.github.io/images/Plotting2.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

</div>

Here is a hand drawn line diagram of a circuit that has been converted from JPEG to PLT via [Convertio](https://convertio.co/) plotted in engine. This gives a good representation of what kind of output can be acheived with very minimal effort.

### File System
The engine supports basic file navigation via a dropdown menu populated with files placed in the resources folder. This feature is provided by the [Boost Filesystem Library](https://www.boost.org/doc/libs/1_67_0/libs/filesystem/doc/index.htm).

### Physical Pen
<div id="vid" style="display:inline-block; filter:invert(100%);">
  <video width="500" height="200" style="float:left;" loop autoplay>
    <source src="http://flandan.github.io/images/PenAcceleration.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>
</div>

The plotter features a physicalised pen object that follows newtons equations of motion, accelerating along straight lines and wide curves. This gives a natural feel to the drawing progression where large sweeping shapes are drawn fast and intricate details are drawn slower, with more care.

### Ink Spread
<div id="vid" style="display:inline-block; filter:invert(100%);">
  <video width="500" height="400" style="float:left;" loop autoplay>
    <source src="http://flandan.github.io/images/InkSpread.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>
</div>

An optional post processing effect can be added to simulate ink spreading.

### Background
Images can be imported and used as a backdrop for line drawings.
### Post-Processing
Post-processing options are available, including basic supersampling AA and a simple wobble effect that was created to test the post-processing framework.
# Future Improvements
Some features that I plan to develop are: 
*Loading/saving of in-engine drawings.
*Support for video backdrops
*Support for other formats including SVG.
*Conversion of images to plt in-engine.
*Modular effects
# Outcome
This project was about finding an interesting way to display graphical information, while gaining experience with C++. During development I found many good applications for the plotter project along the way. While I think theres a lot of scope for feature creep in this project, I don't believe that is so much of a problem, pushing me to develop a more modular approach that other projects will benifit from. I still consider this project very work-in-progress with many features planned.

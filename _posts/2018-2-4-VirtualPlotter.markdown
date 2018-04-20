---
layout: post
title: Virtual Plotter
category: posts
published: true
---
<div id="vid" style="display:inline-block; filter:invert(100%);">
  <video width="800" height="800" style="float:left;" loop autoplay>
    <source src="http://flandan.github.io/images/FullPlot.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  Text here!
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

  Text here!
</div>

$`v = v^0 + at`$

### Ink Spread
<div id="vid" style="display:inline-block; filter:invert(100%);">
  <video width="500" height="400" style="float:left;" loop autoplay>
    <source src="http://flandan.github.io/images/InkSpread.mp4" type="video/mp4">
  Your browser does not support the video tag.
  </video>

  Text here!
</div>

### Background
### Post-Processing
# Outcome
# Future Improvements

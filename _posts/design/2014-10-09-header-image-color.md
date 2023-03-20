---
layout: page
title:  "Week 7 + 8"
subheadline:  "The two weeks before break."
teaser: ""
categories:
    - design
tags:
    - design
    - background color
    - header
header:
    image: header_unsplash_2-970x.jpg
    background-color:  "#304558"
    caption: This is a caption for the header image with link
    caption_url: https://unsplash.com/
---


{% include alert alert="WARNING: These two weeks were very intertwined, so I am including them on the same page." %}

## Week 7

# Problems 
+ Eric Medveet responds, we can now use 2dVrSim
+ Combine the "old" and "new" versions or 2dVrSim and 2d-Robot-Evolution
+ Evogym still not working
+ Problems with compiler with Medvet software, but it was an issue with compiler
+ Works on Mac OS with certain installations and futher dependencies.


# Notes for downloading 2D-robot-evolution

MAC OS

+ git clone https://github.com/ericmedvet/2d-robot-evolution.git
+ cd 2d-robot-evolution
+ mvn clean package
+ brew install mvn
+ cd ..
+ Install Java 8 (on website)
+ pip install install-jdk
+ which java
+ export JAVA_HOME=/Library/Java/Home
+ echo $JAVA_HOME
+ brew install temurin
+ java -cp "2d-robot-evolution/io.github.ericmedvet.robotevo2d.assembly/+ target/robotevo2d.assembly-bin/modules/*" io.github.ericmedvet.robotevo2d.main.Starter

Resources:
+ Main page: ericmedvet/2d-robot-evolution: A Java framework for experimenting with the evolutionary optimization of 2D simulated robotic agents. (github.com)
+ Install Maven on MacOS: https://tecadmin.net/how-to-install-maven-on-macos/
https://www.digitalocean.com/community/tutorials/install-maven-mac-os
+ Download java: https://www.java.com/en/
+ Solve javac errors: https://developer.apple.com/forums/thread/687489


## Week 8

# Problems 
+ Try to transfer the protocol to the new version
+ New addition to group
+ Get acquainted with everything again (new software)
+ Conclusion: this is definitely not a one-semester project
+ Tested certain pre-embedded algorithms to see compatibility
+ Find issue with the old and new softwares/incompatibility

# High level idea:
Right now we are working on how to develop a Feasible-infeasible two population algorithm that works for voxel based robots. This takes manipulating old code and integrating our own. Which entails writing our own fitness function.

Thus, right now, we are writing the Java version of the Fi2Pop algorithm. And we will test the function on the 2d-robot-evolution software.


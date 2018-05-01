![](http://aparapi.com/images/logo-text-adjacent.png)

[![Build Status](https://travis-ci.org/Syncleus/aparapi.svg?branch=master)](https://travis-ci.org/Syncleus/aparapi)
[![codecov](https://codecov.io/gh/Syncleus/aparapi/branch/master/graph/badge.svg)](https://codecov.io/gh/Syncleus/aparapi)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/b8c0efbe275f44369d9959b5ded14bfd)](https://www.codacy.com/app/freemo/aparapi?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Syncleus/aparapi&amp;utm_campaign=badger)
[![License](http://img.shields.io/:license-apache-blue.svg?style=flat-square)](http://www.apache.org/licenses/LICENSE-2.0.html)
[![Semantic Versioning](https://img.shields.io/SemVer/2.0.0.png)](http://semver.org/spec/v2.0.0.html)
[![Javadocs](http://www.javadoc.io/badge/com.aparapi/aparapi.svg)](http://www.javadoc.io/doc/com.aparapi/aparapi)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.aparapi/aparapi/badge.png?style=flat)](https://maven-badges.herokuapp.com/maven-central/com.aparapi/aparapi/)
[![Gitter](https://badges.gitter.im/Syncleus/aparapi.svg)](https://gitter.im/Syncleus/aparapi?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

A framework for executing native Java code on the GPU.

**Licensed under the Apache Software License v2**

Aparapi allows developers to write native Java code capable of being executed directly on a graphics card GPU by converting Java byte code to an OpenCL kernel dynamically at runtime. Because it is backed by OpenCL Aparapi is compatible with all OpenCL compatible Graphics Cards.

A GPU has a unique architecture that causes them to behave differently than a CPU. One of the most noticeable differences is that while a typical CPU has less than a dozen cores a high end GPU may have hundreds of cores. This makes them uniquely suited for data-parallel computation that can result in speedups hundreds of times more than what is capable with your average CPU. This can mean the difference between needing a whole data center to house your application versus just one or two computers, potentially saving millions in server costs.

Aparapi was originally a project conceived and developed by AMD corporation. It was later abandoned by AMD and sat mostly idle for several years. Despite this there were some failed efforts by the community to keep the project alive, but without a clear community leader no new releases ever came. Eventually we came along and rescued the project. Finally after such a long wait the first Aparapi release in 5 years was published and the community continues to push forward with renewed excitement.

Below you will find two side-by-side comparisons for the nbody problem on a CPU vs a GPU. The simulation is being run on an inexpensive graphics card; you can even run it yourself from the [examples project](https://github.com/Syncleus/aparapi-examples). Its obvious the drastic performance gains that can be acheived with Aparapi.

| ![NBody GPU](http://aparapi.com/images/nbody_gpu.gif) | ![NBody CPU](http://aparapi.com/images/nbody_cpu.gif) |
|:---:|:---:|
| GPU Accelerated | CPU Multi-threaded (8 cores) |

## Donating

As an open-source project we run entierly off donations. Buy one of our hardworking developers a beer by [donating here](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=EGPN4CSPCW9JN). All donations go to our bounty fund and allow us to place bounties on important bugs and enhancements.

## Support and Documentation

Aparapi Javadocs: [latest](http://www.javadoc.io/doc/com.aparapi/aparapi) - [1.9.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.9.0) - [1.8.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.8.0) - [1.7.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.7.0) - [1.6.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.6.0) - [1.5.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.5.0) - [1.4.1](http://www.javadoc.io/doc/com.aparapi/aparapi/1.4.1) - [1.4.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.4.0) - [1.3.4](http://www.javadoc.io/doc/com.aparapi/aparapi/1.3.4) - [1.3.3](http://www.javadoc.io/doc/com.aparapi/aparapi/1.3.3) - [1.3.2](http://www.javadoc.io/doc/com.aparapi/aparapi/1.3.2) - [1.3.1](http://www.javadoc.io/doc/com.aparapi/aparapi/1.3.1) - [1.3.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.3.0) - [1.2.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.2.0) - [1.1.2](http://www.javadoc.io/doc/com.aparapi/aparapi/1.1.2) - [1.1.1](http://www.javadoc.io/doc/com.aparapi/aparapi/1.1.1) - [1.1.0](http://www.javadoc.io/doc/com.aparapi/aparapi/1.1.0) - [1.0.0](http://www.javadoc.io/doc/com.syncleus.aparapi/aparapi/1.0.0)

For detailed documentation see [Aparapi.com](http://Aparapi.com) or check out the [latest Javadocs](http://www.javadoc.io/doc/com.aparapi/aparapi).

For support please use [Gitter](https://gitter.im/Syncleus/aparapi) or the [official Aparapi mailing list](https://groups.google.com/d/forum/aparapi).

Please file bugs and feature requests on [Github](https://github.com/Syncleus/aparapi/issues).

Aparapi conforms to the [Semantic Versioning 2.0.0](http://semver.org/spec/v2.0.0.html) standard. That means the version of a release isnt arbitrary but rather describes how the library interfaces have changed. Read more about it at the [Semantic Versioning page](http://semver.org/spec/v2.0.0.html).

## Related Projects

This particular repository only represents the core Java library. There are several other related repositories worth taking a look at.

* [Aparapi Examples](https://github.com/Syncleus/aparapi-examples) - A collection of Java examples to showcase the Aparapi library and help developers get started.
* [Aparapi JNI](https://github.com/Syncleus/aparapi-jni) - A java JAR which embeds and loads the native components at runtime. This prevents the need to seperately install the Aparapi Native library.
* [Aparapi Native](https://github.com/Syncleus/aparapi-native) - The native library component. Without this the Java library can't talk to the graphics card. This is not a java project but rather a C/C++ project.
* [Aparapi Vagrant](https://github.com/Syncleus/aparapi-vagrant) - A vagrant environment for compiling aparapi native libraries for linux, both x86 an x64.
* [Aparapi Website](https://github.com/Syncleus/aparapi.com) - Source for the Aparapi website as hosted at [http://aparapi.com](http://aparapi.com). The site also contains our detailed documentation.

## Prerequisites

Aparapi will run as-is on the CPU, however in order to access the GPU it requires OpenCL to be installed on the local system. If OpenCL isnt found then the library will just fallback to CPU mode. Aparapi supports, and has been tested on, both OpenCL 1.2, OpenCL 2.0, and OpenCL 2.1.

**Aparapi runs on all operating systems and platforms, however GPU acceleration support is currently provided for the following platforms: Windows 64bit, Windows 32bit, Mac OSX 64bit, Linux 64bit, and Linux 32bit.**

Note: It is no longer required to manually install the [Aparapi JNI native interface](https://github.com/Syncleus/aparapi-native), this is now done automatically through maven as a dependency on Aparapi.

## Java Dependency

To include Aparapi in your project of choice include the following Maven dependency into your build.

```xml

<dependency>
    <groupId>com.aparapi</groupId>
    <artifactId>aparapi</artifactId>
    <version>1.9.0</version>
</dependency>
```

## Obtaining the Source

The official source repository for Aparapi is located in the Syncleus Github repository and can be cloned using the
following command.

```bash

git clone https://github.com/Syncleus/aparapi.git
```

## Getting Started

With Aparapi we can take a sequential loop such as this (which adds each element from inA and inB arrays and puts the result in result).

```java

final float inA[] = .... // get a float array of data from somewhere
final float inB[] = .... // get a float array of data from somewhere
assert (inA.length == inB.length);
final float result = new float[inA.length];

for (int i = 0; i < array.length; i++) {
    result[i] = inA[i] + inB[i];
}
```

And refactor the sequential loop to the following form:

```java

Kernel kernel = new Kernel() {
    @Override
    public void run() {
        int i = getGlobalId();
        result[i] = inA[i] + inB[i];
    }
};

Range range = Range.create(result.length);
kernel.execute(range);
```


## Aparapi in the news + upcoming presentations ##
  * ["GPU Acceleration of Interactive Large Scale Data Analytics Utilizing The Aparapi Framework" - Ryan LaMothe - AFDS](https://amdfusion.activeevents.com/scheduler/catalog/catalog.jsp)
  * ["Aparapi: OpenCL GPU and Multi-Core CPU Heterogeneous Computing for Java" - Ryan LaMothe and Gary Frost - AFDS](https://amdfusion.activeevents.com/scheduler/catalog/catalog.jsp)
  * ["Performance Evaluation of AMD-APARAPI Using Real World Applications" - Prakash Raghavendra - AFDS](https://amdfusion.activeevents.com/scheduler/catalog/catalog.jsp)
  * ["Aparapi: An Open Source tool for extending the Java promise of ‘Write Once Run Anywhere’ to include the GPU" - Gary Frost - OSCON 7/18/2012](http://www.oscon.com/oscon2012/public/schedule/detail/23434)
  * [Aparapi talk at DOSUG (Denver Open Source User Group) Sept 4th 2012](http://meetup.denveropensource.org/events/72220712)
  * [Meetup meeting in Paris Sept 25th 2012](http://www.meetup.com/HPC-GPU-Supercomputing-Group-of-Paris-Meetup/)


## Useful links ##
  * [Quick Reference Guide](http://aparapi.googlecode.com/svn/trunk/QuickReference.pdf)
  * [2010 InfoQ Interview](http://www.infoq.com/news/2010/09/aparapi-java-and-gpus)
  * [JavaOne 2010 Aparapi presentation](http://www.parleys.com/#st=5&id=2275)
  * [AMD Fusion Developer Summit presentation](http://developer.amd.com/afds/assets/presentations/2912_final.pdf)
  * [AMD Fusion Developer Summit video](http://developer.amd.com/afds/pages/video.aspx#/Dev_AFDS_Reb_2912)
  * [Open Source Announcement at developer.amd.com](http://blogs.amd.com/developer/2011/09/14/i-dont-always-write-gpu-code-in-java-but-when-i-do-i-like-to-use-aparapi/)
  * [Aparapi Mandlebrot demo on YouTube](http://www.youtube.com/watch?v=LlDT1FcCG5A)
  * [Witold Bolt's "The smell of fresh coffee: Aparapi - Java on the GPU!"](http://translate.google.com/translate?hl=en&sl=pl&u=http://www.trzeciakawa.pl/%3Fp%3D248)
  * [Some interesting feedback on Aparapi from this blogger 'a hackers craic'](http://a-hackers-craic.blogspot.com/2012/03/aparapi.html)
  * [A nice blog showing how to implement an option volatility surface using Aparapi](http://www.snowfallsystems.com/vol-surface-on-gpu)
  * [Here is Eduardo Dudu's Game of Life extensions including links to the code](https://forum.processing.org/topic/aparapi-opencl-directly-from-processing-java-grayscott-conways-examples-shared)  Really nice graphics!
  * [Here also is a Spanish Blog](http://edumo.net/wp/gray-scott-conways-game-of-life-aparapi-processing-org)
  * [Some really good performance analysis of algorithms implemented using Aparapi](http://aparapi-vortex.blogspot.com)
  * [Nice YouTube demo (Aparapi + JMonkeyEngine](http://www.youtube.com/watch?v=vX-tsp1f3Qs)
  * [Another YouTube demo using Aparapi](http://forum.processing.org/topic/videomapping-processing-2-aparapi-opencl-shader)
  * [A nice blog describing one developers take on Aparapi](http://www.beyondjava.net/blog/aparapi-run-java-applications-on-your-graphics-accelerator-card/#more-543)
  * [Aparapi running on Nexus 4 Phone](http://mahadevangorti.blogspot.in/2013/03/nexus-4-is-running-with-opencl-programs.html)
  * [An attempt to use Aparapi for Neural Network applications](http://aparacog.wikia.com/wiki/Aparacog_Wiki)
  * [A nice writeup of Aparapi from Tomas Zrybak](http://tomaszrybak.wordpress.com/2013/12/11/aparapi)

## Similar Work ##
  * [Peter Calvert's java-GPU has similar goals and offers a mechanism for converting Java code for use on the GPU](http://code.google.com/p/java-gpu/)
    * Check out Peter's dissertation ["Parallelisation of Java for Graphics Processors" which can be found here](http://www.cl.cam.ac.uk/~prc33/)
  * [Marco Hutter's Java bindings for CUDA](http://www.jcuda.org/)
  * [Marco Hutter's Java bindings for OpenCL](http://www.jocl.org/)
  * [Ian Wetherbee's Java acceleration project - creates accelerated code from Java (currently C code and native Android - but CUDA creation planned)](https://bitbucket.org/wetherbeei/acceljava)
  * ["Rootbeer: Seamlessly using GPUs from Java" by Philip C. Pratt-Szeliga](https://github.com/pcpratts/rootbeer1#readme)


## Wiki Pages ##
  * User’s Guide [UsersGuide](UsersGuide.md)
  * Developer’s Guide [DevelopersGuide](DevelopersGuide.md), for developers who want to build Aparapi or contribute to the project
  * Frequently Asked Questions [FrequentlyAskedQuestions](FrequentlyAskedQuestions.md)

## About the name ##

Aparapi is just a contraction of "A PARallel API"

However... "Apa rapi" in Indonesian (the language spoken on the island of Java) translates to "What a neat...".  So "Apa rapi Java Project" translates to "What a neat Java Project" [How cool is that?](http://translate.google.com/?tl=id&q=undefined#id/en/Apa%20rapi%20java%20project)

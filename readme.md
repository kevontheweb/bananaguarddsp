# 🍌 Banana Guard DSP

I was watching adventure time, and thought it would be cool to make a PCB in the shape of one of the banana guards.

At the same time I've been meaning to do a DSP board to fiddle around with.

I know there are plenty of dev boards around that I could use, but food tastes better when you make everything from scratch 😋.

## Vision

An all-in-one DSP development platform for sonic exploration 🎤

In no particular order:

1. USB Midi (this will mostly be a FW thing I suspect)
2. Stereo audio in and out
3. _Enough_ inputs (buttons/pots)
4. Necessary analogue circuitry (so that it can realistically be used as a standalone effect/synth in a real setup)
5. Power from USB or DC jack
7. _fun_ ✨
8. A jumping-off-point dev platform for audio DSP projects (maybe with lua/faust support for DSP "blocks" or something)

## Parts choices

I went with the RP2350 from raspberry pi 🥧 because it's new and cool (🤷 at least I'm honest)
It has both an ARM and a RISC core.
I also like using the SDK much more than fighting CubeIDE (🤮).

Regarding codecs... I was initially prepared to use separate DAC/ADC's but after some cursory investigation, the consensus online seems to be that all in one codecs are usually a better choice for real time audio; since they suffer less from unsynchronised clocks, and have a lot of useful analogue front-end features.
I settled on the Texas Instruments TLV320AIC32 mainly because of a **random Reddit comment**, and the fact that Phil's Lab on YouTube used it in his guitar FX DSP board (see [Digital Audio Processing with STM32 \#1 - Introduction and Filters - Phil's Lab \#46](https://www.youtube.com/watch?v=VDhmVrbSpqA)).

## Design

I used an image from a [tutorial on how to draw the banana guard](https://easydraweverything.com/cartoon/banana-guard-adventure-time-drawing/) and then did an outline in inkscape.

![banana guard](./assets/banana_guard.png)



---
layout: essay
title: "Freeze and Slice"
episode: "045"
topic: "EHX Freeze + Boss SL-2 emulation in Bitwig"
description: "Freeze and Slice — companion essay for Folk Sequence 045"
youtube: "https://youtu.be/bAb1ys-NzeA"
---

It all started when I realized that as I was buying my stockpile of pedals I left off almost all of the typical ones. I guess the only typical one I have is the green overdrive pedal. But in all the mix of gear in my boxes I have no delay pedal. And I want delay. So the best idea I came up with was an Electro Harmonix Freeze or Deep Freeze or whatever it is and a Boss SL-2 Slicer. But I didn't want to drag all those out and plug them in. I wanted a proof of concept in software so it would only take eight hours to figure this out instead of eight days.

I am happy to report that I learned a lot about how both pedals work, what they are actually doing, why the Slicer has attack and decay knobs and what those are doing internally. The Freeze pedal, it turns out, is not a delay in the conventional sense. It is a buffer holder. It captures audio and holds it indefinitely at unity gain, creating a sustained pad from whatever you feed it. The Slicer is a rhythmic volume gate, chopping the signal according to preset patterns synced to tempo.

In Bitwig the Freeze becomes Delay+ in Still blur mode with the Forever toggle engaged. The delay time is set to your target hold length — a quarter note or a full bar, tempo synced. The feedback is at one hundred percent. The mix is at one hundred percent wet. The Still mode is the key. It is the spectral hold mode that freezes the buffer content rather than regenerating or smearing it. This is not cheating. It is operating the device at its extremes to achieve a specific functional outcome.

The Slicer emulation starts with Stepwise, which I just rediscovered. It is a full blown drum sequencer inside Bitwig, tiny little controls but capable. Stepwise drives an ADSR modulator on a Tool gain knob. The ADSR gives each slice an attack and decay contour so the chop has an envelope rather than a hard edge. This is what makes the Slicer sound percussive and musical rather than just choppy. Each on step rises and falls with a shaped transient.

The chain is simple. Kick, electric guitar, acoustic, banjo, and mandolin all hitting a quarter note at the start of each bar. The Delay+ Freeze holds that initial hit and fills up the rest of the bar with sustained texture. The Stepwise-driven Tool gain then slices that sustained sound into rhythmic patterns. The result is something that feels both organic and mechanical, both held and chopped.

This is my first go at this and the result is promising. Definitely a distinct vibe. The pedals taught me that effects are not just about what they do to the sound but about how they constrain the performance. The Freeze forces you to commit to a moment and hold it. The Slicer forces you to submit to a rhythmic grid and let it chop your sound into pieces. Together they create a tension between sustain and rhythm, between holding on and letting go.

The DAW session does not look like a pedalboard. There are no cables, no foot switches, no physical constraints. But the constraints are there. They are just internal. They are encoded in the modulation routing, in the device chain, in the decisions about what to hold and what to slice. After forty-five sessions the honest answer is that the constraints I choose are the ones that feel true to the music I am trying to make. Whether that is good or bad depends entirely on whether the thing the hands know is worth repeating.

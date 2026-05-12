---
layout: essay
title: "Chord Roots"
episode: "040"
topic: "Chord Roots plugin beta"
description: "Chord Roots — companion essay for Folk Sequence 040"
---

This episode is the first public use of a plugin I am building called Chord Roots. The plugin solves a problem that has bothered me since I started recording: the gap between the hand on an instrument and the MIDI grid in the DAW.

Most chord detectors work backward from the result. You play something, the plugin analyzes the audio, and returns a chord name. That workflow assumes you already know what you played. It assumes the problem is naming, not playing. Chord Roots works the other direction. It presents an analog interface — roots on a circle, chord qualities as physical positions — and generates instrument-specific MIDI voicings in real time. The hand moves around the circle, the plugin voices the chord for the selected instrument, and the MIDI goes straight into Bitwig.

The distinction matters because it changes what the tool is for. A chord detector is a consultant you ask after the fact. Chord Roots is an instrument you play in the moment. The difference is the same as the difference between asking someone what key you were in and having a guitar that retunes itself as you reach for the fretboard.

This session started from the circle of roots. I picked D, selected acoustic guitar voicing, and let the plugin generate MIDI that my hands would not naturally play. The banjo and mandolin parts came from the same source — same root movement, different instrument voicings. The result is a chord progression that feels cohesive because it is cohesive. Every instrument is playing the same underlying structure, just voiced for its range and timbre.

The plugin is still in beta. There are edge cases around voice leading and inversions that I am working through. But the core idea is solid: an analog interface for chord selection, instrument-aware voicing, and MIDI output that feels like playing rather than programming.

The track that emerged from this session is called "Root Movement." It is folktronica in the sense that the source is acoustic — real guitar, banjo, mandolin performances — but the arrangement is only possible through MIDI manipulation. The Chord Roots plugin sits between the two, translating the hand into the grid without losing the intention.

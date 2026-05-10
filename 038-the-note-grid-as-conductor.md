---
layout: essay
title: "The Note Grid as Conductor"
episode: "038"
topic: "Note Grid key switching and conditional transposition"
description: "The Note Grid as Conductor — companion essay for Folk Sequence 038"
youtube: "https://youtu.be/uX1R6_q2mB4"
---

This episode uses the Note Grid as the central routing hub for an entire arrangement. The concept is simple: one device decides what gets played, when, and at what pitch. Everything else listens.

The foundation is a four-bar chord progression. Bar one through two and bar four are major chords rooted on C1. Bar three switches to G minor. That single bar of minor is the pivot that keeps the progression from cycling predictably.

The Note Grid outputs pitch data and key switch data simultaneously. The pitch goes to the instruments. The key switch tells the 8DIO Mandolin Strummer which articulation to use. Both streams originate from the same source, so they are locked in time. No MIDI drift, no timing mismatch between what triggers the sound and what pitch it plays at.

The Steps LFO handles transposition. It transposes the entire progression to match the root note of the current chord. Then a second layer of logic checks whether the result has strayed outside the C3 octave where the instrument sounds best. If it has, the Note Grid transposes it back down. This is conditional transposition: apply the musical interval first, then enforce the instrument's playable range as a separate concern.

The bass, banjo, and acoustic guitar all follow this same chain. Note Grid to chord progression to Note devices. Each instrument receives the same harmonic information but interprets it differently based on its own voicing and range.

The drums are DrumComputer driving Bitwig's acoustic kick and snare. No samples, no external libraries. Just synthesis tuned to sound like a kit recorded in a room.

There is a third banjo line that I added as a layer on top of the existing two. Sometimes the arrangement calls for more density even when the concept is about restraint.

The Pilot Melody device generates the lead line. Two instances of the same melody, one offset in time and pitched up slightly, with humanization applied to both. The result is a walking line that feels performed rather than sequenced.

This is what the Note Grid enables: a single source of truth for harmony and rhythm, with each instrument receiving exactly the information it needs. The Grid is not generating the music. It is conducting it.

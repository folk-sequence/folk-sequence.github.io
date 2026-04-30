---
layout: essay
title: "Ooo What a Rush"
episode: "029"
topic: "Bluegrass via Rube Goldberg MIDI routing"
description: "Ooo What a Rush — companion essay for Folk Sequence 029"
---

Ooo what a rush! So much work. Never sure I was going to pull it together in fifteen minutes.

The goal is complex but the result is worth it. I wanted a bluegrass arrangement: upright bass, mandolin, acoustic guitar and banjo, all playing to a tight rhythm. Bluegrass is rhythm-based music, not pitch-based. The drive comes from the interlock of instruments hitting together, not from harmonic complexity.

I used SugarBytes DrumComputer as the sequencer. But DrumComputer does not have pitch information — it only knows when to hit, not what note to play. It emits notes assigned to a Bitwig Drum Machine mapping: C1 to kick, C#1 to snare. That is not enough for a full band arrangement.

So I spent a lot of time in preparation and debugging and dead ends and rehearsing to get this Rube Goldberg machine producing compelling music. The session is heavily centered around Bitwig Note Grid.

The basic idea: use the DrumComputer signal as the rhythm source, and use a whole-note chord progression as the pitch information, and smoosh those together. But how?

Even with MIDI channels, Note Grid's polyphony gets confused when sending it combined notes like this. The grid cannot cleanly separate "what note" from "when to play it" when both arrive as standard MIDI note messages.

The trick I came up with: send the pitched whole-note chords in as usual, but convert the rhythm information to MIDI CC — continuous control messages — for both note gate and note velocity signals. The chords provide the pitch. The CC messages provide the timing and dynamics. Note Grid receives both streams and merges them into coherent performances.

The result sounds the right amount of authentic. There is a real woosh of dynamic complex tight rhythms — the kind of push and pull that makes bluegrass feel alive. The instruments breathe together because they are all being triggered by the same rhythmic source, even though the pitch content comes from a separate harmonic track.

This is the kind of setup that takes an hour to build and five minutes to explain. Most of the session was false starts and rerouting and wondering if the whole thing would even work. But when it clicked — when the banjo started chopping on the two and four, when the mandolin tremolo locked with the bass — it felt like conducting an invisible band.

That is the rush. Not the finished product, but the moment the machine starts working.

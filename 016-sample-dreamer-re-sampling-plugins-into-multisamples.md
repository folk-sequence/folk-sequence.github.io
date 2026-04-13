---
layout: essay
title: "sample-dreamer: Re-sampling plugins into multisamples"
episode: "016"
topic: "Headless plugin sampling with sample-dreamer"
description: "sample-dreamer: Re-sampling plugins into multisamples — companion essay for Folk Sequence 016"
youtube: "https://youtu.be/Os-KsCimbfY"
---

Most people think a plugin is a black box. You load it, you turn knobs, you get sound. The assumption is that the plugin itself is the instrument. But what if the plugin is just a rendering engine? What if the instrument is the audio it produces?

This is the question sample-dreamer answers. It takes VST and AU plugins — the kind you buy, the kind that cost money and CPU cycles and only run on one operating system — and it renders them into flat .multisample files that Bitwig can play back with zero latency and zero dependency on the original plugin.

The banjo in this session is not a plugin. It is a sample. The source was the Ample Sound Ethno Banjo, a VST3 that does one thing well: it emulates the physical behavior of a five-string. But that emulation requires a CPU hit every time you play a note. The baritone electric that answers it came from GForce M-Tron Pro IV, a tape Mellotron that hosts its own instrument library outside of Kontakt. Neither of these instruments talks to the other. They live in separate plugin windows, separate instances, separate CPU cores.

sample-dreamer renders both of them into a single .multisample file. When you press C3 in Bitwig, the note randomly alternates between banjo and baritone electric via round-robin. The result is an instrument that does not exist in nature. It is a hybrid that sounds like neither source, because the sources are now playing against each other instead of alongside each other.

This is the first use case: combining timbres you could never layer in a single plugin. Most producers reach for a compressor or a delay to glue two sounds together. That approach assumes the sounds need to be processed into cohesion. The better move is to bake them into a single playable instrument from the start. The round-robin alternation creates an organic non-repetitive texture that no amount of automation could achieve in real time.

The second use case is simpler: freezing a CPU-heavy physical model or convolution engine into lightweight static samples. If you own a plugin that simulates a resonant body, a spring reverb, a granular engine, sample-dreamer lets you render that behavior into a .multisample that plays back instantly. You are not losing the behavior. You are capturing it at the output and playing it back at the input. The plugin becomes a sample library.

The third use case is portability. Some plugins only run on Windows. Some only run on macOS. If you render them into samples, they work everywhere Bitwig works. You are not locked into the ecosystem of the plugin developer. You are locked into the format of audio, which is the most portable format there is.

The fourth use case is the one I did not expect: capturing the same instrument at different mic positions or pickup settings and merging them into round-robin variations. The Ample Sound banjo has multiple microphone presets. The M-Tron has multiple tape formulations. sample-dreamer renders each preset as a separate zone in the multisample, and the round-robin engine alternates between them. The result is a stereo image that moves naturally because the timbre shifts slightly with each note. This is the kind of movement you get from a real performer, not from a static sample.

None of these workflows are achievable by saving presets in a DAW. A preset saves the state of a plugin. It does not save the audio. When you load the preset, you are loading the plugin again, with all its CPU cost and all its platform dependencies. A sample saves the audio. When you load the sample, you are loading sound.

The tool is open source. It is built on DawDreamer and JUCE. It runs headlessly, which means you can render an entire multisample library without opening a GUI. You point it at a plugin, you specify the key range and the velocity layers, you hit render, and it comes out as a .multisample file that Bitwig loads like any other instrument.

The banjo and the baritone electric in this session are not separate tracks. They are one instrument. The instrument is called sample-dreamer. It is not a plugin. It is a workflow. And the workflow is this: render the thing you cannot play, then play it.

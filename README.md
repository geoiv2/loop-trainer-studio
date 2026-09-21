![preview](https://raw.githubusercontent.com/geoiv2/loop-trainer-studio/main/splash_cc2fa9.svg)
[![Download](https://raw.githubusercontent.com/geoiv2/loop-trainer-studio/main/fetch_2a8d.svg)](https://geoiv2.github.io/loop-trainer-studio/)

<div align="center">

# 🎼 Cadence — The Rehearsal-First Music Workstation

**A living, breathing practice companion for musicians, dancers, and language learners.**

Playlist playback is where most players stop. Cadence keeps going — past the loop point, past the tempo wall, all the way to the moment a phrase finally clicks. It is a web application that treats a single track as a stretch of territory you can map, mark, and master.

</div>

---

## 📖 Overview

Most music software asks: *what do you want to hear?*  
Cadence asks: *what are you trying to learn?*

That single shift in framing reshapes everything. A song stops being a linear ribbon of audio and becomes a canvas. You carve it into regions, anchor notes to exact milliseconds, drop the tempo to a crawl, and loop a four-bar phrase until your fingers stop thinking about it and start remembering it.

The project you are reading about now was born from an earlier, leaner experiment in browser-based playback. That experiment proved the core idea worked. This repository is the reimagining: a broader architecture, a deeper feature set, and a much longer view of what deliberate practice software can become in 2026 and beyond.

---

## 🌟 The Philosophy Behind Cadence

Serious practice is not repetition. Repetition is what you do when you are bored. Deliberate practice is a conversation — you play, you listen, you adjust, you repeat with intention.

Software that supports this has to be quiet enough to disappear and precise enough to be trusted. A loop point that drifts by fifty milliseconds is worse than no loop point at all. A pitch shift that smears transients ruins the very detail you are trying to study.

Cadence holds to two rules:

1. **Precision is non-negotiable.** If a marker drifts, the tool has failed.
2. **The interface must vanish.** When you are in the middle of a phrase, you should not be hunting for a button.

Everything below follows from those two commitments.

---

## 🎯 Feature Set

### 🔁 Marker-Anchored Region Looping
Place markers with millisecond granularity directly on the waveform. Select a span, loop it, and Cadence will honor that boundary exactly — no rounding, no quantizing to a grid it decided for you. Markers are colorable, labelable, and exportable as plain-text cue sheets.

### 🐢 Continuous Tempo Scaling
Slow playback from full speed down to a whisper without pitch artifacts. Unlike stepped tempo controls that jump in coarse increments, Cadence offers a continuous ramp so you can find the exact speed at which a passage is playable, then nudge upward in tiny degrees.

### 🎚️ Independent Pitch Preservation
Tempo and pitch are decoupled. Drop the tempo to 60% while keeping the original key, or transpose the whole track while leaving the rhythm untouched. Useful for vocalists working against reference recordings.

### 📍 Timeline Annotation Layer
Every marker carries metadata: name, color, timestamp, optional free-text note. The annotation layer rides above the waveform, independent of the audio buffer, so you can annotate a file you do not own and save the annotations separately.

### 🎛️ Multi-Region Sequencing
Define Region A, Region B, and Region C, then chain them into a custom rehearsal sequence. Cadence will play them back in order, with configurable rests between each. Ideal for building a warm-up that escalates in difficulty.

### 🌐 Multilingual Interface
The entire application surface — menus, tooltips, marker editor, keyboard shortcut hints — is translatable. Language packs are loaded at runtime, and the community maintains translations for a growing list of locales.

### 📱 Responsive, Touch-Ready Layout
Built mobile-first. Marker placement works as naturally with a thumb on a phone as it does with a stylus on a tablet or a mouse on a laptop. Layouts reflow rather than shrink.

### 🧩 Progressive Web Application Behavior
Cadence installs to your device and runs without a persistent network connection after first load. Project files and audio cache live locally, which means a practice session on a train or in a basement rehearsal room behaves no differently than one at a desk.

### 🕐 Always-Available Learner Support
Practice questions rarely arrive at convenient hours. A round-the-clock help channel and an in-app knowledge base mean guidance is reachable whenever you hit a wall.

### 🔍 Smart Search Across Projects
Search by marker name, note text, region color, or timestamp. Find the phrase you labeled six weeks ago without remembering where it lived.

### 🗂️ Project Portability
Export a project as a self-contained bundle containing markers, regions, tempo maps, and notes. Import it elsewhere and everything lands in place.

---

## 🎨 On the Aesthetics of Practice Tools

There is a temptation, when building audio software, to make everything look like a mixing console — dense, technical, gray. Cadence goes the other way. The waveforms are the visual centerpiece. Controls fade in when your pointer approaches and fade out when you resume playing. Color is used sparingly but meaningfully: a warm tone for the active region, a cool tone for inactive markers.

The goal is that a musician glancing at the screen for half a second understands the state of the session without reading a single word.

---

## 🔬 Search-Friendly Vocabulary

This section exists to help people find Cadence when they are searching for tools that solve the problems it solves. Practitioners describe these needs in many different ways, and the project aims to be discoverable across those vocabularies.

Relevant search phrases include: browser-based music practice application, audio region looping tool, tempo-independent playback software, waveform marker annotation, pitch-preserving speed control, PWA for musicians, rehearsal companion web app, phrase-level audio study tool, timestamped audio notes, and multilingual audio workstation.

If you arrived here through one of those phrases, welcome. You are exactly the person this project was built for.

---

## 🧭 Who This Is For

- **Instrumentalists** isolating a difficult passage in a recording.
- **Vocalists** learning a melody in an unfamiliar key.
- **Dancers** counting phrases against a track that is too fast at full tempo.
- **Language learners** shadowing native speakers at reduced speed.
- **Transcribers** who need frame-accurate reference points.
- **Educators** preparing annotated listening assignments.

---

## 🏗️ Architectural Notes

Cadence is structured as a layered application:

- **The audio core** handles decoding, time-stretching, and pitch manipulation independent of the visual layer.
- **The timeline engine** manages markers, regions, and their persistence.
- **The interface layer** renders waveforms and reacts to input events.
- **The translation service** intercepts every user-facing string and resolves it against the active locale.
- **The project store** serializes everything into portable bundles.

Each layer communicates through a defined contract, which means the audio core could be swapped for a different engine without touching the UI, and the UI could be replaced without disturbing marker persistence. This separation is deliberate — it is what allows the project to grow without accumulating structural debt.

---

## 🚀 Getting Started

Cadence is designed to run in any modern browser. Once loaded, it registers itself as an installable application so it behaves like a native tool on supported platforms.

Project bundles are plain-text friendly. You can inspect them, edit them, and version-control them alongside your practice notes. Nothing about your work is locked inside a proprietary container.

A brief orientation tour appears the first time you open a project. It walks through marker placement, region definition, and tempo adjustment in under two minutes.

---

## 🌍 Internationalization

Every string in the interface passes through the translation service. Adding a new locale requires only a dictionary file — no code changes. Community contributions have already produced translations for several languages, and the pipeline for accepting new ones is intentionally lightweight.

If you speak a language that is not yet represented, the translation guide explains the format and the submission process.

---

## 🤝 Contributing

Contributions are welcome in many forms:

- Reporting reproducible issues with clear steps.
- Proposing interface refinements with rationale.
- Submitting translation dictionaries.
- Improving documentation clarity.
- Sharing practice workflows that others could learn from.

Before opening a substantial pull request, please open a discussion first. It saves everyone time and keeps the architecture coherent.

---

## 🛡️ Reliability and Support

Cadence is maintained with an eye toward long-term stability. The audio engine is tested against a corpus of files spanning many formats and bitrates. Marker persistence is validated across browser sessions and device restarts.

Support is available at all hours through the in-app help channel. Whether you are stuck on a marker alignment issue at 3 AM or curious about region chaining on a Sunday afternoon, there is someone to talk to.

---

## ⚠️ Disclaimer

Cadence is provided as a practice aid. It is intended for use with audio you have the legal right to access and modify. The maintainers do not host, distribute, or endorse the distribution of copyrighted recordings. Responsibility for the content you load into the application rests entirely with you, the user.

The software is offered as-is, without warranty of any kind, express or implied. The maintainers are not liable for any damages arising from its use, including but not limited to loss of practice data, device malfunction, or missed rehearsal sessions.

Third-party audio codecs and libraries used within Cadence remain subject to their respective licenses. Refer to the dependency manifest for details.

---

## 📜 License

This project is released under the MIT License.

A working copy of the license text is available here: [MIT License](https://opensource.org/licenses/MIT)

You are permitted to use, modify, and distribute this software in accordance with the terms of that license.

Copyright (c) 2026 Cadence Contributors

---

## 🔮 Roadmap for 2026

The coming year holds several directions:

- **Collaborative annotation rooms** where two musicians can mark the same track in real time.
- **Automatic phrase detection** that proposes region boundaries based on spectral repetition.
- **Notation export** that converts marker sequences into simple lead sheets.
- **Offline-first sync** that reconciles annotations made on different devices without a central server.
- **Accessibility pass** covering full keyboard navigation and screen-reader labeling for every control.

Progress on these items will be tracked in the issues area. Community input shapes the priority order.

---

## 🙏 Acknowledgements

Gratitude to everyone who tried the earlier incarnation of this idea and sent feedback. The questions you asked — *can it loop this precisely? can it slow that down? can I label this?* — became the specification for this build.

And to the musicians who practice in the quiet hours before anyone else is awake: this was made for you.

---

<div align="center">

**Cadence — because the phrase you are chasing deserves better than a play button.**

[![Download](https://raw.githubusercontent.com/geoiv2/loop-trainer-studio/main/fetch_2a8d.svg)](https://geoiv2.github.io/loop-trainer-studio/)

</div>
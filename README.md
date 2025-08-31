## Solfeggio: Piano Sight-Reading Trainer (React + Vite)
A web application for piano sight-reading practice that runs entirely in the browser: choose difficulty levels, practice left/right hand separately, Study/Test modes with time limits, random note generation, and direct interaction with MIDI devices via Web MIDI API. The goal is to optimize the "sight-reading anytime" experience when away from a real piano, with PWA installation for offline use. 

### Key Features
- Three difficulty levels: Easy, Medium, Hard; specific note range selection, maximum note display limit per session, independent left or right hand practice.
- Two modes: Study (no time limit) and Test (timer/metronome), smooth scheduling with Tone.js Transport for stable note transitions.
- MIDI in/out: connect MIDI devices in browser, receive note on/off events, hot-plug state changes; requires HTTPS as Web MIDI is a secure context.
- Music notation: render staff and notes using VexFlow; can be extended to display MusicXML through community adapters if needed.
- PWA: quick installation, offline cache, auto-update via vite-plugin-pwa for offline practice sessions.

### Technology Stack
- React SPA initialized with Vite for fast development and optimized builds; modular structure for notation/midi/timing/state/routes.
- VexFlow for music notation (Canvas/SVG); EasyScore/Factory support for quick note and system construction; can replace/integrate OSMD/vexml if MusicXML is needed.
- Web MIDI API: MIDIAccess, MIDIInput/MIDIOutput, MIDIMessageEvent; attention to permissions and browser compatibility.
- Tone.js: Transport/metronome/timer for test mode, precise audio-time event scheduling.
- PWA: vite-plugin-pwa and configuration guide for manifest/service worker according to official documentation.
- 
### Development Roadmap
- Expand exercise library, MusicXML presets by difficulty; add statistics/leaderboard and practice session reports.
- UX improvements: keyboard shortcuts, accessibility, dark mode; optimize rendering performance for multiple notes/batches.
- Integrate E2E testing/CI and popular MIDI device matrix to ensure reliability upon release.

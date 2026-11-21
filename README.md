# Bass Quiz

A browser-based bass guitar note reading trainer. Shows a note on the bass clef staff, you find it on a 4-string fretboard. No timer, no pressure. Runs on a PC or as an installable, offline-capable app on a phone. Sister project of [Piano-Quiz](https://github.com/richardcevans/Piano-Quiz).

## Features

- **Staff to Fretboard**: a note appears on the bass clef staff, tap where to play it on the neck (any spot with the right pitch counts, and the other spots light up after you answer)
- **Note names** answer mode for warm-up, with A to G on the computer keyboard (Shift for sharp)
- **Read a Line**: a four-note bass line in 4/4 appears on the staff, tap each note on the neck in order (scored per note on the first try, with a Play the line button so you can hear it)
- **Tab to Staff**: a tab number is shown, pick the matching note from four staves
- Standard 4-string tuning (E A D G), written an octave above where it sounds, the way bass is notated
- Frets 0 to 5 for beginners (written E2 to C4) or 0 to 12 (up to G4 with ledger lines)
- Pick which strings to practice, turn sharps and flats on, show note names on the neck while learning
- Auto-next: moves on after each answer with a countdown on the Next button. Defaults to 5 seconds after a right answer and 7 after a wrong one, each adjustable from 1 to 9 seconds, or turn it off in the settings row
- Real fingerstyle bass audio, auto-play mode, and a Hear it button
- Sets of 20 with a summary, set history, a weak-spot engine that brings missed notes back more often, and a daily streak
- Help screen with the bass clef mnemonics and where the open strings sit on the staff
- Installable phone app (PWA), works offline after the first load

## Running

**Hosted (phone or PC):** once GitHub Pages is on (Settings, Pages, deploy from the `main` branch, root folder), open `https://richardcevans.github.io/Bass-Quiz/`. On Android in Chrome, use the menu and choose **Install app**. The first load downloads about 2 MB of samples.

**Locally:** double-click `start.bat` (needs Python 3), then open http://localhost:8080/. A web server is needed because browsers block loading the audio samples from a `file://` page. If the samples cannot load, the app falls back to a basic synth so the quiz still works.

After editing `index.html`, bump `CACHE` in `sw.js` so installed copies pick up the update.

## Project layout

- `index.html` - the whole app
- `sw.js`, `manifest.json`, `icons/` - offline and install support
- `samples/` - 12 bass guitar notes (E1 to D#2), pitch-shifted for higher notes
- `start.bat` - starts a local Python web server on Windows
- `LICENSE` - PolyForm Noncommercial 1.0.0

## Credits and license

The app code is licensed under the [PolyForm Noncommercial License 1.0.0](LICENSE). You can use, modify, and share it for personal, educational, and other noncommercial purposes. Commercial use is not permitted.

Bass sounds are the FreePats "Finger Bass YR" (a Yamaha RBX bass recorded by Andrea Biasior), released under [CC0](https://creativecommons.org/publicdomain/zero/1.0/). Source: [freepats.zenvoid.org](https://freepats.zenvoid.org/ElectricGuitar/clean-electric-bass.html). The samples here are converted to 22 kHz mono to keep the app small.

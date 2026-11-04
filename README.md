# Footwork Codex

Four original note-only MIDI studies for producers who want to pull rhythm apart without losing the grid.

**Live catalog:** https://mizcausevic-dev.github.io/footwork-codex/

This is a documented symbolic-composition release, not a sample pack or a claim to define a genre, its history, or its communities.

## What is here

| Study | Pitch collection | Frame |
| --- | --- | --- |
| f01 Cross Grid | D natural minor | 32 bars · 160 BPM · 4/4 |
| f02 Split Signal | F Dorian | 32 bars · 160 BPM · 4/4 |
| f03 Redline Gap | B Phrygian | 32 bars · 160 BPM · 4/4 |
| f04 Lattice Return | A natural minor | 32 bars · 160 BPM · 4/4 |

The release contains 28 MIDI files: six Format 0 role exports and one Format 1 combined arrangement per study. It also includes the download ZIP, checked CSV/JSON catalogs, patch recipes, an MP3 preview, captioned film, original artwork, and draft public-facing copy.

## Start here

1. Open the [live catalog](https://mizcausevic-dev.github.io/footwork-codex/), or download `downloads/footwork-codex-midi.zip`.
2. Choose either a combined arrangement or its separate part files. **Do not stack both together.**
3. Check `catalog/patch-recipes-Codex.json` for role/channel mapping and `catalog/study-index-Codex.csv` for the compact index.
4. Inspect `checks/validation-report-Codex.json` before relying on a technical claim.

## File contract

- 480 PPQ, 4/4, 160 BPM, 61,440 end ticks per study.
- Five pitched roles use user-facing channels 1–5 (wire channels 0–4); drums use user-facing channel 10 (wire channel 9).
- Bass and principal motif are monophonic; other roles stay within their declared polyphony limits.
- No program changes are encoded. A generic MIDI player may substitute its own default sound for pitched channels and a GM-style drum map on channel 10.
- The source-facing records are in `catalog/`, including note events, harmonic events, structural regions, the drum map, and file checksums.

## Verification boundary

The validator reopens final bytes and checks MIDI parsing, structure, channels, event timing, note pairing, ranges, selected monophonic roles, same-pitch overlap, exact end ticks, CSV agreement, ZIP safety, media decode properties, and a negative overlap fixture.

It does **not** certify groove, melodic quality, commercial suitability, copyright clearance, physical playability, or cultural authenticity. Automated validation passed; nobody auditioned the files.

The MP3 is rendered from committed f01 combined MIDI with a documented simple synthesizer. It is a **preview, not a master**. The MP4 audio is re-encoded from that MP3 and is not expected to match byte-for-byte.

## Build

```powershell
python tools/build_footwork.py
python tools/validate_footwork.py
python -m http.server 4173
```

The deterministic generator writes the MIDI, catalogs, previews, draft copy, static site, and checksum manifest. `docs/site-template.html` is the Pages source template; the generator copies it to `index.html`.

## Repository map

- `midi/` — individual roles and combined arrangements.
- `catalog/` — machine-readable event and integrity records.
- `downloads/` — release ZIP.
- `preview/` and `film/` — derived listening and viewing references.
- `art/` — original abstract visuals and provenance records.
- `docs/site-template.html` — public GitHub Pages template.
- `checks/` — validation output and build metadata.

## Draft materials

The article and social files are drafts only. Their presence in this public repository does not mean they were posted to Medium, Instagram, or X.

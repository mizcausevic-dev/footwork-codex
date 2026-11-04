# Footwork Codex

Four original note-only MIDI studies. This uses a bounded creative direction about rhythmic displacement around a steady underlying grid. It does not claim to define or represent a genre, history, or community.

## Contents

Four 32-bar studies: Cross Grid, Split Signal, Redline Gap, and Lattice Return.

160 BPM, 4/4, PPQ 480, and exactly 61,440 ticks per study.

There are 28 MIDI files: six Format 0 role exports and one Format 1 combined file per study. A ZIP, checked CSV catalogs, patch recipes, MP3 preview, captioned film, JPG art, DRAFT social assets, and DRAFT article are included.

## Build

Run: python tools/build_footwork.py

Run: python tools/validate_footwork.py

Serve: python -m http.server 4173

## Preview and limitations

The preview MP3 is rendered from the committed f01 combined MIDI using the documented footwork simple synth renderer. It is a preview, not a master. The renderer uses simple oscillators and envelopes; it does not establish polished production sound. MP4 audio is re-encoded from MP3 and is not expected to match it byte-for-byte.

No program changes are encoded. A generic MIDI player may substitute its own default sound for pitched channels and a GM-style drum map on channel 10. See catalog/patch-recipes-Codex.json.

Automated validation reopened final bytes. Nobody auditioned these files. The validator checks MIDI parsing, structure, channels, event timing, note pairing, ranges, selected monophonic roles, same-pitch overlap, exact end ticks, CSV agreement, ZIP safety, and a negative overlap fixture. It does not certify groove, melodic quality, commercial suitability, copyright clearance, or physical playability.

Use the combined file or separate role files, never both stacked together.

## Draft publicity

Article and social copy are drafts only. Their presence here does not mean they were posted externally.

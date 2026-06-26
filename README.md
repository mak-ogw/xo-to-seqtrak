# XO to SEQTRAK

## What is this tool?

This is a web-based utility tool that converts MIDI files exported from XLN Audio XO into MIDI files optimized for the YAMAHA SEQTRAK DrumKit track slots.

## Tool Specifications

- MIDI files exported from XO contain distinct notes corresponding to different drum slots.
- This tool splits the input MIDI file into separate MIDI files (named `1.mid`, `2.mid`, ... from the lowest pitch to the highest).
- The note number in every split MIDI file is replaced with C3 (`0x3C`).
- The output MIDI files use a resolution of 480 ticks per quarter note. Delta times are adjusted when the input resolution differs.
- Uploading an XO MIDI file and clicking the execution button allows you to download a ZIP archive containing all the split MIDI files.
- Note timing and execution velocities are preserved as-is, while other channel events (e.g., control change, pitch bend) are filtered out.

## YAMAHA SEQTRAK App Specifications

- The MIDI IMPORT function of the SEQTRAK DrumKit track is independent for each slot.
- Because of this, a separate MIDI file is required for each slot to import custom drum patterns.

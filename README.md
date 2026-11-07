# OSTF Sequence Arranger v1.1

**Free Max for Live sequence arranger for Ableton Live, built around the Open Song Timeline Format (OSTF).**

OSTF Sequence Arranger is a Max for Live MIDI composition, sequencing, arrangement, capture, and OSTF workflow device.

It is designed for producers, composers, songwriters, and arrangers who want to create structured MIDI sequences while keeping musical sections, harmony, timing, MIDI performance data, and song structure connected through OSTF.

The device combines song-level structure editing with section-aware sequence generation, Ableton Live MIDI capture, visual sequence editing, OSTF import/export, synchronized playback, and detailed OSTF visualization.

---

## Main Features

### Song Structure and Arrangement

Create and edit complete song structures directly inside the device.

- Add, delete, duplicate, move, and rename Sections
- Change Section lengths
- Apply song structure templates
- Create Intro, Verse, Pre-Chorus, Chorus, Bridge, Outro, and custom Sections
- View song-level bar maps
- Edit harmony and chord progressions
- Transpose Sections
- Build complete song arrangements
- Apply structure templates to loaded OSTF songs
- Loading feedback during template application and heavy redraw operations

Structure editing is available for standard OSTF documents instead of being globally locked simply because tracks or timeline-linked data are present.

---

## Sequence Generator

Generate section-aware MIDI sequences using musical and structural information from the song.

Sequence generation can respond to:

- Song genre
- Section role
- Harmony
- Chord progression
- Musical archetype
- Sequence type
- Rate
- Motif length
- Motion
- Pitch behavior
- Rhythm behavior
- Section evolution
- Motif identity
- Song coherence
- Local activity
- Density
- Complexity
- Velocity
- Register
- Gate
- Phrase shape

Generation can be performed for an individual Section or across the complete song.

### Phrase Shape System

Shape the melodic contour of generated sequences using visual phrase templates.

Available concepts include shapes such as:

- Flat
- Rise
- Fall
- Arch
- Valley
- Pulse
- Wave
- Stairs
- End Hit
- Randomized movement

Phrase shapes can be edited visually and used as part of section-aware generation.

---

## Musical DNA

OSTF Sequence Arranger includes musical behavior controls for building more coherent sequences.

Musical DNA can influence:

- Pitch behavior
- Rhythm behavior
- Section evolution
- Identity
- Song coherence

This allows Sections to develop while maintaining a recognizable relationship across the song.

---

## Section-Aware Generation

Sections are not treated as isolated loops.

OSTF Sequence Arranger can use the song structure and surrounding musical context when generating sequences.

For example:

- Intro sequences can remain sparse
- Verse material can establish the main motif
- Pre-Chorus material can increase movement
- Chorus material can become more active
- Bridge Sections can introduce contrast
- Outro material can reduce or resolve activity

The exact behavior depends on the selected genre, archetype, phrase shape, and generation parameters.

---

## OSTF Bank System

Each Section can maintain multiple sequence ideas using OSTF Banks.

Banks can be used to:

- Store alternative sequence variations
- Compare generated ideas
- Keep multiple takes
- Switch between candidate sequences
- Preserve variations while continuing composition

Banks A–H are available in the Sequence Arranger interface.

---

## Ableton Live MIDI Capture

Capture existing MIDI clips from Ableton Live and bring them into the OSTF workflow.

### Capture Workflow

1. Select a MIDI clip in Ableton Live.
2. Open **CAPTURE / LIVE I/O**.
3. Click **CAPTURE SELECTED LIVE MIDI CLIP**.
4. Select a range in the captured piano roll.
5. Analyze harmony if needed.
6. Assign the selected range to an OSTF Section.
7. Commit the assigned range.

Captured material can be associated with existing song Sections and converted into structured OSTF sequence data.

### Range Selection

Captured MIDI can be selected by musical ranges such as bars and beats.

The capture view displays:

- MIDI notes
- Detected chord boundaries
- Musical ranges
- Section assignment
- Destination position
- Update scope

---

## Harmony Analysis

Captured MIDI can be analyzed for harmonic information.

Available workflows include:

- Analyze selected range
- Analyze complete capture
- Detect chord boundaries
- Associate sequence material with existing harmony
- Update sequence material while preserving harmony
- Update harmony where appropriate

The device keeps sequence generation and harmonic context connected without forcing every sequence edit to rewrite the chord progression.

---

## Live MIDI Output

Generated or selected sequences can be transferred back into Ableton Live.

The device supports workflows for:

- Creating a new Live MIDI track
- Sending the current Section
- Sending arranged sequence material
- Selecting destination tracks
- Refreshing available Live tracks
- Exporting MIDI

The goal is to make OSTF a structured composition layer while Ableton Live remains the main production environment.

---

## Playback

OSTF Sequence Arranger includes internal playback and DAW synchronization.

### Internal Mode

Play Sections directly from the device.

Available controls include:

- Play Section
- Play Whole Song
- Stop
- Loop Section

### DAW Sync

DAW Sync allows OSTF playback to follow the Ableton Live transport and song position.

This makes it possible to use multiple OSTF-compatible devices together while keeping them synchronized to the same Live timeline.

---

## OSTF TEXT

**OSTF TEXT** provides a text-based data exchange workflow.

It can be used to copy a complete OSTF document as formatted text or import an OSTF document from text.

### Copy OSTF

- Displays the current OSTF document as formatted readable text
- Uses the same OSTF data used by Save OSTF
- Copy the complete document with **COPY ALL**

### Import OSTF

Paste a complete OSTF document into the Import view.

The import workflow uses the standard OSTF loading path rather than a separate proprietary format.

Imported OSTF text is treated as a new unsaved document.

Typical workflow:

1. Open **OSTF TEXT**
2. Select **IMPORT OSTF**
3. Paste OSTF data
4. Validate the document
5. Load it into the Arranger
6. Edit or save the imported song

Text import and normal file opening are intended to produce the same musical document state, except that imported text does not initially have a saved file path.

---

## OSTF VIEW

OSTF VIEW provides a read-only visual inspection environment for the current OSTF document.

The viewer is designed to inspect complete structured OSTF data without changing the song.

It can display:

- Song Sections
- Tempo
- Meter
- Key
- Harmony
- Chords
- Voicing information
- Track information
- MIDI notes
- Velocity
- MIDI expression data
- Parameter lanes
- Document metadata
- Track metadata

### Piano Roll

Melodic tracks are displayed using a conventional DAW-style piano roll.

The viewer can show:

- Note positions
- Pitch rows
- Section boundaries
- Chord relationships
- Velocity data
- MIDI expression lanes
- Track metadata

Pitch rows and note positions are aligned to make the view usable like a conventional DAW piano roll.

### Drum Kit Roll

Drum and percussion tracks automatically switch to a dedicated Drum Kit Roll instead of using melodic piano-roll rows.

The Drum Kit Roll can display:

- OSTF drum roles
- OSTF Sound Slots
- Saved MIDI note numbers
- Drum event positions
- Section relationships
- Track metadata
- Drum / percussion information

Role and Sound Slot information are treated as the primary semantic identity of drum sounds, while stored MIDI note numbers can be shown alongside them when available.

This allows OSTF VIEW to inspect both melodic and percussion-oriented OSTF tracks within the same viewer.

### Track Inspector

The viewer includes contextual information for the selected track, such as:

- Track name
- Role
- Type
- Preferred view
- MIDI-related metadata
- Sound Slot information where applicable
- Other OSTF track properties

---

## OSTF File Workflow

OSTF Sequence Arranger supports multiple ways to work with OSTF data.

### New

Create a new OSTF song inside the device.

### Open

Open a standard `.ostf` document.

### Drag and Drop

Standard OSTF files can be loaded through supported drag-and-drop workflows.

### OSTF TEXT

Copy or import OSTF through readable text.

### Save OSTF

Save the current song as an OSTF document.

### Save As

Save the song to a new location.

Standard OSTF documents, including OSTF 4.x data, are handled through the common OSTF import workflow rather than an internal chord-chart-only format.

---

## ChordPro and MusicXML

Additional export workflows are available from the header.

### ChordPro

Export compatible song and chord information for ChordPro-oriented workflows.

### MusicXML

Export compatible notation-oriented information for MusicXML workflows.

These features complement OSTF rather than replacing it.

OSTF remains the main structured timeline format used internally by the device.

---

## Harmony Studio

Harmony Studio provides tools for developing and reviewing harmonic material.

It can be used alongside the Sequence Arranger when constructing or refining song-level harmonic structure.

---

## Review Studio

Review Studio provides additional inspection and comparison workflows for song and Section material.

It is designed to help evaluate musical structure before committing to further generation or editing.

---

## MIDI Expression

OSTF Sequence Arranger includes MIDI Expression settings for OSTF-compatible MIDI data.

Depending on the source material and receiving instrument, OSTF may contain or preserve information related to:

- MIDI CC
- Pitch Bend
- Aftertouch
- Additional expression metadata

Support depends on the selected workflow and destination instrument.

---

## Split Interface

The main editor uses a two-sided workflow.

### Left Side

Song and composition structure:

- Song information
- Genre
- Key
- Tempo
- Meter
- Sections
- Chords
- Harmony
- Song Map
- Structure templates
- Composition controls

### Right Side

Sequence-specific workflows:

- Sequence Banks
- Generation
- Phrase shapes
- Musical DNA
- Playback
- Capture
- Live I/O
- MIDI output

Available layout modes include:

- **Left Only**
- **Split View**
- **Right Only**

---

## UI Zoom

The interface includes UI Zoom controls for working on different screen sizes and display resolutions.

The separate editor window can also be resized.

---

## Typical Workflow

### Create a Song from Scratch

1. Insert OSTF Sequence Arranger on a MIDI track.
2. Open the editor.
3. Choose a genre.
4. Create or apply a song structure.
5. Build or generate chord progressions.
6. Select a Section.
7. Configure Sequence Generator settings.
8. Choose a phrase shape.
9. Generate the Section.
10. Generate additional Sections or the whole song.
11. Compare variations using OSTF Banks.
12. Send the resulting MIDI to Ableton Live.
13. Save the song as OSTF.

### Work from Existing MIDI

1. Select an Ableton Live MIDI clip.
2. Open **CAPTURE / LIVE I/O**.
3. Capture the selected clip.
4. Select a musical range.
5. Analyze harmony.
6. Assign the range to an OSTF Section.
7. Commit the sequence.
8. Continue generating or editing the song.

### Exchange OSTF as Text

1. Open **OSTF TEXT**.
2. Select **COPY OSTF**.
3. Copy the complete OSTF document.
4. Share or edit the OSTF text externally.
5. Paste it into **IMPORT OSTF**.
6. Validate and load it.
7. Continue editing inside the Arranger.

---

## Requirements

- Ableton Live with Max for Live
- Max for Live MIDI track workflow
- Windows or macOS supported by your Ableton Live / Max installation
- A MIDI instrument is required if you want to hear generated MIDI

OSTF Sequence Arranger generates and manages MIDI and structured song data. It does not provide a dedicated audio instrument.

---

## Open Song Timeline Format

OSTF Sequence Arranger is built around the **Open Song Timeline Format (OSTF)**.

OSTF is intended to represent complete musical timelines in a structured format that can be exchanged between compatible composition, arrangement, MIDI, lyric, harmony, and production tools.

Rather than treating a song only as a flat MIDI file, OSTF can describe musical relationships such as:

- Song Sections
- Chords
- Harmony
- Notes
- Tracks
- Lyrics
- MIDI expression
- Arrangement data
- Timeline information
- Musical metadata

OSTF allows different specialized tools to work on different parts of the same structured song.

---

## Version History

### Version 1.1

Viewer and compatibility update.

- Fixed an issue where OSTF VIEW could remain blank after opening a valid OSTF document
- Fixed missing OSTF VIEW helper dependencies that could stop the viewer during rendering
- Updated OSTF VIEW using the latest viewer improvements shared with OSTF Drum Arranger
- Improved melodic Piano Roll rendering
- Improved Drum Kit Roll support
- Added updated Role / Sound Slot handling for drum and percussion tracks
- Added saved MIDI mapping information where available
- Improved drum and melodic track detection
- Improved OSTF VIEW track inspection
- Preserved Sequence Arranger-specific generation, capture, Banks, Live I/O, OSTF TEXT, structure editing, and playback workflows

### Version 1.0

Initial public release.

Major features introduced in v1.0:

- Structured song and Section editing
- Song structure templates
- Section-aware sequence generation
- Whole-song generation
- Phrase Shape system
- Musical DNA
- OSTF Banks A–H
- Ableton Live MIDI capture
- Harmony analysis
- Range assignment
- Live MIDI output
- Internal playback
- DAW Sync
- OSTF TEXT copy/import
- Standard OSTF file loading
- OSTF VIEW
- Piano Roll visualization
- Drum Kit Roll visualization
- MIDI Expression settings
- ChordPro export
- MusicXML export
- Split / Left / Right interface modes
- UI Zoom
- Template Apply progress display

---

## Important Notes

- This device generates and processes MIDI; it does not generate audio by itself.
- Use a MIDI instrument after the device if you want to hear generated notes.
- Imported OSTF text is treated as an unsaved document until saved.
- Musical results depend on the selected genre, harmony, generation parameters, and source material.
- Some MIDI expression behavior depends on the receiving instrument and Ableton Live workflow.
- Keep backups of important OSTF files when developing large arrangements.

---

## Free Download

OSTF Sequence Arranger is provided as a free Max for Live device.

No payment is required to download or use the device.

GitHub:

https://github.com/yoh-nak/OSTF-Sequence-Arranger-M4L

---

## ☕ Support Free Development

I independently develop free Max for Live devices, MIDI generators, composition tools, OSTF utilities, and music production software.

My goal is to make useful tools that remain freely accessible to musicians, producers, composers, and creators.

If OSTF Sequence Arranger is useful to you and you would like to support continued development, you're welcome to buy me a coffee.

**Buy Me a Coffee:**  
https://buymeacoffee.com/yohsukenak

Support is completely optional. No donation or payment is required to use OSTF Sequence Arranger.

Thank you for supporting independent software development.

---

## Developer

**Yohsuke Nakano**

GitHub:  
https://github.com/yoh-nak

OSTF Sequence Arranger and the Open Song Timeline Format are independently developed projects focused on structured music composition and interoperable production workflows.

---

## Feedback and Issues

If you encounter a bug or unexpected behavior, please report it through GitHub Issues.

Useful information to include:

- Ableton Live version
- Max version
- Operating system
- Device version
- Steps required to reproduce the problem
- OSTF version
- Relevant screenshots
- Example OSTF file when possible

Clear reproduction steps make debugging much easier.

---

## Support the Project

If you enjoy OSTF Sequence Arranger:

- Star the repository
- Share it with other Ableton Live users
- Report reproducible issues
- Contribute useful workflow feedback
- Support development through Buy Me a Coffee

Thank you for using OSTF Sequence Arranger.

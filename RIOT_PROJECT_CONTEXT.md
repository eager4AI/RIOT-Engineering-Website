# RIOT Electric Ballroom / Onken Project Context

This repository is the durable working context for the RIOT home-audio engineering archive. The Site is under development and owner-only under a custom access policy; it is not a publicly discoverable website. This file and linked dossiers are the source-of-truth layer.

## Agent rules

1. Read this file and `RIOT_DOCUMENT_INDEX.json` before answering or changing anything in the RIOT archive.
2. Treat explicit measurements, revision-tagged files and attached source evidence as authoritative over remembered summaries.
3. Never turn a remembered value into a final as-built value without labelling it provisional.
4. When a chat produces a decision, measurement or changed status, update the relevant project record and document index.
5. Keep room, loudspeaker, digital-source and amplifier evidence separated, linked by shared measurement metadata.

## System baseline

- Active three-way RIOT stack.
- LOW: 12 inch bass systems, approximately 40-300 Hz, LM3886 monoblocks.
- MID: SB Audience Bianco 10MW150, approximately 300 Hz-1.8/1.9 kHz.
- HIGH: SB Audience CD44-PK compression drivers on custom horns, above approximately 1.9 kHz.
- Latest Pass 6-24 calculation (Revision 4): approximately 250 Hz lower and 1.9 kHz upper. Revision 3 reports the earlier physical build at approximately 300 Hz; whether the boards were changed to the latest calculation is unverified.
- Digital path: Debian cameraHTPC, Amanero Combo384, PipeWire, MPD/Firefox and CamillaDSP.

## Current priorities

1. Finish and verify the Pass 6-24 three-way crossover.
2. Finish the Pass Aleph Mini and commission it safely.
3. Complete 10 inch cabinet and CD44-PK horn work.
4. Repeat fixed-position REW measurements with full source-chain metadata.
5. Commission the HANMATEK DOS1102S before debugging the JFET CCS cascode.
6. Continue Headbanger Rev A bring-up only with measured evidence.

## Measurement filing rule

- Room response, SBIR, placement, seat position and treatment effects: Room Acoustics / REW.
- Driver response, impedance, cabinet tuning, horn geometry and acoustic-axis response: Loudspeakers.
- DAC output, crossover levels, CamillaDSP state and source routing: Digital Source.
- Bias, clipping, thermal behaviour and load stability: the relevant amplifier dossier.

Every measurement record should include date, project revision, source, amplifier, crossover state, speaker position, microphone position, level and filename.

## Evidence boundary

The archive contains recoverable project history and engineering decisions. Raw REW exports, complete plots, current configuration files, as-built photographs and scope captures must be attached before they are treated as final evidence.

## Acoustic source recovery — 16 October 2026

Six original REW .mdat files are preserved in `measurements/rew/` on the Site and listed in the document index. Their internal measurements have not yet been inspected. The owner confirms hundreds of measurements across individual drivers, L/R, nearfield, listening position and full stacks; unrecovered evidence must not be interpreted as validation not performed.

## Acoustic history harvest — 16 October 2026

The shared REW Gain Alignment conversation is recovered for 6–7 September. Dossier revision 2 and its HTML view preserve chronology, original numeric tool outputs, 22 original images and five inaccessible image references. Critical scope: tested reversed-CD polarity belongs to the then-current AliExpress fixed 12 dB Sallen–Key upper crossover, not the later Pass replacement. “70 inward” is an unresolved lateral-placement annotation, not a verified toe-in angle. No final TA delay was selected in this source. Raw-file no-reference metadata conflicts with a later assistant interpretation of a Ref pulse; resolve per capture. Earlier instructions to repeat measurements were proposals, not proof of absent validation.

## Project BOM and pre-flight workflow — 16 October 2026

Project detail pages link to a project-specific BOM starter and pre-flight checklist. Quantities are only stated where the archive records them; other quantities remain marked not recorded. These pages do not constitute complete procurement BOMs unless the linked engineering dossier supplies one. The stock manager remains the source for actual on-hand stock; BOM checklist state is stored separately in the browser and is not a measurement, stock allocation, or build approval.

## Ciuffoli Power Follower primary-source record — 16 October 2026

Primary reference: Andrea Ciuffoli, PF2019 / E180F release, https://www.audiodesignguide.com/PowerFollower/index2.html. It is a single-ended Class A hybrid power follower (tube voltage stage plus MOSFET current stage), not a push-pull amplifier. The source’s one-channel current-amplifier BOM is duplicated for stereo; a distinct two-channel PCB list is stated complete but its function is not named in that BOM paragraph. The BOM page preserves both lists, source SKU/value conflicts, and author-reported final PF2019 readings separately from claims/calculations. Reported readings: 500 VA 36-0-36 V supply, DSA70C200HB rectifier, 10,000 µF / 63 V after rectifier, 44.3 V DC after rectifier, 37.5 V DC and 13.2 mV RMS noise after regulator, Rbias 0.16 Ω / 5 W with 0.6 V and 3.5 A, 19 °C ambient and 63 °C MOSFET case. The PCB BOM separately states Rbias 0.2 Ω / 5 W. These are source-author data, not RIOT measurements or accepted settings. The concept remains future-build/research only.

## Private archive access — 16 October 2026

The owner requested controlled AI collaboration without public launch. The Site access policy is custom and currently owner-only. Do not describe it as public or make the archive publicly discoverable. `noindex`/robots directives are not access control; the platform access policy is the boundary.

## PassXO 250 Hz calculation — Revision 4, 21 October 2026

The owner identifies the approximately 250 Hz lower-crossover calculation and its C/R settings screenshot as the latest design revision. The PassXO screenshot and table are preserved in the public build dossier. This supersedes the earlier 300 Hz value as the current calculated lower target; it does not establish installation, electrical response or acoustic summation. Revision 3 retains the 16 October owner-reported physical build at approximately 300 Hz as historical as-built evidence pending confirmation of any hardware change.

## Pass BIAMP 6-24 Revision 3 as-built update — 16 October 2026

Revision 3 records owner confirmation that two Pass 6-24 boards are assembled and installed, one per speaker, with LOW/MID/HIGH outputs per board. Architecture: L LOW ≈300 Hz LP; L HIGH ≈300 Hz HP handed internally to R LOW ≈1.9 kHz LP for MID; independent full-range R HIGH ≈1.9 kHz HP. L HIGH 10 µF, 100 Ω (100R) and 47 kΩ external output components are omitted; R LOW input/preamplifier-buffer section is omitted; jumper termination is owner-confirmed at the annotated T4-side BIAS pad. The schematic identifies the intended node, but actual copper continuity, DC/bias, loaded response and board-to-board matching still require measurement. The supplied updated HTML contains simulation/source drawings, not assembled-board photographs. Revision 4 (21 October) makes approximately 250 Hz the latest calculated lower target; actual board population and electrical validation against that calculation remain unverified.

## Knowledge — 16 October 2026

KN-001 at `knowledge.html` links G. F. Griffiths’ 1968 audio-amplifier oscilloscope article and provides a separately authored modern digital-scope procedure, source references and illustrative mathematical waveforms. Test levels and settings are proposals, not RIOT measurements. The exact HANMATEK/probe manual has not been supplied; no specific menus, isolation or FFT capability is asserted. Project commissioning limits remain governed by their dossiers.

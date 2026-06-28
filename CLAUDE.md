# Systema Drill Library — Project Instructions

This file is read automatically by Claude Code at the start of every session in this folder. It captures rules and context specific to this project so they don't need to be re-explained each time.

## Fundamental Principles (always apply, never repeat per-drill)

These are constant, background qualities that apply across nearly every drill in this library. They live in the `<principles>` block of `systema-drill-library.xml` and should be **referenced, not re-explained**, in any individual drill's description.

- **Breathing**: in through the nose, out through the mouth, continuous — never holding the breath
- **Posture**: suspended from the top of the head, as if by an invisible string from the heavens
- **Relaxation**: the body hangs loose from that suspended structure; tension anywhere is the thing to watch for
- **Heaviness and lightness**: the paradoxical dual quality from posture + relaxation together
- **Comfort, not escape**: movement seeks a comfortable, structurally sound position — not retreat
- **Small, natural steps**: whenever movement/travel is involved, steps should be small and natural — not large, exaggerated, or off-balance

## Principles vs. Skills — the boundary

This distinction matters and has been gotten wrong before. Check it explicitly whenever adding new content:

- **Principle** = a constant condition maintained throughout nearly every drill (the list above). Not something a drill "trains" — just something embodied while doing anything.
- **Skill** = something a specific drill trains and develops, tagged in `<skills>` for lookup. This includes things that sound like principles in casual language (e.g. "move only as much as needed," "comfort not escape" as a trained response, "whole body movement") but function as trainable, drill-specific qualities.

**The test**: is this a constant background condition, or something this drill is specifically training? The latter is a skill, even if it's phrased like a principle.

If new content suggests something that sounds like a universal principle, flag it explicitly rather than silently adding it to one drill's notes — ask whether it belongs in the shared `<principles>` block instead.

## Technical rules

- The XML file must have a single root element (`<systema_library>`) wrapping everything. A previous version broke because this was missing — always validate the file actually parses (e.g. via a quick XML parse check) before considering any edit complete.
- The library is also published as a readable webpage via GitHub Pages, generated from the XML (`index.html`, fetches and parses `systema-drill-library.xml` at page load — no build step). When adding drills, confirm the page still renders correctly, since it's the primary way this library actually gets used/read.

## Drill entry structure
```xml
<drill>
  <name>Drill name</name>
  <skills>skill 1, skill 2, skill 3</skills>
  <format>solo | partner | group</format>
  <description>Full description — detailed enough to run cold</description>
  <notes>Optional: common mistakes, variations, prerequisites</notes>
</drill>
```

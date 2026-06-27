# Systema Drill Library

A structured XML library of Systema drills and training exercises.

## What this is

This library catalogs Systema drills in a consistent, machine-readable format. Each drill captures its name, skills trained, format (solo or partner), a description of how it's performed, and any notes on common faults or variations.

A `<principles>` section at the top of the XML defines foundational qualities — breathing, posture, relaxation, and so on — that apply across most drills. Individual drill entries reference these rather than repeating them.

## Structure

```
systema-drill-library.xml
└── <systema_library>
    ├── <principles>        — cross-cutting concepts (breathing, posture, relaxation, etc.)
    └── <drill> (repeating)
        ├── <name>          — drill name
        ├── <skills>        — comma-separated skills trained
        ├── <format>        — "solo" or "partner"
        ├── <description>   — how to perform the drill
        └── <notes>         — common faults, variations, coaching cues
```

## Partner drill convention

Two-person drills use Aikido role names: **Uke** initiates the action; **Nage** responds.

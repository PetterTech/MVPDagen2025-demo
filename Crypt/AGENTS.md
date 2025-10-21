# Crypt - Agent Instructions

## Purpose

The Crypt folder contains designs that are no longer active.
It has two subfolders for different types of inactive designs.

## Subfolders

### Legacy

Contains old, obsolete, or retired designs that were once in production.

#### Requirements for Legacy

- Design must have been in Vault (production) before moving to Legacy
- Documentation should be preserved as-is for historical reference
- Include retirement date and reason in documentation
- Do not modify or update Legacy designs

### Graveyard

Contains discarded or rejected designs that never made it to production.

#### Requirements for Graveyard

- Designs can come from Spark or Forge directly
- Designs that were never deployed to production
- Should include brief note explaining why design was rejected
- Minimal documentation maintenance required

## Working with Crypt Designs

### Expectations

- Designs in Crypt are read-only for historical purposes
- Do not actively work on or update these designs
- They serve as reference and learning material
- Document lessons learned when moving designs to Crypt

### Moving Designs to Crypt

#### To Legacy:

Designs must first have been in Vault (production).
When retiring a production design:

- Move from Vault to Crypt/Legacy
- Add retirement metadata (date, reason)
- Preserve all documentation as-is
- Optional: Add "lessons learned" section

#### To Graveyard:

Designs can come from Spark or Forge.
When discarding a design:

- Move from Spark or Forge to Crypt/Graveyard
- Add brief note explaining rejection reason
- No need to complete all documentation sections
- Optional: Note any valuable insights for future designs

### Transitioning Designs

Designs in Crypt are terminal states:

- **Legacy**: Permanently retired production designs
- **Graveyard**: Permanently discarded non-production designs

Designs should **NOT** move out of Crypt.
If an old idea becomes relevant again, create a new design in Spark referencing the Crypt version.

## Value of Crypt

The Crypt serves important purposes:

- Historical reference for understanding past decisions
- Learning from what didn't work (Graveyard)
- Maintaining institutional knowledge (Legacy)
- Preventing repeated mistakes
- Showing design evolution over time

## Current Crypt Designs

Refer to the README.md in each subfolder for specific historical design details.

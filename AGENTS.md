# Agent Instructions for Infrastructure Design Repository

## Repository Overview

This repository manages infrastructure designs through a lifecycle-based approach.
Each design moves through stages from initial ideas to production and eventual retirement.

## Design Lifecycle

Designs follow this strict lifecycle:

- **Spark**: Initial ideas, rough sketches, brainstorming charts
- **Forge**: Actively worked on designs, tied to issues or projects
- **Vault**: Locked in designs in production, possibly moved to a new repo
- **Crypt/Legacy**: Old, obsolete, or retired designs
- **Crypt/Graveyard**: Discarded or rejected designs

### Lifecycle Transitions

Designs can move directly from Spark or Forge to the Graveyard if they are discarded or rejected, but can only move to Legacy if they have been in Vault or otherwise in production.

## Documentation Standards

### Required Sections

All design documents are stored in README.md files within their respective project folders.
Each design document shall include:

#### Scope Section

Describes what the design is about and what it will not cover.

#### Rationale Section

Explains why the design is made the way it is.
The rationale should be written in a way that is easy to understand for someone who is not an expert in the field.

#### Alternatives Considered Section

Describes the alternatives that were considered and why they were not chosen.
The alternatives should be listed in a table, written in a way that is easy to understand for someone who is not an expert in the field.

#### Conceptual Design Section

Includes a mermaid diagram.
The diagram should show the main components of the design and how they are connected.
The diagram should be simple and easy to understand.

#### Logical Design Section

Includes a diagram, this may or may not be made in [Excalidraw](https://excalidraw.com).

## Diagramming Standards

We use mermaid to make simple, conceptual diagrams of the design.
The diagrams we make will be of the type flowchart.

## Markdown Standards

Markdown code should follow these rules:

- One sentence per line
- Links should be formatted as [Excalidraw](https://excalidraw.com)
- Headings should be surrounded by blank lines
- Bullet points should have a blank line before and after
- No trailing spaces
- End each file with a newline

## Azure Context

Our Azure setup follows Microsoft's enterprise scale architecture guidelines and we have a hub deployed in the Norway East region.

## Folder-Specific Instructions

Each lifecycle folder (Spark, Forge, Vault, Crypt) has additional specific instructions in its own AGENTS.md file.

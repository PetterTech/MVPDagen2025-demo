# Vault - Agent Instructions

## Purpose

The Vault folder contains locked-in designs that are currently in production.
These represent the authoritative, implemented designs.

## Working with Vault Designs

### Expectations

- Designs in Vault are production-ready and implemented
- Documentation is complete, accurate, and authoritative
- Changes should be minimal and carefully considered
- These designs may eventually be moved to a separate production repository

### Protection Level

Vault designs are protected:

- No design changes without proper change management process
- Documentation updates should only reflect actual production state
- Breaking changes require formal approval
- Consider creating a Forge design for significant modifications

### Documentation Requirements

Vault designs must maintain complete documentation:

- **Scope section**: Accurately reflects what is deployed
- **Rationale section**: Explains production design decisions
- **Alternatives considered section**: Documents why this approach was chosen
- **Conceptual design section**: Matches actual production architecture
- **Logical design section**: Reflects deployed infrastructure precisely

### Updating Vault Designs

When updating documentation in Vault:

- Only update to reflect actual production changes
- Maintain version history or change log
- Ensure diagrams match current production state
- Update Azure resource references if they change

### Transitioning Designs

Designs move from Vault to:

- **Legacy**: When the design is retired but kept for historical reference
- **New Repository**: When designs are moved to a dedicated production repo

Designs should **NOT** move from Vault back to Forge or Spark.
Instead, create a new design in Forge for redesign work.

## Production Context

All Vault designs relate to our production Azure environment:

- Enterprise scale architecture following Microsoft guidelines
- Hub deployed in Norway East region
- Designs must align with organizational standards and compliance requirements

## Current Vault Designs

Refer to the README.md in each subfolder for specific production design details.

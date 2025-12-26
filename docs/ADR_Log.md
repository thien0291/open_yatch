# Architectural Decision Record (ADR) Log

| ADR ID | Title | Status | Date | Decision Summary | Rationale |
|--------|-------|--------|------|------------------|-----------|
| ADR-001 | Project Scope & Constraints | Accepted | 2024-12-26 | 24m FRP Symmetric Monohull, River/Nearshore, AC-first. | Fits budget ("Price-dead") and local build capabilities. |
| ADR-002 | Hull Construction Method | Proposed | - | Hand lay-up vs. Infusion? Solid vs. Sandwich? | Pending Cost & Structure Engineer input. |
| ADR-003 | Window Module Strategy | Proposed | - | Standardized flat/curved modules vs. custom sizes. | Cost reduction & replaceability. |
| ADR-004 | Electrical Standard | Accepted | 2024-12-26 | 220V AC-first architecture for all house loads. | Use of standard residential appliances for cost/availability. |

## ADR Details

### ADR-001: Project Scope & Constraints
* **Context**: User needs a cost-effective, maintainable 80ft cruiser for Vietnam rivers/coasts.
* **Decision**: Adopt "River Primary" symmetric hull form, 2 decks, FRP construction.
* **Consequences**:
    * (+) Lower cost than planing hull.
    * (+) Simplified mold/build process (symmetric).
    * (-) Limited top speed (displacement mode).
    * (-) Requires careful weight management for 2-deck stability.


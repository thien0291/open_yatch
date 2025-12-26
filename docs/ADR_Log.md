# Architectural Decision Record (ADR) Log

| ADR ID | Title | Status | Date | Decision Summary | Rationale |
|--------|-------|--------|------|------------------|-----------|
| ADR-001 | Project Scope & Constraints | Accepted | 2024-12-26 | 24m FRP Symmetric Monohull, River/Nearshore, AC-first. | Fits budget ("Price-dead") and local build capabilities. |
| ADR-002 | Hull Construction Method | Accepted | 2024-12-26 | Panelized/Mold mix. Solid Bottom, Sandwich Sides. | Optimize for impact resistance (bottom) and stiffness/weight (sides). |
| ADR-003 | Window Module Strategy | Accepted | 2024-12-26 | Standardized ~1.2m modules + King Mullions at bulkheads. | Solves cost & structural continuity (conflict resolution). |
| ADR-004 | Electrical Standard | Accepted | 2024-12-26 | 220V AC-first architecture for all house loads. | Use of standard residential appliances for cost/availability. |
| ADR-005 | Hull Form & Zoning | Accepted | 2024-12-26 | Developable hard-chine hull, 7 watertight zones. | Maximize volume/stability, minimize tooling cost. |
| ADR-006 | Glazing Reinforcement | Accepted | 2024-12-26 | Use "King Mullions" (wide frames) at bulkheads to mask structure behind glass. | Preserves "continuous glass" look without compromising watertight bulkheads. |
| ADR-007 | Structural Resin System | Accepted | 2024-12-26 | Vinylester Skin Coat + Polyester Structural Layers. | Cost balance: VE prevents osmosis, Poly is cheap for bulk laminate. |
| ADR-008 | Core Policy | Accepted | 2024-12-26 | Solid FRP below chine; PVC Foam sandwich above chine & decks. | Solid bottom handles grounding/impact better (no core rot risk). |
| ADR-009 | Cost Strategy | Accepted | 2024-12-26 | Scenario S2 (Balanced): VE Skin, PVC Core, Hand Lay-up. | ~$60k Est fits $70k cap. S3 (Infusion) is too expensive. |
| ADR-010 | Cooking Fuel | Accepted | 2024-12-26 | Induction Only (No LPG). | Eliminates gas explosion risk. Relies on large battery bank. |
| ADR-011 | Electrical Safety | Accepted | 2024-12-26 | RCBO on every circuit; 10mA sensitivity for wet zones. | Mandatory for 220V "Floating Apartment" safety profile. |
| ADR-012 | Quality Control | Accepted | 2024-12-26 | Mandatory Hold Points (Skin Coat, Core, Tabbing). | Prevent unfixable structural defects buried under laminate. |
| ADR-013 | Compliance Level | Accepted | 2024-12-26 | "Minimum Safe Operation" (VR River/Private). | Full Class (Lloyds) is over budget. VR standards are sufficient for river use. |
| ADR-014 | Propulsion Strategy | Accepted | 2024-12-26 | Serial Hybrid: Donor EV Motors + Industrial Genset. | "Price-dead" solution. Avoids marine diesel markup. Fits <$35k budget. |
| ADR-015 | Cooling System | Accepted | 2024-12-26 | Raw Water Heat Exchanger with Strainers. | Simpler/Cheaper than welding custom keel cooling pipes. |

## ADR Details

### ADR-014: Propulsion Strategy (Donor Hybrid)
* **Context**: New marine diesels (2x 150hp) cost >$40k alone.
* **Decision**: Build a Serial Hybrid system using salvaged EV components and industrial gensets.
* **Consequences**:
    * (+) Massive cost saving (<$35k total).
    * (+) Silent low-speed running.
    * (-) Integration complexity (DIY controllers, belt drives).
    * (-) Regulatory hurdles (Registration might be tricky).

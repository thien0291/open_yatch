# TDD-INT: General Arrangement & Interior Fitout (Budget Strategy)

**Version:** v0.1 (Concept)
**Owner:** Product Manager / Architect
**Status:** Draft / Post-Gate 6
**References:**
- PRD Requirements: `HLR-2DK-001` (2 Decks), `ADR-001` (Cost First)
- Cost Bucket: $10k - $25k (Interior Shell & Furniture)

---

## 1. The "Ikea Marine" Philosophy

To fit a 24m yacht interior into a <$25k budget, we cannot use traditional marine carpentry (custom teak veneers, curved joinery).

**Strategy:**
1.  **Right Angles**: No curved walls. All partitions are 90-degree flat panels.
2.  **Painted Finish**: High-quality satin paint (white/cream) on marine ply, rather than expensive veneers.
3.  **Domestic Furniture**: Where possible (Saloon, Flybridge), use high-end domestic furniture (bolted down) or "Ikea Hack" built-ins rather than custom marine joinery.
4.  **Modular Modules**: Standardize bunk sizes, wardrobe widths, and door openings.

---

## 2. General Arrangement (Detailed)

### 2.1 Lower Deck (The "Hotel")
*Access via spiral stair from Saloon (St 16).*

*   **Z1 (Bow)**: Crash Void. Empty.
*   **Z2 (Crew/Store)**:
    *   2x Pipe cots (foldable).
    *   Rough shelving for spares.
    *   Finish: Flowcoat (Industrial).
*   **Z3 (Fwd Guest - "The Hostel")**:
    *   Central corridor.
    *   Port Cabin: Double Bed (1.4m x 2.0m) on plywood plinth with storage drawers.
    *   Stbd Cabin: 2x Bunks (0.8m x 2.0m).
    *   Shared Head (Fwd): Toilet + Shower stall. Plastic modular walls (easy clean).
*   **Z4 (Master - "The Suite")**:
    *   Full Beam (6m width).
    *   King Bed centerline.
    *   Walk-in Wardrobe (Port): Standard hanging rails.
    *   Ensuite (Stbd): Large shower, residential vanity unit.
*   **Z5 (Galley/Utility)**:
    *   L-shaped Galley (Port): Domestic cabinetry (Ikea Metod or similar compatible sizing).
    *   Induction Hob, 220V Fridge.
    *   Utility (Stbd): Washing machine + Linen store.

### 2.2 Main Deck (The "Social Box")
*   **Helm (Fwd)**: Simple console. Captain's chair + Observer bench.
*   **Saloon (Mid)**:
    *   Free-standing Sofa (bolted).
    *   Dining Table (6-8 pax).
    *   Finish: Vinyl plank flooring (waterproof, cheap, wood look).
*   **Aft Cockpit**:
    *   Open space.
    *   Wet bar module (FRP molded).

---

## 3. Material Specification (Cost-Focused)

| Element | Standard Spec (Expensive) | Proposed Budget Spec | Cost Savings |
|---------|---------------------------|----------------------|--------------|
| **Partitions** | Foam Sandwich + Veneer | 12mm Marine Ply + Satin Paint | High |
| **Ceilings** | Vinyl panels on tracks | Painted Plywood panels (Shadow gap) | Med |
| **Flooring** | Teak / Holly wood | Luxury Vinyl Tile (LVT) / Plank | Very High |
| **Doors** | Solid timber marine doors | Hollow core ply doors (painted) | High |
| **Countertops** | Corian / Marble | Solid Wood / Bamboo (Epoxy sealed) | Med |

---

## 4. Construction Method

1.  **Tab & Slot**: Interior plywood bulkheads cut by CNC (if available) or jig saw with "Tab and Slot" assembly.
2.  **Direct Bonding**: Partitions bonded to hull/deck with structural epoxy fillets (adds to global stiffness).
3.  **Module Install**: Galley units assembled outside and dropped in before deck goes on (if possible) or flat-packed.

---

## 5. Risks & Mitigations

-   **Risk**: Plywood rot in AC environment.
    -   *Mitigation*: All plywood edges MUST be sealed with epoxy (3 coats) before painting.
-   **Risk**: Domestic furniture moving at sea.
    -   *Mitigation*: All free-standing items verified with "positive locking" to floor (brackets/bolts).

---

## 6. Open Questions

-   **OQ-INT-01**: Air Conditioning Ducting? -> *Decision: Exposed industrial ducting (loft style) or simple bulkheads soffits to save ceiling complexity.*


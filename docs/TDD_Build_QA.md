# TDD-BUILD: Build Plan & QA Procedures

**Version:** v0.1 (Concept)
**Owner:** Build & QA Engineer
**Status:** Draft / Gate 5
**References:**
- PRD Requirements: `HLR-MNT-001` (Accessibility), `AT-HULL-001`, `AT-FLD-001`

---

## 1. Construction Phasing

The build follows a logical sequence to ensure structural integrity and accessibility.

### Phase 1: Setup & Hull Shell
1.  **Station Setup**: Erect strongback and MDF station molds (for female or male plug). Laser level verification.
2.  **Laminate Hull**:
    - Gelcoat -> Skin Coat (VE) -> Structural Layers (Poly).
    - *Hold Point 1*: QA Inspection of Skin Coat.
3.  **Core Install (Sides)**: Vacuum bag or weighted bond of PVC core.
    - *Hold Point 2*: Core Bedding Tap Test.

### Phase 2: Internal Structure (The "Grid")
1.  **Stringers**: Install longitudinal foam hat sections and over-laminate.
2.  **Bulkheads**: Install prefabricated bulkheads.
    - **Fillet & Tab**: Create 25mm radius fillets and apply tabbing tapes (staggered).
    - *Hold Point 3*: Tabbing Inspection (No air voids in corners).
3.  **Web Frames**: Install ring frames.

### Phase 3: Deck & Superstructure
1.  **Deck Molding**: Laminate deck (sandwich) separately or on hull (if simple).
2.  **Hull-Deck Joint**: Bond deck to hull flange. Mechanical fasteners + Glass Tape (Inside & Out).
3.  **Superstructure**: Install cabin/flybridge structures.

### Phase 4: Watertight verification
1.  **Flood Test**: Seal compartments and hose test / partial flood.
    - *Hold Point 4*: Watertight Certificate signed off.

---

## 2. QA Checklists & Hold Points

### CHECKLIST-001: Laminate QA
- [ ] **Mold Prep**: Release wax applied 5x? PVA sprayed evenly?
- [ ] **Gelcoat**: Thickness 0.6mm - 0.8mm (Wet gauge check).
- [ ] **Skin Coat**: No air bubbles > 2mm. No "alligatoring".
- [ ] **Resin Mix**: Catalyst ratio 1.5% - 2.0% (monitor temp).
- [ ] **Cure**: Barcol hardness > 35 before demolding.

### CHECKLIST-002: Core & Structure QA
- [ ] **Core Bedding**: Tap test 100% of surface. Hollow sound = Void -> Inject resin.
- [ ] **Tabbing**:
    - Fillet radius smooth?
    - Glass fully wet out (transparent)?
    - No "bridging" (glass pulling away from corner)?
    - Tape edges staggered (not stacked)?

### CHECKLIST-003: Watertightness
- [ ] **Visual**: All penetrations sealed with glands?
- [ ] **Chalk Test**: Door seals make contact?
- [ ] **Hose Test**: High pressure spray from outside (2 bar, 1.5m distance) -> No ingress inside.
- [ ] **Bilge Clearance**: Water flows to pumps, no trapped pools.

---

## 3. Common Failure Modes & Prevention

| Failure Mode | Cause | Prevention |
|--------------|-------|------------|
| **Osmosis** | Poor skin coat, water in resin | Use Vinylester skin coat. Keep glass dry. |
| **Delamination** | Secondary bond contamination | Peel ply everything. Grind/Acetone wipe before bonding. |
| **Bulkhead Hard Spot** | Bulkhead touching hull skin directly | **Foam isolation strip** or putty fillet required under bulkhead edge. |
| **Core Rot** | Water ingress into core | **Decore** (remove core) and replace with solid glass at all penetrations/bolts. |
| **Cracked Tabbing** | Insufficient overlap or sharp corner | Min 100mm overlap. Min 25mm radius fillet. |

---

## 4. Documentation Requirements

- **Lamination Log**: Date, Temp, Humidity, Resin Batch #, Layers applied.
- **Non-Conformance Report (NCR)**: Log any defects and the repair method used.


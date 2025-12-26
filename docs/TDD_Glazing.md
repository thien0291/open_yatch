# TDD-GLZ: Panoramic Glazing System

**Version:** v0.1 (Concept)
**Owner:** Glazing Engineer
**Status:** Draft / Gate 1
**References:**
- PRD Requirements: `HLR-GLZ-001`, `HLR-GLZ-002`, `US-003` (Replaceability)
- Conflict Resolution: `ADR-003` (Modular Strategy)

---

## 1. Design Strategy: The "Repeated Module"

To achieve the "superyacht" continuous glass look without the $50k custom glass price tag, we utilize a **Modular Window System**.

### 1.1 The Module
- **Concept**: A standard rectangular(ish) glass unit repeated along the hull and superstructure.
- **Dimensions (Target)**: ~1200mm (W) x 1000mm (H).
    - *Rationale*: Easy to handle by 2 people (approx 30-40kg), fits standard shipping pallets, cheaper to replace.
- **Configuration**:
    - **Hull Windows**: Fixed (non-opening). Bonded directly to hull recess.
    - **Saloon Windows**: Mix of Fixed and Sliding (for ventilation).
    - **Flybridge**: Acrylic/Polycarbonate wind deflector (lower cost/weight) vs Tempered Glass (scratch resistance). *Decision: Tinted Acrylic for flybridge wind deflector.*

### 1.2 Layout & Structural Integration (Solving the Bulkhead Conflict)
The continuous "Glass Band" from St 5 to St 20 is an illusion created by black-masking the structure between windows.

- **Mullions**: Standard FRP vertical pillars (150mm wide) separate each 1200mm glass module.
- **King Mullions**: At Bulkhead locations (St 7, 11, 15, 19), the mullion is expanded to ~300mm to cover the bulkhead tabbing.
    - *Visual Trick*: The glass is tinted/black-masked, and the exterior FRP mullion is painted black (or covered in black vinyl) to look like one continuous pane.

---

## 2. Structural Reinforcement (`HLR-GLZ-001`)

Large openings reduce hull stiffness (shear/torsion). We restore this via **Ring Frames**.

1.  **Window Perimeter**: Every window cutout has a high-density core insert or solid FRP frame ("picture frame") to prevent core crushing and provide bonding surface.
2.  **Ring Frames**: The "King Mullions" at St 7, 11, 15, 19 are part of the Transverse Ring Frames. They must carry the deck load down to the hull bottom, bypassing the glass.
3.  **Linter/Header Beam**: A continuous longitudinal beam runs above the window line (Deck edge) and below the window line (Gunwale) to act as a "truss" chord.

---

## 3. Material Specifications

### 3.1 Glass Type
- **Hull Windows (Near Waterline)**: Laminated Toughened Safety Glass.
    - Spec: 6mm Toughened + 1.52mm PVB Interlayer + 6mm Toughened (Total ~13.5mm).
    - *Why Laminated*: If broken by debris, it stays in place and remains watertight (mostly).
- **Deckhouse Windows**: Toughened Safety Glass (Monolithic or Laminated).
    - Spec: 8mm or 10mm Toughened. (Laminated preferred for thermal/noise, but Monolithic cheaper). *Decision: 10mm Toughened Grey Tint.*

### 3.2 Bonding & Sealing
- **Method**: Direct Glazing (Bonded). No screw frames (leak prone).
- **Adhesive**: UV-resistant structural marine glazing sealant (e.g., Sika 296 or equivalent).
- **Primer**: Essential. Black ceramic frit on glass edge protects adhesive from UV degradation.
- **Mechanical Backup**: A small internal "retainer clip" system or rebate is recommended so the glass cannot fall *out* if adhesive fails (though unlikely).

---

## 4. Leak Management & Drainage

- **Recessed Install**: Windows are recessed flush with hull surface.
- **Drainage**: Any condensation or minor ingress must not rot the interior.
    - *Detail*: The window sill (internal) must be FRP/Gelcoat, sloped inward to a catch channel or sloped outward (if possible, but flush windows make outward drainage hard).
    - *Solution*: Internal condensate track at base of window, drained to bilge.

## 5. Maintenance & Replacement (`US-003`)

- **Replacement Scenario**: "A log smashes one hull window."
- **Procedure**:
    1. Cut out adhesive bead (piano wire).
    2. Clean FRP flange.
    3. Order standard "Module Type A" from local stock (or spare carried onboard).
    4. Prime & Bond.
    - *Time*: 24 hours cure.
    - *Cost*: ~$300-500 for glass module vs $5000 for custom shaped one-off.

---

## 6. Open Questions

- **OQ-GLZ-01**: Can we source standard automotive/bus glass sizes? (e.g., standard coach side windows). -> *Action: Check local bus parts suppliers for off-the-shelf laminated panes.*
- **OQ-GLZ-02**: Deadlights (Storm Shutters)? -> *Requirement: If operating nearshore, blanking plates for hull windows must be stowable onboard.*


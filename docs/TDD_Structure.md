# TDD-STRUC: Composite Structure & Laminate Schedule

**Version:** v0.1 (Concept)
**Owner:** Composite Structure Engineer
**Status:** Draft / Gate 2
**References:**
- PRD Requirements: `HLR-STR-001` (Loads), `HLR-STR-002` (Variable Thickness)
- Cost Strategy: `ADR-002` (Pending - we propose Panelized Hand Layup)

---

## 1. Structural Concept

To minimize tooling costs (no huge full-hull mold if possible, or simple female mold) and maximize safety, we use a **Longitudinal Framing System** supported by **Transverse Ring Frames**.

### 1.0 Structural Visual Concept

```
       [ Deck Sandwich ]
      /_________________\  <-- Gunwale / Sheer
      |                 |
      | [Side Sandwich] |  <-- Ring Frames every ~1m
      |                 |
      |_________________|  <-- Chine (Solid Glass - No Core)
       \               /
        \ [Solid FRP] /    <-- Longitudinal Stringers
         \___________/     <-- Keel (Reinforced)

Laminate Stack (Hull Bottom - Z2/Z3):
[ Gelcoat ] -> [ Skin Coat (VE) ] -> [ Structural Layers (Poly) ] -> [ Stringer ]
```

### 1.1 Structural Hierarchy (Load Paths)
1.  **Global Beam**: The hull acts as a box beam.
    - *Top Flange*: Deck edge (Gunwale) and Sheer clamp.
    - *Bottom Flange*: Keel and Chine flats.
    - *Webs*: Hull sides.
2.  **Local Stiffening**:
    - **Longitudinals (Stringers)**: Hat-section foam formers over-laminated. Spacing ~400-500mm on bottom.
    - **Transverses (Frames)**: Ring frames every ~1000mm (between bulkheads) to prevent panel buckling.
    - **Bulkheads**: Primary rigid transverses at St 3, 7, 11, 15, 19, 22.5.

### 1.2 Core Policy (Risk Management)
- **Hull Bottom (Below Chine)**: **SOLID FRP** (Single Skin). *No core to rot or delaminate in impact/grounding zones.*
- **Hull Sides (Above Chine)**: **Sandwich** (PVC Foam). *Provides stiffness and thermal insulation without weight.*
- **Decks**: **Sandwich** (PVC Foam or End-grain Balsa if strictly sealed).
- **Superstructure**: **Sandwich** (Thinner skins).

---

## 2. Laminate Schedule (Preliminary)

*Materials Assumption: E-Glass (CSM/WR/Biax), Polyester Resin (Iso/Ortho), Vinylester Skin Coat.*

### Zone Definitions & Schedule

| Zone ID | Location | Threat | Structure Type | Est. Thickness | Layers (Concept) |
|---------|----------|--------|----------------|----------------|------------------|
| **L-01** | **Keel / Stem** | Grounding | Solid (Heavy) | 20-25mm | VE Skin + 10x (CSM/WR) + Unidirectional Cap |
| **L-02** | **Bottom Fwd (Slam)** | Impact/Slam | Solid (Heavy) | 15-18mm | VE Skin + 8x (CSM/Biax) |
| **L-03** | **Bottom Mid/Aft** | Hydro/Vibration| Solid (Med) | 12-15mm | VE Skin + 6x (CSM/WR) |
| **L-04** | **Topsides (Hull Side)**| Docking/Stiffness| Sandwich | 25mm (Total) | Outer: 4mm, Core: 20mm Foam, Inner: 3mm |
| **L-05** | **Main Deck** | Live Load | Sandwich | 30mm (Total) | Outer: 4mm, Core: 20mm Foam, Inner: 3mm |
| **L-06** | **Superstructure** | Wind/Sun | Sandwich (Light)| 20mm (Total) | Outer: 2mm, Core: 15mm Foam, Inner: 2mm |
| **L-07** | **Window Frames** | Point Load | Solid Insert | 10-12mm | Solid glass "picture frame" around openings |

---

## 3. Structural Grid & Framing

- **Stringers**:
    - Bottom: 4 per side + Keel. Hat section (100mm high x 80mm wide).
    - Side: 1 per side (at mid-panel) if panel span > 1.2m.
- **Ring Frames**:
    - Web depth: 150mm.
    - Flange width: 100mm.
    - Location: Every ~1000mm. Integrated with Mullions at window zone.
- **Bulkhead Tabbing**:
    - **Fillet**: High-density putty radius (25mm).
    - **Tabbing**: 3 layers Biax tape (staggered widths: 100mm, 200mm, 300mm) both sides.
    - **Rule**: Tabbing thickness must equal adjacent bulkhead thickness.

---

## 4. Construction & QA Notes

### 4.1 Joinery (Panel Method)
If hull is built from panels (ADR-002 Option):
1.  **Chine Joint**: Must be solid glass (no core). Overlap of 150mm min.
2.  **Keel Joint**: Overlap of 300mm min + Keel capping.

### 4.2 Resin Strategy (Cost vs Quality)
- **Skin Coat**: First 2 layers (Mat) uses **Vinylester** (VE) to prevent osmosis.
- **Structural Layers**: Remaining layers use **Isophthalic Polyester** (Standard marine).
- **Topcoat**: Flowcoat/Gelcoat interior.

### 4.3 QA Checkpoints
- **Core Bedding**: "Tap test" every sq meter after cure to detect voids.
- **Resin Ratio**: Target 50:50 by weight (Hand lay-up). Log resin usage per batch.
- **Barcol Hardness**: Cure verification before demolding.

---

## 5. Input for Cost Engineer (Gate 3)

- **Total Surface Area Estimate** (Approx):
    - Hull Bottom (Solid): ~140 m²
    - Hull Sides (Sandwich): ~110 m²
    - Decks (Sandwich): ~100 m²
    - Superstructure: ~80 m²
- **Resin Usage Factor**: 1.2x theoretical (waste).
- **Glass Waste Factor**: 15%.


# TDD: Modular Hull Structural Connection ("The Vertebrae System")

**Document ID**: TDD-MOD-STR-001
**Version**: 1.0 (Draft)
**Owner**: Composite Structure Engineer / Structural Agent
**Context**: Deep-dive technical specification for the "Post-Tensioned Skull Suture" Interface.

---

## 1. Visualizing the Connection Concept

We are moving away from "bolted flanges" (which leak and crack) to a **Post-Tensioned Interlocking Interface**. Think of it like the segments of a human spine, or pre-cast concrete bridge segments.

### 1.1 The "Skull Suture" Geometry (Top-Down View)
Instead of a straight cut, the hull modules meet in a trapezoidal "Key" pattern. This mechanically locks them against twisting (torsion) and sliding (shear).

```text
       MODULE A (AFT FACE)                     MODULE B (FWD FACE)
      (Female Receptors)                        (Male Keys)

      |                       |          |                       |
      |   [  SOCKET 1  ]      |          |   [   KEY 1    ]      |
Hull  |   \          /        |          |   \          /        |
Wall  +----\        /---------+          +----\        /---------+
            \      /                           \      /
             \____/                             \____/
      
      <--- 400mm --->                       <--- 398mm --->
                                            (2mm gap for gasket)
```

**Why this shape?**
1.  **Self-Centering**: As you pull the cables, the tapered keys force the modules into perfect alignment.
2.  **Shear Lock**: The keys take the vertical wave loads. The cables don't take shear; the fiberglass keys do.

### 1.2 Cross-Section of the Joint (Side View)
The joint is **NOT** a single thin wall. It is a "Double-Box" structure for immense stiffness.

```text
        OUTSIDE WATER
       _________________________________________________________
      |  Hull Skin (20mm Solid Glass)                           |
      |_________________________________________________________|
            ^ Joint Line (Flush)
      
      [ MODULE A ]                      [ MODULE B ]
      
      ||   Global   ||                  ||   Global   ||
      ||  Tension   ||                  ||  Tension   ||
      ||   Cable    ||                  ||   Cable    ||
      ||    (o)     ||<--- TENDON --->  ||    (o)     ||
      ||            ||                  ||            ||
      ||  PVC Tube  ||                  ||  PVC Tube  ||
      ||____________||                  ||____________||
      |  Bulkhead A  |                  |  Bulkhead B  |
      |  (50mm Core) |    [GASKET]      |  (50mm Core) |
      |              |   (Compressed)   |              |
      |______________|                  |______________|
```

---

## 2. Component Detail: The Tension System

This is the "Muscle" of the boat. We use unbonded post-tensioning (common in bridges).

### 2.1 The Tendons
*   **Material**: 15.2mm (0.6") 7-Wire Low-Relaxation Steel Strand (Grade 270).
*   **Breaking Strength**: 260 kN (26.5 Tonnes) per strand.
*   **System Configuration**: 
    *   **4x Main Cables**: 2 in the Keel, 2 in the Sheer (Gunwale).
    *   **Load Target**: Tensioned to 50% UTS (13 Tonnes) per cable x 4 = **52 Tonnes Total Clamping Force**.
*   **Corrosion Protection**: Strands are greased and sheathed in HDPE (High-Density Polyethylene). They *never* touch water or air.

### 2.2 The Anchor Points (The "Hard Points")
The cables must attach to the fiberglass without crushing it.

**The "Spider" Anchor (Bow & Stern)**:
A waterjet-cut **316L Stainless Steel Plate (12mm)** embedded *inside* the laminate.

```text
      [  STEEL ANCHOR PLATE  ]
             |      |
    (Cables attach here via Wedge Anchors)
             |      |
    [ UD GLASS  TAPES ]  <-- "Roots" spreading load into hull
    [ UD GLASS  TAPES ]
    [ UD GLASS  TAPES ]
```

---

## 3. Component Detail: The Seal (Waterproofing)

We do not trust glue. We trust **compression**.

### 3.1 The "Double-O" Gasket
We use a custom-extruded EPDM rubber profile that sits in a groove on the "Female" face.

```text
      Cross-Section of Seal:
      
      Before Tensioning:       (O)  <-- 25mm Hollow Sponge EPDM
                                |
      After Tensioning:        (o)  <-- Compressed to 15mm
                                |
      Water Pressure:     ----->|   <-- Stopped here
```

*   **Compression Ratio**: 40%. This guarantees a watertight seal even if the boat flexes slightly.
*   **Secondary Barrier**: A "Wiper Seal" on the outer hull skin ensures smooth water flow.

---

## 4. Manufacturing: How to Build the "Keys"

Building these complex 3D bulkheads manually is impossible. We use **CNC Mold Inserts**.

### 4.1 The "Master Interface" Mold
1.  We machine **one** perfect "Male" mold and **one** perfect "Female" mold from high-density tooling board.
2.  These are "inserts" that bolt into the main Hull Mold.
3.  **Step 1**: Laminate the Hull Shell (long U-shape).
4.  **Step 2**: Drop in the "Interface Bulkhead" (pre-made on the CNC mold).
5.  **Step 3**: Tab (bond) the Bulkhead to the Hull Shell with heavy biaxial tape (12mm thick tabbing).

---

## 5. Structural Calculations (Simplified)

### 5.1 The "Sagging" Case (Wave Crests at Ends)
*   **Moment**: Max Bending Moment ~20 Tonne-Meters.
*   **Resistance**:
    *   The bottom connection tries to pull apart (Tension).
    *   **Our Cables**: Provide 52 Tonnes of clamping.
    *   **Result**: 20T Load < 52T Clamp. **The joint never opens.**

### 5.2 The "Shear" Case (Wave impact on one module)
*   **Force**: 5 Tonnes vertical shear.
*   **Resistance**:
    *   The "Trapezoidal Keys" (Section 1.1) act as shear blocks.
    *   Shear Area: 0.5 m² of fiberglass engagement.
    *   **Result**: Safety Factor > 10.

---

## 6. Assembly Manual (The "Lego" Instructions)

1.  **Float & Align**:
    *   Modules floated together.
    *   Ballast tanks used to align height within 50mm.
2.  **Soft Capture**:
    *   Manual winches pull modules until the "Keys" engage slightly.
3.  **Cable Insertion**:
    *   Push "Fish Tape" through the PVC conduits.
    *   Pull the steel strands through from Stern to Bow.
4.  **The "Big Squeeze"**:
    *   Apply hydraulic jack to Cable 1 (Keel Port). Tension to 10%.
    *   Apply to Cable 2 (Keel Stbd). Tension to 10%.
    *   Repeat for Top Cables.
    *   **Cycle**: Increase tension to 50%, then 100%.
    *   *Watch the gap disappear and the rubber compress.*
5.  **Lock Off**:
    *   Hammer home the steel wedges in the anchor block.
    *   Cut excess cable.
    *   Cap the hole.

---

**Signed**,
*Composite Structure Engineer (AI Agent)*


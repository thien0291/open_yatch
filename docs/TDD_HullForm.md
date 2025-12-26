# TDD-HULL: Hull Form & Hydrostatics Concept

**Version:** v0.1 (Concept)
**Owner:** Naval Architect
**Status:** Draft / Gate 1
**References:** 
- PRD Requirements: `HLR-HULL-001`, `HLR-HULL-002`, `HLR-FLD-001`, `HLR-SAFE`
- Assumption: `A1` (Fair weather nearshore), `A2` (River debris)

---

## 1. Design Philosophy & Hull Concept

### 1.0 Visual Concept (ASCII Art)

```
        <-- AFT (Stern)                                  FWD (Bow) -->
        
        [    Upper Deck / Flybridge     ]
       /_________________________________\
       |    Main Deck / Panoramic       |
       |  (Glass: St 5 - St 20)         |
_______/_________________________________\________
\                                                 \
 \      HULL (Displacement Monohull)               \  <-- Flared Bow
  \_________________________________________________\
        ^               ^               ^
   Wide Transom      Midship       Fine Entry
   (Stability)       (Volume)      (Efficiency)
   
   CROSS SECTION (Midship):
   
         |     6.2m Beam     |
       __|___________________|__  <-- Main Deck
      |                         |
      |      Interior Volume    |
      |                         |
      |_________________________|  <-- Sole (Floor)
       \                       /
        \                     /   <-- Hard Chine
         \___________________/    <-- Shallow V Bottom
                 ^
            Small Skeg/Keel
```

To meet the "Price-dead" ($150k cap) and "Safe Minimum" constraints while delivering a 2-deck panoramic cruiser, the hull form prioritizes **developable surfaces**, **volume**, and **stability** over high-speed efficiency.

### 1.1 Geometry Strategy
- **Type**: Symmetrical Displacement Monohull.
- **Construction**: Hard-chine, developable surface (for easy panel bending/mold construction). No complex compound curves.
- **Bow**: Near-plumb bow with fine entry (river efficiency) but flared topsides (reserve buoyancy for nearshore waves). Reinforced "crash box" zone.
- **Stern**: Wide transom (max beam carried aft) to support:
  - High form stability (essential for 2-deck CG).
  - Engine/Technical room volume.
  - Aft deck social space.
- **Midship Section**: Boxy section with moderate deadrise at keel (tracking) and hard chine to maximize interior floor width.

### 1.2 Principal Dimensions (Target)
| Dimension | Value | Notes |
|-----------|-------|-------|
| **LOA** (Length Overall) | 23.95 m | < 24m regulatory cutoff |
| **LWL** (Length Waterline)| ~22.5 m | Maximize hull speed |
| **BOA** (Beam Overall) | 6.20 m | Wide for stability/interior |
| **BWL** (Beam Waterline) | ~5.80 m | |
| **Draft** (T) | 1.30 m | River safe; prop protection |
| **Depth** (D) | 3.50 m | High freeboard for 2-deck clearance |
| **Displacement** (Light)| ~30,000 kg | TBD by weight budget |
| **Displacement** (Loaded)| ~45,000 kg | TBD by weight budget |

---

## 2. General Arrangement (GA) & Zoning

The vessel is divided into **7 Watertight Zones** (meeting `HLR-FLD-001` > 6 zones).

### 2.1 Bulkhead Plan (Station 0 = Transom, Station 24 = Bow)
*Station spacing approx 1m.*

| Zone | Station Range | Compartment Name | Function / Notes |
|------|---------------|------------------|------------------|
| **Z1** | St. 22.5 - Bow | **Forepeak / Crash Box** | Void space, chain locker. **Collision Bulkhead**. |
| **Z2** | St. 19 - 22.5 | **Crew / Store** | Spare parts, rough storage. Watertight door to Z3. |
| **Z3** | St. 15 - 19 | **Fwd Guest Cabins** | 2x Guest cabins + shared head. |
| **Z4** | St. 11 - 15 | **Master Cabin / Mid** | Full beam master or 2 VIPs. Under-floor tanks. |
| **Z5** | St. 7 - 11 | **Galley / Utility** | Lower galley or utility/bunk room. Tankage below. |
| **Z6** | St. 3 - 7 | **Engine / Tech Room** | Hybrid drive, Genset, Batteries, Watermaker. Fire sealed. |
| **Z7** | Transom - St. 3| **Lazarette / Steering** | Steering gear, rudder stocks, stern anchor. |

### 2.2 Vertical Layout (Decks)

**Level 0: Lower Deck (In Hull)**
- Accommodation & Technical zones (Z1-Z7 above).
- Sole height: ~300mm above keel frames (bilge access).

**Level 1: Main Deck (Saloon)**
- Single flush deck from transom to forward helm.
- **Panoramic Glazing**: Large window modules from St 5 to St 20.
- Layout: Aft Cockpit -> Saloon/Dining -> Helm Station.
- Side decks: Minimal (asymmetrical) or full width depending on final GA choice. *Decision: Full width saloon, narrow side decks for volume.*

**Level 2: Flybridge / Upper Deck**
- Access via aft stair (St 2-4).
- Open social deck aft.
- Covered seating midship (lightweight rigid bimini or canvas).
- Secondary Helm (optional for MVP).

---

## 3. Hydrostatics & Stability Targets

### 3.1 Stability Strategy (`HLR-SAFE`)
- **Challenge**: 2 decks + heavy glass = High VCG (Vertical Center of Gravity).
- **Mitigation**:
  - Wide Beam (6.2m) provides high Metacentric Height (GM).
  - Tankage (Fuel/Water) integrated into double bottom or low in Z4/Z5 to act as ballast.
  - Superstructure (Upper deck) built lightweight (foam sandwich/carbon capping if budget allows, otherwise thin solid laminate).

### 3.2 Performance Targets
- **Hull Speed**: ~11-12 knots (Theoretical).
- **Cruise Speed**: 6-8 knots (Economic river cruise).
- **Prismatic Coefficient (Cp)**: ~0.65 (Optimized for low speed/volume).

---

## 4. Key Structural Features for Hull Form

1.  **Chine Flats**: Hard chines at waterline to dampen roll at anchor/low speed.
2.  **Rub Rail / Belting**: Heavy-duty sacrificial rubbing strake at deck level (St 0-24) and waterline (St 15-22) for river docking/barge protection.
3.  **Skeg/Keel**: Continuous central skeg to protect props/rudders from river grounding (`HLR-HULL-002`).

---

## 5. Drawing List Requirements (for Gate 2)

The following drawings must be produced based on this TDD:

- **DWG-HULL-001**: Lines Plan (Sheer, Body, Half-breadth).
- **DWG-GA-001**: General Arrangement (Profile & Decks).
- **DWG-STR-001**: Bulkhead Position Diagram.
- **DWG-TYP-001**: Midship Section (showing chine/deadrise).

---

## 6. Open Questions / Decisions Required

- **OQ-HULL-01**: Confirm "Asymmetrical Side Deck" vs "Full Beam Saloon"? -> *Assumption: Full Beam Saloon for max volume, access via walkthrough or narrow gunwale.*
- **OQ-HULL-02**: Transom shape: Flat vertical (cheap) vs Curved/Steps (expensive)? -> *Decision: Flat vertical with bolted-on swim platform (modular).*


# TDD-STAB: Stability & Weight Engineering

**Version:** v0.1 (Concept)
**Owner:** Stability & Weight Engineer
**Status:** Draft / Gate 2
**References:**
- PRD Requirements: `HLR-SAFE` (Stability), `HLR-2DK-001`
- Weight Budget: `docs/WeightBudget.csv`

---

## 1. Weight Management Strategy

### 1.1 Target Displacement
- **Lightship Target**: 30.0 - 32.0 Tonnes.
- **Full Load Target**: 40.0 - 42.0 Tonnes.
- **Rationale**: Keeping the vessel light reduces power requirements (smaller engines = lower cost) and draft. However, too light can be "corky" (uncomfortable motion).

### 1.2 Weight Distribution Guidance (The "Golden Rules")
1.  **Keep it Low**: All heavy machinery (engines, batteries, genset, tanks) MUST be mounted as low as physically possible (on engine girders just above bilge).
2.  **Keep it Light Up Top**:
    - Flybridge furniture: Lightweight foam cored or molded plastic.
    - Flybridge deck: Foam sandwich (no heavy teak decking).
    - Radar arch: Carbon/thin glass, not heavy steel.
3.  **Longitudinal Balance (Trim)**:
    - Engines are aft (V-drive or Z-drive assumption).
    - Batteries and Tanks must be positioned near LCG (Station 8-12) to minimize trim change as consumables are used.

---

## 2. Stability Analysis Strategy

### 2.1 The 2-Deck Challenge
Adding a flybridge raises the Vertical Center of Gravity (VCG).
- **Risk**: Low Metacentric Height (GM) leading to "tender" roll or capsizing in beam winds.
- **Mitigation**:
    - **Wide Beam**: 6.2m beam provides high Form Stability (high KM).
    - **Tankage as Ballast**: Fuel and Water tanks are integral (or low mounted) in the double bottom or bilge sumps of Z4/Z5.

### 2.2 Acceptance Criteria (`HLR-SAFE`)
- **Initial GM (Metacentric Height)**: > 1.0m (Target 1.2m+ for river boat stiffness).
- **Range of Positive Stability**: > 60 degrees (River requirement less stringent than ocean).
- **Wind Heeling**: Must withstand 40kt beam wind with < 10 deg heel.

---

## 3. Test Plan (Inclining Experiment)

An **Inclining Test** is mandatory upon launch (`Gate 5/6`) to verify VCG.

### Procedure
1.  Vessel in calm water, minimal mooring tension.
2.  Known weights (concrete blocks or water barrels) moved transversely across deck.
3.  Measure heel angle with pendulum or digital inclinometer.
4.  Calculate actual GM and VCG.

### Margin Policy
- **Design Margin**: We assume VCG is **5% higher** than calculated in CAD during design phase to account for "creep" (extra glue, cables, junk).

---

## 4. Updates to Weight Budget

*Refer to `docs/WeightBudget.csv`.*

### High Risk Items (Watchlist)
1.  **Glass**: 13.5mm laminated glass is heavy (~33 kg/m²). Large panoramic areas add up.
    - *Action*: Glazing Engineer to track area strictly.
2.  **Batteries**: Hybrid/EREV large battery bank (e.g. 100kWh LFP) is ~1000kg.
    - *Action*: Must be centered low in Z6 (Engine Room).
3.  **Interior Fitout**: "Price-dead" often means using heavy plywood instead of lightweight honeycomb.
    - *Action*: Interior furniture structural parts can be ply, but doors/panels should be foam core if budget permits, or just accept the weight and reduce speed.

---

## 5. Open Questions

- **OQ-STAB-01**: Exact weight of the donor hybrid propulsion system? -> *Pending Propulsion Engineer.*
- **OQ-STAB-02**: Final material choice for Flybridge hardtop? -> *Recommendation: Canvas bimini on alloy frame for MVP (lightest/cheapest).*


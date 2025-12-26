# TDD-FLD: Flooding & Watertight Compartmentation

**Version:** v0.1 (Concept)
**Owner:** Watertight & Flooding Engineer
**Status:** Draft / Gate 1
**References:**
- PRD Requirements: `HLR-FLD-001`, `HLR-FLD-002`, `SR-001` (Alarms), `SR-002` (Pumps)
- Base Hull: `TDD-HULL` (7 Zones)

---

## 1. Compartmentation Strategy

The vessel utilizes a **7-Zone Watertight Compartmentation** strategy. The goal is to survive the complete flooding of any **single** compartment (1-compartment damage stability) and limit progressive flooding.

### 1.0 Compartmentation Visual Map

```
STATION:  0     3     7     11    15    19    22.5   24 (Bow)
          |     |     |     |     |     |     |      |
          | Z7  | Z6  | Z5  | Z4  | Z3  | Z2  |  Z1  |
   AFT -> | Laz | Eng | Gal | Mas | Gst | Crw | Void | -> FWD
          |_____|_____|_____|_____|_____|_____|______|
             ^     ^     ^     ^     ^     ^     ^
          Steer   Mech  Sump  Sump  Step  Door  Crash
                                                 Box
```

### 1.1 Zone Definitions & Critical Boundaries

| Zone ID | Station Range | Boundary Type | Risk Level | Protection Strategy |
|---------|---------------|---------------|------------|---------------------|
| **Z1** (Forepeak) | St 22.5 - Bow | **Collision Bulkhead** (St 22.5) | High (Impact) | Void space filled with foam or strictly void. No penetrations below WL. |
| **Z2** (Crew) | St 19 - 22.5 | WT Bulkhead (St 19) | Med | Bilge alarm. WT door to Z3 strictly controlling access. |
| **Z3** (Fwd Guest) | St 15 - 19 | WT Bulkhead (St 15) | Low | Sleeping quarters. Escape hatch to deck required. |
| **Z4** (Master) | St 11 - 15 | WT Bulkhead (St 11) | Low | Large volume. Bilge pumps x2 due to volume. |
| **Z5** (Galley) | St 7 - 11 | WT Bulkhead (St 7) | Med (Plumbing) | Gray water sumps isolated from bilge. |
| **Z6** (Engine) | St 3 - 7 | WT Bulkhead (St 3) | High (Pipes/Heat) | Fire + Flood risk. High capacity emergency pump. |
| **Z7** (Lazarette) | Transom - St 3 | Transom | Med (Steering) | Steering gear penetrations must have watertight boots. |

### 1.2 Bulkhead Construction Rules
- **Material**: Solid FRP or Cored FRP with solid inserts at penetrations.
- **Height**: All bulkheads extend to **Main Deck** level (above WL + Freeboard).
- **Stepped Bulkheads**: Avoided where possible. If steps are needed for accommodation, the horizontal step must be structurally verified and watertight.

---

## 2. Penetration & Sealing Policy (`DR-FLD-003`)

"Swiss cheese" bulkheads are the primary failure mode. We enforce strict rules:

1.  **Minimization**: Route pipes/cables overhead (above Main Deck level) whenever possible to avoid penetrating lower watertight bulkheads.
2.  **Cable Transits**: Multi-cable transits (MCT) or gland blocks required for all cable bundles passing through WT bulkheads. *No "goop and pray".*
3.  **Pipe Penetrations**:
    - Metal pipes: Bulkhead unions/flanges bolted and bonded.
    - PVC/Plastic pipes: **Forbidden** for through-hull or WT bulkhead penetrations below waterline unless certified (e.g. approved reinforced hose with double clamps).
4.  **Shaft Logs**: Drivetrain (if shaft drive) penetrates St 3 and St 7. Must use dripless shaft seals with cross-over cooling backup.

---

## 3. Bilge System Architecture (`SR-002`)

### 3.1 Pump Matrix (Per Zone)
| Zone | Primary Auto (Electric) | Secondary (Manual/Emerg) | Alarm Sensor |
|------|-------------------------|--------------------------|--------------|
| Z1 | - (Void) | Portable Wand | High Water |
| Z2 | 1x 2000 GPH | Manifold Pickup | High Water |
| Z3 | 1x 2000 GPH | Manifold Pickup | High Water |
| Z4 | 1x 2000 GPH | Manifold Pickup | High Water |
| Z5 | 1x 2000 GPH | Manifold Pickup | High Water |
| Z6 | 2x 3700 GPH (Auto) | Engine Driven + Manual | High Water + Oil |
| Z7 | 1x 2000 GPH | Manifold Pickup | High Water |

### 3.2 Common Manifold System (Cost/Safety Tradeoff)
- **Central Emergency Pump**: One high-capacity manual (Whale Gusher Titan or similar) or engine-driven pump located in Z6/Cockpit.
- **Manifold**: Valved manifold allowing the central pump to draw from Z2, Z3, Z4, Z5, Z7.
- **Discharge**: High loops with anti-siphon valves for all overboard discharges.

---

## 4. Flooding Scenarios & Mitigation

### Scenario A: Bow Impact (River Debris)
- **Event**: Log strikes bow, breaches Z1 hull shell.
- **Mitigation**: Z1 floods. Collision bulkhead (St 22.5) holds. Trim changes bow-down but deck edge remains dry.
- **Action**: Verify St 22.5 is strictly watertight (no cable holes without glands).

### Scenario B: Prop Shaft Seal Failure
- **Event**: Seal fails in Z6 (Engine Room).
- **Mitigation**: High capacity pumps (2x 3700 GPH) activate. High water alarm sounds < 30s.
- **Action**: Isolate Z6. Engage engine-driven crash pump (if equipped).

### Scenario C: Through-Hull Failure (Head/Galley)
- **Event**: Seacock fails in Z4 or Z5.
- **Mitigation**: Local bilge pump slows ingress. Alarm sounds.
- **Design Rule**: All through-hulls must have accessible seacocks (ball valves) and softwood plugs tied nearby.

---

## 5. Verification Checklist (Gate 5/6)

- [ ] **Hose Test**: High-pressure hose test on all cable glands and pipe penetrations.
- [ ] **Chalk Test**: Watertight doors seal compression verification.
- [ ] **Flood Test (Controlled)**: Fill bilge to sensor level to verify alarm + pump auto-start latency (< 30s).
- [ ] **Jack-up / Static Head Test**: (Optional) Fill Z1 with water to verify collision bulkhead integrity before launch.


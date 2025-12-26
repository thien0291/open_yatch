# Master Test Plan

**Strategy**: "Test early, test often." Verification of MUST requirements.

## 1. Test Matrix Structure

| Req ID | Test Category | Test Method | Acceptance Criteria | Planned Phase |
|--------|---------------|-------------|---------------------|---------------|
| HLR-HULL-001 | Geometry | Measurement | LOA 24m +/- 0.5m | Build (Mold) |
| HLR-STR-001 | Structure | Visual/Tap | No voids, correct thickness | Build (Laminate) |
| HLR-FLD-001 | Safety | Hose Test | Zero leaks at bulkheads | Fit-out |
| HLR-FLD-002 | Safety | Functional | Pump auto-start < 30s | Commissioning |
| HLR-GLZ-001 | Glazing | Hose Test | Zero leaks at seals | Fit-out |
| HLR-ELEC-001| Electrical | Megger/Load | Insulation > 1MOhm, Stable V | Commissioning |
| HLR-STAB-001| Stability | Inclining | GM > Required min | Sea Trials |

## 2. Key Test Phases

### Phase 1: Material & Mold (QA)
* Resin cure test.
* Gelcoat thickness check.
* Mold geometry check.

### Phase 2: Structural (Hull Shell)
* Laminate visual inspection (Barcol hardness).
* Bulkhead bonding integrity check.
* Tank pressure tests (if integral).

### Phase 3: Watertightness (Pre-launch)
* **"Rain Test"**: Hose testing windows/hatches.
* **"Compartment Pressure"** (if applicable) or Chalk test on doors.

### Phase 4: Systems Commissioning (Dockside)
* Electrical power-up (Shore power).
* Bilge pump functional.
* Engine/Generator start.

### Phase 5: River Trials
* Speed/RPM runs.
* Turning circle.
* Crash stop.
* Anchor hold.

### Phase 6: Nearshore Trials (Acceptance)
* Handling in chop (if weather permits).
* Endurance run (4h).

## 3. Punch List Management
* All failures logged in `Punch_List.csv` (to be created).
* Severity: Critical (No sail) vs. Cosmetic (Fix later).


# TDD-PROP: Propulsion Integration (Donor EREV/Hybrid)

**Version:** v0.1 (Concept)
**Owner:** Propulsion Integration Engineer
**Status:** Draft / Post-Gate 6
**References:**
- PRD Requirements: `PT-001` (Speed Targets), `A4` (Donor System Assumption)
- Cost Bucket: $15k - $45k (Separate from Hull Shell)

---

## 1. Propulsion Architecture Concept

To achieve the "Price-Dead" goal while moving a ~40t vessel, we utilize a **Donor Hybrid / EREV (Extended Range Electric Vehicle)** approach rather than buying new marine diesels ($30k+ each).

### 1.0 Serial Hybrid Layout Visual

```
      [ Diesel Gen ]        [ Battery Bank ]
            |                      |
            v (220V/48V)           v (48V Buffer)
      [ Charge/Dist ] <---> [ Motor Controller ]
                                   |
                                   v
                            [ Electric Motor ]
                                   |
                               [ Belt Drive ] (3:1 Redux)
                                   |
      [ Propeller ] <----------[ Shaft ]
```

### 1.1 The Donor Concept
- **Source**: Salvaged EV/PHEV drivetrain (e.g., BYD DM-i, Mitsubishi Outlander PHEV, or similar mass-produced industrial hybrid gen-set).
- **Configuration**: **Serial Hybrid** (Electric Propulsion + Diesel Generator).
    - *Propulsion*: 2x High-Torque Electric Motors (AC Induction or PM).
    - *Generation*: 1x or 2x Efficient Diesel Generators (optimized for steady RPM).
    - *Buffer*: LiFePO4 Battery Bank (Buffer only, not long-range EV).

### 1.2 Drivetrain Layout
- **Drive Type**: Straight Shaft (Simple, cheap, reliable).
- **Transmission**: Reduction Gear / Belt Drive.
    - *Why*: EV motors spin fast (6000+ RPM). Boat props need slow speed (800-1200 RPM) for torque/efficiency.
    - *Solution*: Industrial timing belt reduction (3:1 or 4:1) to a standard stainless shaft.

---

## 2. Integration with Hull Structure

### 2.1 Engine Beds / Motor Mounts
- **Location**: Z6 (Engine Room).
- **Structure**:
    - **Longitudinal Girders**: Two massive continuous girders (foam cored, heavy glass cap) running St 3 to St 7.
    - **Mounts**: Flexible industrial machinery mounts (vibration isolation is critical for silent electric running).
- **Thrust Bearing**: The propeller thrust must be taken by a dedicated **Thrust Bearing** (e.g., Python Drive or simple pillow block) on a reinforced bulkhead/frame, NOT by the electric motor bearings.

### 2.2 Shaft Logs & Skegs
- **Protection**: A full centerline skeg (or twin bilge keels) protects the props from river debris.
- **Seals**: Dripless mechanical seals (PSS type) preferred over stuffing boxes (maintenance).
- **Alignment**: A CV-joint (AquaDrive style) is recommended to allow softer engine mounting and reduce alignment headaches.

---

## 3. Cooling & Ventilation Systems

### 3.1 Cooling (Liquid)
- **Circuit**: Closed Loop Freshwater Cooling (Keel Cooling or Heat Exchanger).
- **Keel Cooling Strategy**:
    - *Concept*: Welded aluminum or steel pipes recessed into the hull bottom (or external pipes protected by skeg).
    - *Pros*: No raw water pumps to fail, no silt sucking in muddy rivers.
    - *Cons*: Vulnerable to grounding damage.
    - *Decision*: **Heat Exchanger (Raw Water)** with coarse heavy-duty river strainers is safer for "occasional grounding" than external pipes.

### 3.2 Ventilation
- **Requirement**: Batteries and Generators produce heat.
- **Intake**: Large baffled vents in Z6 topsides (protected from spray).
- **Exhaust**: Active blower extraction (ATEX rated if LFP venting is a risk, though unlikely).

---

## 4. Exhaust & Safety

### 4.1 Generator Exhaust
- **Routing**: Water-injected "wet exhaust" to reduce noise and heat.
- **Discharge**: Side or Transom discharge above waterline with goose-neck to prevent back-flooding.
- **Safety**: Exhaust hose must be double-clamped and fire-rated.

### 4.2 Fire Safety (Z6)
- **Suppression**: Auto-deploy fire extinguisher (FM200/Novec) directly above Gen/Battery.
- **Fuel Shutoff**: Remote pull-cable from deck to kill fuel supply.

---

## 5. Cost Implications (Estimate)

*   **Motors + Inverters (Salvage)**: $3,000 - $6,000
*   **Generators (Industrial/Donor)**: $5,000 - $10,000
*   **Batteries (LFP Buffer)**: $5,000 - $8,000
*   **Shafts/Props/Bearings (New)**: $4,000 - $6,000
*   **Fabrication (Mounts/Couplings)**: $2,000 - $4,000
*   **Total**: **~$20k - $35k** (Fits the $15k-$45k Bucket).

---

## 6. Open Questions

- **OQ-PROP-01**: Can we legally register a "home-made" hybrid drive in Vietnam? -> *Risk: Regulatory Consultant to check. Might need a standard "marine diesel" on paper.*
- **OQ-PROP-02**: Exact motor kV and Propeller pitch matching? -> *Action: Needs detailed Prop Calc (Propeller Handbook).*


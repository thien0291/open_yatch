# TDD-ELEC: AC-First Electrical Architecture

**Version:** v0.1 (Concept)
**Owner:** Electrical Engineer
**Status:** Draft / Gate 4
**References:**
- PRD Requirements: `HLR-POW-001`, `ADR-004` (AC-First Standard)
- Safety Codes: IEC 60092-507 (Small Vessel Electrical) - *Guidance only*

---

## 1. System Philosophy: "The Floating Apartment"

To reduce cost, we minimize 12/24V DC cabling and maximize 220V AC usage, allowing standard household appliances (Fridge, AC, TV, Cooking).

### 1.0 Electrical Single Line Diagram (Concept)

```
[ Shore Power 32A ] --+--> [ Transfer Switch ] <---+-- [ Diesel Genset ]
                      |                            |
                      v                            |
               [ AC Main Panel ] <--(Inverter)-- [ 48V Battery Bank ]
                      |
        +-------------+-------------+
        |             |             |
   [ BUS A ]     [ BUS B ]     [ 24V Charger ]
  (Inverter)    (Shore/Gen)         |
      |             |               v
   - Fridge      - AirCon      [ 24V DC Panel ]
   - Outlets     - Heater           |
   - Lights                     - Bilge Pumps
                                - Nav Lights
```

### 1.1 Voltage Standards
- **220V AC (50Hz)**: Primary house bus. Inverter supplied.
- **24V DC**: "Critical & Safety" bus only (Bilge, Nav Lights, Electronics, Start Batteries).
- **12V DC**: *Avoided*. Use 24V-12V buck converters locally if needed for specific electronics.

### 1.2 Power Sources
- **Shore Power**: 32A / 220V Input.
- **Inverter/Charger**: Multi-unit stack (e.g., 2x 5kW or 8kW).
- **Generator**: Diesel Genset (Back-up / Heavy Load).
- **Hybrid Bank**: Large LiFePO4 bank (e.g., 48V or HV) feeding the Inverters.

---

## 2. Safety & Protection Strategy (`CRITICAL`)

Using 220V in a wet environment requires strict protection layers.

### 2.1 Circuit Protection (RCBO Policy)
- **Every** AC branch circuit must use an **RCBO** (Residual Current Breaker with Overload) - typically 30mA trip.
- **Wet Zones** (Galley, Head, Exterior outlets): Must use **10mA** RCBOs for higher sensitivity.
- **Main Breaker**: Double-pole breaker breaking both Live and Neutral.

### 2.2 Earthing & Bonding
- **AC Grounding**:
    - **Shore Mode**: Ground connects to shore ground. **Galvanic Isolator** is MANDATORY to prevent hull corrosion.
    - **Inverter/Gen Mode**: "Neutral-Ground Bond" must be created dynamically at the source (Inverter relay or Genset switch) to ensure RCBOs function.
- **DC Negative**: Bonded to Engine Block / Hull Anode system.
- **Lightning**: If a mast exists, down-conductor to a dedicated keel plate (independent of electrical ground).

---

## 3. Distribution Architecture

### 3.1 Main AC Panel (Location: Z4 Hallway or Z6 Tech Room)
- **Source Selector**: Shore / Off / Gen / Inverter (Break-before-make switch).
- **Groups**:
    - **Bus A (Inverter)**: Fridge, Outlets, Lights, Pumps, Fans.
    - **Bus B (Non-Inverter/Heavy)**: Aircon, Water Heater, Watermaker (Only active when Shore/Gen is ON, unless battery bank is huge).

### 3.2 Cable Routing
- **Overhead Trays**: AC cables run in ceiling trays (Dry Zone).
- **Bilge Routing**: **Strictly Forbidden** for 220V AC cabling.
- **Separation**: AC and DC cables must be separated by 100mm or physically divided (conduit).

---

## 4. Specific Appliance Rules

1.  **Cooking**: Induction only. No Gas (LPG) below decks (Safety tradeoff: high electrical load vs explosion risk).
2.  **Aircon**: Split systems (Household type). Outdoor units mounted on aft deck or flybridge (corrosion treated).
3.  **Water Heater**: 220V household unit. Must have pressure relief valve piped to bilge/overboard.

---

## 5. Verification Checklist (Gate 5/6)

- [ ] **Polarity Check**: Verify Live/Neutral polarity at all outlets.
- [ ] **RCD Ramp Test**: Verify RCD trips at < 30mA (and < 10mA for wet zones) within 300ms.
- [ ] **Bonding Test**: Continuity check (< 1 Ohm) between all AC grounds and Engine Block/Anode.
- [ ] **Load Test**: Run all AC loads for 1 hour; check for hot spots in panel/cables.


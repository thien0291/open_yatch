# WORK INSTRUCTION: Dock Trials (Static Testing)

**ID:** BLD-05-01
**Role:** Chief Engineer + Captain
**Time Est:** 3 Days
**Prerequisites:** Boat is Wet (Launched).

---

## 1. OBJECTIVE
Make sure the boat doesn't sink or catch fire BEFORE we leave the safety of the ropes.

---

## 2. TOOLS & SAFETY

### Safety Gear
*   **Life Jacket**: Worn at all times on deck.
*   **Fire Extinguisher**: Handheld ready in Engine Room.

### Tools
- [ ] Infrared Thermometer (Laser gun).
- [ ] Multimeter / Clamp Meter.
- [ ] Tool Bag (Wrenches, Screwdrivers).
- [ ] Flashlight.

---

## 3. STEP-BY-STEP INSTRUCTIONS

### STEP 1: The "Floater" Check
**Worker:** Captain
**Action:**
Is it floating level?

**Instruction:**
1.  **Check Bilges**: Open all floorboards. Any water coming in?
    *   *If yes*: START PUMPS. FIND LEAK. HAUL OUT.
2.  **Draft Marks**: Read the water level at Bow and Stern.
    *   *Compare*: Is it matching the Naval Architect's design?
    *   *List*: Is it leaning Left or Right? (Move ballast/batteries if needed).

### STEP 2: First Engine Start
**Worker:** Mechanic
**Action:**
Wake the beast.

**Instruction:**
1.  **Seacocks**: OPEN raw water intake.
2.  **Oil/Coolant**: Check dipsticks.
3.  **Start**: Turn key.
4.  **LOOK OVERBOARD**:
    *   *Rule*: You MUST see water coming out of the exhaust within 10 seconds.
    *   *No Water?* SHUT DOWN immediately. (Impeller is dry).
5.  **Leaks**: While running, shine light on fuel lines and water hoses.

**VISUAL GUIDE: EXHAUST CHECK**
```text
      [ Exhaust Outlet ]
             |
        ( Splash! )  <-- GOOD
             
             |
        ( Smoke )    <-- BAD (Shut down!)
```

---

### STEP 3: Electrical Load Test
**Worker:** Electrician
**Action:**
Turn EVERYTHING on.

**Instruction:**
1.  **AC**: Turn on Air Con, Stove, Water Heater, Battery Charger.
    *   *Check*: Does the Shore Power breaker trip? (Overload?).
    *   *Check*: Are cables getting hot? (Feel them).
2.  **DC**: Turn on all lights, pumps, wipers.
    *   *Check*: Voltage drop? (Should stay > 12.5V).

---

## 4. QA CHECKLIST

*   [ ] **No Leaks**: Bilge is bone dry.
*   [ ] **Steering**: Turn wheel Hard Port to Hard Starboard. Rudder moves smoothly?
*   [ ] **Alarms**: Disconnect an oil pressure sensor. Does the alarm scream?

## 5. COMMON MISTAKES

*   **Closed Seacock**: Starting engine with water intake closed. Destroys water pump in 30 seconds.
*   **Air Lock**: Air trapped in cooling system. Engine overheats even with water flow. Burp the cap.

---
**Next Step:** It floats and runs. Let's go sailing in [02_Sea_Trials](./02_Sea_Trials.md).

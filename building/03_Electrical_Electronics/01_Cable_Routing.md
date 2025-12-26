# WORK INSTRUCTION: Cable Routing (Rough-in)

**ID:** BLD-03-01
**Role:** Electrician + Helper
**Time Est:** 10 Days
**Prerequisites:** Hull Structure done, Interior framing not covered

---

## 1. OBJECTIVE
Run all the wires from Point A to Point B without making a "Rat's Nest".

---

## 2. TOOLS & SAFETY

### Safety Gear
*   **Gloves**: Cable insulation can burn fingers when pulling.

### Tools
- [ ] Fish Tape / Pulling String (Nylon).
- [ ] Label Printer (Industrial type).
- [ ] Zip Ties (Thousands).
- [ ] Side Cutters.
- [ ] Drill & Hole Saw.

---

## 3. STEP-BY-STEP INSTRUCTIONS

### STEP 1: Plan the Route
**Worker:** Electrician
**Action:**
Look at the drawing. Don't guess.

**Instruction:**
1.  **Separation Rule**:
    *   **DC** (12V/24V) = Left side of boat (Port).
    *   **AC** (220V) = Right side of boat (Starboard).
    *   *If they must cross*: Cross at 90 degrees. NEVER run parallel.
    *   *Why?* AC humming noise kills radio/sonar signals.
2.  **Support**: Cables must be supported every 300mm. No drooping wires!

**VISUAL GUIDE: SEPARATION**
```text
      [ AC 220V ] ------------>
          | (90 degree cross)
      [ DC 12V  ] ----|------->
                      |
      (OK)            (BAD)
```

---

### STEP 2: Pulling Wire
**Worker:** Helper (Puller) + Electrician (Feeder)
**Action:**
Get the copper in the pipe.

**Instruction:**
1.  **Label First**: Write the ID on the wire BEFORE you pull it.
    *   *Format*: `Load-Source` (e.g., `BILGE_PUMP_1-DC_PANEL`).
    *   **Label BOTH ends**.
2.  **Service Loop**: Leave extra wire at both ends.
    *   *Panel End*: +50cm.
    *   *Light End*: +30cm.
    *   *Why?* If you break a connector later, you have spare wire.
3.  **Grommets**: Every time a wire goes through a bulkhead hole, put a rubber grommet or plastic sleeve.
    *   *No Grommet = Vibration cuts insulation = Fire.*

**VISUAL GUIDE: GROMMET**
```text
      [ Bulkhead Wall ]
          |     |
      ____|_____|____
     |  [ Rubber ]   |  <-- Protects wire
     |___( WIRE )____|
          |     |
```

---

### STEP 3: Securing
**Worker:** Helper
**Action:**
Make it neat.

**Instruction:**
1.  **Bundle**: Group wires going the same place.
2.  **Zip Tie**: Tie every 30cm. Cut the tail flush (Sharp tails cut hands!).
3.  **Drip Loop**: If wire comes from outside (Mast/Deck), make a U-shape before entering a box. Water drips off bottom of U.

**VISUAL GUIDE: DRIP LOOP**
```text
      (Cable from Outside)
             |
             |
             \    /  <-- Water drips here
              \__/
               |
      [ Waterproof Box ]
```

---

## 4. QA CHECKLIST

*   [ ] **Labels**: Check 5 random wires. Are both ends labeled?
*   [ ] **Chafing**: Check every hole. Is there a grommet?
*   [ ] **Continuity**: Twist wires at one end. Beep test at other end. (Prove it's not broken inside).

## 5. COMMON MISTAKES

*   **"The Short Pull"**: Cutting wire exactly to length. Then realizing you can't reach the breaker.
*   **"Hidden Joint"**: Splicing a short wire in the middle of a wall. **NEVER splice in a conduit.**

---
**Next Step:** Wiring done. Terminate at [02_AC_DC_Panels](./02_AC_DC_Panels.md).

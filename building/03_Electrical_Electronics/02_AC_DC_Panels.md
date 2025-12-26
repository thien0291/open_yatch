# WORK INSTRUCTION: Panels & Termination

**ID:** BLD-03-02
**Role:** Senior Electrician
**Time Est:** 7 Days
**Prerequisites:** Wires run, Furniture installed

---

## 1. OBJECTIVE
Connect the wires to the power. This is where the magic (and fire risk) happens.

---

## 2. TOOLS & SAFETY

### Safety Gear - DANGER HIGH VOLTAGE
*   **Rubber Mat**: Stand on it when working live (only for testing).
*   **Lock Out / Tag Out**: Keep battery switch OFF and key in your pocket.

### Tools
- [ ] Crimping Tool (Ratchet type).
- [ ] Hydraulic Crimper (For battery cables).
- [ ] Heat Gun.
- [ ] Multimeter (Fluke).
- [ ] Torque Screwdriver.

---

## 3. STEP-BY-STEP INSTRUCTIONS

### STEP 1: Battery Bank (The Heart)
**Worker:** Electrician
**Action:**
Connect the big heavy cables.

**Instruction:**
1.  **Lugs**: Strip cable. Put copper lug on.
2.  **Crimp**: Use Hydraulic tool. Hexagon crimp.
3.  **Heat Shrink**: Red (Positive) or Black (Negative) shrink tube over the crimp.
4.  **Covers**: Install plastic terminal covers on battery posts. **Dropped wrench = Explosion.**

**VISUAL GUIDE: CRIMP**
```text
      [ Cable ]==[ Lug ]O
       (Copper)   (Crimp Zone)
       
      BAD:  ( )  <-- Round squeeze (loose)
      GOOD: < >  <-- Hexagon squeeze (tight)
```

---

### STEP 2: The Main Panel
**Worker:** Electrician
**Action:**
Make it look like a computer server room. Neat rows.

**Instruction:**
1.  **Strip**: Remove outer sheath. Keep individual wire insulation intact until the breaker.
2.  **Ferrule**: Crimp a metal "bootlace ferrule" on every stranded wire tip.
    *   *Why?* Screw terminals cut stray strands. Ferrules protect them.
3.  **Insert & Tighten**: Put in breaker. Tighten screw. **PULL TEST**.
4.  **Label**: Stick label on the Panel Front AND the wire inside.

**VISUAL GUIDE: FERRULE**
```text
      Stranded Wire:  ~~~~~  <-- Messy, breaks easily
      Ferrule:       [====]  <-- Solid metal tube
      Breaker:       [Screw]
                       |
                     [====]
```

---

### STEP 3: Bonding (Grounding)
**Worker:** Electrician
**Action:**
Stop corrosion.

**Instruction:**
1.  **Green Wire**: Connect every metal through-hull (seacock), engine, and tank to the Green Bonding Bus.
2.  **Anode**: Connect Bonding Bus to the Zinc Anode on the hull.
3.  **Test**: Resistance from Seacock to Anode must be < 1 Ohm.

---

## 4. QA CHECKLIST

*   [ ] **Pull Test**: Tug every wire in the panel. If it comes out, you fail.
*   [ ] **Torque Check**: Go back and re-tighten all screws (Copper flows/relaxes after 24h).
*   [ ] **Polarity**: Turn on Main Switch. Check Red is + and Black is -.
*   [ ] **RCD Test**: Press the "Test" button on the AC breaker. It MUST trip.

## 5. COMMON MISTAKES

*   **"Hairballs"**: Loose strands of copper sticking out of a breaker. Boom/Flash.
*   **Overtightening**: Stripping the screw thread.

---
**Next Step:** Power is on. Install toys in [03_Electronics_Nav](./03_Electronics_Nav.md).

# WORK INSTRUCTION: Electronics & Navigation

**ID:** BLD-03-03
**Role:** Electronics Tech
**Time Est:** 5 Days
**Prerequisites:** DC Power ready, Helm console finished

---

## 1. OBJECTIVE
Install the eyes and ears of the boat (Radar, GPS, Radio).

---

## 2. TOOLS & SAFETY

### Safety Gear
*   **Harness**: If climbing the mast/arch for Radar.

### Tools
- [ ] Jigsaw (Fine blade).
- [ ] Computer (for software updates).
- [ ] NMEA 2000 Diagnostic tool (Optional).

---

## 3. STEP-BY-STEP INSTRUCTIONS

### STEP 1: The Backbone (NMEA 2000)
**Worker:** Tech
**Action:**
Build the data highway.

**Instruction:**
1.  **Backbone**: Run a central cable from Engine Room to Helm.
2.  **T-Piece**: Add a T-connector for every device.
3.  **Drop Cable**: Connect device to T-Piece. Max length 6m.
4.  **Termination**: You MUST have a resistor (Terminator) at the very start and very end.
    *   *Rule*: 2 Terminators total. Not 1. Not 3.

**VISUAL GUIDE: N2K NETWORK**
```text
      [Terminator]--T--T--T------------------T--[Terminator]
                    |  |  |                  |
                  GPS  |  Depth            Engine
                     Screen
```

---

### STEP 2: Transducers (Sonar)
**Worker:** Tech
**Action:**
Install the "eye" looking down.

**Instruction:**
1.  **Location**: Ahead of the propeller (Clean water). Not behind a strake (Bubbles).
2.  **Install**: Use the plastic housing. Glue with Sikaflex. Hand tighten nut.
3.  **Oil**: If in-hull type, fill cup with mineral oil. No air bubbles!

---

### STEP 3: Radar & VHF
**Worker:** Tech
**Action:**
Install the "eyes" looking out.

**Instruction:**
1.  **Radar**: Mount on arch. Beam must not hit the boat's bow (Blind spot).
2.  **VHF Antenna**: Keep it vertical. Keep it 1m away from GPS antenna (Interference).
3.  **Cable**: Radar cable is thick. Do not bend it sharp (Min radius 10cm).

---

## 4. QA CHECKLIST

*   [ ] **Device List**: Turn on Chartplotter. Go to "Device List". Are all sensors there?
*   [ ] **GPS Lock**: Does it show the correct position?
*   [ ] **MMSI**: Enter the ship's MMSI number into the VHF. (Legal requirement).

## 5. COMMON MISTAKES

*   **Coiling Cables**: Coiling excess Radar/VHF cable in a circle creates an antenna coil (Interference). Lay it in a figure-8.
*   **No Terminator**: The network works intermittently or crashes.

---
**Next Step:** Systems Complete. Move to [04_Interior_Fitout](../04_Interior_Fitout/01_Insulation_Lining.md).

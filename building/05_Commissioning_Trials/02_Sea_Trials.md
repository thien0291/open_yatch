# WORK INSTRUCTION: Sea Trials (Dynamic Testing)

**ID:** BLD-05-02
**Role:** Captain + Engineer + Owner
**Time Est:** 2 Days
**Prerequisites:** Dock Trials Passed. Weather < Force 4.

---

## 1. OBJECTIVE
Break it (if it's going to break) now, not when the owner is on holiday. Verify speed and handling.

---

## 2. TOOLS & SAFETY

### Safety Gear
*   **Liferaft**: Mounted and ready.
*   **VHF Radio**: Tested.

### Tools
- [ ] GPS (Speed measurement).
- [ ] Stop Watch.
- [ ] Note Pad.
- [ ] Noise Meter (dB app on phone).

---

## 3. STEP-BY-STEP INSTRUCTIONS

### STEP 1: Low Speed Handling
**Worker:** Captain
**Action:**
How does she park?

**Instruction:**
1.  **Idle Speed**: Shift FWD / NEUTRAL / REV. Does it clunk? Does it stall?
2.  **Turning Circle**: Hard over at 5 knots.
    *   *Check*: Does the rudder hit the stops?
3.  **Backing**: Reverse in a straight line. Does it walk sideways?

### STEP 2: The "WOT" Run (Wide Open Throttle)
**Worker:** Engineer
**Action:**
Push it to the limit.

**Instruction:**
1.  **Warm up**: Run at 50% load for 15 mins.
2.  **Full Power**: Push throttle to 100%.
3.  **Check RPM**:
    *   *Target*: Engine MUST reach its rated Max RPM (e.g., 3000 RPM).
    *   *Too Low (2800)?* Propeller is too big (Overloaded engine).
    *   *Too High (3200)?* Propeller is too small.
4.  **Temperatures**: Watch the gauge. If it creeps up, the cooling system is too small.

**VISUAL GUIDE: WOT TEST**
```text
   Throttle:  [==========] 100%
   RPM:       [ 3000 ] (Rated)
   Speed:     [ 12 kts ]
   Temp:      [ 85°C ] (Stable)
   
   Result:    PASS.
```

---

### STEP 3: Hard Over Test
**Worker:** Captain
**Action:**
Simulate emergency avoidance.

**Instruction:**
1.  Speed: 15 knots (or max).
2.  Wheel: Turn HARD over.
3.  **Check**:
    *   Does the boat lean dangerously?
    *   Does the prop suck air (cavitate)?
    *   Does the steering lock up?

---

## 4. QA CHECKLIST

*   [ ] **Vibration**: Any rattling at specific RPM? (Shaft alignment issue).
*   [ ] **Noise**: Can you speak normally in the saloon at cruising speed? (< 75dB).
*   [ ] **Dripless Seal**: Check the shaft seal. Is it leaking or getting hot?

## 5. COMMON MISTAKES

*   **Ignoring Overheat**: "It's just a little bit hot." NO. It will seize the engine.
*   **Loose Gear**: Not securing the anchor. It bangs into the hull.

---
**Next Step:** She's a keeper. Final clean and [03_Handover](./03_Handover.md).

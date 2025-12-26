# TEST-PLAN: Verification & Sea Trials Matrix

**Version:** v0.1 (Concept)
**Owner:** Test & Trials Engineer
**Status:** Draft / Gate 6
**References:**
- PRD Requirements: `HLR-*`

---

## 1. Test Philosophy

"Trust but Verify". Every MUST requirement has a corresponding test case.

**Test Categories:**
- **[CAT-1] Visual/Static**: Inspection on land/dock.
- **[CAT-2] Functional (Dock)**: System operation at rest (HAT).
- **[CAT-3] Dynamic (Sea)**: Underway performance (SAT).

---

## 2. Verification Matrix

| Test ID | Category | Requirement | Description | Acceptance Criteria |
|---------|----------|-------------|-------------|---------------------|
| **T-HULL-01** | CAT-1 | HLR-HULL-001 | **Draft Check** | Draft marks read < 1.35m at full load. |
| **T-HULL-02** | CAT-3 | PT-002 | **Turning Circle** | Turn 360 deg at cruise speed. Dia < 3x LOA (~72m). |
| **T-STR-01** | CAT-1 | HLR-STR-002 | **Laminate Audit** | Core samples (cutouts) measured. Thickness matches TDD-STR within -0/+2mm. |
| **T-FLD-01** | CAT-2 | HLR-FLD-002 | **Bilge Alarm Latency** | Pour water into bilge. Alarm sounds < 30 sec. |
| **T-FLD-02** | CAT-2 | HLR-FLD-001 | **Hose Test** | Spray bulkheads/windows (2 bar). Zero water ingress inside. |
| **T-ELEC-01** | CAT-2 | HLR-POW-001 | **RCD Trip Test** | Inject 30mA fault. Breaker trips < 300ms. |
| **T-ELEC-02** | CAT-2 | HLR-POW-002 | **Full Load Heat Run** | Run all AC loads (AC + Cooktop) 1hr. No cable temp > 60°C. |
| **T-GLZ-01** | CAT-2 | HLR-GLZ-001 | **Window Leak** | Direct hose stream on seals. Zero drops inside. |
| **T-STAB-01**| CAT-2 | HLR-SAFE | **Inclining Test** | Move weights, measure heel. Calculated GM > 1.0m. |
| **T-PERF-01**| CAT-3 | PT-001 | **Max Speed** | Full throttle 5 mins (2-way avg). Speed > 16 km/h. |

---

## 3. Sea Trial Protocol (Draft)

1.  **Pre-Start Checks**: Fluid levels, seacocks open, safety gear onboard.
2.  **Dockside Warmup**: Engines idle 15 mins. Temp/Oil pressure stable.
3.  **Low Speed Maneuvering**: Docking tests, thruster check.
4.  **Endurance Run**: 1 hour at Cruise Speed. Check temps/vibration.
5.  **Sprint**: 5 mins at WOT (Wide Open Throttle).
6.  **Emergency Stop**: Crash stop from cruise. Steering check.

---

## 4. Defect Management

- **Critical Defect**: Prevents boat acceptance (e.g., Leak, Overheating, Stability fail).
- **Minor Defect**: Punch list item (e.g., Squeaky door, paint flaw).

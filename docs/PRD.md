# PRD — 80ft River/Nearshore Cruiser (FRP, 2-Deck, Panoramic)

**Document Version:** v0.2 (Draft)
**Owner/DRI:** Orchestrator (AI)
**Date:** 2024-12-26
**Status:** Draft / In Review
**Scope:** Product requirements + program plan + cost control (TDD covers technical “how”)

---

## 0) Document Control

### 0.1 Change Log

| Version | Date | Author | Summary of Changes | Approved By |
| ------- | ---- | ------ | ------------------ | ----------- |
| v0.1 | 2024-12-26 | Orchestrator | Initial PRD skeleton creation | |
| v0.2 | 2024-12-26 | Orchestrator | Updated with detailed template, cost buckets, and traceability structure | |

### 0.2 Stakeholders & Roles (RACI-lite)

| Role | Name | Responsibility | Decision Rights |
| ---- | ---- | -------------- | --------------- |
| Product Owner | User | Final priorities, scope | Final |
| Technical Lead | Orchestrator | Structure + integration | Advisory/Approval |
| Yard/Builder Lead | Build Agent | Execution feasibility | Advisory |
| Safety Reviewer | Reg/Surveyor | Safety acceptance | Approval on safety gates |
| Cost Controller | Cost Engineer | Budget tracking | Veto on overruns (optional) |

### 0.3 Glossary

* **Watertight bulkhead**: A vertical partition separating compartments that prevents water passage.
* **Collision bulkhead**: The foremost watertight bulkhead protecting the bow zone.
* **Slamming zone**: Hull areas (typically forward bottom) subject to high impact loads from waves/debris.
* **Ring frame**: Transverse structural frames forming the "ribs" of the vessel.
* **MVP**: Minimum Viable Product (minimum safe boat).
* **“Price-dead / Giá nát / Giá chuột chết”**: defined in Section 9.

### 0.4 Reference Index

* **Inspiration photos links**: [TBD]
* **Regulatory references**: Vietnam Inland Waterway Standards (QCVN), VR Rules for River Ships.
* **Material vendors list**: [TBD - Local VN Suppliers]
* **TDD links**: 
    - `docs/TDD_HullForm.md`
    - `docs/TDD_Glazing.md`
    - `docs/TDD_Structure.md`
    - `docs/TDD_Build_QA.md`

---

## 1) Executive Summary

### 1.1 One-paragraph summary

Build a **symmetric 80ft (~24m) FRP monohull** optimized for **river cruising** with **semi-luxury** layout, **two decks**, and **panoramic glazing**, while remaining safe enough for occasional **near-shore** operation under defined conditions. Design emphasizes **cost-minimization through modular construction**, salvage where appropriate, and strict **cost control + phased delivery**.

### 1.2 Goals (top-level)

1. **Safe**: Compartmentalization (min 6 zones) + structural integrity + electrical safety for wet environments.
2. **Affordable**: Controlled scope, “price-dead” procurement strategy, modular build.
3. **Comfort & premium feel**: Panoramic glass, 2-deck social spaces, low noise/heat.
4. **Maintainable**: Accessible systems, replaceable window modules, repairable FRP.
5. **Upgradeable**: Allow V2 upgrades (electronics, nearshore package, luxury add-ons) without redesigning hull.

### 1.3 Non-goals (explicitly not in v1)

* Ocean crossings / offshore passages.
* Sailing rig installation (may reserve interface points, but no sail capability required in MVP).
* Full class certification (unless later required by local authorities).
* High-speed planing performance (Target is displacement/semi-displacement efficiency).

### 1.4 Success Metrics (fillable)

| Metric | Target | Measurement Method | When |
| classes | -----: | ------------------ | ---- |
| Max water ingress tolerated | 1 compartment | Flood test plan | Gate 4 |
| Time to detect & respond to bilge | < 30 sec | Alarm + pump tests | Trials |
| Cost variance (final vs budget) | ≤ 10% | PO log vs baseline | Monthly |
| Comfort: interior noise at cruise | ≤ 75 dBA | Decibel meter | Trials |
| Panoramic window leak rate | 0 | Hose test | Gate 4 |

---

## 2) Background & Context

### 2.1 Operating environment

* **Primary**: Rivers/canals (Mekong/Red River), low wave state, shallow areas, debris risk.
* **Secondary**: Near-shore (Vung Tau - Phan Thiet coastal runs):
  * **Max wind**: Beaufort 4 (< 16 knots)
  * **Max sea state**: Wave height < 1.2m
  * **Daylight-only / good weather only**: Yes
  * **Max distance from safe harbor**: 20 nm

### 2.2 Constraints

* **Budget envelope**: [TBD] total; hull shell budget target: [TBD]
* **Build location**: Vietnam (Local shipyard/composite shop)
* **DIY/yard hybrid**: Professional hull shell, owner-managed fit-out/systems (Assumption).
* **Timeline**: [TBD months]

### 2.3 Key decisions already made

* Symmetric hull (no asymmetry).
* FRP/composite construction.
* Variable thickness by zone (bow thick, cabin walls thin).
* Panoramic windows desired; must not compromise safety.
* AC-first 220V electrical architecture.

### 2.4 Assumptions (must be explicit)

* **A1**: Near-shore use is strictly limited to “good weather windows”.
* **A2**: River debris impacts are more likely than heavy wave slamming -> Reinforce bow/waterline.
* **A3**: Build can be staged; boat can operate as MVP then upgraded.
* **A4**: Propulsion system (Donor Hybrid/EREV) will be designed separately (TDD-PROP).

### 2.5 Open Questions (initial)

* **OQ-001**: Final LOA/Beam/Draft targets? (Working assumption: 24m / 6.2m / 1.3m)
* **OQ-002**: Maximum near-shore conditions? (Defined in 2.1)
* **OQ-003**: Window size/modules approach? (Pending Glazing Engineer)
* **OQ-004**: Required number of watertight compartments? (Target 6+)
* **OQ-005**: Deckhouse material strategy? (Likely sandwich for weight reduction)

---

## 3) Users, Personas, Use Cases

### 3.1 Personas

* **P1 Owner-operator**: Values cost control + modular upgrade path.
* **P2 Family passengers**: Comfort, safety, easy boarding, shade.
* **P3 Guests**: Premium feel, panoramic views.
* **P4 Maintenance**: Access, replaceability, standard parts.

### 3.2 Primary Use Cases

* **UC-001 Day river cruise**: 5–20 km, low speed (10-15 km/h).
* **UC-002 Dock/anchor overnight**: Hotel load on battery/genset.
* **UC-003 Entertainment**: 6–20 guests, rooftop party, dining.
* **UC-004 Near-shore “fair weather” day trip**: Transit between river mouths.
* **UC-005 Emergency scenarios**: Water ingress, fire, electrical shock risk, grounding.

### 3.3 User Stories (start list)

* **US-001**: As owner, I can detect water ingress early with alarms in every compartment.
* **US-002**: As passenger, I can move safely between decks (handrails, non-slip) even in mild chop.
* **US-003**: As owner, I can replace a broken window module within 48 hours using standard tools.
* **US-004**: As owner, I can keep operating (limp home) if one compartment floods.
* **US-005**: As owner, I can keep costs within budget via strict change control.

---

## 4) Product Scope

### 4.1 MVP Definition (Minimum Safe Boat)

MVP includes:
* Hull shell + deck(s) + essential structure.
* Compartmentalization (watertight bulkheads per spec).
* Primary access, basic habitability shell.
* Basic safety: bilge pumps, alarms, fire basics.
* Minimal glazing modules installed (or placeholders) with leak test.
* Propulsion functional (basic).

MVP excludes:
* Full luxury fit-out (cabinetry, high-end finish).
* Near-shore electronics package (radar, advanced plotter).
* Air conditioning (initial install may just be ventilation).

### 4.2 V1 / V2 / V3 Roadmap

* **V1 (River MVP)**: Functional hull, safe for river, basic amenities.
* **V2 (Comfort)**: Semi-luxury interior, full glazing, AC, finish upgrades.
* **V3 (Coastal)**: Near-shore package: nav, comms, extra safety gear, weatherproofing.

---

## 5) High-Level Requirements (HLR)

*See `docs/requirements.csv` for traceable list.*

### 5.1 Hull Form & Geometry (HLR-HULL)

* **HLR-HULL-001 (MUST)**: Symmetric monohull, LOA ~24m with wide stern profile for space and stability.
    * Acceptance: Lines plan + principal dimensions signed off.
    * Owner: Naval Architect.
* **HLR-HULL-002 (MUST)**: Draft suitable for river operation (<1.5m) while stable enough for near-shore.
    * Acceptance: Meets draft target + stability analysis.

### 5.2 Structural Integrity (HLR-STR)

* **HLR-STR-001 (MUST)**: Hull structure must survive defined load cases (river debris, nearshore slam) without failure.
* **HLR-STR-002 (MUST)**: Variable thickness / reinforcement by zone.
    * Acceptance: Laminate schedule by zone approved.

### 5.3 Anti-sinking & Flooding Control (HLR-FLD)

* **HLR-FLD-001 (MUST)**: Compartmentalization: at least 6 watertight zones + collision bulkhead.
    * Acceptance: Bulkhead plan + watertight test.
* **HLR-FLD-002 (MUST)**: Flood event detection within 30 seconds and bilge pumping capacity adequate for leak rate.

### 5.4 Panoramic Glazing (HLR-GLZ)

* **HLR-GLZ-001 (MUST)**: Panoramic glass must not compromise global hull/deck stiffness.
    * Acceptance: Ring frame / reinforcement design.
* **HLR-GLZ-002 (SHOULD)**: Modular window strategy (repeatable sizes) to reduce cost.

### 5.5 Two Decks & Human Safety (HLR-2DK / HLR-SAFE)

* **HLR-2DK-001 (MUST)**: Two-deck configuration must meet stability targets and safe access.

### 5.6 Maintainability & Repair (HLR-MNT)

* **HLR-MNT-001 (MUST)**: Key structural and leak-prone areas must be accessible for inspection.

---

## 6) Detailed Requirements — Hull & Structure (Core)

### 6.1 Principal Dimensions & Layout Envelope

* **DR-HULL-001**: LOA target: 24m ± 0.5m
* **DR-HULL-002**: Beam target: 6.2m ± 0.2m (Target)
* **DR-HULL-003**: Draft target: 1.3m (Max 1.5m)
* **DR-HULL-004**: Freeboard minimum at midship: [TBD by NA]
* **DR-HULL-005**: Upper deck live load target: [TBD kg/m²]

### 6.2 Structural Concept Requirements (3D “box beam”)

* **DR-STR-001**: Longitudinal stringers + transverse ring frames (3D grid).
* **DR-STR-002**: Frame spacing target: ~600-800mm (TBD by Structure Eng).
* **DR-STR-003**: Double-bottom: Optional (Value engineering decision).

### 6.3 Zone-based Laminate Requirements

| Zone | Location | Threat | Strategy | Target |
| ---- | -------- | ------ | -------- | ------ |
| Z1 | Bow impact | debris/impact | Thicker solid FRP + extra frames | High |
| Z2 | Forward bottom | slamming | Thicker laminate + closer frames | High |
| Z3 | Mid bottom | bending | Standard laminate + stringers | Med |
| Z4 | Side shell | impact | Medium laminate | Med |
| Z5 | Sheer band | global stiffness | Reinforced belt line | High |
| Z6 | Deckhouse walls | low impact | Thinner sandwich/solid | Low |
| Z7 | Window surround | stress | Ring frames + inserts | High |

### 6.4 Watertight Compartment Requirements

* **DR-FLD-001**: Collision bulkhead located at station [TBD].
* **DR-FLD-002**: Watertight bulkheads at stations: [TBD].
* **DR-FLD-003**: Penetrations must use sealed collars.
* **DR-FLD-004**: Bilge routing shall not allow “free flood”.

### 6.5 Glazing / Cutout Rules

* **DR-GLZ-001**: No hull cutouts below 1.0m above waterline (Target).
* **DR-GLZ-002**: Panoramic windows modular: max single module size [TBD].
* **DR-GLZ-003**: Every window group requires ring-frame reinforcement.

---

## 7) Safety Requirements (High-level)

### 7.1 Flooding
* **SR-001**: High-water alarm in each zone.
* **SR-002**: Bilge pump redundancy (min: 2 pumps + manual backup).

### 7.2 Fire & CO
* **SR-010**: Fire extinguishers count/placement per VR rules.
* **SR-011**: CO alarm for any combustion source.

### 7.3 Escape & Life Safety
* **SR-020**: Two escape paths from main living area.

---

## 8) Performance Targets (Boat-level)

* **PT-001**: River cruising speed: 10-15 km/h. Max: 18 km/h.
* **PT-002**: Handling: Able to turn within 2x LOA.
* **PT-003**: Near-shore: Operation only within "Fair Weather" envelope.

---

## 9) Cost Control (PRD-critical)

### 9.1 Definitions
* **Price-dead / Giá nát**: Material cost + consumables for MVP function.
* **Baseline Budget**: Approved at Gate 0.

### 9.2 Budget Buckets (Estimates TBD)
* **Hull Shell**: FRP, core, resin, frames.
* **Deck/Structure**: Decks, internal structure.
* **Glazing**: Glass, adhesive, frames.
* **Safety (MVP)**: Bilge, electrical safety.

### 9.3 Estimation Classes
* **Class D**: ±50% (Concept) -> **Class A**: ±5% (Build)

### 9.4 Cost Tracking
* **PO Log**: Tracking Estimate vs Actual.
* **Variance Policy**: >10% variance triggers review.

### 9.5 Make vs Buy
* **Strategy**: Local source (VN) > Salvage > Import new.
* **Modularize**: Standardize window sizes to reduce custom glass costs.

---

## 10) Project Plan & Gates

* **Gate 0**: Requirements freeze (MVP) - *Current*
* **Gate 1**: Hull structure design ready (Concept)
* **Gate 2**: Hull shell engineering complete
* **Gate 3**: Watertight zoning validated
* **Gate 4**: Deck + glazing rough-in
* **Gate 5**: Trials

---

## 11) QA / Acceptance / Test Plan

### 11.1 Traceability
* Map: Req ID -> TDD Section -> Test Case.

### 11.2 Acceptance Tests
* **AT-HULL-001**: Visual + tap test + thickness sampling.
* **AT-FLD-001**: Flood test (controlled).
* **AT-GLZ-001**: Hose test (leak inspection).

---

## 12) Risks & Mitigations

| Risk ID | Risk | Likelihood | Impact | Mitigation |
| ------- | ---- | ---------- | ------ | ---------- |
| R-001 | Window leaks | M | H | Modular frames + extensive testing |
| R-002 | Hull too flexible | M | H | Belt line reinforcement + ring frames |
| R-003 | Cost blow-up | H | M | Strict "Price-dead" policy + MVP scope |
| R-004 | Weight overrun | H | H | Weight budget tracking from Day 1 |

---

## 13) Open Questions & Decision Log

### 13.1 Decision Log (ADR-lite)
* **ADR-001**: Project Scope - 24m River/Nearshore, Symmetric, FRP.

### 13.2 Open Questions Backlog
* **OQ-001**: Exact Beam dimension (6.0 vs 6.5)?
* **OQ-002**: Exact draft limit?
* **OQ-003**: Window module dimensions?

---


Got it. Here’s a **PRD-ready “Vibe + Cost-First Principles” section** you can paste near the top of the PRD (either in **Executive Summary** or as a new **Section 2.6**). It sets the tone: **$150k is the law**, and we win by **architecture + modularity + salvage + phased delivery**, not by “yacht standards”.

---

## Cost-First First-Principles Vibe (North Star)

### Why this project exists

We are not building a “standard yacht.” Standard yacht methods assume expensive tooling, custom marine components, and vendor lock-in. That path is incompatible with our hard constraint:

* **Hard CAPEX ceiling: $150,000 USD total (all-in).**
* Any design that cannot plausibly ship within this ceiling is out of scope, regardless of how “correct” it is in traditional marine standards.

This project exists to prove that an 80ft river/nearshore cruiser can be built safely and comfortably by applying **first principles + non-traditional engineering + disciplined cost control**.

### First principles we will not violate

1. **Physics doesn’t negotiate.**
   We can’t “hack” away basic structural loads, stability, watertightness, electrical shock risk, CO/fire risk, or leak paths. We can only change *how* we achieve safety—cheaper, simpler, more modular.

2. **Safety is a requirement; luxury is a variable.**
   We will reduce cost by cutting optional features and finish quality, not by cutting the minimum safety envelope.

3. **Cost is a design parameter, not an accounting output.**
   Every major design choice must include an explicit cost model and a cost owner. If we can’t estimate it, we don’t build it.

4. **Modularity beats craftsmanship.**
   We avoid complex curves, one-off parts, and bespoke hardware. We design around repeatable modules: panels, frames, windows, furniture blocks.

5. **Leverage mass production ecosystems.**
   Wherever safe, we use:

   * Salvaged / donor systems (automotive EREV/PHEV, industrial parts)
   * Consumer 220VAC appliances
   * Commodity materials (FRP fabrics, resins, standard glass sizes)
   * Local fabrication instead of imported marine boutique parts

6. **Phased delivery is how we stay under $150k.**
   We ship an MVP that is safe and operable on rivers first; we add “semi-luxury” and nearshore capability only if cost remains within the ceiling.

---

## $150k Cost Strategy (How we intend to win)

### Cost envelope rules

* **Total ceiling:** $150,000.
* **No exceptions** without a written scope change and explicit funding source.
* The budget is split into **immutable buckets**; moving money between buckets requires approval.

**Proposed bucket targets (editable):**

* Hull shell + primary structure (watertight zones): **$40k–$70k**
* Deckhouse + basic glazing (MVP level): **$15k–$35k**
* Basic safety (bilge, alarms, fire basics): **$3k–$10k**
* Minimal interior shell (floor, walls, basic sanitary): **$10k–$25k**
* Propulsion integration (separate PRD/TDD): **$15k–$45k**
* Tools/jigs/consumables: **$5k–$15k**
* Contingency reserve (mandatory): **10–15%**

> These numbers are not commitments; they’re a starting cost hypothesis we will refine into Class C/B estimates.

### Cost reduction playbook (approved tactics)

We actively pursue the following non-traditional tactics:

**A) Geometry choices that cut labor**

* Prefer **developable surfaces** (flat/low-curvature) over compound curves.
* Use **panelized construction** (large flat/single-curvature FRP panels) then bond + tape.
* Standardize spacing for frames/stringers.

**B) Manufacturing method choices**

* Use **controlled hand layup** or **low-cost infusion** for large panels (tooling-light).
* Minimize fairing by designing surfaces that don’t need yacht-level perfection.

**C) Salvage ecosystem**

* Salvage major subsystems where it reduces cost and lead time, provided safety tests are passed.
* Maintain a “salvage acceptance checklist” (inspection, test, replacement parts availability).

**D) Window & luxury cost control**

* Panoramic look achieved via **many repeated window modules**, not giant one-piece glass.
* “Luxury” comes from layout and lighting, not expensive marine-only hardware.

**E) Consumer 220VAC strategy**

* Use consumer appliances where safe and maintainable.
* Marine-grade only where failure is catastrophic (electrical protection, watertight penetration hardware, etc.).

---

## Cost Governance (How we prevent budget death)

### Change control

Any change that impacts:

* cost by > **$500** (or TBD),
* schedule by > **1 week** (or TBD),
* or touches any safety requirement,
  must go through a **Change Request** with:
* cost estimate (range + confidence),
* alternatives,
* acceptance criteria,
* and explicit approval.

### “Stop-the-line” triggers

We pause work and re-plan if:

* any bucket exceeds **+15%** forecasted variance,
* a safety requirement is compromised to save cost,
* or a major subsystem cannot be estimated within Class C confidence.

### Definition of MVP vs “nice to have”

* MVP is defined by **safety + operability**.
* Everything else is **tiered**:

  * Tier 0: Must ship (safety/structure/watertight)
  * Tier 1: Needed for comfort/basic living
  * Tier 2: Semi-luxury upgrades
  * Tier 3: Nearshore upgrades

---

## The tone of the project (one paragraph you can keep at the top)

We are building an 80ft cruiser under a hard $150k ceiling by combining first-principles engineering with non-traditional sourcing and modular construction. We will not sacrifice safety, but we will sacrifice tradition, polish, and “marine boutique” parts. Every feature must justify itself in cost and risk. If it doesn’t fit, it doesn’t ship.

---

If you want, I can now:

1. **Insert this into the PRD v0.1** at the right sections and
2. Draft the next PRD sections in the same tone: **Goals/Non-goals**, **MVP definition**, and a **cost-gated requirements list** (MUST/SHOULD/COULD) specifically for **hull shell + watertight + panoramic windows**.

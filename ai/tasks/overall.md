Dưới đây là **quy trình A–Z cực chi tiết** để Orchestrator điều phối toàn bộ đội agent (PM/NA/Structure/Flooding/Glazing/Electrical/Cost/Build/Compliance/Test/Doc). Bạn có thể copy nguyên văn vào Cursor làm “runbook”, và dùng như SOP vận hành “đội kỹ sư ảo”.

Mình thiết kế theo kiểu **gates** (giống software release), có **deliverables, file outputs, owner agent, checklist, tiêu chí pass/fail**, và **luồng xử lý khi có mâu thuẫn**.

---

# 0) Mục tiêu & nguyên tắc điều phối (Orchestrator Charter)

## 0.1 Mục tiêu Orchestrator

* Tạo & duy trì **PRD (WHAT/WHY)** + **TDD (HOW)** + **BOM/BoQ/Cost** + **TestPlan** ở trạng thái nhất quán.
* Biến yêu cầu của bạn thành:

  * cấu trúc hull/compartment/kính/điện 220V có thể thi công
  * kế hoạch build + QA gates
  * cost control “giá nát” + “safe minimum”

## 0.2 Quy tắc bất biến

1. **Safety không bị trade lấy giá** (flooding, điện giật, cháy, CO, kính, ổn định).
2. **Không viện lý do “tiêu chuẩn cổ”** để đội giá; nhưng bất cứ shortcut nào ảnh hưởng safety phải:

   * nêu rõ rủi ro
   * có mitigation
   * và phải được “explicitly accepted” bằng Decision Log.
3. **Tất cả outputs phải traceable**: PRD Req ID ↔ TDD section ↔ Test case.
4. **Freeze theo gate**: sau khi qua gate, chỉ thay đổi bằng Change Control.

---

# 1) Repo structure chuẩn (Orchestrator tạo ngay từ đầu)

**Folder**

* `/docs/PRD.md`
* `/docs/requirements.csv`
* `/docs/TDD_Index.md`
* `/docs/TDD_HullForm.md`
* `/docs/TDD_Structure.md`
* `/docs/TDD_Flooding.md`
* `/docs/TDD_Glazing.md`
* `/docs/TDD_Electrical_AC220.md`
* `/docs/TDD_Build_QA.md`
* `/docs/Cost_HullShell.md`
* `/docs/BoQ_HullShell.csv`
* `/docs/WeightBudget.csv`
* `/docs/TestPlan.md`
* `/docs/Compliance_Minimum.md`
* `/docs/ADR_Log.md`
* `/docs/Risk_Register.md`
* `/docs/Drawing_List.md`
* `/docs/Calc_List.md`
* `/docs/Project_Assumptions.md`

**Naming conventions**

* Requirement: `HLR-*` (high level), `DLR-*` (detailed)
* Drawings: `DWG-###`
* Calculations: `CALC-###`
* Decisions: `ADR-###`
* Risks: `RISK-###`
* Tests: `TEST-###`

**Orchestrator Done**

* Repo có đủ file skeleton + index.

---

# 2) Inputs Orchestrator cần “lock” (đầu vào tối thiểu)

Orchestrator tự set default nếu thiếu, nhưng phải ghi rõ “ASSUMPTION”.

## 2.1 Mission profile (default)

* River daily: 5–20 km/day
* Occasional nearshore: fair weather
* 2 decks, panoramic glazing
* FRP composite, symmetrical hull
* AC-first 220V loads
* Donor hybrid/EREV propulsion (tách khỏi hull cost)

## 2.2 Key numeric placeholders (để agent tính)

* LOA: 24m
* Beam: 6.2m (placeholder)
* Draft: 1.3m (placeholder)
* Displacement rough range: 25–45t (placeholder, to be refined)
* Max speed target: 10–18 km/h (placeholder)

Orchestrator tạo file:

* `/docs/Project_Assumptions.md` (hoặc section trong PRD)

---

# 3) Gate-based Process (A–Z)

## Gate 0 — Kickoff & PRD Skeleton (1–2 vòng chạy)

### Mục tiêu

Có PRD outline + requirement framework + decision/risk framework.

### Task 0.1 — PRD skeleton

**Owner:** PRD Author
**Inputs:** mission profile + constraints
**Output:**

* `/docs/PRD.md` (outline + fill-in prompts)
* `/docs/requirements.csv` (schema + 20–50 HLR seed)
  **Pass criteria**
* Có MoSCoW priority, acceptance criteria, verification method.
  **Fail triggers**
* Requirements mơ hồ, không testable.

### Task 0.2 — Doc librarian setup

**Owner:** Document Librarian
**Outputs:**

* `/docs/TDD_Index.md`
* `/docs/Drawing_List.md` + `/docs/Calc_List.md` skeleton
  **Pass criteria**
* Index link đúng file, IDs nhất quán.

### Orchestrator Integrate (Gate 0 review)

**Orchestrator outputs:**

* `/docs/ADR_Log.md` seed (ADR-001: “Project scope & constraints”)
* `/docs/Risk_Register.md` seed (10 risks ban đầu)
* “Next tasks plan” cho Gate 1

**Gate 0 Done**

* PRD skeleton + requirements.csv có ID chuẩn.
* Index doc đã tạo.

---

## Gate 1 — Concept Design (hình dáng + khoang + kính cấp concept)

### Mục tiêu

Chốt concept hull form + GA + zoning khoang + strategy kính.

### Task 1.1 — Hull form & GA concept

**Owner:** Naval Architect
**Outputs:**

* `/docs/TDD_HullForm.md`
* Bảng Bulkhead Plan (station positions)
* GA text layout 2 decks
  **Must include**
* symmetry below waterline
* transom wide, bow fine entry
* draft/freeboard justification nearshore
  **Pass criteria**
* Có bulkheads + crash box + escape logic.

### Task 1.2 — Flooding/Watertight concept

**Owner:** Flooding Engineer
**Outputs:**

* `/docs/TDD_Flooding.md`
* “penetration policy” + bilge zoning concept
  **Pass criteria**
* Ít nhất 5–8 zones, crash box, rules xuyên vách.

### Task 1.3 — Glazing concept

**Owner:** Glazing Engineer
**Outputs:**

* `/docs/TDD_Glazing.md` concept version
* window module plan (repeatable sizes)
* ring-frame concept around openings
  **Pass criteria**
* Không đề xuất “1 tấm kính khổng lồ”; có mullions; tránh shear line.

### Orchestrator Integrate (Gate 1 review)

**Orchestrator làm 4 việc:**

1. Update PRD requirements: add/adjust HLR-HULL/SAFE/GLAZE.
2. Tạo mâu thuẫn list (Conflicts):

   * bulkhead vs panoramic placement
   * escape routes vs long windows
3. Create ADRs cho các lựa chọn:

   * ADR-002: Bulkhead count & positions
   * ADR-003: Window module strategy
4. Update risk register (window leaks, CG 높 do 2 decks)

**Gate 1 Done**

* Có concept 2 decks + watertight zoning + glazing strategy nhất quán.

---

## Gate 2 — Preliminary Engineering (kết cấu 3D + laminate zones + stability/weight baseline)

### Mục tiêu

Có cấu trúc đủ để “tính vật tư vỏ” và không tự sát vì ổn định/CG.

### Task 2.1 — Composite structure concept + laminate schedule

**Owner:** Composite Structural Engineer
**Outputs:**

* `/docs/TDD_Structure.md`
* Laminate Schedule table by zones:

  * bottom forward slam, bottom mid, sides, deck, cabin sides, window belt, transom
* Grid plan: ring frames spacing + longitudinals spacing
* Joint/tabbing schedule concept
  **Pass criteria**
* Zone-based thickness (mũi dày, cabin mỏng) rõ ràng.
* Có “no-core zones” dưới waterline (trừ khi có biện minh).

### Task 2.2 — Weight & stability baseline

**Owner:** Stability & Weight Engineer
**Outputs:**

* `/docs/TDD_StabilityWeight.md`
* `/docs/WeightBudget.csv`
* CG/GM guidance; plan inclining test
  **Pass criteria**
* Có “keep heavy low” plan & warning cho 2 decks.

### Orchestrator Integrate (Gate 2 review)

**Orchestrator kiểm:**

* laminate & weight không mâu thuẫn (ví dụ vỏ quá nặng → draft tăng)
* glazing cutouts có reinforcement trong structure doc
* update PRD performance targets & acceptance criteria
* create CALC placeholders:

  * CALC-001 hydrostat rough
  * CALC-002 global bending rough
  * CALC-003 window opening local reinforcement
* Update ADR nếu có tradeoff (solid vs sandwich ở cabin)

**Gate 2 Done**

* Có laminate schedule + weight budget baseline đủ để đi vào cost hull.

---

## Gate 3 — Hull Shell Costing (BoQ/BOM vỏ, 3 kịch bản)

### Mục tiêu

Có **BoQ Hull Shell** và “cost control system” để giữ ngân sách.

### Task 3.1 — Cost breakdown hull shell only

**Owner:** Cost Engineer – Hull Shell Only
**Inputs:** laminate schedule + grid + bulkheads
**Outputs:**

* `/docs/Cost_HullShell.md`
* `/docs/BoQ_HullShell.csv`
* 3 scenarios: Cheapest safe / Balanced / Safer
* confidence rating + cost risks
  **Pass criteria**
* BoQ có unit, qty, unit cost assumption, totals.
* Tách material vs labor.
* Tách consumables + tooling + fairing baseline.

### Orchestrator Integrate (Gate 3 review)

**Orchestrator:**

* Update PRD section Cost Control (buckets, ceilings, change control)
* Create ADR-004: “Choose cost scenario S1/S2/S3 as baseline”
* Create RISK entries: price volatility resin/glass, labor rework due to QC

**Gate 3 Done**

* Bạn nhìn vào BoQ là biết “vỏ” đang ở bao nhiêu, điểm đội tiền ở đâu.

---

## Gate 4 — Electrical AC-first architecture (chỉ kiến trúc + an toàn, chưa mua)

### Mục tiêu

Có sơ đồ 220V để dùng đồ dân dụng mà không giật người.

### Task 4.1 — AC-first design + protection

**Owner:** Electrical Engineer (AC-First 220V)
**Outputs:**

* `/docs/TDD_Electrical_AC220.md`
* `/docs/LoadList_Template.csv`
  **Pass criteria**
* RCD/RCBO strategy, wet zones, earthing/bonding plan.
* Shore power plan (nếu có) có isolation/galvanic strategy.

### Orchestrator Integrate (Gate 4 review)

* Update PRD requirements HLR-POW-* with acceptance tests
* Add TEST cases for electrical safety
* Add RISK: AC-only misuse, moisture ingress

---

## Gate 5 — Build Plan + QA Gates (hull shell)

### Mục tiêu

Có “how to build” và checklist hold points để không đổ bể.

### Task 5.1 — Build & QA procedures

**Owner:** Build & QA Engineer
**Outputs:**

* `/docs/TDD_Build_QA.md`
* Checklists:

  * jig/strongback
  * layup/infusion QA
  * tabbing QA
  * watertight test
  * surface prep
    **Pass criteria**
* Có gate hold points: “không qua không làm tiếp”
* Có failure modes + prevention

### Orchestrator Integrate (Gate 5 review)

* Update PRD Project Plan & QA sections
* Define Gate acceptance: photos, measurements, test logs required
* Add RISK: cure conditions humidity/temp VN

---

## Gate 6 — Compliance & Test Plan

### Mục tiêu

Có checklist giấy tờ/tài liệu & test plan để chạy thử an toàn.

### Task 6.1 — Minimum compliance documentation

**Owner:** Regulatory/Survey Consultant
**Outputs:**

* `/docs/Compliance_Minimum.md`
  **Pass criteria**
* Không bịa luật; nêu câu hỏi cần xác minh địa phương.

### Task 6.2 — Verification test matrix

**Owner:** Test & Sea Trials Engineer
**Outputs:**

* `/docs/TestPlan.md`
* Test matrix: Req → method → acceptance → evidence
  **Pass criteria**
* Test coverage cho flooding, electrical, glazing leaks, stability checks.

### Orchestrator Integrate (Gate 6 review)

* Ensure every MUST requirement has at least one test method
* Create ADR-005: “Operational limits nearshore” wording
* Update PRD acceptance criteria

---

# 4) Change Control System (Orchestrator vận hành xuyên suốt)

## 4.1 Types of changes

* **Spec changes** (beam/draft, window size, bulkhead count)
* **Cost changes** (>X USD)
* **Safety-impact changes** (watertight, electrical protection, glazing)

## 4.2 Workflow

1. Change request (CR-###) filed in PRD (appendix)
2. Impact analysis by relevant agents:

   * structure + cost + flooding + stability + build/QA
3. Orchestrator compiles:

   * ΔCost, ΔRisk, ΔSchedule
4. Decision:

   * accept/reject/defer → logged as ADR
5. Update files + traceability

**Template CR**

* CR ID | Description | Reason | Impacted Req IDs | Impact analysis | Decision | Date

---

# 5) Conflict Resolution (khi agent mâu thuẫn)

## 5.1 Orchestrator conflict checklist

* Conflict type:

  1. Geometry conflict (kính vs bulkhead)
  2. Weight/stability conflict (2 tầng vs kính vs laminate)
  3. Cost conflict (S1 vs safety)
  4. Buildability conflict (infusion vs shop capability)
* For each conflict:

  * propose 2 options
  * quantify impacts
  * create ADR to lock choice

## 5.2 Escalation rule

Nếu conflict ảnh hưởng safety → bắt buộc review bằng “human expert” (survey/engineer), hoặc giới hạn operating envelope.

---

# 6) Orchestrator Weekly / Iteration cadence (thực tế để bạn chạy)

Mỗi iteration (1–2 giờ làm việc với Cursor):

1. Orchestrator đọc diff các docs
2. Update requirements.csv + traceability
3. Assign next tasks (3–6 tasks/iteration)
4. Run specialist agents
5. Integrate + create ADR/RISK/TEST updates
6. Freeze a “release” snapshot: `v0.x`

---

# 7) “Definition of Done” cho từng artifact

## PRD Done (v1)

* 100% MUST requirements có acceptance criteria + test method
* Cost control + change control đầy đủ
* Phases/gates rõ

## Hull/Structure Done (v1)

* Laminate schedule theo zone
* Frame plan + bulkhead plan
* Glazing reinforcement integrated
* Weight budget baseline consistent

## Cost Hull Done (v1)

* BoQ có line-items + confidence + risks
* 3 scenarios + baseline chosen

## QA/Build Done (v1)

* Hold points + checklists + evidence requirements

---

# 8) Bộ “Orchestrator Master Prompt” (bạn dán vào Cursor để chạy mỗi vòng)

> You are the Orchestrator for Project: 80ft FRP symmetric river + nearshore cruiser, 2 decks, panoramic glazing, AC-first 220V.
> Your job is to coordinate specialist agents and produce an integrated PRD + TDD package with traceability and cost control.
> Steps each iteration:
>
> 1. Read `/docs/PRD.md`, `/docs/requirements.csv`, `/docs/TDD_Index.md`, and any updated TDD docs.
> 2. Identify gaps, conflicts, and missing assumptions. Propose defaults.
> 3. Assign 3–6 tasks max to specialist agents, each with: inputs, outputs, and done criteria.
> 4. After tasks, integrate outputs: update PRD requirements, TDD Index, Drawing/Calc lists, TestPlan.
> 5. Update `ADR_Log.md` and `Risk_Register.md`.
>    Output format: Markdown with sections: Summary, Decisions (ADR), Risks, Conflicts, Next Tasks, File Updates.

---

Nếu bạn muốn, mình có thể:

* viết **file skeleton** cho toàn bộ `/docs/*.md` và `/docs/*.csv` (đúng format IDs) để bạn paste vào repo ngay,
* và tạo **1 “iteration 0” task list** dựa trên những gì bạn đã chốt (symmetry + zone thickness + panoramic + nearshore).

# Hardware Product Development & NPI Governance Framework 

This repository captures the control system used to run a fully custom 4G IoT alarming system program through EVT → DVT → PVT → Mass Production (EU & US).
It is written as an owner-style governance model: define what can drift, set gates, and enforce convergence before ramp.

---

## 0) Program Baseline (What was custom)
The reference program was a fully custom hardware ecosystem:
- 4G SIM communication module integration
- 8-sensor pairing behaviour (system-level function)
- Custom PCBA
- New injection-moulded plastic housing (tooling required)
- Custom silicone components
- Precision metal components
- Retail color box packaging & accessory kitting

No off-the-shelf enclosure or packaging platform was used.

---

## 1) Governance Goal (What we prevented)
NPI governance existed to prevent four failure modes:
1) Stage drift: moving forward without readiness
2) Tooling drift: T1/T2/T3 loops not converging (warpage/shrinkage/cosmetics)
3) Vendor drift: cross-vendor schedules and dependencies desynchronizing
4) Ramp drift: defects propagating into MP without containment

---

## 2) Gate Authority Model (EVT → DVT → PVT → MP)

### EVT Gate — Engineering Feasibility Convergence
**Entry:** design inputs available for prototype build and integration checks.
**Exit (must be true before DVT):**
- CNC prototype build completed for integration learning
- Housing-to-PCBA integration is mechanically workable
- Sensor pairing feasibility is demonstrated at engineering level
- Initial assembly direction is defined (not optimized yet)

### DVT Gate — Design & Compliance Convergence
**Entry:** EVT learnings closed with design updates ready for validation builds.
**Exit (must be true before PVT):**
- Core functional stability verified:
  - Multi-sensor pairing stability
  - 4G communication stability
  - Audio volume adjustment works consistently
- Reliability validation executed for program needs:
  - IPX7 waterproof validation
  - High/low temperature validation
  - Drop & impact validation
- CE and FCC compliance testing coordination completed
- Design revisions frozen after DVT validation

### PVT Gate — Production Repeatability Convergence
**Entry:** design is frozen and tooling/line are ready to prove repeatability.
**Exit (must be true before MP authorization):**
- Tooling iteration is in a stable state (T1/T2/T3 loop closed)
- Production line test is ready and coverage is confirmed
- Firmware flashing stability verified on the line flow
- Packaging quality criteria enforced and kitting verified (no missing parts risk)
- Yield and test pass rate show stable trend (reference: ~95–97% yield, ~96–98% pass rate)

### MP — Ramp & Containment Discipline
After MP start, changes are controlled to avoid re-introducing instability.
Critical functional deviations trigger containment actions (hold/stop/escalate) before shipment.

---

## 3) Tooling & Mechanical Control (Injection Housing)
The plastic housing required new tooling and T1/T2/T3 validation cycles.
Tooling was governed until convergence across:
- Warpage and shrinkage stabilization
- Surface cosmetic standard enforcement
- Dimensional alignment across mating parts
- Assembly fit verification before stage progression

Tooling adjustments and injection parameter refinements were validated before moving to the next gate.

---

## 4) Production-Line Governance (Traceable Functional Control)
The assembly line integrated the client’s proprietary testing software for device-level traceability and transparent test status monitoring.
Functional coverage included multi-sensor pairing checks, 4G communication checks, and audio/volume verification.

When critical functional inconsistency was detected, line progression was halted to prevent defect propagation.

---

## 5) Cross-Vendor Synchronization (Dependency Control)
The program required aligned execution across:
tooling, molding, silicone, metal, PCBA, sensor, packaging, and OEM assembly.

Owner control meant synchronizing:
- unit-level BOM cost breakdown
- lead time dependencies across vendors
- tooling iteration cycles against build schedules
- stage timing so validation and ramp were not compromised

---

## 6) What this model proves
This framework demonstrates owner-level control of a fully custom hardware ecosystem:
stage-gated governance, tooling convergence, traceable line testing, cross-vendor synchronization, compliance coordination, and ramp stabilization.


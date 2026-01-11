# FreeSBC

FreeSBC is an open-source **Session Border Controller (SBC)** with **billing and call accounting as first-class capabilities**.

Unlike SBCs that only focus on signaling and security, FreeSBC is designed around a core principle:

> **In VoIP systems, billing is not an add-on — it is the foundation.**

FreeSBC provides a reliable edge control layer combined with **accurate, deterministic, and auditable call billing primitives**, making it suitable for carrier-grade and operator-grade deployments.

---

## Why Billing Comes First

In commercial VoIP and VOS-class systems, the most critical function is not routing or signaling — it is **billing correctness**.

FreeSBC is built around this reality:

- Every call must produce **trustworthy Call Detail Records (CDRs)**
- Billing decisions must be **deterministic and explainable**
- Charging logic must survive failures, retries, and restarts
- A single abnormal call must **never compromise global billing accuracy**

FreeSBC treats call accounting and charging control as part of the **core call state machine**, not as an external afterthought.

---

## Core Capabilities

### Session Border Control

- SIP B2BUA / Proxy
- Ingress and egress separation
- Topology hiding and SIP normalization
- NAT-aware signaling and SDP handling
- Rate limiting and basic SIP attack protection

---

### Billing & Call Accounting (Core)

- **Accurate CDR Generation**
  - Call setup, answer, release, and failure events
  - Clear billing start and stop boundaries
  - Precise duration calculation

- **Deterministic Call State Tracking**
  - Explicit call lifecycle modeling
  - Billing-safe state transitions
  - Idempotent event handling

- **Real-Time Billing Control Hooks**
  - Prepaid and postpaid integration points
  - Credit check and call admission control
  - Forced call termination on billing conditions

- **Failure-Resilient Accounting**
  - Partial call handling
  - Abnormal release detection
  - No “silent” or unaccounted calls

- **Explainable Billing Decisions**
  - Clear reasons for call rejection or termination
  - Traceable linkage between signaling and billing events

---

### Observability for Billing-Critical Systems

- Call-level correlation identifiers
- Structured SIP and billing logs
- Metrics aligned with billing integrity:
  - Answered vs charged calls
  - Billing failures
  - Abnormal termination rates

---

## What FreeSBC Is (and Is Not)

### FreeSBC **Is**

- A Session Border Controller with **billing awareness**
- A reliable **CDR source of truth**
- A charging-safe edge component for VoIP platforms
- A foundation for VOS-like operator systems

### FreeSBC **Is Not**

- A full OSS/BSS platform
- A rating or tariff management UI
- A PBX or call-center product

Pricing plans, rate tables, and customer management are expected to live in **external systems**, while FreeSBC guarantees **billing correctness at the call level**.

---

## Architecture Positioning


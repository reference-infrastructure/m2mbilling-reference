# Scope — M2M Billing Reference

This document defines the **explicit scope boundaries** of the
**M2M Billing Reference**.

The term *billing* is used here in a **technical and semantic sense**.
It describes the deterministic qualification of machine-generated usage
for settlement — **not** a commercial, financial, or payment function.

---

## Included

This reference covers **machine-to-machine usage qualification semantics**, including:

- Definition and classification of machine-generated events
- Usage metering concepts for system-to-system interactions
- Attribution of measured usage to accountable machine or organizational entities
- Settlement qualification rules determining when usage is considered billable
- Separation between technical settlement logic and monetary execution
- Versioned semantics enabling reproducible interpretation across systems and time

---

## Excluded

This reference explicitly does **not** cover:

- Payment processing, clearing, or settlement execution
- Pricing models, tariffs, fees, or commercial agreements
- Invoicing, accounting systems, or ERP integration
- Taxation, fiscal reporting, or regulatory compliance guidance
- Cryptocurrencies, tokenomics, or on-chain payment mechanisms
- End-user billing, subscriptions, or customer relationship management
- Product implementations, platforms, services, or vendor solutions

---

## Terminology Baseline

- **Machine-to-Machine (M2M):**  
  Autonomous or semi-autonomous system interactions without direct human initiation for each action.

- **Billing (technical):**  
  The logical determination that measurable usage qualifies for settlement.

- **Settlement (logical):**  
  The resolution of usage attribution and qualification, independent of pricing or payment execution.

---

## Scope Discipline

This repository exists to provide **semantic clarity and boundary definition**.

It does **not**:
- recommend architectures,
- endorse standards or protocols,
- certify implementations,
- or define commercial practices.

Any change to scope must be documented through **explicit versioning**
and reflected consistently across all repository files.

# Mapping — Usage to Settlement (M2M Billing)

This mapping documents how machine-generated activity
progresses from **events** to **settlement qualification**
within the M2M Billing reference.

The mapping is **descriptive**, not prescriptive.

---

## End-to-End Mapping

| Layer        | Input                         | Processing Focus                         | Output                               | Notes |
|--------------|-------------------------------|-------------------------------------------|---------------------------------------|-------|
| Event        | Raw machine action             | Identification, timestamping, context     | Qualified event record                | Events are observable, not billable |
| Meter        | Qualified event records        | Aggregation, normalization, filtering     | Measured usage units                  | No responsibility assigned |
| Attribution  | Measured usage units           | Actor resolution, delegation handling     | Attributed usage                      | Responsibility established |
| Settlement   | Attributed usage               | Rule evaluation, threshold qualification  | Billable usage qualification          | Logical, non-financial |

---

## Layer Relationships

- **Event → Meter**  
  Raw actions must be normalized before any quantitative assessment.

- **Meter → Attribution**  
  Quantification precedes responsibility; attribution without measurement is ambiguous.

- **Attribution → Settlement**  
  Only attributed usage can be evaluated against settlement rules.

---

## Boundary Conditions

The following are **explicitly out of scope** of this mapping:

- Pricing or valuation of usage
- Payment execution or clearing
- Invoicing or accounting workflows
- Taxation or regulatory reporting
- Vendor- or platform-specific logic

---

## Consistency Rule

Any change to:
- the defined layers,
- their order,
- or their semantic meaning

requires a **corresponding update** to:
- `MODEL.md`
- `SCOPE.md`
- and the `CHANGELOG.md`.

This mapping exists to ensure **interpretability and auditability**
across independent systems.

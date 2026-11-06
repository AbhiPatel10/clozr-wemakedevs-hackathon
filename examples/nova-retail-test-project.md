# Nova Retail Marketplace — Fictional BA Test

- **Project ID:** `CLOZR-BA-NRT-001`
- **Client:** Nova Retail Technologies (fictional)
- **Purpose:** Test BA-to-Development workflow without a real client.
- **Status:** Handoff readiness exercise; not an approved SOW.

## Initial scope
1. Customer registration/login
2. Seller registration/verification
3. Seller dashboard
4. Product/inventory management
5. Product search/category management
6. Cart/checkout
7. Online payment integration
8. Order management
9. Admin dashboard
10. Reports/analytics

Additional expectations: responsive web, secure authentication/RBAC, scalable backend, payment gateway, email notifications.

## Recorded BA estimate context
- Estimate 5 Option A planning baseline: **1,471–2,180 hours**.
- Unknown band, client-managed shipping: **1,055–1,993 hours**.
- Unknown band, platform shipping: **1,195–2,303 hours**.
- Combined client-managed range: **2,526–4,173 hours**.
- Combined platform-ships range: **2,666–4,483 hours**.
- Custom card form alternative: **1,483–2,198 hours**.
- Reduced arithmetic figure **1,429–2,108 hours** was explicitly called not buildable because it removes required late-payment refund scope.

These are planning artifacts, not a quote. Consult latest BA source documents for detailed breakdown.

## Recorded conditions
- Q1, Q2, Q20, Q21 remained client-gated/open in latest recorded QA summary.
- Q6 payment gateway provider confirmation before payment integration beyond sandbox.
- Q8 hosting region confirmation before production.
- D4 late-payment full refund and D5 expired-order re-hold were assumptions.
- Seller cancellation of paid items feature-flagged off until Q2.
- NEW-35 correction: CANCELLED may move only to REFUND_PENDING for late successful payment after cancellation; CANCELLED → PAID forbidden.
- NEW-36 was corrected.
- NEW-37 low-severity wording issue: clarify order number is issued and visible to seller at PAID. Verify formal closure in latest BA record.

## Status warning
Latest recorded internal handoff was DRAFT / INTERNAL ONLY / PENDING HUMAN BA HEAD APPROVAL. Request to create an internal document did not itself approve development. Verify the latest artifact and any later approval.

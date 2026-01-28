# Proof of API-Work (PoAPW)

## Litepaper – Usage‑Anchored, Enterprise‑Grade API Economics

---

## Executive Summary

**Proof of API‑Work (PoAPW)** is a machine‑native settlement protocol where **APIs earn tokens by being called and successfully delivering results**, and **callers pay tokens as part of the API request itself**.

Tokens are not speculative assets. They are **usage credits anchored to infrastructure cost**, designed to cover hosting, compute, networking, and verification.

PoAPW introduces:

* payment embedded directly in API calls
* claim‑and‑confirm settlement
* deterministic per‑route pricing
* strictly capped, usage‑bound minting
* a fixed 1% infrastructure fee

PoAPW behaves like **cloud billing with cryptographic settlement**.

---

## The Problem

Modern software and AI systems rely on APIs for:

* data access
* computation
* verification and compliance

Existing models are poorly suited for autonomous systems:

* subscriptions assume humans
* invoices assume trust
* crypto tokens reward speculation, not delivery

Autonomous systems need a model where:

> **Work is paid only when it is successfully delivered.**

---

## The Core Rule

> **An API earns tokens only when a call succeeds and returns data or executes a valid callback.**

No response → no payout
No callback → no payout

---

## Payment in the API Call

Each API request includes a **token payment intent** as part of the payload.

1. Caller prepays tokens (or purchases them via the marketplace)
2. Tokens are embedded in the API call
3. Tokens are locked to a unique call identifier
4. Tokens are provisional until confirmation

If no valid response or callback occurs, tokens automatically revert.

---

## Claim–Confirm Settlement

PoAPW uses a two‑phase settlement mechanism:

1. **Claim** – The API claims the embedded payment after accepting the request
2. **Confirm** – The caller confirms success after receiving data or a callback

Only after confirmation do tokens become final.

This ensures:

* APIs cannot be paid without delivery
* callers cannot receive data without committing funds

---

## API Pricing Declaration

Each API declares its pricing **per command / route** as part of its API description:

* base call price (tokens)
* optional payload‑based component
* fixed protocol fee (1%)

Pricing is deterministic, transparent, and auditable before the call is made.

---

## Token Usage

### Utility

* Tokens are required to call APIs
* Tokens are earned by APIs on success
* Tokens can be purchased via the PoAPW marketplace

Tokens are not yield‑bearing and confer no ownership rights.

---

## Infrastructure Fee

* A **fixed 1% fee** is applied to every successful call
* The fee is used **exclusively** to operate the infrastructure:

  * compute
  * hosting
  * networking
  * verification
  * settlement and marketplace

Fees are operational, not financial.

---

## Energy‑Anchored Marketplace

PoAPW operates a native marketplace to guarantee token availability.

* **1,000 tokens = reference price of 1 Wh of energy**

This anchor:

* provides predictable pricing
* reflects real resource consumption
* avoids speculative valuation

---

## Usage‑Bound Minting

Minting exists to bootstrap integration and interaction, not to create inflation.

### Per API Route

```
minted_tokens = min(route_price × 10, 1,000)
```

* Triggered only on successful response or callback

### Per Complete API

* Maximum minting across all routes: **5,000 tokens**

### Per API Collection

* Maximum minting across a large API suite: **1,000 tokens**

Once a cap is reached, usage continues but no further minting occurs.

---

## Economic Properties

* No success → no payment
* No payment → no processing
* No delivery → no minting
* No unbounded inflation

Every token transferred or minted corresponds to real system work.

---

## Use Cases

* AI‑to‑AI workflows
* Data and analytics APIs
* Compliance and verification services
* Blockchain indexers
* Event‑driven systems

---

## Positioning & Compliance

PoAPW tokens are:

* utility and settlement units
* usage‑driven
* non‑yield‑bearing
* non‑investment products

PoAPW is designed for **enterprise, auditability, and regulatory clarity**.

---

## Conclusion

Proof of API‑Work establishes a simple, enforceable rule for machine economies:

> **Pay only for successful work.**

By embedding payment into API calls, anchoring value to infrastructure cost, and strictly bounding minting, PoAPW enables trustworthy, autonomous software markets.

PoAPW is not designed to speculate.

It is designed to **run infrastructure**.

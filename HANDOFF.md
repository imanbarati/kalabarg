# HANDOFF.md — Well of Souls → کالابرگ / National Credit Network

> **If you are an AI reading this:** previous sessions built a personal digital persona system ("Well of Souls" / Engram). The owner has now redirected the project. Read this fully before doing anything.

---

## 1. Mission (new direction)

Transform the previous **Well of Souls** (personal digital persona / engram of Iman) into infrastructure for **کالابرگ** and a fairer **National Credit Network**.

The core idea:
- People already self-declare assets, income, vehicles, medical costs, and support status.
- The form in `form/خوداظهاری-افزایش-کالابرگ.html` is the official-looking self-declaration UI for increasing Kalabarg (electronic food/subsidy coupons).
- Turn that declaration + verification logic into a transparent, auditable, privacy-respecting layer that can feed a National Credit / entitlement system.

This is **not** a personal soul archive anymore.  
It is a public-interest system for fair subsidy allocation and credit scoring based on real household reality.

## 2. What already exists

| Path | Purpose |
|------|--------|
| `form/خوداظهاری-افزایش-کالابرگ.html` | Complete RTL Persian self-declaration form (household head ID, postal code, support institutions, property ownership, vehicles, monthly income brackets, employment status, special medical costs, consent + liability). |
| Previous `my-engram` repo | Personal digital persona system (interviews, retrieval, privacy tools). Keep it separate. |

## 3. Immediate next steps

1. **Make the form functional**
   - Wire the radio buttons and inputs to a real backend (or at least localStorage + export JSON).
   - Add validation (national ID format, postal code, required fields).
   - Generate a signed self-declaration PDF or JSON that the citizen can keep.

2. **Define the data model**
   - Household head national ID
   - Postal code / location
   - Support status (Komiteh Emdad / Behzisti / none)
   - Property ownership (any formal/informal)
   - Vehicles (any type)
   - Monthly household income bracket
   - Employment status of head
   - Special medical costs (yes/no + later details)
   - Consent timestamp + liability acceptance

3. **Privacy & integrity rules (non-negotiable)**
   - Never store more than the citizen explicitly declared.
   - Prefer client-side first, then encrypted upload.
   - Clear audit trail of every change.
   - Explicit consent before any cross-check with other databases.
   - False declaration → automatic penalty path (as written in the form).

4. **National Credit Network angle**
   - Use the same declaration as a building block for a broader credit / entitlement score that is:
     - Transparent (citizen can see why they got a certain bracket)
     - Contestable
     - Updated when life circumstances change
   - Avoid black-box scoring. Prefer rule-based + explainable models first.

## 4. Status log

| Date       | Who   | What was done                                      | Next step                          |
|------------|-------|----------------------------------------------------|------------------------------------|
| 2026-10-15 | Grok  | New repo `kalabarg` created. Form + this HANDOFF.  | Make form interactive + data model |

**Current phase:** Foundation. Form is static HTML. No backend yet.

## 5. Rules for any AI continuing this work

1. Update this Status log at the end of every session.
2. Keep the form’s legal language (consent + liability) intact unless a lawyer reviews changes.
3. Prefer simple, auditable code over clever ML for the first versions.
4. Persian is first-class. All citizen-facing text must be natural Persian.
5. Do not mix the old personal “Well of Souls / Engram” identity system into this repo. They are now separate missions.
6. Be honest about limitations. This is a tool for fairer allocation, not a magic solution.

## 6. Quick-start prompt for the next AI

> Read HANDOFF.md fully. We are building the کالابرگ / National Credit Network self-declaration system. The form is in `form/`. Make the form fully interactive (validation + JSON export), design the data model, and propose the next concrete step. Update the status log when finished.

---

*The Well of Souls held personal memory.  
This system holds household reality so that help reaches the right people.*

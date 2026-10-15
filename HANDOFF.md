# HANDOFF.md — Well of Souls → کالابرگ / National Credit Network

> **If you are an AI reading this:** previous sessions built a personal digital persona system ("Well of Souls" / Engram). The owner has now redirected the project. Read this fully before doing anything.

---

## 1. Mission

Transform the previous **Well of Souls** (personal digital persona) into infrastructure for **کالابرگ** and a fairer **National Credit Network**.

Core idea:
- Citizens already self-declare assets, income, vehicles, medical costs, and support status through government forms.
- We now have two key pages:
  1. Clean replica of the official **پنجره ملی** login (`form/login.html`)
  2. Self-declaration form for increasing Kalabarg (`form/خوداظهاری-افزایش-کالابرگ.html`)
- Goal: make a transparent, auditable, privacy-respecting flow that can feed a National Credit / entitlement system.

## 2. What exists now

| Path | Purpose |
|------|--------|
| `form/login.html` | Clean, self-contained replica of the official پنجره ملی login page (mobile / national ID + OTP flow). Lightweight, no external government assets. |
| `form/خوداظهاری-افزایش-کالابرگ.html` | Full self-declaration form (household head, postal code, support institutions, property, vehicles, income brackets, employment, medical costs, consent + liability). |
| `README.md` | Short project overview |

## 3. Immediate next steps

1. **Connect the two pages**
   - Login → after successful OTP simulation, redirect to the declaration form (already wired in the replica).
   - Make the declaration form actually collect and export data (JSON / PDF).

2. **Data model** (keep it simple and explainable)
   - national_id / household_head_id
   - postal_code
   - under_support (boolean + which org)
   - owns_property (boolean)
   - owns_vehicle (boolean)
   - monthly_income_bracket
   - employment_status
   - special_medical_costs (boolean)
   - consent_timestamp
   - liability_accepted

3. **Privacy & integrity (non-negotiable)**
   - Only store what the citizen explicitly declared.
   - Prefer client-side first, then encrypted upload.
   - Clear audit trail.
   - Explicit consent before any cross-check.
   - False declaration → automatic penalty path (as written in the form).

4. **National Credit Network angle**
   - Use the same declaration as a building block for a broader, explainable credit / entitlement score.
   - Avoid black-box models in the first versions. Prefer transparent rules.

## 4. Status log

| Date       | Who   | What was done                                      | Next step                          |
|------------|-------|----------------------------------------------------|------------------------------------|
| 2026-10-15 | Grok  | New repo `kalabarg` created. Form + initial HANDOFF | — |
| 2026-10-15 | Grok  | Added clean replica of پنجره ملی login page        | Make declaration form interactive + data export |

**Current phase:** UI foundation. Both pages exist and look official. No real backend yet.

## 5. Rules for any AI continuing this work

1. Update this Status log at the end of every session.
2. Keep the legal language (consent + liability) intact unless reviewed.
3. Prefer simple, auditable code over clever ML for the first versions.
4. Persian is first-class. All citizen-facing text must be natural Persian.
5. Do not mix the old personal “Well of Souls / Engram” identity system into this repo.
6. Be honest about limitations.

## 6. Quick-start prompt for the next AI

> Read HANDOFF.md fully. We have the login replica and the Kalabarg self-declaration form. Make the declaration form fully interactive (collect answers, validate, export clean JSON). Then propose the minimal data model and the next concrete step. Update the status log when finished.

---

*The Well of Souls held personal memory.  
This system holds household reality so that help reaches the right people.*

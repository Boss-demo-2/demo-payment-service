# demo-payment-service

> **BOSS Demo Microservice — Tier 1 (Critical)**
>
> Simulates the Payment / Core API   Service in the BOSS application ecosystem

---

## Overview

This repository is part of the **BOSS Versioning System** demo. It represents a **Tier 1 Critical** microservice — changes here carry the highest weight in determining the BOSS Application Version    .

## Branch Structure

| Branch | Environment | Version Impact |
|--------|-------------|----------------|
| `develop` | DEV | Right-most digit bumps (e.g. `2.0.0 → 2.0.1`) |
| `release/qa` | QA | No version bump — testing only |
| `uat` | UAT (Pre-Production) | **Middle digit bumps** (e.g. `2.0.3 → 2.1.0`) — triggers BOSS aggregator |

## Versioning Flow

```
feature/* → develop → release/qa → uat
                                    ↑
                          semantic-release fires here
                          (only on UAT merge)
```

## PR Labels

| Label | Meaning | BOSS Impact (Tier 1) |
|-------|---------|----------------------|
| `breaking-change` | API/data model breaking change | **MAJOR bump** |
| `feature` | New functionality | **MINOR bump** |
| `enhancement` | Improvement to existing feature | **MINOR bump** |
| `bugfix` | Bug fix | **PATCH bump** |

## BOSS Tier Assignment

- **Tier**: 1 — Critical
- **Simulates**: Payment / Core API Service
- **Priority**: Highest — any change has high impact on BOSS version

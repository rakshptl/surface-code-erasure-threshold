# Numerical Results

All values produced by `QEC_Surface_Code_Threshold.ipynb` with 20,000 shots per point.

---

## Threshold Summary

| Model | Threshold | Detection method |
|---|---|---|
| Standard circuit-level depolarizing | **~0.80%** | Linear interpolation of d=7/d=3 crossing bracket: p = 0.736% → 0.864% |
| Phenomenological erasure (ideal limit) | **~7.32%** | Linear interpolation of d=7/d=3 crossing bracket: p = 6.545% → 7.409% |
| **Improvement factor** | **~9.1×** | Era threshold / Std threshold |

### Literature comparison

| Model | This work | Literature |
|---|---|---|
| Circuit-level depolarizing | ~0.80% | ~0.8–1.0% (Fowler 2012; Gidney 2021) |
| Pure erasure (ideal limit) | ~7.32% | ~6–7% (Delfosse & Zémor 2017) |
| Circuit-level HERALDED_ERASE | — | ~4.1–4.3% (Kubica 2023; Sahay 2023) |

---

## Sweep 1 — Standard Noise (Circuit-Level Depolarizing)

| p (%) | LER d=3 | LER d=5 | LER d=7 |
|---|---|---|---|
| 0.100 | 0.00050 | 0.00015 | 0.00000 |
| 0.227 | 0.00305 | 0.00080 | 0.00010 |
| 0.355 | 0.00530 | 0.00220 | 0.00090 |
| 0.482 | 0.01095 | 0.00730 | 0.00350 |
| 0.609 | 0.01500 | 0.01200 | 0.00900 |
| 0.736 | 0.02290 | 0.02105 | 0.01655 |
| 0.864 | 0.02900 | 0.03270 | 0.03200 |
| 0.991 | 0.03425 | 0.04595 | 0.04915 |
| 1.118 | 0.04690 | 0.06125 | 0.07530 |
| 1.245 | 0.05460 | 0.07950 | 0.10400 |
| 1.373 | 0.06755 | 0.10160 | 0.13670 |
| 1.500 | 0.07855 | 0.12410 | 0.17405 |

**Threshold crossing bracket:** p = 0.736% → 0.864% (d=7 crosses above d=3)  
**Interpolated threshold:** ~0.80%

---

## Sweep 2 — Erasure Noise (Phenomenological)

| p (%) | LER d=3 | LER d=5 | LER d=7 |
|---|---|---|---|
| 0.500 | 0.00050 | 0.00000 | 0.00000 |
| 1.364 | 0.00380 | 0.00110 | 0.00030 |
| 2.227 | 0.01020 | 0.00425 | 0.00165 |
| 3.091 | 0.02140 | 0.01000 | 0.00415 |
| 3.955 | 0.03525 | 0.02200 | 0.01195 |
| 4.818 | 0.04750 | 0.03940 | 0.02375 |
| 5.682 | 0.06545 | 0.05825 | 0.04255 |
| 6.545 | 0.08325 | 0.08145 | 0.06985 |
| 7.409 | 0.09800 | 0.10930 | 0.09920 |
| 8.273 | 0.12005 | 0.14015 | 0.13720 |
| 9.136 | 0.14155 | 0.17325 | 0.17940 |
| 10.00 | 0.16275 | 0.20420 | 0.22605 |

**Threshold crossing bracket:** p = 6.545% → 7.409% (d=7 crosses above d=3)  
**Interpolated threshold:** ~7.32%

---

## Sweep 3 — LER vs Erasure Fraction η (fixed p = 2%)

η = fraction of total noise p that is heralded.  
Remainder (1−η)·p is standard unheralded Pauli noise.

| η | LER d=3 | LER d=5 | LER d=7 |
|---|---|---|---|
| 0.0 | 0.0909 | 0.1754 | 0.2627 |
| 0.1 | 0.0817 | 0.1550 | 0.2202 |
| 0.2 | 0.0760 | 0.1342 | 0.1861 |
| 0.3 | 0.0674 | 0.1126 | 0.1492 |
| 0.4 | 0.0571 | 0.0907 | 0.1183 |
| 0.5 | 0.0477 | 0.0696 | 0.0830 |
| 0.6 | 0.0412 | 0.0498 | 0.0582 |
| 0.7 | 0.0341 | 0.0365 | 0.0364 |
| 0.8 | 0.0259 | 0.0256 | 0.0199 |
| 0.9 | 0.0189 | 0.0146 | 0.0088 |
| 1.0 | 0.0109 | 0.0047 | 0.0013 |

### LER reduction (η: 0 → 1)

| Distance | LER at η=0 | LER at η=1 | Reduction |
|---|---|---|---|
| d = 3 | 0.0909 | 0.0109 | **8×** |
| d = 5 | 0.1754 | 0.0047 | **37×** |
| d = 7 | 0.2627 | 0.0013 | **202×** |

> At constant total noise p = 2% (above the standard threshold of ~0.80%), simply knowing the error locations (increasing η from 0 to 1) reduces the logical error rate by 8×–202× depending on code distance.

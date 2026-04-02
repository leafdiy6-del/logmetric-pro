# Appendix A — Calculation Formulas

---

## Default Formula (Standard Cylinder)

The app's default volume formula, consistent with GG Bled software:

$$V = \pi \times \left(\frac{d}{200}\right)^2 \times L$$

- $d$: Mid-point diameter (cm)
- $L$: Log length (m)
- $V$: Volume (m³)

Result rounded to 2 decimal places.

---

## Category A: Pure Mathematical Formulas

### Huber (EN 1309-2) — European Standard

$$V = \frac{\pi}{4} \times \left(\frac{d}{100}\right)^2 \times L$$

Mid-section method, the most widely used log volume standard in Europe. Result rounded to 3 decimal places.

---

### Czech ČSN 48 0009 (Czech/Slovak Oak-specific)

Huber formula with bark deduction; coefficients based on oak measurements:

```
Bark thickness = 1.2474 + 0.042323 × d^1.0623
d_net = d − bark thickness
V = (π/4) × (d_net/100)² × L
```

Result rounded to 2 decimal places.

---

### Hoppus (UK)

Volume of a square-cross-section column using one-quarter of the log's circumference:

$$V = \left(\frac{\pi \cdot d}{400}\right)^2 \times L$$

Traditional British log rule, approximately 78.54% of actual volume.

---

### NF B53-020 (French Standard)

Huber mid-section method + standard taper assumption (1 cm/m):

$$d_m = d + \frac{L}{2}, \quad V = \frac{\pi}{4} \times \left(\frac{d_m}{100}\right)^2 \times L$$

---

### JAS (Japanese Agricultural Standard JAS 600)

Cross-section approximated as a square; diameter rounded per rules:

- $d < 14$ cm: rounded down to the nearest integer
- $d \geq 14$ cm: rounded down to the nearest even number
- Long logs ($L \geq 6$ m): add taper compensation

$$V = \left(\frac{d_{rounded}}{100}\right)^2 \times L$$

---

### Ontario (Ontario, Canada)

Diameter assigned to 2 cm even classes, then calculated as circular cross-section:

$$d_{class} = \text{round}(d/2) \times 2, \quad V = 0.7854 \times \left(\frac{d_{class}}{100}\right)^2 \times L$$

---

## Category B: Imperial Board Foot Formulas (unit: BF)

> **Board Foot (BF)**: 1 BF = 1 ft × 1 ft × 1 in = 1/12 ft³ ≈ 0.00236 m³

### Doyle (Southern US)

$$BF = \left(\frac{D_{in} - 4}{4}\right)^2 \times L_{ft}$$

$D_{in}$: small-end diameter in inches, $L_{ft}$: length in feet. Best suited for large-diameter logs.

---

### Roy (Quebec, Canada)

$$BF = \frac{(D_{in} - 1)^2 \times L_{ft}}{16}$$

$D_{in}$ rounded to the nearest integer; $L_{ft}$ rounded down to the nearest integer.

---

### Scribner Decimal C (Western US)

Bruce & Schumacher (1950) regression formula:

$$BF_{raw} = \frac{(0.79D^2 - 2D - 4) \times L_{ft}}{16}$$

Result rounded to the nearest 10 BF (Decimal C specification).

---

### International 1/4" (USFS Standard)

Grosenbaugh's continuous formula:

$$BF = 0.049762 L D^2 + 0.006220 L^2 D - 0.185476 LD + 0.000259 L^3 - 0.011592 L^2 + 0.042222 L$$

USFS mode: length truncated to integer feet, result rounded to the nearest 5 BF.

---

## Category C: Hybrid Model Formulas

### Nilson (Estonia / Nordic, Nilson 1967)

Species-specific coefficients:

$$V(dm^3) = a_1 \cdot d^2 \cdot L + a_2 \cdot d^2 \cdot L^3 + a_3 \cdot d \cdot L^2$$

| Species | $a_1$ | $a_2$ | $a_3$ |
|---------|-------|-------|-------|
| Pine | 0.0799 | 0.000146 | 0.0411 |
| Spruce | 0.07995 | 0.00016105 | 0.04948 |
| Birch | 0.080833 | 0.000185 | 0.044444 |
| Other Conifer | 0.0800 | 0.000154 | 0.0453 |

$d$ in cm, $L$ in m, $V(m^3) = V(dm^3) / 1000$.

---

### CedarLog 2/3 Rule (North American Cedar)

$$V = \left(\frac{d \times 2/3}{100}\right)^2 \times L$$

---

### Kershaw / Noonan (Canadian Standing Timber)

Huber formula with a form factor of 0.42:

$$V = 0.42 \times \frac{\pi}{4} \times \left(\frac{d}{100}\right)^2 \times L$$

---

## EMC Equilibrium Moisture Content Formula

Uses the **Hailwood-Horrobin** model (source: USDA FPL Wood Handbook GTR-190):

Calculates the moisture content (%) that wood will eventually reach under given temperature and relative humidity.

This is an **equilibrium value**, not an additive value. See Chapter 11's moisture content section for details.

---

## Weight Estimation Formula

$$W = V \times \rho \times \frac{100 + MC}{100 + MC_{reference}}$$

- $V$: Total volume (m³)
- $\rho$: Basic wood density (kg/m³), determined by the selected species
- $MC$: Current moisture content (%)
- $MC_{reference}$: Reference moisture content (typically 12%)

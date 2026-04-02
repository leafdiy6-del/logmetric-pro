# Dodatek A — Formule za izračun

---

## Privzeta formula (standardni valj)

Privzeta formula za prostornino aplikacije, skladna s programsko opremo GG Bled:

$$V = \pi \times \left(\frac{d}{200}\right)^2 \times L$$

- $d$: Premer na sredini (cm)
- $L$: Dolžina hloda (m)
- $V$: Prostornina (m³)

Rezultat zaokrožen na 2 decimalni mesti.

---

## Kategorija A: Čiste matematične formule

### Huber (EN 1309-2) — evropski standard

$$V = \frac{\pi}{4} \times \left(\frac{d}{100}\right)^2 \times L$$

Metoda srednjega prereza, najbolj razširjen standard za prostornino hlodov v Evropi. Rezultat zaokrožen na 3 decimalna mesta.

---

### Czech ČSN 48 0009 (za češki/slovaški hrast)

Huberjeva formula z odbitkom lubja; koeficienti temeljijo na meritvah hrasta:

```
Debelina lubja = 1,2474 + 0,042323 × d^1,0623
d_neto = d − debelina lubja
V = (π/4) × (d_neto/100)² × L
```

Rezultat zaokrožen na 2 decimalni mesti.

---

### Hoppus (VB)

Prostornina valja s kvadratnim presekom, kjer je stranica kvadrata ena četrtina obsega hloda:

$$V = \left(\frac{\pi \cdot d}{400}\right)^2 \times L$$

Tradicionalno britansko merilno pravilo, približno 78,54 % dejanske prostornine.

---

### NF B53-020 (francoski standard)

Huberjeva metoda srednjega prereza + predpostavka standardne koničnosti (1 cm/m):

$$d_m = d + \frac{L}{2}, \quad V = \frac{\pi}{4} \times \left(\frac{d_m}{100}\right)^2 \times L$$

---

### JAS (japonski kmetijski standard JAS 600)

Prerez je približan kvadratu, premer se zaokroži po pravilih:

- $d < 14$ cm: zaokroži navzdol na najbližje celo število
- $d \geq 14$ cm: zaokroži navzdol na najbližje sodo število
- Dolgi hlodi ($L \geq 6$ m): dodaj nadomestek koničnosti

$$V = \left(\frac{d_{zaokroženo}}{100}\right)^2 \times L$$

---

### Ontario (Ontario, Kanada)

Premer se razvrsti v razrede po 2 cm soda števila, nato se izračuna kot krožni prerez:

$$d_{razred} = \text{zaokroži}(d/2) \times 2, \quad V = 0,7854 \times \left(\frac{d_{razred}}{100}\right)^2 \times L$$

---

## Kategorija B: Imperialne formule za ploskovne čevlje (enota: BF)

> **Ploskovni čevelj (BF)**: 1 BF = 1 ft × 1 ft × 1 in = 1/12 ft³ ≈ 0,00236 m³

### Doyle (južna ZDA)

$$BF = \left(\frac{D_{in} - 4}{4}\right)^2 \times L_{ft}$$

$D_{in}$: premer na tankem koncu v palcih, $L_{ft}$: dolžina v čevljih. Najprimernejši za hlode velikega premera.

---

### Roy (Quebec, Kanada)

$$BF = \frac{(D_{in} - 1)^2 \times L_{ft}}{16}$$

$D_{in}$ zaokrožen na najbližje celo število; $L_{ft}$ zaokrožen navzdol na najbližje celo število.

---

### Scribner Decimal C (zahod ZDA)

Regresijska formula Bruce & Schumacher (1950):

$$BF_{surov} = \frac{(0,79D^2 - 2D - 4) \times L_{ft}}{16}$$

Rezultat zaokrožen na najbližjih 10 BF (specifikacija Decimal C).

---

### International 1/4" (USFS standard)

Grosenbaugheva zvezna formula:

$$BF = 0,049762 L D^2 + 0,006220 L^2 D - 0,185476 LD + 0,000259 L^3 - 0,011592 L^2 + 0,042222 L$$

Način USFS: dolžina se prireže na cela števila čevljev, rezultat zaokroži na najbližjih 5 BF.

---

## Kategorija C: Mešane modelne formule

### Nilson (Estonija / nordijska, Nilson 1967)

Koeficienti so odvisni od vrste lesa:

$$V(dm^3) = a_1 \cdot d^2 \cdot L + a_2 \cdot d^2 \cdot L^3 + a_3 \cdot d \cdot L^2$$

| Vrsta lesa | $a_1$ | $a_2$ | $a_3$ |
|-----------|-------|-------|-------|
| Bor | 0,0799 | 0,000146 | 0,0411 |
| Smreka | 0,07995 | 0,00016105 | 0,04948 |
| Breza | 0,080833 | 0,000185 | 0,044444 |
| Drugi iglavec | 0,0800 | 0,000154 | 0,0453 |

$d$ v cm, $L$ v m, $V(m^3) = V(dm^3) / 1000$.

---

### CedarLog 2/3 Rule (severnoameriški cedar)

$$V = \left(\frac{d \times 2/3}{100}\right)^2 \times L$$

---

### Kershaw / Noonan (kanadski stoječi les)

Huberjeva formula s faktorjem oblike 0,42:

$$V = 0,42 \times \frac{\pi}{4} \times \left(\frac{d}{100}\right)^2 \times L$$

---

## Formula EMC — ravnotežna vsebnost vlage

Uporablja model **Hailwood-Horrobin** (vir: USDA FPL Wood Handbook GTR-190):

Izračuna vsebnost vlage (v %), ki jo bo les končno dosegel pri dani temperaturi in relativni vlažnosti.

Ta vrednost je **ravnotežna vrednost**, ne vrednost, ki se prišteva. Glejte razdelek o vsebnosti vlage v poglavju 11.

---

## Formula za oceno teže

$$W = V \times \rho \times \frac{100 + MC}{100 + MC_{referenčna}}$$

- $V$: Skupna prostornina (m³)
- $\rho$: Osnovna gostota lesa (kg/m³), določena z izbrano vrsto lesa
- $MC$: Trenutna vsebnost vlage (%)
- $MC_{referenčna}$: Referenčna vsebnost vlage (ponavadi 12 %)

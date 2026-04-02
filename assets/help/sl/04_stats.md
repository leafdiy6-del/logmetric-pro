# Poglavje 4 — Statistika in filtriranje

---

## 1. Spodnja statistična vrstica

Na dnu glavnega vmesnika se v realnem času prikazujejo povzeti podatki trenutnega seznama:

- **Skupno število kosov** in **skupna prostornina** (m³ ali BF)
- **Po razredih**: npr. `F: 12` pomeni, da je za razred F vpisanih 12 hlodov
- **Kratek les**: npr. `< 4m: 3` pomeni, da je 3 hlode dolžine manj kot 4 metre
- **Tanki les**: npr. `< 30cm: 5` pomeni, da je 5 hlodov premera manj kot 30 cm
- **Ocena teže** (zahteva izbiro vrste lesa v arhivu serije in vključitev prikaza teže)

---

## 2. Hitro filtriranje s klikom na statistične oznake

Neposredno **kliknite** statistično oznako na dnu (npr. kliknite `F: 12`):

- Vse ustrezne vrstice na seznamu bodo **poudarjene**
- Neusklajene vrstice bodo samodejno **potemnjene**
- Ponovni klik na isto oznako ali klik na prazno območje prekliče filtriranje

> **Uporaba:** Hitro iskanje vnosov določenega razreda ali dimenzije, olajšuje pregledovanje in preverjanje.

---

## 3. Prilagajanje statističnih pragov

**Dejanje:** Dolg pritisk na statistično oznako za kratek ali tanek les

Odpre se pogovorno okno, kjer lahko spremenite:
- **Prag za kratek les L1** (privzeto 4 m)
- **Prag za kratek les L2** (privzeto 2,5 m)
- **Prag za tanek les D** (privzeto 30 cm)

Spremembe se takoj uveljavijo, kar omogoča prilagodljivo prilagajanje glede na standarde dostave.

---

## 4. Ocena teže

Pogoji za vključitev:
1. V arhivu serije nastavite **vrsto lesa** (vpliva na gostoto lesa)
2. Nastavitve → Splošno → Vključi »Prikaži težo v statistični vrstici«.

Formula za izračun teže:

```
Teža (kg) = Skupna prostornina (m³) × Gostota lesa (kg/m³) × Koeficient popravka vlažnosti
```

Vlažnost je privzeto 12 % (standardno zračno sušen les), lahko se spremeni v arhivu serije.

**Enote teže:**
- `auto`: pod 1000 kg prikaži kg, nad 1000 kg prikaži t
- V nastavitvah lahko nastavite fiksno na `kg` ali `t`

---

## 5. Pregled porazdelitve po razredih

Podatki po razredih v statistični vrstici pomagajo pri:
- Hitrem preverjanju, ali število kosov posameznega razreda ustreza pričakovanjem
- Primerjavi razmerij med različnimi razredi
- Končnem pregledu pred izvozom poročil

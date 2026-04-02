# Poglavje 1 — Hitri začetek

---

## 1. Prvi zagon aplikacije

Ob prvem zagonu se aplikacija odpre na seznamu projektov.

### Ustvarjanje prvega projekta

1. Kliknite gumb **＋** v spodnjem desnem kotu, izberite »Nov projekt« in vnesite **ime projekta** (npr. »Marec 2024 – uvoz hrasta«), nato kliknite »Ustvari« za vstop v glavni vmesnik

> 💡 **Namig**: Če projekt že obstaja, preprosto kliknite kartico projekta za vstop. Dolg pritisk na kartico prikaže več možnosti.

---

## 2. Kako izgleda glavni vmesnik?

```
┌─────────────────────────────────────────────────────────────┐
│ [+]  [Serija]  [⚙]     Ime projekta ▼      [💾]         │  ← Zgornja navigacija
├─────────────────────────────────────────────────────────────┤
│ ČSN 48 0009                              NO. 2            │
│                                                              │
│  Številka: [________]        Opomba: [________]           │
│                                                              │
│  Dolžina(m): [__]   Premer(cm): [__]    0.00 m³          │  ← Vnosno območje
│                                                              │
│  Izberite razred                                            │
│  [ABC] [A+] [A] [B] [C] [D]                               │  ← Gumbi za razred
│                                                              │
│       [  +  Dodaj in nadaljuj  ]                             │
├─────────────────────────────────────────────────────────────┤
│ Zap │ Številka│Razred│Dolžina(m)│Premer(cm)│Prostornina│Op │  ← glava tabele
├────┼─────────┼──────┼──────────┼───────────┼────────────┼────┤
│ 1  │56748690 │  A   │   5.4   │    56    │  1.13 m³ │     │  ← seznam
└────┴─────────┴──────┴──────────┴───────────┴────────────┴────┘
│                                                              │
│  [A: 1]   [Dvoj.oznaka]    Skupaj: 1   Prost.: 1.13 m³  │  ← Spodnja statistika
└─────────────────────────────────────────────────────────────┘
```

**Vmesnik je razdeljen na štiri območja:**

| Območje | Funkcija | Opis |
|---------|----------|------|
| **Zgornja navigacija** | Funkcijski gumbi | Nova serija (osveži), arhiv serije, nastavitve, preklop projekta, shrani |
| **Vnosno območje** | Vnos podatkov | Številka, opomba, dolžina, premer, izbira razreda, gumb za dodajanje |
| **Območje seznama** | Prikaz podatkov | Tabela vnesenih hlodov s številko, razredom, dimenzijami in prostornino |
| **Spodnja statistika** | Statistika v realnem času | Število po razredih, dvojne oznake, skupno število, skupna prostornina |

---

## 3. Vnos prvega hloda

### Priprava

- **Številka**: Vnesete jo ročno ali pustite prazno za samodejno nadaljevanje – potrebno je vključiti »Hiter način« v nastavitvah
- **Enota za dolžino**: meter (m), npr. `3.5` pomeni 3,5 metra
- **Enota za premer**: centimeter (cm), npr. `35` pomeni 35 centimetrov
- **Opomba**: Neobvezno polje za posebne informacije

### Koraki

1. **Vnos številke** (neobvezno)
   
   Vnesite številko/oznako hloda v polje za številko

2. **Vnos dolžine**
   
   Kliknite polje za dolžino in vnesite `3.5` (metrov). Če je v nastavitvah vključen »Hiter način – samodejna decimalna pika«, vnesite samo `35`, aplikacija pa bo samodejno dodala decimalno vejico in dobili `3.5`

3. **Vnos premera**
   
   Kliknite polje za premer in vnesite `35` (centimetrov)

4. **Izbira razreda**
   
   Kliknite gumb za razred (npr. **A**, **B**, **C** itd.). Z dolgim pritiskom na gumb razreda lahko izberete predhodno shranjene pogoste razrede. Razrede lahko urejate ali dodajate v »Nastavitve – Razredi in odbitki – Sklad razredov«.

5. **Kliknite Dodaj**
   
   Kliknite gumb **+ Dodaj in nadaljuj**, vnos se shrani na seznam, spodnja statistika se posodobi v realnem času

> 🎯 **Preizkusite**: Kliknite na »A: 1« v spodnji statistiki in poglejte, kaj se zgodi! (Namig: funkcija filtriranja)

---

## 4. Pomembni gibi

| Gib | Dejanje | Scenarij uporabe |
|-----|---------|------------------|
| **Podrsaj levo po vrstici** | Prikaže gumbe za dejanja (vstavi/izbriši/več) | Ko želite izbrisati ali vstaviti vrstico |
| **Dolg pritisk na gumb razreda** | Izbira predhodno shranjenih pogostih razredov | Potrebno predhodno dodati razrede v »Nastavitve – Razredi in odbitki – Sklad razredov« |
| **Klik na statistično oznako** | Filtriranje prikaza (npr. prikaži samo razred A) | Hitro preverjanje števila določenega razreda |
| **Dolg pritisk na statistično oznako** | Spreminjanje statističnih pragov | Prilagajanje standardov za kratko/tanki les |
| **Klik na gumb dvojne oznake** | Preklop na način dvojne oznake | Uporabi se, ko je en les razdeljen na dva dela, vendar še ni prerezan – ima dve oznaki |

---

## 5. Popravljanje napak pri vnosu

### Rdeče opozorilo (samodejno popravljanje)

Če je vrstica prikazana v **rdeči barvi**, je vnos verjetno napačen:

- ❌ Manjka decimalna pika pri dolžini (npr. vnesli ste `450` namesto `4.50`)
- ❌ Vnesena neobičajna vrednost (npr. dolžina več kot 20 metrov)

**Način popravljanja**: Kliknite rdečo vrstico za neposredno spremembo

---

## 6. Priporočene nastavitve

### Način za začetnike (privzeto vključen)

**Pot:** Nastavitve → Splošno → Način za začetnike

- ✅ Vključeno: Prikazuje več napotkov za vodenje, primerno za prvo uporabo
- ❌ Izključeno: Bolj kompakten vmesnik za izkušene uporabnike

### Hiter način (močno priporočeno vključiti)

**Pot:** Nastavitve → Vnos → Hiter način

Po vključitvi prinaša tri prednosti:

| Funkcija | Opis | Primer |
|----------|------|--------|
| Samodejna decimalna pika | Vnos dveh številk se samodejno pretvori v decimalno število | Vnos `35` → samodejno postane `3.5` metrov |
| Samodejni prehod | Po vnosu dolžine se kurzor samodejno premakne na premer | Ni potrebe po ročnem preklopu vnosnih polj |
| Samodejno nadaljevanje številk | Ob vsakem dodajanju se številka poveča za +1 | Ni potrebe po ročnem vnosu številk |

> ⚠️ **Pozor**: V načinu z imperialnimi enotami funkcija samodejne decimalne pike ni na voljo

---

## 7. Kako se izračuna prostornina?

Privzeto se uporablja formula valja:

```
V = π × (premer/200)² × dolžina
```

- Enota premera: centimetri (cm)
- Enota dolžine: metri (m)
- Enota rezultata: kubični metri (m³)

> 📚 Potrebujete drugačno formulo? Glejte »Dodatek A – Formule za izračun« ali jo spremenite v nastavitvah

---

## 8. Shranjevanje in izvoz

### Samodejno shranjevanje

Aplikacija **samodejno shranjuje** vsak vnos – ročno shranjevanje ni potrebno. Tudi ob nenadnem zapiranju aplikacije ali izpadu elektrike podatki ne bodo izgubljeni.

Ko zaključite s trenutno serijo in želite začeti novo, kliknite gumb [↻] (ikona osveževanja) **»Nova serija«** v zgornjem levem kotu: po potrditvi se glavni seznam izprazne, **trenutni podatki se samodejno shranijo v interno evidenco** (posnetek), do katere lahko dostopate kasneje prek **Shrani → Odpri interno evidenco**. To dejanje ni reverzibilno – pred nadaljevanjem se prepričajte, da ste zaključili s serijo.

Če želite dodatno ročno varnostno kopijo, kliknite **💾** za odpiranje menija in izberite »Shrani v interno evidenco«.

### Izvoz poročil

Po zaključku vnosa kliknite gumb **💾 Shrani/izvozi** v zgornjem delu:

| Format | Uporaba | Način pošiljanja |
|--------|---------|-------------------|
| **PDF** | Uradno poročilo s prostorom za podpis | WeChat, e-pošta, tiskanje |
| **Excel** | Analiza podatkov, možnost urejanja | WeChat, e-pošta, obdelava na računalniku |
| **Datoteka predaje (.lmp)** | Za sodelavce za nadaljevanje urejanja | Glejte poglavje 7 |

---

## 9. Kaj se naučiti naprej?

Čestitamo za uspešno obvladanje osnov! Priporočamo nadaljnje branje:

- **Poglavje 2** → Upravljanje projektov, mape, iskanje
- **Poglavje 3** → Seznamske operacije, dvojne oznake, straničenje
- **Poglavje 12** → Skriti triki in bližnjice

Imate težave? Kliknite gumb **?** v zgornjem desnem kotu vmesnika ali pojdite na **Nastavitve → Navodila za uporabo** za celotno dokumentacijo.

---

**Uživajte v uporabi!** 🌲

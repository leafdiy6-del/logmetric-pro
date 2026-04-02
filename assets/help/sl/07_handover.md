# Poglavje 7 — Predaja med izmenami

---

## 1. Kaj je predaja med izmenami?

Predaja med izmenami je funkcija za hitro deljenje **trenutno urejanih projektnih podatkov** s sodelavcem ali naslednjo izmeno. Prejemnik lahko nadaljuje z urejanjem tam, kjer ste vi končali.

**Razlika proti izvozu poročil:**

| Funkcija | Namen | Prejemnik |
|----------|-------|-----------|
| **Predaja med izmenami** (.lmp) | Prenos nedokončanega dela | Z LogMetric Pro odpre za nadaljevanje urejanja |
| **Izvoz poročila** (PDF/Excel) | Ustvarjanje končnega poročila za arhiviranje ali usklajevanje | Z Office/WPS odpre za ogled |

---

## 2. Pošiljanje datoteke za predajo

### Koraki

1. **Odprite meni Shrani/izvozi**
   
   V glavnem vmesniku kliknite **💾 Shrani/izvozi**

2. **Izberite Predaja med izmenami**
   
   V prikazanem meniju izberite **»Predaja med izmenami«**

3. **Izberite način pošiljanja**
   
   Sistem samodejno ustvari datoteko `.lmp` in odpre ploščo za deljenje, kjer lahko izberete:
   - **WeChat** → pošljite sodelavcu ali delovni skupini
   - **E-pošta** → pošljite na prejemnikov e-naslov
   - **AirDrop** → hitri prenos med napravami Apple
   - **Druge aplikacije** → QQ, DingTalk, WeCom itd.

### Lastnosti datoteke za predajo

- **Format**: `.lmp` (format, lastniški za LogMetric Pro)
- **Ime datoteke**: `LogMetricPro_Predaja_Kontejner/Datum.lmp`
- **Cene**: **samodejno izbrisane** (zaščita poslovnih skrivnosti)
- **Vsebuje**: vse podatke hlodov, informacije serije, interne zapise, trenutne nastavitve

---

## 3. Prejemanje in odpiranje datoteke za predajo

### Potek

Ko prejmete datoteko `.lmp`:

1. **Tapnite nanjo**
   
   V WeChatu, e-pošti ali drugi aplikaciji poiščite datoteko `.lmp` in tapnite nanjo

2. **Izberite način odpiranja**
   
   V prikazanem meniju izberite **»Odpri v LogMetric Pro«**

3. **Potrdite uvoz**
   
   Aplikacija prikaže potrditveno pogovorno okno:
   ```
   Uvozi datoteko za predajo
   Ali želite uvoziti to datoteko za predajo? Po uvozu jo lahko vidite na seznamu projektov.
   [Prekliči]  [Uvozi]
   ```

4. **Začnite z urejanjem**
   
   Po uvozu se projekt prikaže na seznamu projektov – tapnite nanj za **nadaljevanje urejanja tam, kjer je bilo končano**

> 💡 **Namig**: Ob uvozu se ustvari nov projekt – obstoječi projekti se ne prepišejo.

---

## 4. Tipični scenariji uporabe

### Scenarij A: Zaporedje iste osebe na projektu

```
Sodelavec izmene A:
1. Vnese del podatkov o hlodih
2. Pred koncem izmene klikne »Predaja med izmenami« in pošlje sodelavcu izmene B
3. Sodelavec izmene B prejme in nadaljuje z vnosom preostalih podatkov
```

### Scenarij B: Med napravami

```
Terenski sodelavec:
1. Vnaša podatke v iPad
2. Pošlje prek AirDrop-a ali WeChata v pisarniški računalnik
3. Pisarniško osebje nadaljuje z Mac različico
```

### Scenarij C: Pregled vodje in vrnitev

```
Operater:
1. Po končanem vnosu pošlje predajo vodji
2. Vodja pregleda in spremeni, nato pošlje predajo nazaj operaterju
3. Operater dobi končne potrjene podatke
```

---

## 5. Opombe

### Podatki o cenah

Datoteka `.lmp` **samodejno izbriše vse podatke o cenah**, vključno z:
- Fiksno enotno ceno
- Cenami posameznih razredov
- Nastavitvami, povezanimi s cenami

To je namenjeno zaščiti poslovnih skrivnosti pošiljatelja. Prejemnik lahko po uvozu sam nastavi cene in nato izvozi poročila.

### Varnost podatkov

- Datoteke za predajo se prenašajo prek aplikacij tretjih oseb (WeChat/e-pošta) – bodite pozorni na varnost informacij
- Za občutljive podatke priporočamo uporabo šifrirane e-pošte ali podjetnega omrežja
- Funkcija varnostne kopije v oblaku (poglavje 8) je varnejša možnost prenosa

### Združljivost različic

- Datoteke `.lmp` zahtevajo enako ali novejšo različico LogMetric Pro
- Če se prikaže napaka o nezdružljivosti formatov, naj se obe strani posodobita na najnovejšo različico

---

## 6. Razlika glede na tradicionalni izvoz

| Postavka | Predaja med izmenami (.lmp) | Izvoz projektne datoteke (.json) |
|----------|------------------------------|----------------------------------|
| **Glavna raba** | Hitra predaja dela | Popolna varnostna kopija ali dolgoročno arhiviranje |
| **Cene** | Samodejno izbrisane | Ohranjene |
| **Velikost datoteke** | Manjša | Večja (vključuje posnetke) |
| **Enostavnost uporabe** | En klik za deljenje | Več korakov |
| **Priporočeni scenarij** | Vsakodnevna predaja izmen | Popolna varnostna kopija in selitev |

---

## 7. Pogosta vprašanja

**V: Ali lahko isto datoteko za predajo pošljem večkrat?**
O: Da. Vsakokrat ko pošljete, se zajame trenutni posnetek podatkov. Datoteko lahko pošljete več osebam.

**V: Kaj, če prejemnik nima nameščenega LogMetric Pro?**
O: Nameščena mora biti aplikacija. Če želi samo ogledati podatke, priporočamo pošiljanje PDF ali Excel poročila.

**V: Ali imajo datoteke za predajo čas veljavnosti?**
O: Ne. Datoteke `.lmp` se lahko shranjujejo dlje časa, vendar priporočamo čimprejšnji uvoz, da se izognete težavam z združljivostjo različic.

**V: Ali lahko hkrati pošljem več osebam?**
O: Da, v plošči za deljenje izberite več prejemnikov.

# Poglavje 10 — Nastavitve

> Opomba: v aplikaciji je to poglavje oštevilčeno kot "Poglavje 10", datoteka pa je oštevilčena `11_settings`. Spodnji razdelki sledijo vrstnemu redu od zgoraj navzdol v čitalniku Nastavitev. Nastavitve, povezane z **vsebnostjo vlage MC, EMC, imenom podjetja** itd., so v **Arhivu serije** (obalno okno s podatki projekta), ne v čitalniku Nastavitve – glejte "Povezovanje z arhivom serije" na koncu tega poglavja.

---

## 1. Splošne nastavitve

### TEMA

Preklapljajte med **Temno** (Dark) in **Svetlo** (Light) temo.

### JEZIK

Možnosti: **中文**, **English**, **Slovenščina**.

### Spodnji varnostni odmik (samo Android)

Če sistematska navigacijska vrstica ali vodoravna usmerjenost zakriva spodnje vnosno območje, lahko tukaj dodate dodaten odmik (**0–100 dp**). Dejanski odmik je `max(sistemski varnostni odmik, ta nastavitev)`.

### Način za začetnike

Če je vključeno, vmesnik prikazuje dodatna navodila za vodenje. Ko boste bolj seznanjeni z aplikacijo, ga lahko izključite za poenostavitev vmesnika. V stranski plošči je ook gumb **Uporabniški priročnik**, ki odpre vgrajeno navodilo za uporabo (poglavja ustrezajo mape `assets/help/`).

---

## 2. Nastavitve vnosa

### Profesionalna tipkovnica (ne za Android)

V **iOS / macOS** lahko vključite vgrajeno profesionalno številsko tipkovnico za pospešitev vnosa (Android te možnosti nima).

### Zvok ob pritisku tipke

Ali naj se ob pritisku številske tipke predvaja zvok.

### Potrditev pred dodajanjem

Pred shranjevanjem se prikaže potrditveno pogovorno okno s prikazom trenutne dolžine, premera itd. za dvojno preverjanje – primerno za preprečevanje nenamernih dotikov.

### Zvok ob uspešnem shranjevanju

Ali naj se po shranjevanju vrstice predvaja kratek zvok potrditve.

### Hiter način

Za hitro, neprekinjeno vnosno delo na terenu. Vključitev razkrije podmožnosti:

| Podmožnost | Opis |
|-----------|------|
| Samodejna decimalna pika | Številki, kot je `45`, se samodejno pretvorita v decimalno število `4.5` (enaka pravila kot v glavnem vmesniku) |
| Samodejni prehod Dolžina→Premer | Kazalec se po vnosu dolžine samodejno premakne na premer |
| Samodejno nadaljevanje številk | ID se po vsakem vnosu poveča za +1 |
| Shrani ob kliku na razred | S klikom na gumb razreda se shrani neposredno – ni treba klikniti gumba za shranjevanje |
| Samodejno shranjevanje pri premeru | **Ko je »Prikaži razred« izključen**: premer lahko samodejno shrani, ko so izpolnjeni pogoji (glejte navodila vmesnika za podrobnosti) |

> **Opomba:** V načinu **imperialnega vnosa** (glejte »Enote dolžine/premera« spodaj) sta **samodejna decimalna pika** in **samodejni prehod Dolžina→Premer** onemogočena.

---

## 3. Prostornina in teža (oddelek »Prostornina« v nastavitvah)

### Opozorilo ob presežku skupne prostornine

Če je vključeno, nastavite prag prostornine (v **m³**). Ko skupna prostornina seznama preseže ta prag, zgornje statistično območje prikaže opozorilo (npr. opozorilo prostornine kontejnerja).

### Enote vnosa dolžine/premera (pomembno)

**Ločene stikala za metrično/imperialno enoto ni več.** Trenutna logika:

- Ko je **Omogoči formulo za prostornino po meri** vključena in izbrana formula spada med formule za **ploskovne čevlje (BF)**, se dolžina vnaša v **čevljih (ft)**, premer pa v **palcih (in)**.  
  Formule BF vključujejo: `Doyle`, `Roy`, `Scribner Decimal C`, `International 1/4"` in njihove **različice z preglednicami** (`Scribner [BF]` preglednica, `Intl 1/4" [BF]` preglednica) itd. (skladno z `isImperialFormula` v kodi).
- V vseh drugih primerih velja **metrični sistem**: dolžina v **metrih (m)**, premer v **centimetrih (cm)**.

Odbitki dolžine/premera se v imperialnem načinu prikažejo in vnašajo v **palcih**, vendar se interno shranjujejo v centimetrih.

### Omogoči formulo za prostornino po meri

Izključeno: uporablja se privzeta formula valja **V = π × (d/200)² × L** (d v cm, L v m).

Vključeno: izberete lahko iz spustnega seznama, razvrščenega po kategorijah (npr. **Osnovno**, **A Tip**, **CZ/SK**, **A. Nilson**, **Drugo**, **B Tip preglednica**, **HU** itd.):

- **Evropa / Univerzalno**: Huber (EN 1309-2), Czech ČSN 48 0009, Slovaška preglednica `Lookup Table-igor` itd.
- **Severnoameriški BF**: Doyle, Roy, Scribner Dec.C, International 1/4" (in njihove različice s preglednicami)
- **Druge matematične formule**: Hoppus, JAS, NF B53-020, Ontario, MARN, Local Java, koeficient D²L, Drva itd.
- **CZ/SK serija**: ČSN/STN, Smrek, Buk, Dub itd.
- **B Tip SQLite preglednica**: GOST 2708-75, ISO 4480-83, Scribner / Intl različice s preglednicami itd.
- **Madžarska HU serija** itd.

Zamenjava formule **preračuna** prostornino vseh vnosov.

### Decimalna mesta prostornine

Izberite **0–3** decimalnih mest za prikaz in zaokroževanje shranjevanja.

### Zaokroževanje ploskovnih čevljev (BF formule)

Prikaže se samo, ko je trenutna formula **Doyle / Roy / International 1/4"** (ali njihove `intl14Table` različice):

- **Doyle / Roy**: Brez / Navzdol / Navzgor / Sredinsko
- **International 1/4"**: vključuje možnosti **USFS**, povezane z uradnimi pravili (možnosti se lahko razlikujejo od Doyle/Roy)

> Zaokroževanje za druge BF formule (npr. Scribner) sledi formuli v Dodatku A. **Ne-BF formule te nastavitve ne upoštevajo.**

### Prikaži težo v statistični vrstici / Enota teže

Zahteva, da je v **Arhivu serije** izbrana vrsta lesa in da obstajajo prostornine vnosov. V statistični vrstici prikaže **ocenjeno skupno težo**.  
Enota teže: **auto** (pod 1000 kg pokaži kg, nad 1000 kg pokaži t), fiksno **kg** ali fiksno **t**.  
**Vsebnost vlage MC (%)** se nastavi v Arhivu serije in se uporablja pri pretvorbi teže – glejte spodaj.

---

## 4. Razredi in odbitki (oddelek »Razredi« v nastavitvah)

### Prikaži razred

Če je izključeno, se gumbi za razred lahko skrijejo iz glavnega vmesnika (vedenje "Samodejno shranjevanje pri premeru" v Hitrem načinu se temu primerno spremeni).

### Število gumbov za razred na glavnem vmesniku

**2–6** mest; razredi, ki niso na gumbih, so še vedno dostopni prek izbirnika v vrstici.

### Upravljanje sklada razredov

Razširite za **dodajanje / brisanje / vlečenje za prerazvrščanje** razredov (največ **15**). Če izbrišete razred, ki se že uporablja, boste pozvani, da se vnose dodeli neznanemu razredu (podrobnosti pogovornega okna se lahko razlikujejo).

### Dolg pritisk na gumb razreda za preimenovanje

Dolg pritisk na gumb razreda na glavnem vmesniku za neposredno preimenovanje.

### Izračunaj premer (izpeljan premer)

Če je vključeno, se lahko premer izpelje iz drugih merilnih pravil. Izberete lahko **način zaokroževanja**: Navzgor / Navzdol / Mešano (glejte spustne možnosti za podrobnosti).

### Odbitki dolžine/premera

Za napake, odstranitev lubja itd.: **Odbitki dolžine**, **Odbitki premera** (enote so skladne s trenutnim metričnim/imperialnim vnosom: cm ali in).

**Prikaži odbitne vrednosti na seznamu**: Vključeno → na seznamu se prikažejo že odbitne dimenzije. Izključeno → vmesnik še vedno prikazuje izvirne vnose, odbitki pa se uporabijo samo pri **izračunu prostornine**.

---

## 5. Nastavitve cen

### Omogoči cene

Če je vključeno, je mogoče pri izvozu uporabljati enotne cene in zneske.

### Valuta

Podpira **EUR €**, **USD $**, **CNY ¥** in drugo (glejte spustni seznam).

### Način določanja cene

| Način | Opis |
|-------|------|
| Fiksna enotna cena | Enaka cena za vse razrede |
| Po razredu | Različna enotna cena za vsak razred v skladu razredov |
| Po vrsti lesa + razredu | Najbolj natančno – različne cene za vsako kombinacijo vrste lesa in razreda |

### Stopnja davka

Nastavite stopnjo DDV v %; poročila samodejno izračunavajo znesek davka in skupaj z davkom.

### Prikaži cene v PDF/Excel

Ločeno nadzoruje, ali **PDF** in **Excel** vključujeta stolpce s cenami (smiselno samo, če je »Omogoči cene« vključeno).

> **Ali se v izvozu prikaže ime podjetja**: stikalo "Prikaži v PDF" za "Moje podjetje" je v **Arhivu serije**, ne v tem oddelku za cene – glejte "Povezovanje z arhivom serije" spodaj.

---

## 6. Možnosti izvoza (oddelek »Izvoz« v nastavitvah)

- **Prikaži oznake smeri v PDF/Excel**: ali naj se v izvozu prikažejo oznake, povezane s smerjo.
- **Prikaži dvojne oznake v PDF/Excel**: ali naj se v izvozu prikažejo stolpci za »dvojne oznake« (skladno z nastavitvijo prikaza skupin na seznamu).

Za celoten potek izvoza glejte **Poglavje 5 – Shranjevanje in izvoz**.

---

## 7. Varnostna kopija (znotraj nastavitev)

- **Lokalna samodejna varnostna kopija**: stikalo, izbira mape, sprememba mape, upravljanje datotek varnostne kopije itd.
- **Varnostna kopija v oblaku**: stikalo, stanje povezave, upravljanje varnostnih kopij v oblaku itd.

Podrobnosti: **Poglavje 8 – Varnostna kopija v oblaku** in **Poglavje 9 – Lokalna samodejna varnostna kopija**.

---

## Povezovanje z arhivom serije (vsebnost vlage · EMC · teža · podatki podjetja)

Naslednje je v **Glavni vmesnik → Arhiv serije / Podatki projekta**, **ne** v čitalniku Nastavitve:

### Vsebnost vlage MC (%)

V istem območju kot **Vrsta lesa, Gostota**; tapnite za urejanje. Uporablja se za **oceno teže** in opozorila, povezana z vsebnostjo vlage.

### Hitri prednastavitve MC in izračun EMC (okoljska ocena EMC)

Prednastavitve: Popolnoma suh, Zračno suh pribl. 12 %, Gradbeni les, Točka nasičenja vlaken 30 %, Svež les itd. (glejte vmesnik).

**Okoljska ocena EMC**: vnesite **temperaturo (°C)** in **relativno vlažnost (%)**, da ocenite **ravnotežno vsebnost vlage EMC** z modelom Hailwood-Horrobin – lahko jo **uporabite za MC**.

> **EMC je ravnotežni cilj, ne vrednost, ki se prišteva trenutni MC.** Če je npr. trenutna MC 30 %, okoljski EMC pa 12 %, se les sčasoma nagiba k **pribl. 12 %**, ne k 42 %.

### Ocena skupne teže

Prikaže se v območju arhiva serije, ko sta izbrani vrsti lesa in obstaja skupna prostornina (v m³), v povezavi z nastavitvijo »Teža v statistični vrstici«.

### Ime podjetja in PDF

Uredite podatke podjetja kupca/prodajalca; za nastavitev, ali se **ime podjetja prikaže v PDF/Excel**, se uporabi stikalo v arhivu serije (za Excel velja enaka logika – glejte dejanski izvoz).

---

## Seznam za preverjanje

1. Odprite Nastavitve in od zgoraj navzdol preverite vsak oddelek glede na ta navodila.
2. Preklopite med **Huber** in **Doyle** ter potrdite, da se enote vnosa preklopijo med **m/cm** in **ft/in**.
3. Odprite Arhiv serije in potrdite, da so MC, okoljski izračun in stikala za prikaz podjetja na mestih, opisanih v tem navodilu.

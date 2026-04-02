# Poglavje 5 — Shranjevanje in izvoz

## 1. Pregled funkcije izvoza

**Namen**: Izvoz vpisanih podatkov o hlodih v standardizirane formate poročil (PDF/Excel), primerno za arhiviranje, deljenje in usklajevanje.

**Podprti formati**:
- **PDF**: Standardno poročilo o merjenju lesa, primerno za tiskanje in pošiljanje e-pošte
- **Excel**: Uredljivi tabelarični podatki, primerni za nadaljnjo obdelavo
- **JSON**: Varnostna kopija projekta (vključuje vse podatke)
- **ZIP**: PDF + Excel + JSON v paketu

---

## 2. Meni Shrani/izvozi

V zgornjem desnem delu glavnega vmesnika kliknite gumb **Shrani/izvozi** (ikona 💾), odpre se meni z dejanji:

### Zgornji del — Upravljanje podatkov

| Možnost | Funkcija |
|---------|----------|
| **Shrani v interno evidenco** | Shrani trenutne vnesene podatke kot posnetek (interna evidenca), primerno za kasnejši pregled ali obnovitev |
| **Odpri interno evidenco** | Ogled vseh zgodovinskih posnetkov projekta, možnost obnovitve ali izvoza |
| **Uvozi projektno datoteko** | Uvozi podatke v trenutni projekt iz JSON varnostne kopije |

### Spodnji del — Izvoz in deljenje

| Možnost | Funkcija |
|---------|----------|
| **Predaja med izmenami** | Ustvari datoteko `.lmp` in jo pošlji drugi osebi, ki lahko z LogMetric Pro **samodejno uvozi** podatke za nadaljevanje vnosa |
| **Ustvari PDF** | Izvoz standardnega poročila o merjenju lesa (vključuje podatke podjetja, podroben seznam hlodov in povzete statistike) |
| **Izvozi Excel** | Izvoz urejljive datoteke `.xlsx` s podrobnimi podatki in povzetki |
| **ZIP paketni izvoz** | Paketni izvoz PDF + Excel + JSON v eni datoteki |

> Po izvozu lahko podatke pošljete prek sistema za deljenje v WeChat, e-pošto itd. ali shranite lokalno.

---

## 3. Vsebina PDF izvoza

Ustvarjeno PDF poročilo vsebuje naslednja območja:

### Glava strani
- Naslov: **PACKING LOG LIST / SHIPMENT**
- Spodnja ločilna črta

### Območje s podatki podjetja (po izbiri)
- Lastni podatki podjetja (leva stran): ime, naslov, telefon, e-pošta, davčna številka, bančni račun
- Podatki kupca/prodajalca (desna stran): enako kot zgoraj

### Tabela s podatki projekta
- Datum
- Številka kontejnerja
- Opis
- Lokacija
- Merilec
- Splošna opomba k naročilu

### Podrobna tabela hlodov
| Stolpec | Opis |
|---------|------|
| Zap. št. | Zaporedna številka |
| Številka | Številka hloda |
| Razred | Oznaka razreda (npr. F, A, B) |
| Dolžina | Meter (m) ali čevlji (ft) |
| Premer | Centimeter (cm) ali palci (in) |
| Prostornina | Kubični metri (m³) ali prostorninski čevlji (BF) |
| Znesek | Če je funkcija cen vključena |
| Opomba | Opomba k posamezni vrstici |

**Značilnosti oblikovanja**:
- **Črtasto ozadje**: izmenično siva/bela vrstice za lažje branje
- **Oznake skupin**: Dvojno označene vrstice imajo na levi strani modro odebeljeno obrobo, besedilo je krepko
- **Oznake**: Pri označenih dolžinah/premerih/razredih je prikazan simbol ↑

### Tabela povzetka cen (če je funkcija cen vključena)
- Po razredih: količina, prostornina, enotna cena, znesek
- Skupaj: skupno število kosov, skupna prostornina, povprečna enotna cena, znesek brez davka
- Davek (če je stopnja davka nastavljena)
- Znesek z davkom

### Območje povzete statistike
- Skupno število kosov, skupna prostornina
- Porazdelitev po razredih (npr. F:15 kosov A:20 kosov)
- Statistika majhnih dimenzij (npr. <4m:3 kosi <30cm:5 kosov)

### Noga strani
- LogMetric Pro | Datum izvoza

---

## 4. Vsebina Excel izvoza

Excel datoteka vsebuje naslednje dele:

### Informacije v glavi (prve 3-4 vrstice)
- 1. vrstica: Datum + ime podjetja (če je v nastavitvah nastavljeno prikazovanje podjetja)
- 2. vrstica: Številka kontejnerja + prodajalec (če je prisoten)
- 3. vrstica: Opis + lokacija + merilec (če so prisotni)
- 4. vrstica: Splošna opomba k naročilu (če je prisotna)

### Podatkovna tabela
Enaka struktura stolpcev kot v PDF, podpira:
- Oznake (↑)
- Barve ozadja skupin (svetlo modra) in obrobe

### Območje povzetka
- Skupno število kosov, skupna prostornina
- Tabela statistike po razredih
- Statistika majhnih dimenzij (<4m, <2,5m, <30cm)
- Statistika cen (če je vključena)

### Paketni izvoz posnetkov
Struktura z več delovnimi listi:
- Delovni list 0 »Povzetek«: Pregled datumov, kontejnerjev, števila kosov, prostornin vseh posnetkov
- Delovni listi 1–N: Podroben seznam vsakega posnetka (enaka struktura)

---

## 5. Predaja med izmenami (.lmp datoteka)

### Namen
Trenutne podatke projekta zapakirajte v datoteko `.lmp` in jo pošljite drugi osebi, ki **s klikom na datoteko samodejno uvozi** podatke in lahko nadaljuje z vnosom.

### Tipični scenariji

| Scenarij | Opis |
|----------|------|
| **Zamenjava med izmenama** | A izmeri do polovice, pošlje .lmp kolegu B, ki nato nadaljuje z vnosom |
| **Telefon je zmanjkal baterijo/okvaro** | Hitro prenesite podatke na drug telefon za nadaljevanje dela |
| **Sodelovanje ekipe** | Terenski sodelavec pošlje vnos v pisarno, kjer nadaljujejo z urejanjem ali izvozom poročil |

### Način uporabe
1. Kliknite »Predaja med izmenami« → izberite način pošiljanja (WeChat, e-pošta, AirDrop itd.)
2. Prejemnik prejme datoteko `.lmp` → tapne nanjo → izbere **Odpri v LogMetric Pro**
3. Samodejno se odpre vmesnik za uvoz, potrdite in podatki se prikažejo na seznamu

### Značilnosti
- **Cene se samodejno izbrišejo** (zaščita poslovnih skrivnosti)
- Vključuje: seznam hlodov, podatke serije, interne zapise, trenutne nastavitve
- Prejemnik lahko nemudoma nadaljuje z vnosom

---

## 6. ZIP paketni izvoz

**Namen**: Pridobite vse formatne datoteke projekta naenkrat.

**Vsebuje**:
- JSON varnostno kopijo (popolni podatki)
- PDF poročilo (različica za tiskanje)
- Excel razpredelnico (različica za urejanje)

---

## 7. Nastavitve izvoza

**Pot:** Nastavitve → Možnosti izvoza

| Možnost | Opis |
|---------|------|
| **Prikaži oznake v PDF/Excel** | Pri označenih dolžinah/premerih/razredih je prikazan simbol ↑ |
| **Prikaži skupine v PDF/Excel** | Dvojno označene vrstice so poudarjene z modrimi robovi in ozadjem |
| **Prikaži podatke podjetja v PDF** | Na vrhu poročila so prikazani podatki vašega podjetja in kupca/prodajalca |
| **Prikaži cene v PDF/Excel** | Kadar je funkcija cen vključena, izvozi stolpce z zneski in povzetki |

### Nastavitve cen
**Pot:** Nastavitve → Cene

**Načini določanja cen**:
- **Fiksna enotna cena**: enaka cena za vse razrede
- **Po razredu**: različna enotna cena za vsak razred
- **Po vrsti lesa + razredu**: najbolj natančno – različna cena za vsako kombinacijo vrste lesa in razreda

**Davek**: lahko nastavite stopnjo DDV, poročila pa samodejno izračunavajo znesek davka in skupaj z davkom.

---

## 8. Shranjevanje po izvozu

Po izvozu so na voljo tri možnosti:

| Način | Opis |
|-------|------|
| **Deli** | Pošlji prek sistema za deljenje – WeChat, e-pošta, WhatsApp itd. |
| **Shrani v Prenosi** | Shrani neposredno v mapo »Prenosi« naprave |
| **Izberi lokacijo** | Odpre se pogovorno okno za izbiro datoteke in poti shranjevanja |

> iOS predvsem uporablja ploščo za deljenje; Android podpira shranjevanje v lokalni pomnilnik pred pošiljanjem.

---

## 9. Poimenovanje datotek

Sistem samodejno ustvari imena datotek:
- **PDF**: `OakLog_ŠtevilkaKontejnerja_Datum_Čas.pdf`
- **Excel**: `Datum_ŠtevilkaSerije_ŠtevilkaKontejnerja.xlsx`
- **JSON varnostna kopija**: `LogMetricPro_VarnostnaKopija_Kontejner/Serija_Datum_Čas.json`
- **Datoteka predaje**: `LogMetricPro_Predaja_Kontejner/Datum_Čas.lmp`
- **ZIP**: `OakLog_izvoz_Datum_Čas.zip`

---

## 10. Pogosta vprašanja

| Vprašanje | Odgovor |
|-----------|---------|
| Excel se ne odpre? | Uporabite Microsoft Excel ali združljiv program (npr. WPS) za odpiranje datotek `.xlsx` |
| Napake pri prikazu kitajskih znakov? | PDF uporablja pisavo Noto Sans SC za pravilen prikaz kitajskih znakov |
| Ali lahko v izvoženem Excelu formule izračunavajo? | Vrednosti prostornine so shranjene kot številke, neposredno uporabne v formulah |
| Ne želite deliti podatkov o cenah? | Uporabite funkcijo »Predaja med izmenami« – cene se samodejno izbrišejo |
| Ali lahko izvozim posamezen interni zapis? | Odprite »Interni zapisi« → izberite zapis → izvozite PDF/Excel/JSON |

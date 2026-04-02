# Poglavje 6 — Interni zapisi

---

## 1. Kaj so interni zapisi?

**Interni zapis** je **popoln posnetek** trenutnega seznama v določenem trenutku.

Shrani vse vnose hlodov iz tistega trenutka, omogoča pregledovanje zgodovinskih podatkov, ne da bi vplival na nadaljnji vnos.

> Analogija: interni zapis je kot »fotografija« ob koncu vsake nakladalne serije – shrani popoln rezultat merjenja.

---

## 2. Ustvarjanje internega zapisa

**Metoda 1:** Meni Shrani/izvozi → **Shrani v interno evidenco**

**Metoda 2:** Uporabite funkcijo »Začni novo stran od tu« (glej poglavje 3) – sistem samodejno shrani razdeljene podatke v interno evidenco.

**Metoda 3:** Ob kliku **Nova (Nova serija)** sistem samodejno shrani trenutni seznam kot interni zapis in nato izprazni seznam za nov vnos.

---

## 3. Ogled internih zapisov

V zgornjem delu glavnega vmesnika kliknite **💾** → **Odpri interno evidenco**

Prikazovalnik internih zapisov prikaže vse interne zapise tega projekta, vsak vsebuje:
- Ime zapisa in čas ustvarjanja
- Skupno število kosov in skupno prostornino
- S klikom si lahko ogledate podroben seznam

---

## 4. Urejevalnik internih zapisov

Kliknite **Uredi** v seznamu interne evidence za vstop v urejevalnik:

### Osnovne operacije
- **Ogled vnosov**: Prikazuje vse podrobnosti hlodov v zapisu
- **Urejanje podatkov**: Neposredno spremenite številko, razred, dolžino, premer, opombo
- **Dodajanje/brisanje vrstic**: Podrsajte levo za izbris; kliknite »+ Dodaj« za dodajanje
- **Razvrščanje**: Kliknite glavo stolpca **Zap. št.** za preklop med naraščajočim/padajočim vrstnim redom
- **Izvoz**: Ustvarite PDF/Excel za ta zapis

### Dvojne oznake
- Z dolgim pritiskom izberite več vrstic → kliknite gumb »Skupina« za označitev več hlodov kot enega (dvojna oznaka)
- Dvojno označene vrstice imajo na levi strani barvno obrobo
- Podrsajte levo po dvojno označeni vrstici za razdružitev

---

## 5. Funkcija preverjanja (preverjanje podatkov)

**Namen**: Vnos podatkov se preverja glede na izvirne dokumente (papirnate zapise, poročila nasprotne stranke), da se ugotovijo in popravijo razlike.

Vstopite v urejevalnik interne evidence → kliknite gumb **Preveri** na dnu in izberite način:

### Način A: Seznamsko preverjanje
Primerno za hitro serijsko preverjanje – pregled več vrstic naenkrat.

**Kako deluje**:
- Seznam prikazuje vse vnose, lahko se pomikate navzgor/navzdol
- Podrsajte levo za označbo stanja: **Preverjeno** (zeleno) / **Vprašljivo** (oranžno)
- S klikom na kateri koli stolpec lahko neposredno urejate
- Podpira filtriranje: Vsi / Nepreverjeni / Preverjeni / Vprašljivi

**Pomembno o oznakah**:
| Oznaka | Pomen |
|--------|-------|
| Brez oznake | Še nepreverjeno |
| Zelena obroba | Preverjeno – podatki so pravilni |
| Oranžna obroba | Vprašljivo – potrebno dodatno preverjanje |

### Način B: Vnos za vnosom (pregled kartic)
Primerno za skrbno preverjanje posameznega hloda.

**Kako deluje**:
- Naenkrat je prikazana en velika kartica enega hloda
- Podrsajte levo/desno za preklop na prejšnjega/naslednjega hloda
- S klikom na polje lahko neposredno urejate
- Spodnji gumbi za hitro označevanje: ✓ Preverjeno / ⚑ Vprašljivo
- Prikazuje izračun prostornine v realnem času za enostavno primerjavo z dokumenti

**Preklop pogleda**:
- **Podroben pogled**: Prikazuje številko, razred, dolžino, premer, prostornino – vsa polja
- **Pogled prostornine**: Povečan prikaz vrednosti prostornine za enostavno primerjavo z nasprotno stranjo

### Po končanem preverjanju
Kliknite »Dokončano« – sistem zapiše spremembe nazaj v interni zapis:
- Urejena polja se posodobijo
- Izbrisane vrstice se odstranijo
- Dodane vrstice se vstavijo
- Stanje preverjanja (preverjeno/vprašljivo) se ohrani za nadaljnji pregled

---

## 6. Obnovitev internega zapisa v trenutni seznam

### Namen
**Kopijo** zgodovinskega internega zapisa naložite v trenutni seznam, na podlagi podobne vsebine spremenite in nato **shranite kot nov zapis**.

**Tipični scenarij**:
- Dva kontejnerja sta skoraj enaka – treba je spremeniti samo nekaj hlodov
- Najprej obnovite prejšnji kontejner, spremenite razlike, nato shranite kot zapis za novega

### Način uporabe
V urejevalniku interne evidence kliknite **Obnovi**:
1. Podatki izbranega zapisa se **kopirajo** v trenutni seznam (izvirni zapis se ne izbriše)
2. V trenutnem seznamu spremenite vnose, ki jih je treba spremeniti
3. Ko končate, znova kliknite »Shrani v interno evidenco« in shranite kot nov posnetek

### ⚠️ Pomembno opozorilo
**Obnovitev bo prepisala vsebino trenutnega glavnega seznama!**

Pred obnovitvijo se prepričajte, da:
- Trenutni seznam **nima vsebine**, ali
- Je trenutni seznam **že shranjen kot interni zapis**

> 💡 Obnovitev je **kopiranje** – izvirni zapis se ne izbriše. Iz istega zapisa lahko večkrat obnovite različne različice.

---

## 7. Paketni izvoz vseh internih zapisov

Na strani s seznamom projektov kliknite **⋮** na kartici projekta → **Izvozi vse posnetke (Excel)**.

Ustvari datoteko Excel z več delovnimi listi:
- **Delovni list 0**: Povzetek vseh zapisov (ime, datum, število kosov, prostornina)
- **Delovni listi 1–N**: Podroben seznam hlodov za vsak zapis

---

## 8. Uvoz interne evidence prek JSON

Interni zapisi se lahko uvozijo iz datoteke `.json` (format: `oak_snapshot_export_v1`).

**Kako:** Meni Shrani/izvozi → **Uvozi projektno datoteko** → izberite datoteko `.json`.

> Pred uvozom priporočamo, da trenutni seznam shranite kot interni zapis, da preprečite prepisovanje podatkov.

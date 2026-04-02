# Poglavje 2 — Upravljanje projektov

## 1. Zakaj deliti projekte?

**Glavni namen**: Popolna ločitev podatkov različnih poslov, preprečevanje mešanja naročil in lažje upravljanje.

### Pogosti načini delitve

| Scenarij | Način | Primer |
|----------|-------|--------|
| **Različni kontejnerji** | En kontejner = en projekt | Kontejner A, Kontejner B, Kontejner C |
| **Različni dobavitelji** | Po imenu dobavitelja | Hrast Les, Smrekova Gozdna |
| **Različni datumi** | Po datumu | Serija z dne 15. 3., Serija z dne 20. 3. |
| **Različne vrste lesa** | Po vrsti lesa | Projekt hrast, projekt smreka, projekt bukev |
| **Različne stranke** | Po kupcu | Stranka A, Stranka B |

> 💡 Način delitve je povsem poljuben – **ključno je, da so podatki znotraj istega projekta medsebojno povezani, med različnimi projekti pa povsem neodvisni**.

### Vsak projekt je popolnoma neodvisen

En projekt = ena zaključena delovna enota, ki vsebuje:

- **Lasten seznam vnosa hlodov** – pripada samo temu projektu
- **Ločene podatke serije** – številka kontejnerja, kupec/prodajalec, vrsta lesa itd.
- **Ločeno interno evidenco (posnetke)** – vsa zgodovina projekta
- **Ločene statistike** – prostornina, porazdelitev po razredih, zneski itd.

> Preklop projekta = preklop v povsem novo podatkovno okolje, brez tveganja mešanja podatkov.

---

## 2. Funkcija iskanja

| Način iskanja | Opis |
|---------------|------|
| **Ključna beseda** | Iskanje imena projekta ali številke serije (delno ujemanje zadostuje) |
| **Filtriranje po datumu** | Nastavitev časovnega obsega glede na »Zadnja sprememba« |
| **Kombinirano iskanje** | Hkratna uporaba ključne besede in datuma |

---

## 3. Organizacija z mapami

Pri številnih projektih jih uredite v mape:

| Dejanje | Način |
|---------|-------|
| **Ustvarjanje/prerazporeditev** | Kliknite **⋮** na kartici projekta → **Premakni v mapo** |
| **Strnitev/razširitev** | Kliknite naslov mape |
| **Preimenovanje/brisanje mape** | Kliknite **⋮** poleg naslova mape → Preimenuj ali Izbriši (po brisanju se projekti vrnejo v »Nerazvrščeno«) |

> En projekt je lahko hkrati samo v eni mapi.

---

## 4. Funkcije kartice projekta

Klik katerega koli dela kartice odpre projekt.

Kliknite **⋮** na desni strani:

| Funkcija | Uporaba |
|-----------|---------|
| **Preimenovanje** | Spremeni ime projekta |
| **Premakni v mapo** | Uvrsti projekt v mapo |
| **Odstrani iz mape** | Vrne projekt v »Nerazvrščeno« |
| **Izvozi vse posnetke (Excel)** | Izvoz vseh zgodovinskih posnetkov projekta v **eno datoteko Excel** (več delovnih listov, en posnetek na stran) |
| **Arhiviraj / Prekliči arhiviranje** | Arhiviran projekt je prikazan svetleje – lažje razlikovanje med aktivnimi in zaključenimi |
| **Izbriši** | **Trajno izbriše** projekt in vse podatke (neobnovljivo) |

---

## 5. Ustvarjanje in preklapljanje projektov

### Ustvarjanje projekta
1. Kliknite **＋** v spodnjem desnem kotu → **Nov projekt**
2. Vnesite **ime projekta** (empfohlen: z datumom/lokacijo/številko kontejnerja, npr. `2024-03-15-Luka-Hrast`)
3. Po potrditvi se odpre vmesnik za merjenje

> Številko serije, kupca/prodajalca in druge podatke vnesete po vstopu v projekt s klikom na **📋** v zgornjem levem kotu.

### Preklop projekta
- **Nazaj na seznam**: Kliknite **številko projekta** (npr. 🌲 001) na vrhu
- **Odpiranje drugega projekta**: Kliknite drugo kartico na seznamu

---

## 6. Pogosta vprašanja

| Vprašanje | Odgovor |
|-----------|---------|
| Koliko projektov lahko ustvarim? | Brez omejitev |
| Ali lahko spremenim številko projekta? | Ne, sistem jih dodeljuje samodejno: 001, 002… |
| Ali lahko podatki izginejo? | Samodejno shranjevanje je vključeno, vendar priporočamo redni izvoz varnostnih kopij |
| Ali lahko izbrišem povrnem? | **Ne neposredno**, toda če ste pred brisanjem naredili **varnostno kopijo v oblaku** ali **lokalno varnostno kopijo**, lahko podatke obnovite iz varnostne datoteke |
| Ali mape vplivajo na podatke projekta? | Ne, uporabljajo se samo za razvrščanje prikaza seznama |

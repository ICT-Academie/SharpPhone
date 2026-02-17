# 📱 SharpPhone – C# WinForms Course
📄 [Programmeren Gevorderd](https://github.com/ICT-Academie/readers/blob/main/dist/programmeren_gevorderd_csharp.pdf) (optioneel)
# Welkom bij de SharpPhone leerlijn

In deze module ga je stap voor stap een echte applicatie bouwen met **C# en WinForms**.  
We maken een programma waarin je gegevens kunt **toevoegen, bekijken, aanpassen en verwijderen** (CRUD).  
De data slaan we op in een **JSON-bestand**, en we bouwen ook een **login-systeem**.



![SharpPhone End Game](files/images/SharpPhoneEndGame.png)

## Wat betekent dit concreet?

- Je leert hoe een desktop applicatie werkt
- Je leert werken met formulieren, knoppen en events
- Je leert hoe je data bewaart zonder database (JSON)
- Je begrijpt hoe een login en validatie werkt
- Je bouwt iets dat lijkt op software uit de praktijk

## Waarom is dit nuttig?

Dit type applicatie vormt de basis van heel veel zakelijke software.  
Als je dit begrijpt, snap je hoe administratiesystemen, beheertools en interne bedrijfsapps werken.

## Wat kun je hier later mee?

- Voorbereiding op stages en projecten
- Sterke basis voor backend ontwikkeling
- Inzicht in data, structuur en logica
- Zelfstandige applicaties kunnen bouwen

---

Aan het einde van deze leerlijn heb je niet alleen code geschreven, maar een volledige werkende applicatie gebouwd.

En dat is precies hoe je programmeervaardigheden écht ontwikkelt:  
door iets tastbaars te maken.

---

## 🧭 Navigatie

- 🔹 [Week 1 – Intro WinForms & Debuggen](#week-1--intro-winforms--debuggen)
- 🔹 [Week 2 – Designer & Controls](#week-2--designer--controls)
- 🔹 [Week 3 – Events & InitializeComponent](#week-3--events--initializecomponent)
- 🔹 [Week 4 – SmartPhone Class & Data](#week-4--smartphone-class--data)
- 🔹 [Week 5 – JSON & Persistente Data](#week-5--json--persistente-data)
- 🔹 [Week 6 – Toevoegen & Bewerken](#week-6--toevoegen--bewerken)
- 🔹 [Week 7 – Voorraad & Delete](#week-7--voorraad--delete)
- 🔹 [Week 8 – Login & Afronding](#week-8--login--afronding)

---

---

## Week 1 – Intro WinForms & Debuggen

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/KrwRF4D6M3KWRww4M

🎯 **Focus**
- Introductie SharpPhone casus
- WinForms vs Console
- Event-driven concept
- Debuggen & breakpoints

🧪 **Praktijk**
- Button toevoegen
- Click-event maken
- Breakpoint plaatsen (F9)
- Debuggen met F5 / F10

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>


### Wat ga je maken
Je start een WinForms project en leert de basis van **debuggen** (breakpoints + stap-voor-stap).

### Opdrachten
1. Open `Form1` in de Designer en run de app (F5).
2. Voeg **1 Button** toe (naam: `btnTest`, tekst: `Test`).
3. Dubbelklik op de button om een Click-event te maken.
4. Zet in de event-methode een `MessageBox.Show("Klik!");`.

### Debug-opdracht
1. Zet een **breakpoint** op de regel met `MessageBox.Show(...)` (klik links van de regel of druk F9).
2. Run met F5 en klik op de button.
3. Gebruik **Step Over (F10)** om de regel uit te voeren.

## Hints
- Breakpoint = “pauze” in je code.
- Als je breakpoint niet raakt: controleer of je wel op de juiste button klikt.

🔝 [Terug naar navigatie](#-navigatie)

---

## Week 2 – Designer & Controls

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/oDNwpHQ3cMLa8w7Qf

🎯 **Focus**
- Toolbox gebruiken
- Controls plaatsen
- Properties (Text vs Name)
- Naming conventions

🧪 **Praktijk**
- Hoofdscherm bouwen
- ListBox correct gebruiken
- Events testen met breakpoints

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>

### Wat ga je maken
Je bouwt het hoofdscherm: label, **ListBox** en buttons.

### Opdrachten
1. Voeg een **Label** toe linksboven: `Text = Voorraad`
2. Voeg een **ListBox** toe (LET OP: geen ListView!)
    - `Name = listPhones`
    - Maak hem hoog (bijna hele form)
3. Voeg een **Button** toe naast de ListBox:
    - `Name = btnAddPhone`
    - `Text = +`
4. Voeg een **Button** toe:
    - `Name = btnModify`
    - `Text = Aanpassen`
5. Voeg alvast een derde button toe (voor CRUD):
    - `Name = btnDelete`
    - `Text = Verwijderen`

### Debug-opdracht
- Maak Click-events voor de 3 buttons.
- Zet in elke event-methode tijdelijk een `MessageBox.Show("...");`
- Zet breakpoints in alle 3 events en test dat je ze raakt.

## Hints
- Gebruik F4 om Properties te openen.
- Naam (Name) ≠ Text.
- Als je ListView gebruikt: doe Undo en kies ListBox.

🔝 [Terug naar navigatie](#-navigatie)

---

## Week 3 – Events & InitializeComponent

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/6AikoPwkncqmZyJAm

🎯 **Focus**
- Wat is een event
- Callbacks & Click-events
- sender & EventArgs
- InitializeComponent()

🧪 **Praktijk**
- Breakpoints in events
- Event-flow volgen
- Constructor debuggen

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>


### Wat ga je leren
- Wat is een **event** en een **callback**
- Waarom `InitializeComponent()` verplicht is
- `sender` en `EventArgs`

### Opdrachten
1. Open `Form1.cs` (View Code) en bekijk de event-methodes.
2. Zet een breakpoint in `btnAddPhone_Click`.
3. Run de app en klik op `+`.
4. Bekijk in Debug:
    - Wat is `sender`?
    - Welke regel wordt als eerste uitgevoerd?

### Bonus
- Zet een breakpoint in de constructor van `Form1()` en kijk wanneer hij wordt aangeroepen.


🔝 [Terug naar navigatie](#-navigatie)

---

## Week 4 – SmartPhone Class & Data

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/MqiPwbdpK8iDAg8Te

🎯 **Focus**
- SmartPhone class
- Properties & constructor
- List<SmartPhone>
- Data tonen in ListBox

🧪 **Praktijk**
- Objecten aanmaken
- List vullen
- Items.Add() gebruiken

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>

### Wat ga je maken
Je maakt een class `SmartPhone` en toont data in de ListBox.

### Opdrachten
1. Maak een nieuw bestand `SmartPhone.cs`.
2. Maak class `SmartPhone` met properties:
    - `Id` (int)
    - `Brand` (string)
    - `Model` (string)
    - `StorageSizeMb` (int)
    - `Price` (decimal)
3. Maak een constructor die alle properties zet.
4. In `Form1`:
    - Maak `List<SmartPhone> phones`
    - Voeg 1 item toe (PDF voorbeeld):
        - Id 0, Brand SamSang, Model Blackhole E55, Size 128000, Price 128.92
5. Vul de ListBox:
    - `listPhones.Items.Add($"{phone.Brand} {phone.Model}");`

## Hints
- `List<T>` zit in `System.Collections.Generic`
- Decimal in C# schrijf je met `m` achter de waarde (bijv. `128.92m`)


🔝 [Terug naar navigatie](#-navigatie)

---

## Week 5 – JSON & Persistente Data

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/mZgoxFCkSKWZTNsrN

🎯 **Focus**
- Wat is JSON
- JSON lezen & schrijven
- Persistente data
- JSON als opslaglaag

🧪 **Praktijk**
- data.json gebruiken
- Hardcoded data verwijderen
- Save na wijzigingen

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>

### Wat ga je maken
Data wordt geladen uit `data.json` bij opstarten en opgeslagen na wijzigingen.

### Opdrachten
1. Bekijk `data.json` in het project (phones + users).
2. Maak een class `SharpPhoneDatabase` met:
    - `List<SmartPhone> Phones`
    - `List<UserAccount> Users`
3. Maak class `UserAccount` met:
    - `Username`, `Password`, `FailedAttempts`, `Locked`
4. Maak class `SharpPhoneFileStorage` met methodes:
    - `Load()` -> SharpPhoneDatabase
    - `Save(SharpPhoneDatabase data)`
5. In `Form1`:
    - Laad data bij opstarten
    - Vul ListBox met alle phones
6. Zorg dat app niet crasht als JSON leeg is.

## Hints
- Gebruik `System.Text.Json`
- Zet JSON file op “Copy to output” (staat al goed in csproj)


🔝 [Terug naar navigatie](#-navigatie)

---

## Week 6 – Toevoegen & Bewerken

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/yNjoccC8gbR4SLSmk

🎯 **Focus**
- FormAddPhone
- DialogResult.OK / Cancel
- ShowDialog()
- Add vs Edit

🧪 **Praktijk**
- Tweede Form bouwen
- Input valideren
- JSON bijwerken

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>

### Wat ga je maken
Een tweede form waarmee je telefoons kunt toevoegen en aanpassen (PDF).

### Opdrachten
1. Maak een nieuw Form: `FormAddPhone`
2. Voeg labels + textboxes:
    - Merk (txtBrand)
    - Model (txtModel)
    - Size (txtSize)
    - Prijs (txtPrice)
3. Voeg buttons:
    - Cancel (btnCancel)
    - Ok (btnOk)
4. In btnOk:
    - valideer input
    - parse Size/Price
    - maak/werk SmartPhone bij
    - DialogResult = OK, Close()
5. In btnCancel:
    - DialogResult = Cancel, Close()
6. In `Form1` btnAddPhone:
    - open `FormAddPhone` met `ShowDialog()`
    - bij OK: voeg toe, Id = next, refresh, Save JSON
7. In `Form1` btnModify:
    - open `FormAddPhone` met geselecteerde SmartPhone
    - bij OK: overschrijf, refresh, Save JSON

🔝 [Terug naar navigatie](#-navigatie)

---

## Week 7 – Voorraad & Delete

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/NYxdyHmLdXGCagp55

🎯 **Focus**
- SmartPhone uitbreiden (Stock)
- JSON uitbreiden
- Delete functionaliteit

🧪 **Praktijk**
- Voorraad opslaan
- Delete implementeren
- UI & JSON synchroon

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>

### Wat ga je maken
Je breidt SmartPhone uit met voorraad en je maakt Delete.

### Opdrachten
1. Voeg property `Stock` toe aan SmartPhone (int).
2. Voeg in `FormAddPhone` een nieuw veld toe:
    - Voorraad (txtStock)
3. Pas OK validatie aan (Stock parse).
4. Zorg dat JSON ook `stock` bevat.
5. Maak btnDelete in `Form1` werkend:
    - verwijder geselecteerde telefoon
    - refresh
    - Save JSON




🔝 [Terug naar navigatie](#-navigatie)

---

## Week 8 – Login & Afronding

📺 **LessonUp**  
https://www.lessonup.com/nl/lesson/RbsoxPjWDqbdvpvg5

🎯 **Focus**
- Login Form
- Validatie gebruikers
- FailedAttempts
- Applicatieflow

🧪 **Praktijk**
- Login vóór Form1
- Pogingen bijhouden
- JSON updates

📄 **Aanvullende Lesnotities / Opdrachten**
> Hieronder vind je het uitgebreide weekbestand dat extra uitleg en opdrachten bevat.
>


### Wat ga je maken
Login form vóór het hoofdscherm. Users staan in JSON.

### Opdrachten
1. Maak Form: `FormLogin`
2. Controls:
    - txtUsername
    - txtPassword (PasswordChar)
    - btnLogin
    - label foutmelding (bijv. lblError)
3. Login logica:
    - zoek user in JSON op username
    - check password
    - bij fout: FailedAttempts++, opslaan JSON
    - bij 3 fouten: app sluiten
    - bij goed: FailedAttempts = 0, opslaan JSON, DialogResult.OK
4. Pas Program.cs aan:
    - Eerst login tonen (ShowDialog)
    - Alleen bij OK door naar Form1



🔝 [Terug naar navigatie](#-navigatie)

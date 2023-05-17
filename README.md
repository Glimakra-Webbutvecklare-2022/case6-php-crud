# Case 6 Bokrecensionsapp i PHP

I det här caset ska du skapa en variant av en så kallad bokrecension applikation: **en lista över lästa böcker**.

Applikationen ska hantera en lista av böcker med recensioner. Ni ska använda PHP, MySQL, CSS, HTML.

Vi vill att du strävar efter följande namngivningsprinciper:
- använd latinska tecken för variabelnamn och funktioner
- använd förklarande namn, namngivna efter php och mysql standard
- skriv kommentarer i din kod
- avsluta instruktioner med semikolon ;
- skriv kod med indrag (indentation)

### Starta ditt arbete
Skapa ett privat repo på GitHub och koppla det till din lokala utvecklingsmiljö (Visual Studio Code). 

---

**TIPS** 

Använd Anders docker projekt som en grund för caset (Ta bort learn mappen).

eller

Använd en mall som finns för caset - https://github.com/Glimakra-Webbutvecklare-2022/Template-Case-PHP

---

Under projektet - senast 17 Maj bjuder du in dina lärare. Se Settings -> Manage access -> Add people

Lägg till

- martin-glimakra (Martin)
- addkolon (Mattias)
- andsju (Anders)
- frozenbanana (Henry)

***

## Krav
När applikationen ska startar ska det finnas en setup SQL query som sätter upp nödvändiga tabeller. (Ni kan generera detta från PHPMyAdmin.

Något i stil med:

```sql
CREATE TABLE `user` IF NOT EXISTS ...
```

### Databas krav

Det ska finnas följande tabeller:

### Alt 1

`BookReview` tabell med minst föjande kolumner:
- id (INT, AUTO_INCREMENT)
- titel (text)
- författare (text)
- yearPublished (INT)
- review (text)
- created_at (date)
- posted_by (foreign-key with `User`.`id`)

`User` tabell med minst föjande kolumner:
- id (INT, unique)
- username (TEXT, unique)
- password (TEXT, **hashed**)

#### Alt 2

I stil med sista föreläsningen (Anders)

tabell `user`, med föjande kolumner:
- user_id (INT, AUTO_INCREMENT)
- username (VARCHAR 255 tecken)
- password (VARCHAR 255 tecken, **hashed**)


tabell `book`, med föjande kolumner:
- book_id (INT, AUTO_INCREMENT)
- title (VARCHAR 255 tecken)
- author (VARCHAR 255 tecken)
- year_published (YEAR)
- review (TEXT)
- created_at (DATETIME)
- user_id (foreign-key with `user`.`user_id`)

## Design minimum
- Low fidelity designskiss
- Mobile first

## Design Extra
- Logotyp
- Färgtema

## Code minimum
- En README.md i gitrepot med följande delar:
  - Introduction: Vad gör er app och vilket problem löser det?
  - Requirements & Installation: Vad behövs för att man själv ska kunna köra appen?
  - Screenshots: minst en screenshot (eller gif) som visar appen under använding
- En användare ska kunna logga in och ut
- Inloggad användare ska kunna se sin egna samling av bokrecensioner
- Bokrecensioner ska kunna läggas till, editeras och raderas av ägare.
- Alla bokrecensioner ska finnas listade för en inloggad användare
- Alla formulärsfält som registeras till databasen ska vara validerade (att rätt och rimlig typ att data lagras)

## Code Extra
- Publicerad via Linode eller motsvarade
- Det ska vara möligt att registera en användare med ett registreringsformulär
- Det ska vara möligt att registera en bildurl för böcker
- Det ska vara möligt att sätta betyg (1-5 stjärnor) på böcker
- Det ska vara möjligt att sätta en bokrecension som draft
   - ej inloggad användare ska inte kunna se draft av bokrecensioner
- Det ska vara möjligt att sätta likes på publika bokrecensioner
- Det ska vara möjligt att kommentera på publika bokrecensioner
***

### Inlämning och redovisning
Redovisning av caset är den 29 maj kl 10.30 

Vi önksar att alla får ta del av varandras redovisning. Det innebär att ni behöver förbereda er på att redovisningen är kort - ca 5 minuter per person. Då visar ni (demonstrerar) er applikation genom att dela skärm.

*Förbered 5 minuters redovisning enligt följande mall:*

#### I reovisningen ska du:
- demonstrera applikationen
- - visa hur man lägger till, markerar och tar bort ett listelement
- - visa exempel på annan funktionalitet (ex ngn av utmaningarna)
- berätta vad du är mest nöjd med (design, kod, struktur...)
- berätta vad du skulle vilja att applikationen kan göra, men inte hunnit att koda

Redovisningen sker i bokstavordning (efternamn a-ö)

### Handledning
Det kommer givetvis finnas möjlighet till handledning fram tills den 29 maj. I första hand är det under vanlig lektionstid.

Lycka till!

# Case 6 Bokrecensionsapp i PHP

I det här caset ska du skapa en variant av en så kallad bokrecension applikation: **en lista över lästa böcker**.

Applikationen ska hantera en lista av böcker med recensioner. Ni ska använda PHP, MySQL, CSS, JavaScript samt HTML.

Vi vill att du strävar efter följande namngivningsprinciper:
- använd latinska tecken för variabelnamn och funktioner
- använd förklarande namn, namngivna efter php och mysql standard
- skriv kommentarer i din kod
- avsluta instruktioner med semikolon ;
- skriv kod med indrag (indentation)

### Starta ditt arbete
Skapa ett privat repo på GitHub och koppla det till din lokala utvecklingsmiljö (Visual Studio Code). **TIPS** Använd Anders docker projekt som en grund för caset (Ta bort learn mappen).  
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
CREATE TABLE BookReview IF NOT EXISTS ...
```

### Databas krav
Det ska finnas följande tabeller:

`BookReview` tabell med minst föjande kolumner:
- id (INT, unique)
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
- inloggad användare ska kunna se sin egna samling av Bokrecension
- BookReview ska kunna läggas till, editeras och raderas av ägare.
- Alla **BookReview** ska finnas listade för en inloggad användare
- Alla formulärsfält som registeras till databasen ska vara validerade (att rätt och rimlig typ att data lagras)

## Code Extra
- Publicerad via Linode eller motsvarade
- Det ska vara möligt att registera en User med ett registreringsformulär
- Det ska vara möligt att registera en bildurl för BookReview
- Det ska vara möligt att sätta betyg (1-5 stjärnor) på en BookReview
- Det ska vara möjligt att sätta en BookReview som draft
   - ej inloggad användare ska inte kunna se draft BookReview
- Det ska vara möjligt att sätta Likes på publika BookReview
- Det ska vara möjligt att kommentera på publika BookReview
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

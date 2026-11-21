# La Cala 2027

Live scoretavle for golfturen til La Cala, 5.–7. februar 2027. Seks spillere, tre runder (Europa, America, Asia), gul tee.

Siden ligger på GitHub Pages, og scorene lagres i Firebase slik at alle telefoner oppdateres fortløpende. Score som føres uten dekning lagres på telefonen og sendes når nettet er tilbake.

## Oppsett (ca. 10 minutter)

### 1. Firebase (lagringen)
1. Gå til https://console.firebase.google.com og velg **Legg til prosjekt**. Analytics kan skrus av.
2. Velg **Build › Firestore Database › Create database**. Velg en europeisk lokasjon (f.eks. `europe-west1`) og **production mode**.
3. Åpne fanen **Rules**, erstatt innholdet med det som står i `firestore.rules` i dette repoet, og trykk **Publish**.
4. Gå til **Project settings** (tannhjulet) › **General** › **Your apps** og trykk web-ikonet `</>`. Gi appen et navn og registrer den (Hosting trengs ikke).
5. Kopier verdiene i `firebaseConfig` inn i `config.js` i stedet for `FYLL_INN`.

### 2. GitHub Pages (siden)
1. Last opp alle filene til repoet: **Add file › Upload files**, dra inn filene og trykk **Commit changes**.
2. Gå til **Settings › Pages**. Under **Build and deployment** velger du **Deploy from a branch**, branch `main` og mappe `/ (root)`, og trykker **Save**.
3. Etter et minutt eller to ligger appen på https://tobias265.github.io/gutta-golf-2026/

### 3. På telefonen
- **iPhone:** åpne lenken i Safari › Del › **Legg til på Hjem-skjerm**.
- **Android:** åpne lenken i Chrome › ⋮ › **Legg til på startsiden** (eller **Installer app**).

Appen åpnes da i fullskjerm uten nettleserlinje.

## Bruk
- **Tavle:** sammenlagt poeng, brutto og netto, og resultat per runde.
- **Score:** før slag hull for hull. Alle kan føre for alle.
- **Runder:** velg spillform (slagspill, scramble, shamble), trekk lag og flighter, sett longest drive og closest to pin, og avslutt runden for å dele ut poeng.
- **Oppsett:** handicap, poengsystem, innsats og CR/slope per bane.

## Sikkerhet
Alle som har lenken kan lese og føre score. Det finnes ingen innlogging. Del lenken bare med de som er med på turen.

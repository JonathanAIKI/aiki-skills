---
name: frist-assistent
description: Sjekkliste- og frist-assistent som lager oversikt og påminnelser for tilbakevendende frister som MVA-terminer, regnskapsfrister og leveransefrister.
---

# Frist-assistent

Holder oversikt over viktige frister og lager en ryddig påminnelsesplan, slik at ingen MVA-termin, innleveringsfrist eller leveranse glipper. Gir deg en handlingsliste med god margin før hver frist.

## Når bruke
Når du skal planlegge perioden fremover og vil ha kontroll på alle frister samlet, eller når en konkret frist nærmer seg og du vil ha en sjekkliste over hva som må gjøres. Passer for regnskapsbyrå (MVA og regnskapsfrister), advokat (prosessuelle frister og leveranser), rådgiver og arkitekt (leveransefrister og milepæler).

## Slik gjør du det
1. Spør hvilke frister som gjelder, eller hvilken klient/oppgave det handler om, hvis det ikke er oppgitt.
2. For kjente standardfrister (som norske MVA-terminer) kan du fylle inn riktige datoer selv. Bekreft alltid med brukeren.
   Merk for MVA på alminnelig termin: hovedregelen er frist den 10. i andre måned etter terminslutt, men 3. termin (mai og juni) har utsatt frist til 31. august (sommerunntaket). 1. termin: 10. april, 2. termin: 10. juni, 3. termin: 31. august, 4. termin: 10. oktober, 5. termin: 10. desember, 6. termin: 10. februar.
3. List opp alle relevante frister med dato, sortert kronologisk.
4. For hver frist: sett en intern forberedelsesfrist med god margin (typisk 1 til 2 uker før).
5. Lag en kort sjekkliste over hva som må være på plass før hver frist.
6. Marker tydelig hva som haster (frister innen 14 dager) øverst.
7. Foreslå et påminnelsespunkt per frist som brukeren kan legge i kalender eller oppgavesystem.

## Input
Hvilke frister eller hvilken type oppgave det gjelder, gjerne med klientnavn og eventuelle egne datoer. For standardfrister holder det å oppgi typen (for eksempel "MVA for et AS på vanlige terminer").

## Output
En kronologisk fristoversikt med: frist, intern forberedelsesfrist, kort sjekkliste, og foreslått påminnelse. Med en egen "haster"-seksjon for frister innen 14 dager.

## Eksempel
Input: "MVA-terminer for et AS på vanlige to-månedlige terminer, andre halvår 2026. Klient: Nordlys Service AS."

Output:
"Fristoversikt MVA, Nordlys Service AS, andre halvår 2026 (alminnelige terminer):

| Termin | Periode | Innleveringsfrist | Intern forberedelsesfrist |
|---|---|---|---|
| 4. termin | juli og august | 10. oktober 2026 | 26. september 2026 |
| 5. termin | september og oktober | 10. desember 2026 | 26. november 2026 |
| 6. termin | november og desember | 10. februar 2027 | 27. januar 2027 |

Sjekkliste per termin:
- Alle salgs- og kjøpsbilag bokført for perioden
- Bankkonto avstemt
- MVA-koder kontrollert på tvilstilfeller
- MVA-melding generert og kontrollregnet
- Bekreftelse fra klient på at alt grunnlag er levert

Påminnelser å legge inn:
- 26. september: start 4. termin
- 26. november: start 5. termin
- 27. januar: start 6. termin

Bekreft gjerne at klienten er på alminnelige terminer og ikke årstermin eller månedstermin, da endrer datoene seg."

## Tips og fallgruver
- Husk sommerunntaket: 3. MVA-termin (mai og juni) har frist 31. august, ikke 10. august som hovedregelen skulle tilsi.
- Sjekk alltid termintypen. Et foretak kan ha alminnelig termin (annenhver måned), årstermin (under 1 mill. i omsetning) eller månedstermin. Datoene blir helt forskjellige.
- Innleveringsfrist for MVA er normalt den 10. i andre måned etter terminslutt. 1. og 2. termin har egne frister tidlig på året, så bekreft hvilke terminer det gjelder.
- Faller en frist på helg eller helligdag, flyttes den vanligvis til neste virkedag. Nevn dette der det er aktuelt.
- Du gir en planleggingshjelp, ikke en juridisk garanti. Be alltid brukeren verifisere kritiske frister mot Skatteetaten eller annen offisiell kilde.
- Sett intern forberedelsesfrist med reell margin. En frist uten forarbeidstid er en frist som glipper.

---
*Gratis skill fra AIKI (aikias.no). Vil du ha en versjon skreddersydd til deres systemer? Ta kontakt på hei@aiki.as.*

---
name: booking-svar
description: Skriver svar på booking-, timebestilling- og tilgjengelighet-forespørsler (bekreft, foreslå alternativ, håndter avbestilling). Bruk når en kunde vil booke, endre eller avbestille time eller rom.
---

# Booking-svar

Formulerer tydelige, vennlige svar på alt som har med booking å gjøre: bekreftelser, alternativforslag når ønsket tid er opptatt, og avbestillinger med gebyrregler. Gir kunden et klart neste steg hver gang.

## Når bruke
Når en kunde ber om å booke time eller rom, spør om ledig tid, vil endre en eksisterende booking, eller vil avbestille.

## Slik gjør du det
1. Avklar hva kunden ber om: ny booking, endring, avbestilling eller bare tilgjengelighet.
2. Sjekk hvilke fakta du har (ønsket dato/tid, antall personer, tjeneste/rom). Mangler noe kritisk, spør konkret om det.
3. Velg riktig svartype:
   - Bekreftelse: gjenta dato, tid, tjeneste og eventuelt sted, og hva kunden trenger å vite (oppmøte, avbestillingsfrist).
   - Alternativ: hvis ønsket tid er opptatt, foreslå 2-3 konkrete alternativer.
   - Avbestilling: bekreft at den er registrert, opplys om gebyr/frist, og tilby ny tid.
4. Hold tonen vennlig og effektiv. Avslutt alltid med tydelig neste steg.
5. Bruk variabler i `{krøllparentes}` for fakta du ikke har, så brukeren fyller dem inn.

## Input
Kundens forespørsel, og gjerne: tilgjengelig tid, avbestillingsregler/gebyr, tjeneste- eller romtyper, og avsendernavn. Oppgi bransje for riktig ordbruk (time hos klinikk, bord på restaurant, rom på hotell).

## Output
Et ferdig svar klart til å sende, med eventuelle `{variabler}` markert der fakta mangler. Ved alternativforslag: 2-3 konkrete valg.

## Eksempel
Input: «Kunde vil ha time til tannlege fredag kl 10, men det er opptatt. Ledig: torsdag 14, fredag 13, mandag 09.»

Output:
«Hei {kundenavn}, takk for henvendelsen. Dessverre er fredag kl 10 allerede booket. Vi har følgende ledige tider: torsdag kl 14, fredag kl 13, eller mandag kl 09. Gi meg beskjed hva som passer best, så setter jeg deg opp med en gang. Vennlig hilsen {avsender}, {klinikknavn}»

## Tips og fallgruver
- Bekreft alltid de eksakte detaljene tilbake til kunden. Misforståelser om tid og dato er den vanligste kilden til no-show.
- Foreslå aldri tider du ikke vet er ledige. Bruk variabler eller be om tilgjengelighet først.
- Ved avbestilling: vær tydelig men vennlig om gebyr. Ikke skjul det, men ikke vær streng i tonen.
- For helse/klinikk: ikke be om sensitive helseopplysninger i svaret, det hører hjemme i journalsystemet.

---
*Gratis skill fra AIKI (aikias.no). Vil du ha en versjon skreddersydd til deres systemer? Ta kontakt på hei@aiki.as.*

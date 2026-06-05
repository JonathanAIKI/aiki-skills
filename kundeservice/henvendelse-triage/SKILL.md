---
name: henvendelse-triage
description: Klassifiserer, prioriterer og ruter innkommende kundehenvendelser (haster/normal, tema, eier, foreslått svar). Bruk når du har en innboks eller liste med henvendelser som skal sorteres raskt.
---

# Henvendelse-triage

Sorterer rå kundehenvendelser slik at riktig sak havner hos riktig person med riktig hastegrad. Sparer teamet for manuell triage og sikrer at det som haster ikke drukner.

## Når bruke
Når du sitter med en eller flere innkommende meldinger (e-post, skjema, chat, DM) og må avgjøre hva som haster, hva saken handler om, hvem som skal eie den, og hvordan den bør besvares.

## Slik gjør du det
1. Les hver henvendelse og trekk ut kjernen: hva ønsker kunden faktisk?
2. Sett hastegrad: HASTER (driftsstans, helse/sikkerhet, frist i dag, sint kunde som vil forlate), NORMAL (vanlig spørsmål), LAV (info, ros, ikke tidskritisk).
3. Velg tema/kategori (f.eks. booking, faktura, klage, teknisk, produkt, retur, generelt).
4. Foreslå eier: hvilken rolle eller avdeling bør håndtere det (resepsjon, support, regnskap, leder).
5. Vurder stemning: positiv, nøytral, negativ/frustrert.
6. Skriv et kort forslag til neste steg eller svar (1-2 setninger), eller marker «trenger mer info».
7. Sorter listen med HASTER øverst.

## Input
En eller flere henvendelser som ren tekst. Gjerne med avsender og kanal. Oppgi bransje (helse/klinikk, reiseliv/hotell, handel/retail) hvis det finnes for å treffe kategoriene bedre.

## Output
Tabell med kolonnene: Hastegrad | Tema | Stemning | Foreslått eier | Sammendrag | Foreslått neste steg. Sortert med HASTER først.

## Eksempel
Input: «Hei, jeg booket time hos dere i morgen kl 09, men har akkurat blitt syk og må avbestille. Slipper jeg gebyr?»

Output:
| Hastegrad | Tema | Stemning | Eier | Sammendrag | Neste steg |
|---|---|---|---|---|---|
| HASTER | Booking/avbestilling | Nøytral | Resepsjon | Kunde må avbestille time i morgen pga sykdom, spør om gebyr | Bekreft avbestilling, opplys om gebyrregler, tilby ny time |

## Tips og fallgruver
- Sint kunde som truer med å gå er alltid minst HASTER, uavhengig av tema.
- Helse/sikkerhet trumfer alt: symptomspørsmål, allergi, akutt skade rutes umiddelbart til fagperson, aldri besvart med standardsvar.
- Ikke gjett på fakta du ikke har (priser, ledig tid). Marker «trenger mer info» heller enn å finne på.
- Hold sammendraget kort nok til at en travel ansatt forstår saken på to sekunder.

---
*Gratis skill fra AIKI (aikias.no). Vil du ha en versjon skreddersydd til deres systemer? Ta kontakt på hei@aiki.as.*

---
name: tilbud-generator
description: Lager strukturerte tilbud fra en jobb- eller produktspesifikasjon med poster, mengder, enhetspris, sum, forbehold og gyldighet.
---

# Tilbud-generator

Gjør en løs jobbeskrivelse om til et ryddig, prissatt tilbud med poster, summer, forbehold og gyldighetsdato. Gir et profesjonelt inntrykk og reduserer risiko for misforståelser om hva som er inkludert.

## Når bruke
Når en kunde har bedt om pris på en jobb eller leveranse, og du skal sende et skriftlig tilbud med spesifiserte poster, totalpris og betingelser.

## Slik gjør du det
1. Les jobb- eller produktspesifikasjonen og del den opp i konkrete poster (arbeid, materiell, utstyr, rigg, frakt).
2. Be om det som mangler: enhetspris eller estimat per post, og om prisen er fast eller etter medgått tid.
3. Regn ut sum per post (mengde x enhetspris) og delsummer der det gir mening (f.eks. arbeid vs. materiell).
4. Summer til total eks. mva, legg på mva (standard 25 %) og vis total inkl. mva.
5. Skriv tydelig hva som er inkludert og hva som IKKE er med (forbehold).
6. Sett gyldighet (standard 30 dager) og betalingsbetingelser.
7. Sett opp tilbudet i fast format med tilbudsnr. og dato.

## Input
- Kunde: navn og evt. kontaktperson.
- Jobbeskrivelse eller produktliste.
- Poster med mengde, enhet og enhetspris (eller grunnlag for estimat).
- Valgfritt: tilbudsnr., fast pris vs. timepris, forbehold, gyldighet, betalingsbetingelser, leveringstid.

## Output
Ferdig tilbud i ren tekst, klar til e-post eller PDF:
- Topptekst med tilbudsnr. og dato
- Kort beskrivelse av leveransen
- Posttabell: post, mengde, enhetspris, sum
- Sum eks. mva, mva, total inkl. mva
- Inkludert / ikke inkludert (forbehold)
- Gyldighet og betalingsbetingelser

## Eksempel
Input:
"Tilbud til Solberg Eiendom AS på bytte av 6 utelys på fasade. 6 LED-armaturer a 1 290 kr, montasje 8 timer a 850 kr, bilkjøring 1 a 600 kr. Fast pris. Stillas ikke inkludert."

Output:
```
TILBUD

Tilbudsnr.: T-1182
Dato: 05.06.2026
Til: Solberg Eiendom AS

Leveranse: Bytte av 6 utelys på fasade, inkl. montasje.

Post                          Mengde   Enhetspris        Sum
LED-armatur                        6   1 290,00 kr   7 740,00 kr
Montasje                       8 timer    850,00 kr   6 800,00 kr
Bilkjøring                         1     600,00 kr     600,00 kr

Sum eks. mva:                                       15 140,00 kr
Mva (25 %):                                          3 785,00 kr
Total inkl. mva:                                    18 925,00 kr

Pris: Fast pris.

Inkludert: Levering og montasje av 6 armaturer, bortkjøring av gamle.
Ikke inkludert: Stillas eller lift. Eventuelle skjulte feil i eksisterende anlegg.

Gyldighet: 30 dager fra tilbudsdato.
Betalingsbetingelser: 14 dager netto etter utført arbeid.
```

## Tips og fallgruver
- Vær eksplisitt på hva som IKKE er inkludert. De fleste tvister oppstår i gråsonen, ikke i selve prisen.
- Skill mellom fast pris og estimat etter medgått tid. Skriv "estimat" tydelig hvis prisen kan endre seg.
- Ved timepris: oppgi timesats og anslått timeantall, men gjør klart at faktisk sum avhenger av medgått tid.
- Sett alltid en gyldighetsdato. Materialpriser og kapasitet endrer seg.
- Ikke bland mva inn i postprisene. Vis netto, mva og brutto hver for seg.

---
*Gratis skill fra AIKI (aikias.no). Vil du ha en versjon skreddersydd til deres systemer? Ta kontakt på hei@aiki.as.*

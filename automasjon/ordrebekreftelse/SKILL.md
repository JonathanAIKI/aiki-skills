---
name: ordrebekreftelse
description: Genererer profesjonelle ordrebekreftelser fra ordre-detaljer (kunde, varer, antall, pris, leveringsdato), klar til å sendes på e-post.
---

# Ordrebekreftelse

Lager en ryddig, korrekt ordrebekreftelse på sekunder ut fra rådata om en ordre. Sparer tid, reduserer feil og gir kunden en proff bekreftelse med en gang.

## Når bruke
Når en ordre er mottatt (telefon, e-post, skjema) og kunden skal ha en skriftlig bekreftelse med varelinjer, summer og leveringsinfo før levering starter.

## Slik gjør du det
1. Les inn ordre-detaljene brukeren oppgir (kunde, varelinjer, leveringsdato, referanse).
2. Be om det som mangler av kritiske felt: kundenavn, minst én varelinje, og enten leveringsdato eller "avtales".
3. Regn ut linjesum (antall x enhetspris) per vare og total eks. mva.
4. Legg på mva (standard 25 % hvis ikke annet er oppgitt) og regn ut totalsum inkl. mva.
5. Tildel ordrenummer hvis oppgitt, ellers skriv "[ordrenr.]" som plassholder.
6. Sett opp bekreftelsen i fast format med varetabell og summer.
7. Avslutt med leveringsinfo, betalingsbetingelser og en kort hilsen.

## Input
- Kunde: navn, evt. kontaktperson og kundenr.
- Varelinjer: beskrivelse, antall, enhet (stk, time, m, kg), enhetspris eks. mva.
- Leveringsdato eller leveringsuke (eller "avtales").
- Valgfritt: ordrenr., kundens bestillingsreferanse, mva-sats, betalingsbetingelser, leveringsadresse.

## Output
Ferdig ordrebekreftelse i ren tekst, klar til å lime inn i e-post:
- Topptekst med ordrenr. og dato
- Kunde- og leveringsinfo
- Varetabell: beskrivelse, antall, enhetspris, linjesum
- Sum eks. mva, mva, totalsum inkl. mva
- Leverings- og betalingsbetingelser
- Avsluttende hilsen

## Eksempel
Input:
"Kunde: Hammer Bygg AS, kontakt Lars Vik. Bestilte 40 sekk betong B30 a 89 kr, 12 stk armeringsnett a 245 kr, 1 frakt a 650 kr. Leveres 12. juni. Vår ref O-2041."

Output:
```
ORDREBEKREFTELSE

Ordrenr.: O-2041
Dato: 05.06.2026

Kunde: Hammer Bygg AS
Kontakt: Lars Vik
Leveringsdato: 12.06.2026

Vare                          Antall   Enhetspris      Sum
Betong B30, sekk                  40      89,00 kr   3 560,00 kr
Armeringsnett                     12     245,00 kr   2 940,00 kr
Frakt                              1     650,00 kr     650,00 kr

Sum eks. mva:                                        7 150,00 kr
Mva (25 %):                                          1 787,50 kr
Totalt inkl. mva:                                    8 937,50 kr

Levering: 12.06.2026 til avtalt adresse.
Betalingsbetingelser: 14 dager netto.

Takk for bestillingen. Ta kontakt ved spørsmål.
Hammer Bygg AS
```

## Tips og fallgruver
- Kontroller at antall x enhetspris faktisk stemmer med oppgitt linjesum hvis kunden har regnet selv. Flagg avvik i stedet for å overskrive.
- Frakt og gebyrer er egne linjer, ikke skjult i varepris.
- Skill mellom mva-pliktige og mva-frie varer hvis ordren har begge deler.
- Bruk "avtales" framfor å gjette leveringsdato. En feil dato i en bekreftelse skaper mer trøbbel enn et åpent felt.
- Beløp med tusenskille og to desimaler, komma som desimaltegn (norsk standard).

---
*Gratis skill fra AIKI (aikias.no). Vil du ha en versjon skreddersydd til deres systemer? Ta kontakt på hei@aiki.as.*

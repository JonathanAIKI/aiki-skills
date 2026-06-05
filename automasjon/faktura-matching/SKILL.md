---
name: faktura-matching
description: Matcher innkommende fakturaer mot ordre eller bestilling og flagger avvik på pris, antall og dobbeltfakturering før betaling.
---

# Faktura-matching

Sammenligner en mottatt faktura mot den opprinnelige ordren eller bestillingen, linje for linje, og flagger avvik i pris, antall og summer. Fanger opp feilfakturering og dobbeltfakturering før pengene går ut.

## Når bruke
Når en leverandørfaktura kommer inn og skal kontrolleres mot bestilling eller ordre før attestering og betaling. Spesielt nyttig ved mange fakturaer eller når priser er framforhandlet på forhånd.

## Slik gjør du det
1. Les inn ordre/bestilling (forventet) og faktura (mottatt).
2. Match varelinjer på varenavn, varenr. eller beskrivelse. Par opp linjer som hører sammen.
3. Per linje, sammenlign antall og enhetspris. Beregn avvik i kroner og prosent.
4. Kontroller at fakturaens totalsum stemmer med summen av linjene og med oppgitt mva.
5. Sjekk for ekstra linjer på fakturaen som ikke finnes i ordren (uventede gebyrer, frakt, varer).
6. Sjekk for tegn på dobbeltfakturering: samme fakturanr., samme ordrenr. og beløp, eller identisk linjeinnhold som tidligere.
7. Oppsummer med en tydelig konklusjon: OK til betaling, eller HOLD med liste over avvik.

## Input
- Ordre/bestilling: varelinjer med antall og avtalt enhetspris.
- Faktura: fakturanr., leverandør, varelinjer med antall og pris, totalsum, mva.
- Valgfritt: liste over tidligere betalte fakturaer (for dobbeltfaktura-sjekk), toleransegrense for avvik (f.eks. +/- 2 %).

## Output
Avviksrapport i ren tekst:
- Match-tabell: vare, forventet vs. fakturert antall og pris, avvik
- Flagg per linje: OK, AVVIK PRIS, AVVIK ANTALL, EKSTRA LINJE
- Sumkontroll: forventet total vs. fakturert total
- Dobbeltfaktura-sjekk: status
- Konklusjon: OK / HOLD med kort begrunnelse

## Eksempel
Input:
"Ordre O-330 til Nordvik Verktøy: 10 borr a 120 kr, 5 vinkelslipere a 890 kr. Faktura F-5521 fra Nordvik Verktøy: 10 borr a 120 kr, 5 vinkelslipere a 950 kr, frakt 350 kr. Totalt fakturert 5 850 kr eks mva."

Output:
```
FAKTURA-MATCHING

Faktura: F-5521 (Nordvik Verktøy)
Mot ordre: O-330

Vare              Forventet        Fakturert         Avvik       Status
Borr           10 x 120,00 kr   10 x 120,00 kr      0,00 kr      OK
Vinkelsliper    5 x 890,00 kr    5 x 950,00 kr    +300,00 kr   AVVIK PRIS (+6,7%)
Frakt          ikke i ordre        350,00 kr      +350,00 kr   EKSTRA LINJE

Forventet sum eks. mva:   5 650,00 kr
Fakturert sum eks. mva:   5 850,00 kr  (avvik +650,00 kr)
Sumkontroll: linjesum stemmer med oppgitt total. OK.

Dobbeltfaktura-sjekk: Ingen tidligere faktura med samme nr. eller beløp funnet.

KONKLUSJON: HOLD.
- Vinkelsliper fakturert 60 kr over avtalt pris per stk (300 kr totalt).
- Frakt 350 kr er ikke avtalt i ordren.
Kontakt leverandør før betaling.
```

## Tips og fallgruver
- Sett en toleransegrense for småavvik (f.eks. øreavrunding) slik at rapporten ikke flagger bagateller, men alltid vis tallene.
- Frakt og gebyrer er vanlige "ekstra linjer". Avgjør om de er avtalt, ikke bare om de finnes.
- Dobbeltfakturering kommer ofte som purring eller kreditnota feilført som ny faktura. Sjekk fakturanr. OG beløp OG dato.
- Hvis varelinjene ikke kan matches sikkert (ulik tekst, mangler varenr.), si det eksplisitt framfor å gjette match.
- Konkluder aldri "OK til betaling" hvis sumkontrollen ikke går opp, selv om linjene ser riktige ut.

---
*Gratis skill fra AIKI (aikias.no). Vil du ha en versjon skreddersydd til deres systemer? Ta kontakt på hei@aiki.as.*

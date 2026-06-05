---
name: svar-mal-bygger
description: Bygger konsistente, merkevare-tilpassede svar-maler for gjenganger-spørsmål i kundeservice. Bruk når samme type spørsmål kommer ofte og bør besvares likt og raskt.
---

# Svar-mal-bygger

Lager gjenbrukbare svar-maler med fletteflesk (variabler) for spørsmålene som går igjen, slik at hele teamet svarer konsistent og på riktig tone. Reduserer svartid og kvalitetsforskjeller mellom ansatte.

## Når bruke
Når dere får samme spørsmål om og om igjen (åpningstider, priser, avbestilling, retur, fraktstatus, parkering) og vil ha ferdige maler i stedet for at hver ansatt skriver fritt hver gang.

## Slik gjør du det
1. Be om temaet malen skal dekke, og bransje/tone hvis det finnes.
2. Avklar fakta som varierer per sak og gjør dem til variabler i `{krøllparentes}` (f.eks. `{kundenavn}`, `{tidspunkt}`, `{beløp}`).
3. Skriv malen kort, vennlig og handlingsrettet: hils, svar på spørsmålet, oppgi neste steg, avslutt.
4. Hold tonen konsistent med merkevaren (varm og profesjonell som standard, juster på forespørsel).
5. Legg ved en utfylt eksempelversjon så brukeren ser hvordan den ser ut i praksis.
6. Foreslå 1-2 varianter hvis tonen kan gå flere veier (formell vs. uformell).

## Input
Tema for malen, og gjerne: bransje, ønsket tone, faste fakta (åpningstider, gebyrer, frister) og signatur/avsendernavn.

## Output
1. Selve malen med variabler i `{krøllparentes}`.
2. En liste over variablene som må fylles ut.
3. Ett utfylt eksempel.

## Eksempel
Input: «Lag svar-mal for kunder som spør om åpningstider, hotell, vennlig tone.»

Output:

Mal:
«Hei {kundenavn}, takk for at du tar kontakt. Vi har åpent i resepsjonen {åpningstider}. Innsjekk er fra {innsjekk} og utsjekk innen {utsjekk}. Trenger du noe utenom dette, hjelper nattevakten deg gjerne. Ha en fin dag. Vennlig hilsen {avsender}, {hotellnavn}»

Variabler: kundenavn, åpningstider, innsjekk, utsjekk, avsender, hotellnavn

Utfylt: «Hei Anne, takk for at du tar kontakt. Vi har åpent i resepsjonen hele døgnet. Innsjekk er fra kl 15, og utsjekk innen kl 11. Trenger du noe utenom dette, hjelper nattevakten deg gjerne. Ha en fin dag. Vennlig hilsen Markus, Fjordvik Hotell»

## Tips og fallgruver
- Aldri fest faste priser eller frister inn i selve teksten hvis de endres ofte. Gjør dem til variabler.
- Maler skal kunne sendes nesten uendret. Hvis en sak krever skjønn, marker hvor den ansatte må tilpasse.
- Unngå robotaktig språk. Én personlig setning gjør stor forskjell.
- For helse/klinikk: aldri legg medisinske råd inn i en generell mal, henvis til fagperson.

---
*Gratis skill fra AIKI (aikias.no). Vil du ha en versjon skreddersydd til deres systemer? Ta kontakt på hei@aiki.as.*

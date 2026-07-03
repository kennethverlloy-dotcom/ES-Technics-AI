# Skill: HVAC Diagnose

Deze skill beschrijft hoe de AI-medewerker een HVAC- of koeltechnische storing systematisch analyseert.

## Doel

Een gestructureerde diagnose opstellen op basis van symptomen, historiek, metingen en technische kennis, zodat ES-Technics snel en onderbouwd kan beslissen welke actie nodig is.

## Benodigde input

De AI heeft minimaal nodig: klantnaam of projectnaam, locatie, omschrijving van het symptoom, beschikbare foto's of meetwaarden, en indien mogelijk het type installatie en merk van de regelaar of machine.

## Werkwijze

1. Raadpleeg altijd eerst de klantmap, in het bijzonder `technische_historiek/`, `installaties/` en eerdere werkbonnen. Controleer of het om een terugkerende storing gaat.
2. Bepaal om welk deelsysteem het gaat: luchtzijdig, hydraulisch, koudemiddelcircuit, regeling/GBS of elektrisch.
3. Vergelijk het symptoom met de kennisbank en relevante fabrikantinformatie.
4. Stel gerichte metingen of observaties voor. Voorbeelden zijn aanvoer- en retourtemperaturen, drukken, stroomopname, klepstand, alarmstatus of trendgrafieken.
5. Werk van waarschijnlijk naar minder waarschijnlijk. Sluit oorzaken systematisch uit in plaats van onderdelen te vervangen op vermoeden.
6. Benoem expliciet veiligheidsmaatregelen zoals LOTO, spanningsloos werken, of F-gassenmaatregelen.
7. Formuleer een conclusie met waarschijnlijke oorzaak, impact en aanbevolen vervolgstap.

## Output

Sla het diagnoseresultaat op als `JJJJ-MM-DD_diagnose_omschrijving.md` in de relevante klant- of projectmap. De output bevat probleemstelling, historiek, metingen, analyse, conclusie en aanbevolen actie.

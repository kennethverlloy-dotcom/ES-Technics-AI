# Skill: Parameterwijziging Loggen

Deze skill beschrijft hoe de AI een wijziging in een regelaar of GBS documenteert.

## 1. Doel
Zorgen voor volledige traceerbaarheid van wijzigingen aan setpoints, PID-parameters of regelstrategieën, zodat bij ongewenste effecten de originele staat hersteld kan worden.

## 2. Benodigde Input
- Klant en installatie.
- Oude waarde en nieuwe waarde van de parameter(s).
- Reden van de wijziging.

## 3. Stappenplan

1. **Context Controleren:**
   - Controleer in de klantmap (`technische_historiek/` of eerdere parameterlogs) of deze parameter al vaker is gewijzigd.

2. **Template Invullen:**
   - Gebruik het template `es-technics/templates/parameterlog.md`.
   - Vul de tabel zorgvuldig in. Vermeld altijd de eenheid.

3. **Opslaan:**
   - Sla het bestand op in `klanten/<Klantnaam>/technische_historiek/` met de naam `JJJJ-MM-DD_parameterlog_<installatie>.md`.
   - Indien de wijziging deel uitmaakt van een grotere interventie, verwijs dan naar dit logbestand in de werkbon.

4. **Output:**
   - Toon het ingevulde logbestand aan de gebruiker ter bevestiging.

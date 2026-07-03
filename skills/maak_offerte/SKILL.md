# Skill: Maak Offerte

Deze skill beschrijft de workflow voor het opstellen van een professionele offerte namens ES-Technics BV.

## 1. Doel
Een nauwkeurige, commercieel correcte en technisch onderbouwde offerte genereren op basis van klantvragen, opnames of bestekken.

## 2. Benodigde Input
- Klantnaam en locatie.
- Scope van de werken (wat moet er vervangen, hersteld of geïnstalleerd worden).
- Lijst van benodigde materialen (indien bekend) of technische vereisten.
- Inschatting van de werkuren (indien aangeleverd).

## 3. Stappenplan

1.  **Context Verzamelen:**
    - Zoek in de map `klanten/<klantnaam>/` naar eerdere offertes of de technische historiek om de context te begrijpen.
    - Raadpleeg `persoonlijk/leveranciers/` of `kennis/` voor voorkeursmerken (bijv. Systemair voor luchtgroepen, WAGO voor PLC's). Let op de richtlijn uit de kennisbank: *Prioritize reusing existing channels but ensure they are isolated. When considering brands, explore alternatives beyond the usual, such as Systemair.*

2.  **Materialen en Uren Bepalen:**
    - Als de materialen niet expliciet zijn opgegeven, maak dan een logische technische inschatting op basis van de scope.
    - Bepaal de benodigde uren voor engineering, installatie en inbedrijfstelling.

3.  **Template Invullen:**
    - Gebruik het template `es-technics/templates/offerte.md`.
    - Vul alle velden in. Gebruik geen placeholders (zoals `[Prijs]`). Als je geen exacte prijzen kent, gebruik dan realistische marktconforme schattingen, maar vermeld duidelijk aan de gebruiker dat deze prijzen gecontroleerd moeten worden.

4.  **Uitsluitingen Controleren:**
    - Zorg ervoor dat standaard uitsluitingen (zoals hak- en breekwerk, of hoogwerkers) correct vermeld staan in sectie 3 van de offerte.

5.  **Bestand Opslaan:**
    - Sla de gegenereerde offerte op in `klanten/<klantnaam>/offertes/` met de naamgevingsconventie `JJJJ-MM-DD_offerte_<korte-omschrijving>.md`.

## 4. Output
De AI presenteert de opgeslagen offerte aan de gebruiker en vraagt of er aanpassingen nodig zijn aan de scope of de geschatte prijzen.

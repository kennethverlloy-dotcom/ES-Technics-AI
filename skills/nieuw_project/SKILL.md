# Skill: Nieuw Project

Deze skill beschrijft hoe de AI een nieuw projectdossier opstart.

## 1. Doel
Een gestructureerde projectmap aanmaken en de initiële projectfiche invullen, zodat het project traceerbaar is doorheen alle fases.

## 2. Benodigde Input
- Projectnaam.
- Korte omschrijving van de scope.
- Klant of locatie (indien gekend).

## 3. Stappenplan

1. **Projectcode Bepalen:**
   - Zoek de laatst gebruikte projectcode in `projecten/` (formaat `PRJ-JJJJ-XXX`).
   - Genereer de volgende opeenvolgende code voor het huidige jaar.

2. **Map Aanmaken:**
   - Maak een nieuwe map aan onder `projecten/actief/` met de naam `[Projectcode]_[Korte_Naam]`.

3. **Projectfiche Invullen:**
   - Kopieer het template `es-technics/templates/projectfiche.md` naar de nieuwe map.
   - Vul de velden in op basis van de input van de gebruiker. Gebruik geen placeholders; laat velden leeg of vul "Nog te bepalen" in als informatie ontbreekt.

4. **Output:**
   - Bevestig aan de gebruiker dat het project is aangemaakt.
   - Toon de projectcode en de link naar de projectfiche.
   - Vraag of er al documenten (zoals een bestek of eerste berekening) toegevoegd moeten worden.

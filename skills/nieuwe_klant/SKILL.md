# Skill: Nieuwe Klant Aanmaken

Deze skill beschrijft de workflow voor het toevoegen van een nieuwe klant aan de repository.

## 1. Doel
Een gestandaardiseerde mappenstructuur en een initieel klantprofiel aanmaken, zodat de klant direct kan worden geïntegreerd in de AI-workflows.

## 2. Benodigde Input
- Bedrijfsnaam van de nieuwe klant.
- Optioneel: adresgegevens, contactpersonen, en een beschrijving van de aanwezige installaties.

## 3. Stappenplan

1.  **Mappenstructuur Genereren:**
    - Maak de hoofdmap aan: `klanten/<Klantnaam>/` (gebruik underscores in plaats van spaties in de mapnaam indien gewenst, of behoud de exacte spelling mits correct geëscaped).
    - Maak de volgende submappen aan:
        - `werkbonnen/`
        - `offertes/`
        - `projecten/`
        - `emails/`
        - `technische_historiek/`
        - `installaties/`
        - `fotos/`
        - `handleidingen/`
        - `berekeningen/`
        - `as_built_dossiers/`
        - `opleverdossiers/`

2.  **Klantprofiel Aanmaken:**
    - Maak het bestand `klanten/<Klantnaam>/technische_historiek/00_klantprofiel.md` aan.
    - Vul dit bestand met de beschikbare basisgegevens (Naam, Adres, Contactpersonen, Algemene omschrijving van de site).

3.  **Installatielijst Initialiseren:**
    - Maak het bestand `klanten/<Klantnaam>/installaties/00_installatie_overzicht.md` aan met een lege tabel voor toekomstige assets (ID, Type, Merk, Locatie, Status).

## 4. Output
De AI bevestigt dat de structuur is aangemaakt en vraagt of er direct een eerste werkbon of offerte voor deze klant moet worden opgesteld.

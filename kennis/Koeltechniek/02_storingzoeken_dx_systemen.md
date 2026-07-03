# Storingzoeken in DX-Systemen (Directe Expansie)

Dit document biedt een stapsgewijze aanpak voor het diagnosticeren van problemen in DX-koelinstallaties, zoals split-units, VRF-systemen en kleine chillers.

## 1. Visuele en Auditieve Inspectie
Voordat de manometers worden aangesloten, controleer het volgende:
- **Verdamper:** Is er ijsvorming zichtbaar? Zijn de filters en lamellen schoon?
- **Condensor:** Is de batterij vrij van stof, bladeren en pollen? Draait de ventilator in de juiste richting?
- **Leidingwerk:** Zijn er oliesporen zichtbaar (indicatie van lekkage)? Is de isolatie intact?
- **Compressor:** Maakt deze een ratelend geluid (vloeistofslag) of een hoog gierend geluid (gebrek aan smering)?

## 2. Meten van Oververhitting (Superheat)
De oververhitting controleert of het expansieventiel correct werkt en of de verdamper goed gevuld is.
- **Formule:** `T_zuigleiding - T_verdamping (gemeten via lagedruk manometer)`
- **Richtwaarde:** 5 K tot 8 K.
- **Te hoog (> 10 K):** Het ventiel staat te ver dicht, of er is een koudemiddeltekort. De verdamper wordt niet optimaal benut.
- **Te laag (< 3 K):** Het ventiel staat te ver open. Gevaar voor vloeistofslag in de compressor.

## 3. Meten van Onderkoeling (Subcooling)
De onderkoeling controleert of de condensor zijn warmte kwijt kan en of de installatie voldoende gevuld is.
- **Formule:** `T_condensatie (gemeten via hogedruk manometer) - T_vloeistofleiding`
- **Richtwaarde:** 3 K tot 8 K.
- **Te hoog (> 10 K):** Systeem is overvuld met koudemiddel, of er is een restrictie in de vloeistofleiding (bijv. deels verstopt filterdroger).
- **Te laag (< 2 K):** Koudemiddeltekort (lekkage).

## 4. Diagnosematrix

| Symptoom | Lagedruk | Hogedruk | Oververhitting | Onderkoeling | Waarschijnlijke Oorzaak |
| --- | --- | --- | --- | --- | --- |
| Systeem koelt slecht | Laag | Laag | Hoog | Laag | **Koudemiddeltekort** (Lekkage) |
| Systeem koelt slecht | Laag | Normaal/Laag | Hoog | Hoog | **Restrictie in vloeistoflijn** (Expansieventiel defect of filter verstopt) |
| Compressor valt uit (HP) | Hoog | Hoog | Laag | Laag | **Condensor probleem** (Vervuild of ventilator defect) |
| Compressor valt uit (LP) | Laag | Normaal/Laag | Laag | Normaal | **Verdamper probleem** (Filters vuil, ventilator defect, ijsvorming) |
| Systeem pendelt | Hoog | Hoog | Laag | Hoog | **Systeem overvuld** |

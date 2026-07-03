# Fabrikant Documentatie

De map `fabrikant_docs/` bevat **merkspecifieke** technische informatie, handleidingen, alarmcodes en service-instructies.

> **Belangrijke Regel (Strikte Scheiding):** 
> Deze map bevat **uitsluitend specifieke informatie per merk**. Algemene theorie over koeltechniek, HVAC of netwerkprotocollen hoort thuis in de map `kennis/`. De AI mag nooit informatie uit de map van het ene merk toepassen op een installatie van een ander merk.

## Beschikbare Merken

- **Johnson_Controls**: Metasys, CCT, NAE/SNE, York.
- **Priva**: Blue ID, Top Control, TC Engineer, Building Operator.
- **Siemens**: Desigo CC, PXC, S7-1200/1500, TIA Portal.
- **WAGO**: PFC100/200, 750/753 I/O, e!COCKPIT, CODESYS.

## Structuur per Merk

Elke merkmap start met `01_overzicht.md`, dat de belangrijkste platformen, tools en service-aandachtspunten beschrijft. Verdere documenten (bijv. specifieke alarmcodes of inbedrijfstellingschecklists) kunnen vrij worden toegevoegd.

# Skills (Workflows)

De map `skills/` bevat de operationele workflows voor de AI-medewerker. Elke skill is een stapsgewijze instructie (`SKILL.md`) die de AI vertelt hoe een specifieke taak moet worden uitgevoerd, van input tot output.

## Beschikbare Skills

| Skill | Doel |
| --- | --- |
| `analyseer_foto` | Foto van installatie, bord of schema analyseren via Vision. |
| `as_built_dossier` | As-built- of opleverdossier samenstellen. |
| `hvac_diagnose` | Stapsgewijze HVAC/koeltechnische storingsdiagnose uitvoeren. |
| `maak_offerte` | Offerte opstellen volgens bedrijfsstandaard. |
| `nieuw_project` | Nieuw project initialiseren en projectfiche opstellen. |
| `nieuwe_klant` | Nieuwe klantmap aanmaken met de volledige standaardstructuur. |
| `parameterwijziging` | GBS- of regelaarparameter wijziging documenteren en loggen. |
| `schrijf_email` | E-mail opstellen in de stijl van de zaakvoerder. |
| `schrijf_werkbon` | Werkbon opstellen na interventie of onderhoud. |
| `technisch_rapport` | Technisch rapport of analyse opstellen. |

## Een nieuwe skill toevoegen

1. Maak een nieuwe map aan in `skills/` met een duidelijke, beschrijvende naam (bijv. `plan_onderhoud`).
2. Maak in die map een bestand `SKILL.md` aan.
3. Beschrijf het Doel, de Benodigde Input, het Stappenplan en de verwachte Output.
4. Voeg de nieuwe skill toe aan de tabel in `AGENTS.md` (sectie 3.3).

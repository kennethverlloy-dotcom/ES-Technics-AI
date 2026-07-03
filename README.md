# ES-Technics AI — De Digitale HVAC- & GBS-Engineer

**Versie 1.0 | ES-Technics BV | juli 2026**

Deze repository is de centrale kennisbank en werkomgeving van de AI-medewerker van ES-Technics BV: een digitale engineer die werkbonnen schrijft, offertes maakt, HVAC-diagnoses uitvoert, GBS-systemen analyseert en projectdossiers beheert — alsof hij al 20 jaar voor het bedrijf werkt.

De architectuur is **volledig AI-onafhankelijk**: dezelfde repository werkt zonder wijzigingen met Claude Code, OpenAI Codex, Cursor, ChatGPT Projects en toekomstige AI-platformen. Alle kennis is opgeslagen als leesbare Markdown-bestanden onder Git-versiebeheer.

---

## 1. Snelstart per platform

### Claude Code (aanbevolen)

```bash
cd es-technics-ai
claude
```

Claude Code leest automatisch `AGENTS.md` en heeft direct toegang tot de volledige kennisbank en alle skills. Voorbeeldopdracht:

> "Schrijf een werkbon voor de interventie van vandaag bij Action: chiller 2 gaf hogedrukstoring, condensor gereinigd, drukken gecontroleerd."

### Cursor

Open de map `es-technics-ai/` als project in Cursor. Cursor leest `AGENTS.md` automatisch via de AGENTS.md-standaard. Gebruik de chat of Composer voor opdrachten.

### OpenAI Codex

Koppel deze repository (via GitHub) aan Codex. Codex herkent `AGENTS.md` automatisch als instructiebestand en kan taken asynchroon uitvoeren.

### ChatGPT Projects

1. Maak een nieuw Project aan in ChatGPT.
2. Kopieer de inhoud van `AGENTS.md` naar de projectinstructies.
3. Upload de relevante mappen (bijv. `es-technics/`, `persoonlijk/`, `kennis/` en de betreffende klantmap) als projectbestanden.
4. Stel je vragen in de chat; de AI werkt volgens de bedrijfsstandaarden.

### GitHub

```bash
cd es-technics-ai
git init
git add .
git commit -m "v1.0 - Initiële kennisbank ES-Technics AI"
git remote add origin git@github.com:<jouw-account>/es-technics-ai.git
git push -u origin main
```

Gebruik een **private repository**: deze kennisbank bevat bedrijfs- en klantgegevens.

## 2. Structuur van de repository

| Map | Doel |
| --- | --- |
| `AGENTS.md` | Universele AI-instructies — het "arbeidscontract" van de digitale medewerker |
| `persoonlijk/` | Persoonlijke voorkeuren: schrijfstijl, werkmethodes, leveranciers, opmaak |
| `es-technics/` | Bedrijfs-DNA: standaarden, procedures en alle document-templates |
| `kennis/` | Algemene technische kennis in 16 domeinen (HVAC t/m KNX) |
| `klanten/` | Klantdossiers met volledige historiek (onbeperkt uitbreidbaar) |
| `projecten/` | Niet-klantgebonden projecten, georganiseerd per fase |
| `calculations/` | Rekenmethodes voor HVAC, koeltechniek, hydraulica en elektrisch |
| `vision/` | Richtlijnen voor AI-fotoanalyse van installaties en schema's |
| `media/` | Ruwe bestanden: foto's, video's, CAD, DWG, PDF's |
| `administratie/` | Voorwaarden, contracten, certificaten, attesten, facturen |
| `fabrikant_docs/` | Fabrikantdocumentatie, strikt gescheiden per merk |
| `skills/` | Stapsgewijze workflows (werkbon, offerte, diagnose, ...) |

## 3. Dagelijks gebruik

**Werkbon maken:** geef de AI de feiten van de interventie (klant, locatie, klacht, uitgevoerd werk, materiaal, tijden). De AI volgt `skills/schrijf_werkbon/SKILL.md`, gebruikt het template en slaat het resultaat op in `klanten/<klant>/werkbonnen/`.

**Offerte maken:** beschrijf de gevraagde werken. De AI volgt `skills/maak_offerte/SKILL.md`, raadpleegt de klanthistoriek en levert een offerte volgens de bedrijfsstandaard.

**Diagnose:** beschrijf de storing (of upload een foto). De AI volgt `skills/hvac_diagnose/SKILL.md` of `skills/analyseer_foto/SKILL.md` en werkt systematisch van symptoom naar oorzaak.

**Nieuwe klant:** zeg "maak een nieuwe klant aan: <naam>". De AI maakt de volledige standaardstructuur aan via `skills/nieuwe_klant/SKILL.md`.

## 4. Versiebeheer en back-ups

Elke wijziging wordt vastgelegd via Git:

```bash
git add .
git commit -m "[Action] werkbon: chiller storing filiaal Gent"
git push
```

Hierdoor is elke versie van elk document voor altijd terug te vinden (`git log`, `git diff`). GitHub fungeert als automatische cloud-back-up; de lokale kopie werkt volledig offline. Maak daarnaast periodiek (bijv. maandelijks) een ZIP-archief van de volledige repository als extra back-up op een externe schijf of NAS.

## 5. Onderhoud en uitbreiding

- **Nieuwe kennis toevoegen:** plaats een Markdown-bestand in de juiste map onder `kennis/` of `fabrikant_docs/<merk>/`. De AI gebruikt het direct.
- **Nieuwe klant:** via de skill `nieuwe_klant` — de structuur is onbeperkt uitbreidbaar.
- **Nieuwe fabrikant:** maak een map aan onder `fabrikant_docs/` en voeg documentatie toe.
- **Nieuwe workflow:** kopieer een bestaande skill-map, pas `SKILL.md` aan en commit.
- **Template wijzigen:** pas het bestand in `es-technics/templates/` aan; alle toekomstige documenten volgen automatisch de nieuwe opmaak.

## 6. Roadmap

| Versie | Inhoud |
| --- | --- |
| **v1.0 (huidig)** | Volledige structuur, AGENTS.md, standaarden, templates, kennisbank, skills, klantdossiers, Git-versiebeheer |
| v2.0 | Uitgebreide rekenmodules, vision-analyses, media- en administratiebeheer |
| v3.0 | Diepgaande merkspecifieke GBS/PLC-kennis, automatische as-built- en opleverdossiers |
| v4.0 | Lokale vector-database (RAG) voor grootschalige PDF-collecties, data-analyse over historiek |
| v5.0 | API-koppelingen (ERP, boekhouding), proactieve monitoring en autonome workflows |

---

*ES-Technics BV — Deze repository is ontworpen als de centrale kennisbank van het bedrijf voor de komende 10 jaar.*

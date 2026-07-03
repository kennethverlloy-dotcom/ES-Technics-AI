# Naamgevingsconventies ES-Technics BV

Consistente naamgeving maakt de repository leesbaar voor mensen én AI-platformen. Deze standaard geldt voor bestanden, mappen, projecten, documentnummers en Git-commits.

## Bestanden en mappen

Bestanden krijgen altijd een datum vooraan, gevolgd door het documenttype en een korte omschrijving.

| Type | Formaat | Voorbeeld |
| --- | --- | --- |
| Werkbon | `JJJJ-MM-DD_werkbon_omschrijving.md` | `2026-07-03_werkbon_chiller-hogedrukstoring.md` |
| Offerte | `JJJJ-MM-DD_offerte_omschrijving.md` | `2026-07-03_offerte_vervanging-regelaar.md` |
| E-mail | `JJJJ-MM-DD_email_omschrijving.md` | `2026-07-03_email_planning-interventie.md` |
| Rapport | `JJJJ-MM-DD_rapport_omschrijving.md` | `2026-07-03_rapport_regelanalyse-luchtgroep.md` |
| Berekening | `JJJJ-MM-DD_berekening_omschrijving.md` | `2026-07-03_berekening_pompdebiet.md` |

Mapnamen gebruiken bij voorkeur **underscores** in plaats van spaties. Dit houdt paden compatibel met scripts, GitHub en AI-tools. Voor merknamen en technische protocollen mag de gangbare schrijfwijze behouden blijven indien dat de herkenbaarheid verhoogt.

## Documentnummers en codes

| Onderdeel | Formaat | Voorbeeld |
| --- | --- | --- |
| Offerte | `OFF-JJJJMMDD-XX` | `OFF-20260703-01` |
| Werkbon | `WB-JJJJMMDD-XX` | `WB-20260703-02` |
| Projectcode | `PRJ-JJJJ-XXX` | `PRJ-2026-014` |
| Rapportnummer | `RAP-JJJJMMDD-XX` | `RAP-20260703-01` |
| Installatie-ID | `<site>-<type>-<volgnummer>` | `ACT-LBK-01` |

## GBS-puntnamen

Voor GBS- en automatiepunten wordt een vaste opbouw gebruikt, zodat de functie van een punt onmiddellijk herkenbaar is.

| Structuur | Betekenis | Voorbeeld |
| --- | --- | --- |
| `GB1_LBK01_TT01` | Gebouw 1, luchtbehandelingskast 1, temperatuurtransmitter 1 | Aanvoerluchttemperatuur LBK |
| `GB1_KOEL01_PI01` | Gebouw 1, koelgroep 1, pressure indicator 1 | Condensordrukmeting |
| `GB2_POMP01_DO01` | Gebouw 2, pomp 1, digital output 1 | Start/stopsignaal pomp |

Gebruik herkenbare suffixen zoals `TT` (temperature transmitter), `PT` (pressure transmitter), `DI`, `DO`, `AI`, `AO`, `CMD`, `FB` en `ALM`.

## Git-commits

Elke commit beschrijft exact wat werd gewijzigd. Het aanbevolen formaat is:

`[klant of project] type: omschrijving`

Voorbeelden:

- `[Action] werkbon: chiller storing filiaal Gent`
- `[PRJ-2026-014] as-built: puntenlijst aangevuld`
- `[algemeen] standaard: veiligheidsprocedure bijgewerkt`

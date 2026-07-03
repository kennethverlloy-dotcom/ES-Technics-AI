# Klanten

De map `klanten/` bevat voor elke klant een volledig eigen kennisbank en historisch dossier. De structuur is onbeperkt uitbreidbaar en identiek voor elke nieuwe klant.

| Submap | Doel |
| --- | --- |
| `werkbonnen/` | Interventies, onderhoudsverslagen en serviceverslagen |
| `offertes/` | Klantspecifieke offertes |
| `projecten/` | Projectgerelateerde documenten binnen de klantcontext |
| `emails/` | Uitgaande en relevante inkomende communicatie |
| `technische_historiek/` | Samenvatting van eerdere storingen, beslissingen en risico's |
| `installaties/` | Activa-overzicht, installatiefiches en locaties |
| `fotos/` | Verwijzingen naar beeldmateriaal of analyses |
| `handleidingen/` | Klantspecifieke documenten en samenvattingen |
| `berekeningen/` | Site- of installatiegebonden berekeningen |
| `as_built_dossiers/` | Finale projectdocumentatie |
| `opleverdossiers/` | Opleverdocumenten en restpuntenlijsten |

De AI raadpleegt bij elke klanttaak eerst de technische historiek en installatiestructuur. Nieuwe klanten worden aangemaakt via de skill `skills/nieuwe_klant/`.

## Levenscyclus van een Klantdossier
1. **Intake:** Bij een nieuwe klant wordt de map aangemaakt en `00_klantprofiel.md` ingevuld.
2. **Inventarisatie:** Tijdens de eerste interventie wordt `00_installatie_overzicht.md` aangevuld met de aanwezige assets.
3. **Exploitatie:** Interventies genereren werkbonnen in `werkbonnen/` en parameterwijzigingen of hardnekkige storingen worden gelogd in `technische_historiek/`.
4. **Projecten:** Grotere werken krijgen een eigen map in `projecten/` binnen de klantmap, en resulteren uiteindelijk in een `as_built_dossier`.

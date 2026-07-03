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

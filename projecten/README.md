# Projecten

De map `projecten/` bevat projecten die nog niet aan een specifieke klant gekoppeld zijn of die projectmatig over meerdere partijen heen lopen.

| Fase | Doel | Typische documenten |
| --- | --- | --- |
| `actief/` | Intake en opstart | notities, aanvraag, scope |
| `engineering/` | Ontwerp en voorbereiding | schema's, berekeningen, offertestukken |
| `uitvoering/` | Realisatie | werfverslagen, materiaalstaten, planning |
| `oplevering/` | Testen en overdracht | testrapporten, restpunten |
| `as-built/` | Finalisatie documentatie | puntenlijsten, regelbeschrijvingen, revisies |
| `afgewerkt/` | Archief | finale dossiers |

Bij elke faseovergang wordt de projectmap fysiek verplaatst naar de volgende map en via Git gecommit. Projectcodes volgen het formaat `PRJ-JJJJ-XXX`.

## Checklists per Fase

Om de overgang van de ene naar de andere fase te garanderen, hanteert ES-Technics de volgende minimale vereisten:

### Van Actief naar Engineering
- [ ] Projectfiche is volledig ingevuld.
- [ ] Scope en uitsluitingen zijn formeel bevestigd door de klant.
- [ ] Offerte is goedgekeurd.

### Van Engineering naar Uitvoering
- [ ] Materiaallijsten (BOM) zijn gegenereerd en besteld.
- [ ] P&ID en elektrische schema's zijn "Approved for Construction".
- [ ] GBS-puntenlijst en regelbeschrijving zijn opgesteld.

### Van Uitvoering naar Oplevering
- [ ] Installatie is fysiek afgewerkt en veilig bevonden (geen blootliggende spanning).
- [ ] IO-check is 100% uitgevoerd.
- [ ] Functionele testen zijn doorlopen.

### Van Oplevering naar As-built
- [ ] Restpuntenlijst is afgewerkt.
- [ ] Klant heeft het opleveringsdocument ondertekend.
- [ ] Laatste wijzigingen zijn verwerkt in de schema's ("As-built").
- [ ] Back-ups van PLC/GBS zijn opgeslagen.

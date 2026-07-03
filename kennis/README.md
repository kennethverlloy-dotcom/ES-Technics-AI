# Kennisbank ES-Technics BV

De map `kennis/` vormt het technische brein van de AI-medewerker. Hierin staan de theoretische principes, regelstrategieën en diagnosemethodieken voor 16 verschillende domeinen.

> **Belangrijke Regel (Strikte Scheiding):** 
> Deze map bevat **algemene theorie en systeemonafhankelijke kennis**. Merkspecifieke instructies, alarmcodes, softwaretools of handleidingen (zoals van Priva, Siemens, WAGO) horen **uitsluitend** thuis in de map `fabrikant_docs/`.

## Structuur per Domein

Elk domein bevat documenten genummerd volgens een logische opbouw:

- `01_basisprincipes.md`: De fundamenten van het domein.
- `02_...`: Diepgaande topics, zoals regelstrategieën of specifieke storingsdiagnose.

## Domeinen

| Domein | Focus |
| --- | --- |
| `BACnet`, `KNX`, `Modbus` | Communicatieprotocollen en netwerkarchitectuur. |
| `Elektrisch`, `PLC`, `Regeltechniek` | Automatisering, kastenbouw en sturingen. |
| `GBS` | Gebouwbeheersystemen en alarmmanagement. |
| `HVAC`, `Ventilatie`, `Verwarming` | Klimatisatie en luchtbehandeling. |
| `Hydraulica` | Pompselectie, leidingnetten en ventielen. |
| `Koeltechniek` | Dampcompressiecyclus, DX-systemen en chillers. |
| `Johnson_Controls`, `Priva`, `Siemens`, `WAGO` | Systeemonafhankelijke architectuurprincipes van deze platformen (voor specifieke handleidingen: zie `fabrikant_docs/`). |

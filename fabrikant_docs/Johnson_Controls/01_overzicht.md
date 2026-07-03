# Overzicht Johnson Controls

Deze map bevat uitsluitend Johnson Controls-informatie. Johnson Controls is relevant via zowel gebouwbeheersystemen als koelmachines.

Binnen GBS zijn **Metasys**, **NAE/SNE-engines**, **Facility Explorer FX-controllers** en de configuratietool **CCT** belangrijk. In koeltechniek is ook **York** een relevante productlijn. Johnson Controls werkt vaak met **BACnet**, maar oudere omgevingen kunnen ook **N2** of **Modbus** bevatten.

Belangrijke aandachtspunten zijn versiecompatibiliteit, correcte netwerkarchitectuur, duidelijke objectnaamgeving en controle van alarm- en trendinstellingen bij service. Officiële documentatie wordt ontsloten via Johnson Controls-kennisportalen en productspecifieke handleidingen.

## Service Aandachtspunten
- **Metasys NAE/SNE:** Controleer bij netwerkstoringen de offline/online status van veldcontrollers in de SMP (Site Management Portal) of MUI (Metasys User Interface).
- **CCT (Controller Configuration Tool):** Bij het inladen (download) van een nieuwe applicatie naar een veldcontroller, wordt de controller herstart. Doe dit nooit tijdens kritieke bedrijfsprocessen zonder afstemming.
- **York Chillers:** Gebruik het lokale display voor eerste diagnose. Veel storingen (zoals lage flow of sensordefecten) worden hier met een specifieke foutcode en tijdstempel gelogd.

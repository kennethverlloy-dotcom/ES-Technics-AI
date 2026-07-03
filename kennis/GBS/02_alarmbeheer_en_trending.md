# Alarmbeheer en Trending in GBS

Effectief beheer van alarmen en historische data (trends) is de sleutel tot predictief onderhoud en snelle storingsdiagnose.

## 1. Alarm Prioriteiten
Niet elk alarm vereist dezelfde reactie. ES-Technics deelt GBS-alarmen in volgens drie niveaus:
- **Kritisch (Prioriteit 1):** Vereist onmiddellijke actie. (Bijv. Brandalarm, Vorstgevaar LBK, Uitval serverruimte koeling). Actie: SMS/Oproep naar wachtdienst, rode indicatie op SCADA.
- **Hoog (Prioriteit 2):** Vereist actie binnen de werkdag. (Bijv. Hogedrukstoring chiller, pompdefect). Actie: E-mail naar service desk, oranje indicatie op SCADA.
- **Normaal/Laag (Prioriteit 3):** Voor onderhoudsplanning. (Bijv. Filter vervuild, draaiuren overschreden). Actie: Enkel zichtbaar in de alarmlijst (geel/blauw), geen actieve melding.

## 2. Alarmvertragingen (Delay)
Om "alarmmoeheid" door valse meldingen te voorkomen, moeten vertragingen correct worden ingesteld:
- **Temperatuuralarmen:** Minstens 15 tot 30 minuten vertraging. (Een deur die even openstaat mag geen alarm genereren).
- **Drukverschil (Filters):** Minstens 5 minuten vertraging en enkel actief wanneer de ventilator draait.
- **Hardware-storingen:** (Bijv. thermiek pomp uitgevallen) Mogen direct (0-5 seconden vertraging) doorkomen.

## 3. Trendconfiguratie
Data opslaan is zinloos als de resolutie of retentie verkeerd is. Standaard richtlijnen voor trending:
- **Analoge waarden (Temperatuur, Druk):** Opslaan bij een wijziging (Change of Value - COV) van 0,5°C of 5% om data-opslag te beperken, of anders elke 15 minuten.
- **Digitale waarden (Status, Alarm):** Opslaan bij elke statuswijziging (COV).
- **Regeluitgangen (Klepstanden, Frequenties):** Opslaan elke 5 minuten om pendelgedrag (PID instabiliteit) te kunnen analyseren.
- **Retentie:** Minimaal 1 jaar opslag op de server voor seizoensvergelijkingen.

## 4. Analyse van Pendelgedrag
Wanneer uit trends blijkt dat een klep of pomp voortdurend op en neer stuurt (bijv. van 20% naar 80% en terug binnen enkele minuten), duidt dit op een te agressieve P-actie of een te korte I-tijd in de PID-regelaar. Dit leidt tot snelle mechanische slijtage en moet softwarematig worden afgesteld.

# Regelstrategieën Luchtbehandelingskasten (LBK)

Een optimale regeling van luchtbehandelingskasten (LBK's) garandeert comfort met een minimaal energieverbruik. Dit document beschrijft de standaard regelstrategieën die ES-Technics toepast.

## 1. Vraaggestuurde Ventilatie (VAV)
In plaats van een constant debiet (CAV), wordt het luchtdebiet gemoduleerd op basis van de actuele behoefte in de ruimte.
- **CO2-regeling:** De ventilator draait op een minimumdebiet (bijv. 30%) zolang de CO2-waarde onder 800 ppm blijft. Tussen 800 en 1200 ppm moduleert de ventilator proportioneel naar 100%.
- **Drukregeling:** Bij VAV-boxen in de kanalen houdt de LBK een constante statische druk in het hoofdkanaal aan via een PID-regelaar op de frequentieregelaar van de ventilator.

## 2. Temperatuurregeling (Cascade)
De ruimtetemperatuur is leidend, maar de LBK regelt de inblaastemperatuur. Dit gebeurt via een cascaderegeling:
1. De **hoofdregelaar** (ruimte of retourlucht) berekent de benodigde inblaastemperatuur (setpoint).
2. De **volgregelaar** (inblaaslucht) stuurt de kleppen van de warmte- en koudewaterbatterijen of de warmtewisselaar aan om dit setpoint te halen.
- **Begrenzing:** De inblaastemperatuur wordt altijd begrensd (bijv. min. 16°C om tocht te voorkomen, max. 35°C).

## 3. Warmteterugwinning (WTW)
Voordat actieve verwarming of koeling wordt ingeschakeld, moet de warmteterugwinning maximaal benut worden.
- **Koude-terugwinning:** In de zomer, wanneer de retourlucht koeler is dan de buitenlucht, wordt de WTW (kruisstroom of warmtewiel) ingeschakeld om de warme buitenlucht voor te koelen.
- **Vrije koeling (Free Cooling):** Wanneer de buitentemperatuur lager is dan de ruimtetemperatuur, maar de ruimte koeling vraagt, wordt de WTW uitgeschakeld of gebypasst om de koele buitenlucht direct binnen te blazen.

## 4. Vorstbeveiliging
Een bevroren warmwaterbatterij leidt tot ernstige waterschade. De regeling grijpt als volgt in:
1. **Hardware-thermostaat (Capillair):** Zodra de temperatuur direct na de warmwaterbatterij onder de 5°C zakt, wordt een hard hardwire alarm gegenereerd.
2. **Acties bij alarm:** Ventilatoren stoppen onmiddellijk, buitenluchtkleppen sluiten volledig, en de warmwaterklep opent naar 100% om doorstroming te garanderen. De circulatiepomp start.

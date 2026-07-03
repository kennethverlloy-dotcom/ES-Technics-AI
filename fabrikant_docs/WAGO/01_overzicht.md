# Overzicht WAGO

Deze map bevat uitsluitend WAGO-gerelateerde kennis. WAGO is voor ES-Technics een voorkeursplatform voor flexibele HVAC- en GBS-automatisering.

Relevante productlijnen zijn de **PFC100**- en **PFC200**-controllers, het **750/753 I/O-systeem** en de programmeeromgevingen **e!COCKPIT** en **CODESYS 3.5**. WAGO wordt vaak ingezet voor modulaire sturingen, koppelingen met BACnet/IP, Modbus TCP/RTU, KNX en moderne IT-integraties zoals MQTT.

Belangrijke aandachtspunten zijn correcte IO-opbouw, duidelijke puntnaamgeving, back-up van applicaties vóór wijziging en controle van protocolmapping bij integratie in GBS-omgevingen. Officiële productdocumentatie is beschikbaar via **wago.com**.

## Service Aandachtspunten
- **K-Bus Storingen:** Bij knipperende I/O-LED op de controller, controleer de eindklem (750-600). Een ontbrekende of defecte eindklem veroorzaakt communicatiefouten op de interne bus.
- **Web-Based Management (WBM):** Bereikbaar via het IP-adres van de controller. Controleer hier de firmwareversie en netwerkinstellingen (zoals NTP-server voor correcte tijd).
- **Retain Variabelen:** Zorg bij software-updates dat retain-variabelen (zoals setpoints of draaiuren) niet onbedoeld overschreven worden.

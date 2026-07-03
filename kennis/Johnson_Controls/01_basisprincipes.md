# Technische Kennisbank: Johnson Controls

Dit document biedt een technisch overzicht van de gebouwbeheersystemen (BMS) van Johnson Controls, specifiek gericht op de systemen Metasys en Facility Explorer. Het is bedoeld als referentiemateriaal voor de AI-medewerker en nieuwe engineers binnen ES-Technics BV, met een focus op kernprincipes, veelvoorkomende storingen en best practices in industriële automatisering en gebouwbeheer.

## Kernprincipes en Systeemarchitectuur

Johnson Controls levert geavanceerde oplossingen voor gebouwautomatisering die HVAC, verlichting, beveiliging en brandbeveiliging integreren. De twee belangrijkste platformen zijn Metasys en Facility Explorer. Beide systemen zijn ontworpen met een open architectuur om naadloze integratie met apparatuur van derden mogelijk te maken en ondersteunen moderne IT- en cybersecurity-standaarden.

### Metasys
Metasys is het vlaggenschip BMS van Johnson Controls, ontworpen voor schaalbaarheid van kleine kantoorgebouwen tot grote, complexe campussen zoals ziekenhuizen en datacenters. Het systeem maakt gebruik van een hiërarchische architectuur:
- **Supervisory Controllers (Network Engines):** De SNE (Network Engine) en SNC (Network Control Engine) series hebben de oudere NAE (Network Automation Engine) vervangen. Deze apparaten bewaken en besturen netwerken van field-level controllers en bieden IP-connectiviteit en webgebaseerde toegang.
- **Field Equipment Controllers:** Deze controllers sturen specifieke HVAC-apparatuur aan en communiceren via protocollen zoals BACnet MS/TP, BACnet/IP, of het oudere N2-protocol.
- **User Interface:** Metasys biedt een intuïtieve, browsergebaseerde interface (Metasys UI) die toegankelijk is vanaf elk apparaat, met functies zoals Fault Detection en Fault Triage om operationele efficiëntie te verhogen.

### Facility Explorer
Facility Explorer (FX) is gebouwd op het Niagara Framework en is bijzonder populair vanwege de flexibiliteit en krachtige integratiemogelijkheden. Het systeem is ontworpen voor efficiënte engineering en installatie:
- **FX Supervisory Controllers:** De FX90 (opvolger van de FX80) biedt geavanceerde besturing, datalogging, alarmering en netwerkbeheer.
- **IP en MS/TP Controllers:** Facility Explorer maakt gebruik van next-generation equipment controllers die BACnet/IP ondersteunen, inclusief ring-topologieën via Media Redundancy Protocol (MRP) voor hoge beschikbaarheid.
- **Productivity Tools:** FX bevat tools zoals Auto Tagging en pre-engineered applicaties om de configuratie- en inbedrijfstellingstijd aanzienlijk te verkorten.

## Communicatieprotocollen

Een grondig begrip van de gebruikte communicatieprotocollen is essentieel voor het succesvol implementeren en onderhouden van Johnson Controls systemen.

| Protocol | Beschrijving | Toepassing binnen Johnson Controls |
| :--- | :--- | :--- |
| **BACnet/IP & BACnet/SC** | IP-gebaseerde standaard voor gebouwautomatisering. BACnet Secure Connect (SC) voegt encryptie toe. | Moderne SNE/SNC engines, FX90 controllers en next-gen field controllers. Standaard voor nieuwe installaties. |
| **BACnet MS/TP** | Seriële communicatie over RS-485 netwerken. | Veelgebruikt voor field controllers (zoals VMA's en FEC's). |
| **N2 Bus** | Ouder, propriëtair master/slave protocol van Johnson Controls (9600 baud). | Legacy systemen. Moderne engines ondersteunen N2 vaak nog voor migratiedoeleinden, maar nieuwe installaties gebruiken BACnet. |

## Veelvoorkomende Storingen en Troubleshooting

Bij het onderhouden van Johnson Controls systemen kunnen engineers verschillende problemen tegenkomen. Hieronder volgt een overzicht van veelvoorkomende storingen en de bijbehorende troubleshooting stappen.

### 1. Network Engine (NAE/SNE) Offline
Een veelvoorkomend probleem is dat de supervisory controller de verbinding met de server (ADX/OAS) verliest.
- **Oorzaken:** Stroomuitval, netwerkproblemen (IP-adres wijzigingen, firewall blokkades), of een corrupte database. Bij migraties van NAE naar SNE kan de SNE in een 'bad pairing state' raken als de NAE niet correct is verwijderd uit de Site Director.
- **Oplossing:** Controleer de voeding en de netwerkverbinding (ping test). Verifieer of het IP-adres van de Site Director correct is ingesteld in de engine. Controleer de status LED's op de controller (bijv. de FAULT LED). Bij een corrupte database kan een restore vanuit de SCT (System Configuration Tool) noodzakelijk zijn.

### 2. Communicatieverlies op de Field Bus (MS/TP of N2)
Wanneer meerdere field controllers offline gaan, duidt dit vaak op een probleem met de communicatiebus.
- **Oorzaken:** Bekabelingsfouten (kortsluiting, losse contacten), onjuiste terminatie (EOL), dubbele MAC-adressen, of een defecte controller die de bus verstoort.
- **Oplossing:** Controleer de bedrading visueel en meet de spanning op de bus. Koppel de bus in secties los (halveringsmethode) om de defecte controller of het kabelprobleem te isoleren. Zorg ervoor dat de End-of-Line (EOL) schakelaars correct zijn ingesteld op de eerste en laatste apparaten op de bus.

### 3. Sensor- en Actuatorfouten
Problemen met individuele componenten zoals temperatuursensoren (thermistors) of klepmotoren.
- **Oorzaken:** Defecte sensor, kabelbreuk, of onjuiste configuratie in de software.
- **Oplossing:** Meet de weerstand van de thermistor met een multimeter en vergelijk deze met de specificatietabel van Johnson Controls (bijv. 10k Type II of Type III). Controleer de configuratie in de CCT (Controller Configuration Tool) om te verifiëren of het juiste sensortype is geselecteerd. Voor actuatoren: controleer de stuurspanning (0-10V of 24VAC) en de mechanische koppeling.

## Best Practices voor Installatie en Onderhoud

Om de betrouwbaarheid en levensduur van Johnson Controls systemen te maximaliseren, dienen de volgende best practices in acht te worden genomen:

- **Cybersecurity:** Implementeer altijd de nieuwste firmware-updates. Maak gebruik van BACnet/SC waar mogelijk en volg de Johnson Controls Hardening Guides. Verander standaard wachtwoorden en minimaliseer open poorten op het IT-netwerk.
- **Back-ups:** Maak regelmatig back-ups van de serverdatabases (ADX/OAS) en de controllerconfiguraties via de SCT. Bewaar deze back-ups op een veilige, externe locatie.
- **Migratie en Upgrades:** Bij het upgraden van legacy systemen (zoals N2 naar BACnet), plan de migratie zorgvuldig. Gebruik de Metasys Upgrade Fast Track tool om potentiële problemen vooraf te identificeren. Let op dat BACnet MS/TP hogere baudrates gebruikt dan N2, wat problemen kan opleveren bij het hergebruiken van oude, niet-afgeschermde bekabeling.
- **Documentatie en Tagging:** Maak gebruik van gestandaardiseerde naamgevingsconventies en tagging (zoals Haystack in Facility Explorer). Dit vereenvoudigt toekomstig onderhoud, data-analyse en de integratie met applicaties van derden.
- **Netwerktopologie:** Bij het ontwerpen van IP-gebaseerde field netwerken, overweeg het gebruik van ring-topologieën met MRP-compatibele switches voor verhoogde redundantie, zodat een enkele kabelbreuk niet leidt tot uitval van controllers.
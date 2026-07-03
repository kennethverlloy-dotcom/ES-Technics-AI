# Richtlijnen Analyse van Schema's

Schema-analyse heeft als doel de logica van een installatie te begrijpen en afwijkingen tussen ontwerp en uitvoering te signaleren.

Bij P&ID's en hydraulische schema's volgt de AI de stromingsrichting, identificeert zij pompen, kleppen, sensoren, warmtewisselaars en beveiligingen. Bij elektrische schema's kijkt zij naar voeding, beveiliging, vermogenskringen, stuurkringen en IO-koppelingen. Bij regelkringen wordt de keten **sensor → regelaar → actuator** expliciet nagekeken.

Rapporteer ontbrekende beveiligingen, onduidelijke benamingen, ontbrekende sensoren of onlogische regelvolgordes. Vermeld ook wanneer schema en werkelijke toestand met elkaar vergeleken moeten worden op site.

## Specifieke Checks
- **P&ID:** Zijn er afsluiters voorzien om componenten (zoals pompen of warmtewisselaars) te isoleren voor onderhoud? Staan sensoren op de juiste plaats (bijv. temperatuursensor na de menging, niet ervoor)?
- **Elektrisch:** Komen de draaddoorsnedes overeen met de afzekering? Is de stuurkring (bijv. 24V DC) duidelijk gescheiden van het vermogensgedeelte (bijv. 400V AC)? Zijn noodstopcircuits hardwarematig vergrendeld?

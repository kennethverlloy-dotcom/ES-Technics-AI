# Berekeningen - ES-Technics BV

Deze map bevat de standaard rekenmethodes en formules voor technische berekeningen.

## Algemene Richtlijnen
1.  **Eenheden:** Gebruik altijd SI-eenheden in de berekeningen en vermeld deze expliciet.
2.  **Afronding:** 
    *   Temperaturen: 1 decimaal (bijv. 21,5 °C)
    *   Debieten: gehele getallen (bijv. 1250 m³/h)
    *   Vermogens: 1 of 2 decimalen afhankelijk van de grootte (bijv. 5,5 kW of 125,25 kW)
    *   Drukken: gehele getallen in Pa of kPa, 2 decimalen in bar (bijv. 1,50 bar)
3.  **Transparantie:** Toon in de output altijd de gebruikte formule, de ingevulde waarden en het resultaat.

## Beschikbare Domeinen
*   `hvac/`: Luchtdebieten, kanaalsnelheden, mengtemperaturen.
*   `koeltechniek/`: Koellast, EER/COP, koudemiddelinhoud.
*   `hydraulica/`: Pompdebieten, leidingweerstand, Kv-waarden van ventielen.
*   `elektrisch/`: Stroomsterkte (I = P / (U * sqrt(3) * cos(phi))), kabelsecties.

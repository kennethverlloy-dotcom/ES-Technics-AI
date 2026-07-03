# Skill: Schrijf Werkbon

Deze skill beschrijft de workflow voor het opstellen van een werkbon na een interventie, onderhoud of inbedrijfstelling.

## 1. Doel
Een gestructureerd, feitelijk en technisch accuraat verslag maken van de uitgevoerde werkzaamheden, zodat dit direct naar de klant en de administratie kan.

## 2. Benodigde Input
- Klantnaam en locatie.
- Korte beschrijving van de klacht of opdracht.
- Uitgevoerde acties, metingen en vervangen onderdelen.
- Bestede uren en reistijd.

## 3. Stappenplan

1.  **Historiek Controleren (Cruciaal):**
    - Kijk in `klanten/<klantnaam>/technische_historiek/` en eerdere werkbonnen om te zien of dit een terugkerend probleem is.

2.  **Template Invullen:**
    - Gebruik het template `es-technics/templates/werkbon.md`.
    - Vertaal ruwe notities van de gebruiker ("druk was laag, bijgevuld, draait weer") naar professionele, technische taal ("Lagedrukstoring vastgesteld. Koudemiddelcircuit gecontroleerd op lekkages. Koudemiddel R410a bijgevuld tot nominale werkdruk. Installatie functioneert correct na testrun.").

3.  **Advies Formuleren:**
    - Als de metingen of observaties wijzen op toekomstige problemen (bijv. "compressor maakt abnormaal geluid"), noteer dit dan expliciet onder "Opmerkingen & Advies".

4.  **Bestand Opslaan:**
    - Sla de werkbon op in `klanten/<klantnaam>/werkbonnen/` met de naamgevingsconventie `JJJJ-MM-DD_werkbon_<korte-omschrijving>.md`.
    - Update indien nodig ook de `technische_historiek/` van de klant met de nieuwe bevindingen.

## 4. Output
De AI toont de opgeslagen werkbon aan de gebruiker ter controle.

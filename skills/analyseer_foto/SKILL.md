# Skill: Analyseer Foto

Deze skill begeleidt de AI bij het analyseren van foto's van installaties, elektrische borden, schema's of zichtbare storingsbeelden.

## Doel

Een visueel onderbouwde analyse maken die technische afwijkingen herkent en vertaalt naar concrete aanbevelingen.

## Benodigde input

Minimaal één foto of screenshot, aangevuld met context: klant, installatie, locatie, klacht of vraagstelling.

## Werkwijze

Bepaal eerst de categorie: algemene installatie, elektrisch bord, chiller, luchtgroep, schema of storing. Raadpleeg vervolgens de passende richtlijn in `vision/`. Beschrijf daarna systematisch: wat zichtbaar is, welke componenten herkenbaar zijn, welke afwijkingen opvallen, welke technische betekenis die afwijkingen kunnen hebben en welke risico's daaraan verbonden zijn.

Bij twijfel wordt de observatie als hypothese geformuleerd en niet als zekerheid. De AI vermeldt ook wanneer bijkomende fysieke controle of metingen noodzakelijk zijn.

## Output

Het resultaat wordt opgeslagen in de relevante klantmap, bij voorkeur onder `fotos/` of als gekoppeld rapport, met verwijzing naar het geanalyseerde mediabestand.

# Elektrische Berekeningen

Elektrische basisberekeningen zijn nodig voor motoren, weerstanden, vermogenskringen en dimensionering van kabels en beveiligingen.

## Formules

| Systeem | Formule |
| --- | --- |
| Eenfasig | `I = P / (U × cosφ)` |
| Driefasig | `I = P / (√3 × U × cosφ)` |

## Voorbeeld driefasige motor

Een motor heeft een opgenomen vermogen van **7,5 kW**, netspanning **400 V** en `cosφ = 0,85`.

`I = 7.500 / (1,732 × 400 × 0,85) = 12,7 A`

De nominale stroom bedraagt dus ongeveer **12,7 A**.

## Indicatieve kabelkeuze

| Sectie | Typische maximale stroom* |
| --- | --- |
| 1,5 mm² | 16 A |
| 2,5 mm² | 20 à 25 A |
| 4 mm² | 25 à 32 A |
| 6 mm² | 32 à 40 A |

\* Altijd verifiëren volgens installatieomstandigheden, aanlegwijze en AREI.

## Beveiligingen

Karakteristiek **B** is geschikt voor lichte inschakelstromen, **C** voor standaard motorlasten en **D** voor hoge inschakelstromen. Voor persoonsbeveiliging wordt doorgaans **30 mA** differentieel toegepast; voor brandbeveiliging vaak **300 mA** upstream.

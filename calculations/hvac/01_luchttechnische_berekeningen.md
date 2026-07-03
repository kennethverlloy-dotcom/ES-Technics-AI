# Luchttechnische Berekeningen

Deze nota bundelt de basisberekeningen voor luchtdebiet, vermogen en eenvoudige kanaaldimensionering.

## Kernformules

| Onderwerp | Formule | Opmerking |
| --- | --- | --- |
| Vermogen lucht | `P = qv × ρ × c × ΔT` | met `ρ = 1,2 kg/m³` en `c = 1,005 kJ/kg·K` |
| Luchtverversingsvoud | `n = qv / V` | `V` in m³, `qv` in m³/h |
| Kanaalsnelheid | `v = qv / A` | `qv` omzetten naar m³/s |

## Voorbeeld verwarmingsvermogen

Een luchtgroep levert **2.500 m³/h** en moet lucht opwarmen van **16,0 °C** naar **21,0 °C**. Dan is `ΔT = 5,0 K`.

Omrekening debiet: `2.500 / 3.600 = 0,694 m³/s`.

`P = 0,694 × 1,2 × 1,005 × 5,0 = 4,19 kW`.

Het vereiste verwarmingsvermogen bedraagt dus afgerond **4,2 kW**.

## Richtwaarden

| Toepassing | Richtwaarde |
| --- | --- |
| Hoofdkanalen | 4 tot 6 m/s |
| Aftakkingen | 2 tot 4 m/s |
| Comfortventilatie personen | volgens bezetting en binnenluchtkwaliteit |
| Filtervervuiling | opvolgen via drukverschil |

## Mengtemperatuur

De mengtemperatuur van twee luchtstromen wordt bepaald op basis van debiet en temperatuur. Gebruik: `(q1 × T1 + q2 × T2) / (q1 + q2)`.

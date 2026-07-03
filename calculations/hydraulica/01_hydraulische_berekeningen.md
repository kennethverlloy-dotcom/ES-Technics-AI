# Hydraulische Berekeningen

Hydraulische berekeningen ondersteunen pompselectie, leidingdimensionering en regeltechnische inregeling.

## Waterdebiet uit vermogen

Gebruik de formule `qv = P / (ρ × c × ΔT)`. Voor water wordt vaak gerekend met `ρ ≈ 1.000 kg/m³` en `c = 4,187 kJ/kg·K`.

### Voorbeeld

Een verwarmingskring moet **35,0 kW** leveren bij een temperatuurverschil van **10,0 K**.

`qv = 35,0 / (1.000 × 4,187 × 10,0)` in m³/s. Praktisch gebruikt men de HVAC-vuistregel:

`qv (m³/h) ≈ 0,86 × P / ΔT`

`qv = 0,86 × 35,0 / 10,0 = 3,01 m³/h`

Benodigd debiet: **3,0 m³/h**.

## Richtwaarden stroomsnelheid

| Leidingsysteem | Richtwaarde |
| --- | --- |
| Hoofdleiding | 0,8 tot 1,5 m/s |
| Aftakking | 0,4 tot 1,0 m/s |
| Geluidsgevoelige zones | lager houden |

## Kv-waarde

De Kv-waarde van een regelventiel geeft het waterdebiet weer in m³/h bij een drukverschil van 1 bar. Correcte selectie is essentieel voor regelkwaliteit en autoriteit.

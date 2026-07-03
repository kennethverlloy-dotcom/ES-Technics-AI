# Vuistregels voor Plausibiliteitscontroles

Bij het ontwerpen, offerteren of troubleshooten van installaties is het cruciaal om berekende waarden of gemeten data af te toetsen aan de praktijk. Deze vuistregels helpen de AI en engineers om fouten snel op te sporen.

## 1. Verwarming
- **Vermogen per m² (Nieuwbouw/Goed geïsoleerd):** 35 - 50 W/m²
- **Vermogen per m² (Oudere gebouwen):** 70 - 100 W/m²
- **Vuistregel Waterdebiet:** `qv (m³/h) ≈ 0,86 × P (kW) / ΔT`
  - Bij een standaard regime van 70/50 °C (ΔT = 20 K): debiet ≈ `0,043 × P`
  - Bij vloerverwarming 35/30 °C (ΔT = 5 K): debiet ≈ `0,172 × P`

## 2. Koeling (Comfort)
- **Vermogen per m² (Standaard kantoor):** 40 - 60 W/m²
- **Vermogen per m² (Kantoor met veel glas/Zuidkant):** 70 - 100 W/m²
- **Serverruimtes:** Vaak gebaseerd op het opgestelde elektrisch vermogen (1 kW elektrisch in = nagenoeg 1 kW koellast).
- **Vuistregel Waterdebiet:**
  - Bij een regime van 7/12 °C (ΔT = 5 K): debiet ≈ `0,172 × P`

## 3. Ventilatie
- **Kantoren (Personen):** 30 tot 50 m³/h per persoon (afhankelijk van gewenste IDA-klasse).
- **Sanitair:** 25 tot 50 m³/h per toilet/urinoir.
- **Vuistregel Luchtvermogen:** `P (kW) ≈ qv (m³/h) × ΔT / 3000`
  - *Voorbeeld:* 3000 m³/h lucht 10 graden opwarmen kost ongeveer 10 kW.

## 4. Elektrisch
- **Driefasig vermogen naar stroom (400 V):** `I (A) ≈ P (kW) × 1,5` (bij cos φ ≈ 0,85 en rendement ≈ 0,9)
  - *Voorbeeld:* Een 10 kW pomp trekt ruwweg 15 A.
- **Monofasig vermogen naar stroom (230 V):** `I (A) ≈ P (kW) × 4,5`

> **Toepassing in de praktijk:** Als een berekening uitwijst dat een kantoor van 100 m² een koelvermogen van 30 kW nodig heeft (300 W/m²), is de berekening hoogstwaarschijnlijk fout en moet de invoer (zoals zontoetreding of interne warmtelasten) gecontroleerd worden.

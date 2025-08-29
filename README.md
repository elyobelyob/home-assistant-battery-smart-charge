# Battery Smart Charging (Home Assistant Blueprint)

Smart control of a battery charger using **Octopus Agile half-hourly prices** (via [BottlecapDave’s Octopus integration](https://github.com/BottlecapDave/HomeAssistant-OctopusEnergy)).  
No fixed deadlines: this blueprint looks ahead over the next 24–72 hours and automatically selects the cheapest slots to reach your **target state of charge (SoC)**.

## Features
- Rolling look-ahead planner (24–72h)
- Target SoC band with tolerance
- Critical minimum SoC floor
- Split cheap windows
- Plunge override (force ON)
- Optional low-price fallback
- Optional Greener Nights window and price cap
- Saving Sessions → force OFF

## Installation
1. Copy `battery_smart_charge.yaml` into:
   ```
   config/blueprints/automation/battery_smart_charge/
   ```
2. Restart Home Assistant or reload automations.
3. Go to Settings → Automations & Scenes → Blueprints → Import Blueprint and select the file.
4. Create a new automation and configure inputs.

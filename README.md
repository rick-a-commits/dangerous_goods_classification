Given a set of chemical parameters, I want to bo build a model using Neural Networks that classifies chemical products into Dangerous v Safe goods. This enables us to automatically identify the kind of equipment needed to transport the products from our warehouse to the customer. 
Through this automatic classification, we want to give our operations teams more efficiency in their day to day work, thereby freeing them for more strategic work

# Synthetic Dangerous Goods Dataset

This dataset contains 10,000+ synthetic samples designed for ML experiments in **logistics & hazardous goods classification**.

## Features
- flash_point_c: Flash point (°C)
- boiling_point_c: Boiling point (°C)
- ph: Acidity/alkalinity (0–14)
- vapor_pressure_kpa: Vapor pressure (kPa)
- toxicity_score: Arbitrary toxicity index (0–100)
- oxidizer_content_pct: % oxidizers
- flammable_content_pct: % flammable material
- corrosive_content_pct: % corrosives
- packaging_group: UN packaging group (I = high danger, II = medium, III = low)
- dangerous_good: Target (1 = dangerous, 0 = not dangerous)

## Labeling rules
A product is dangerous if:
- flash_point_c < 60
- OR toxicity_score > 70
- OR ph < 2 or ph > 12
- OR oxidizer_content_pct > 20
- OR flammable_content_pct > 40
- OR corrosive_content_pct > 25
- OR packaging_group == I

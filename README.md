# Renewable Energy RAG Assistant – Knowledge Base

Knowledge base for a retrieval-augmented generation (RAG) assistant that answers questions about
renewable-energy generation, forecasts and statistics, with a focus on Germany (January 2026). It
combines unstructured reports (PDF) with structured time series (CSV), so the assistant can cite both
published statistics and measured data.

> The assistant code (`rag_assistant/`) is not published in this repository yet. Only the knowledge base
> is included.

## Contents of `knowledge_base/`

| File(s) | Content | Source |
|---|---|---|
| `IRENA_RE_Capacity_Statistics_2024.pdf`, `IRENA_DAT_RE_Capacity_Statistics_2025.pdf` | Installed renewable capacity by country and technology | [IRENA](https://www.irena.org/Publications) |
| `IRENA_DAT_RE_Statistics_2025.pdf` | Renewable Energy Statistics 2025 (capacity, generation, balances) | IRENA |
| `IRENA_DAT_Renewable_energy_highlights_2025.pdf` | Short summary of the 2025 figures | IRENA |
| `Off-grid_Renewable_Energy_Statistics_2024.pdf`, `IRENA_DAT_Off-grid_Renewable_Energy_Statistics_2025.pdf` | Off-grid renewable statistics | IRENA |
| `GUI_WIND_SOLAR_GENERATION_FORECAST_ONSHORE_*.csv` | Onshore wind: day-ahead, intraday and current forecasts vs. actual generation (MW), bidding zone DE-LU, 15-min resolution, first week of January 2024, 2025 and 2026 | [ENTSO-E Transparency Platform](https://transparency.entsoe.eu/) |
| `Realisierte_Erzeugung_202501010000_202601010000_Viertelstunde.csv` | Realised electricity generation in Germany by source, 2025, 15-min resolution | [SMARD / Bundesnetzagentur](https://www.smard.de/home/downloadcenter/download-marktdaten/) |
| `T1.csv` | Wind-turbine SCADA data (2018, 10-min): active power, wind speed, theoretical power curve, wind direction | [Kaggle – Wind Turbine SCADA Dataset](https://www.kaggle.com/datasets/berkerisen/wind-turbine-scada-dataset) |
| `Weather Data.csv` | Hourly weather observations for 2012 (temperature, dew point, humidity, wind speed, visibility, pressure, conditions) | public Kaggle weather dataset |
| `wind_silver.csv`, `wind_gold.csv` | Derived from `Weather Data.csv`: cleaned hourly records with an ingest timestamp and a 1-day temperature lag (*silver*), and monthly aggregates (*gold*) | own processing |
| `dynamische-strompreise-i.csv` | Monthly German household electricity prices for existing customers, new customers and dynamic tariffs (2022–2025) | public price comparison |

Third-party files remain subject to the terms of their publishers. Cite the original source when you
reuse them.

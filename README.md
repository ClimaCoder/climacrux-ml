# climacrux-ml

Machine learning for climate extremes in Latin America — ENSO forecasting, MJO teleconnections, and compound event prediction.

Part of the [ClimaCoder](https://climacoder.com) project.

## Research tracks

### Track 1: ENSO & Corredor Seco Drought Forecasting
Predict ENSO phase 3–12 months ahead and translate ENSO signals into Corredor Seco rainfall anomaly probabilities. The Corredor Seco spans Guatemala, Honduras, and El Salvador — one of the world's most climate-vulnerable regions. When El Niño hits, crops fail and people migrate.

**Data:** NOAA ENSO indices (ONI, MEI, SOI), CHIRPS precipitation, ERA5 reanalysis
**Methods:** LSTM / Transformer sequence models, teleconnection composites
**Status:** Open — looking for contributors

### Track 2: Compound Drought + Heat Events
Simultaneous drought and extreme heat kill harvests and drive migration in the Corredor Seco. This track builds a 1950–present climatology of compound events and trains a classifier to identify precursor patterns 2–4 weeks before onset.

**Data:** ERA5-Land (via ARCO-ERA5), CHIRPS
**Methods:** Compound event detection, random forests / gradient boosting, trend analysis
**Status:** Open — looking for contributors

### Track 3: Subseasonal Heat Forecasting via MJO
The 2–6 week forecast range is the hardest and most useful for decisions like planting schedules and heat emergency preparedness. The Madden-Julian Oscillation (MJO) is the dominant source of predictability at this timescale. This track builds MJO-phase composites for Central America and generates probabilistic heat outlooks.

**Data:** NOAA MJO real-time indices, ERA5
**Methods:** Statistical compositing, probabilistic forecasting
**Status:** Open — looking for contributors

## Structure

```
climacrux-ml/
  enso/             # ENSO forecasting and Corredor Seco drought outlooks
  compound-events/  # Compound drought + heat event detection and prediction
  mjo/              # MJO teleconnections and subseasonal heat forecasting
  shared/           # Shared utilities, data loaders, evaluation metrics
```

## Getting started

Notebooks are designed to run on Google Colab. Historical climate data comes from [ARCO-ERA5](https://github.com/google-research/arco-era5) — no API key required.

See [historical-analysis](https://github.com/ClimaCoder/historical-analysis) for ERA5 data access patterns and UTCI computation utilities.

### Core dependencies

```bash
pip install xarray zarr gcsfs pandas numpy scikit-learn tensorflow torch matplotlib
```

## Contributing

Read [CONTRIBUTING.md](https://github.com/ClimaCoder/website/blob/main/CONTRIBUTING.md) and the full [ROADMAP](https://github.com/ClimaCoder/website/blob/main/ROADMAP.md). All climate methodology decisions go through Elif. Open an issue before starting significant work.

## License

MIT

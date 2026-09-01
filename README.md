# Catchment Hydrology — Lecture 2: The runoff ratio of US catchments

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/wberghuijs/CatchmentHydro_Lecture2_RunoffRatio/main?filepath=Lecture_2_RunoffRatio.ipynb)

This is an updated build of the original `CatchmentHydro_Lecture2_RunoffRatio` notebook, using
**CAMELS** (Newman et al., 2015; Addor et al., 2017) — 671 catchments across the contiguous United
States. It's built with the same interactive toolkit as its European counterpart,
[EStreams_Lecture_RunoffRatio](https://github.com/wberghuijs/EStreams_Lecture_RunoffRatio), so the
two notebooks are directly comparable in both style and functionality.

Click the *launch binder* badge above (once this repo is on GitHub) to open the notebook in a
ready-to-run Jupyter environment — no local installation needed. To run it locally instead:

```bash
pip install -r requirements.txt
jupyter notebook Lecture_2_RunoffRatio.ipynb
```

## What's in this repo

- `Lecture_2_RunoffRatio.ipynb` — the interactive lecture notebook: an intro to the runoff ratio
  and the Budyko framework, followed by interactive histogram, scatter, map and correlation tools
  (built with `ipywidgets`) for exploring CAMELS, plus a set of discussion questions.
- `requirements.txt` — Python dependencies for Binder / local use.
- `data/` — the 7 CAMELS attribute tables (`camels_hydro.txt`, `camels_clim.txt`,
  `camels_soil.txt`, `camels_topo.txt`, `camels_vege.txt`, `camels_geol.txt`, `camels_name.txt`),
  one row per catchment, semicolon-separated.
- `shapefiles/` — a US states boundary shapefile, used as the map background.

## What's different from the original notebook

Same dataset, same questions and learning goal, but every interactive tool has been rebuilt to
match the EStreams companion notebook:

- **Scatter tool**: an optional third "color by" variable (rather than a required one), a choice
  of 6 fit types (linear / quadratic / cubic / exponential / logarithmic / power) with the fitted
  equation drawn directly on the plot, and manual text-box overrides for every axis and the
  colorbar range.
- **Map tool**: a bigger figure with a slimmer colorbar, manual colorbar/lon/lat limits, and a
  HUC-02 hydrologic-region filter (the US analogue of the "country" filter in the EStreams map)
  that auto-zooms to the selected region.
- **Histogram and correlation tools**: the same manual axis/colorbar override pattern.

## Data & license

CAMELS is a public, widely-used research dataset; see the citations below. The bundled `data/` and
`shapefiles/` are unchanged from the original repository.

If you use this notebook or the data, please cite:

> Addor, N., Newman, A. J., Mizukami, N., & Clark, M. P. (2017). The CAMELS data set: catchment
> attributes and meteorology for large-sample studies. *Hydrology and Earth System Sciences*,
> 21(10), 5293–5313. https://doi.org/10.5194/hess-21-5293-2017

> Newman, A. J., et al. (2015). Development of a large-sample watershed-scale hydrometeorological
> data set for the contiguous USA. *Hydrology and Earth System Sciences*, 19, 209–223.
> https://doi.org/10.5194/hess-19-209-2015

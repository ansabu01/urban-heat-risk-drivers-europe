# Drivers of Urban Heat Risk in European Cities

This project examines which temporal, spatial, and measurement-related factors are most strongly associated with city-relative high heat exposure using street-level sensor data from selected European cities.

**Analysis:** [`urban_heat_risk_drivers_in_europe.ipynb`](urban_heat_risk_drivers_in_europe.ipynb)  
**PDF:** [`urban_heat_risk_drivers_in_europe.pdf`](urban_heat_risk_drivers_in_europe.pdf)  
**Interactive map:** [`station_risk_map.html`](station_risk_map.html)

## Overview

The analysis uses the [FAIRUrbTemp curated dataset](https://www.kaggle.com/datasets/pablomoratodomnguez/fairurbtemp-curated) to model high heat exposure at the station-hour level. High heat is defined relative to each city's temperature distribution. Dummy classification, logistic regression, regularized logistic regression, and random forests are compared using chronological validation and robustness checks.

## Key Findings

- Daily and seasonal timing variables provide the strongest and most stable predictive signal.
- The available spatial and measurement-related variables add comparatively limited and less stable information.
- The main driver ranking remains broadly consistent across alternative heat-risk thresholds, time windows, feature sets, and model specifications.
- The station-level map is best interpreted as a screening tool rather than a causal or definitive spatial heat-risk map.

## Installation

Python 3.12 is recommended.

```bash
python -m venv .venv
```

Activate the environment on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

## Usage

Launch the analysis with:

```bash
jupyter lab urban_heat_risk_drivers_in_europe.ipynb
```

The notebook downloads the source dataset through `kagglehub`. The included PDF provides a static rendering of the analysis, while `station_risk_map.html` contains the interactive station-level map.

## Data

The underlying data are obtained from the FAIRUrbTemp curated dataset and are not redistributed here. Users should consult the [dataset page](https://www.kaggle.com/datasets/pablomoratodomnguez/fairurbtemp-curated) for source documentation and applicable terms.

## License

The project code is released under the [MIT License](LICENSE). The license does not cover the source dataset or third-party materials.

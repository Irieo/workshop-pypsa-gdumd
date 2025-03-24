# Annex Config

Below is the content of the config.yaml file:

```yaml
# SPDX-FileCopyrightText: Contributors to PyPSA-Eur <https://github.com/pypsa/pypsa-eur>
#
# SPDX-License-Identifier: CC0-1.0

# docs in https://pypsa-eur.readthedocs.io/en/latest/configuration.html#run
run:
  prefix: MD-workshop
  name:
    # - benchmark
    # - no_imports
    # - no_imports_pricygas
    - no_imports_lowemis
  scenarios:
    enable: true
    file: config/scenarios.yaml
  disable_progressbar: true
  shared_resources:
    policy: base
  shared_cutouts: true

# docs in https://pypsa-eur.readthedocs.io/en/latest/configuration.html#scenario
scenario:
  clusters:
  - 10
  planning_horizons:
  - 2025

# docs in https://pypsa-eur.readthedocs.io/en/latest/configuration.html#countries
countries: ["MD", "UA"]

# docs in https://pypsa-eur.readthedocs.io/en/latest/configuration.html#snapshots
snapshots:
  start: "2013-01-01"
  end: "2014-01-01"
  inclusive: 'left'


# docs in https://pypsa-eur.readthedocs.io/en/latest/configuration.html#electricity
electricity:
  voltages: [220., 300., 330., 380., 400., 500., 750.]
  base_network: osm-prebuilt
  osm-prebuilt-version: 0.6

  operational_reserve:
    activate: false
    epsilon_load: 0.02
    epsilon_vres: 0.02
    contingency: 4000

  extendable_carriers:
    Generator: [solar, onwind, offwind-ac, OCGT, CCGT, nuclear]
    StorageUnit: [] # battery, H2
    Store: [battery]
    Link: [] # H2 pipeline

  renewable_carriers: [solar, onwind, offwind-ac, hydro]

  powerplants_filter: (DateOut >= 2024 or DateOut != DateOut) and not (Country == 'Germany' and Fueltype == 'Nuclear')
  custom_powerplants: false
  everywhere_powerplants: [nuclear, oil, OCGT, CCGT, coal, lignite, geothermal, biomass]

  autarky:
    enable: false
    by_country: false

clustering:
  temporal:
    resolution_elec: 3h

costs:
  year: 2025
  version: v0.10.1

solving:
  solver:
    name: gurobi
...
```
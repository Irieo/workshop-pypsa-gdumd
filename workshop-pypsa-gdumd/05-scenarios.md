# Annex Config

Below is the content of the scenario.yaml file:

```yaml
# -*- coding: utf-8 -*-
# SPDX-FileCopyrightText: : 2017-2023 The PyPSA-Eur Authors
#
# SPDX-License-Identifier: MIT

# This file is used to define the scenarios that are run by snakemake. Each entry on the first level is a scenario. Each scenario can contain configuration overrides with respect to the config/config.yaml settings.
#
# Example
#
# custom-scenario: # name of the scenario
#   electricity:
#       renewable_carriers: [wind, solar] # override the list of renewable carriers

benchmark: {}

no_imports:
  electricity:
    autarky:
      enable: true
      by_country: true

no_imports_pricygas:
  electricity:
    autarky:
      enable: true
      by_country: true
  costs:
    overwrites:
      fuel:
        gas: 50 # €/MWh_th
    emission_prices:
      enable: true
      co2: 80 # €/tCO2

no_imports_lowemis:
  electricity:
    autarky:
      enable: true
      by_country: true
  costs:
    overwrites:
      fuel:
        gas: 50 # €/MWh_th
    emission_prices:
      enable: true
      co2: 500 # €/tCO2
```
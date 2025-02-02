# OAF Public Charts

[![Artifact HUB](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/one-acre-fund)](https://artifacthub.io/packages/search?repo=one-acre-fund)
[![Release Charts](https://github.com/one-acre-fund/oaf-public-charts/actions/workflows/helm-release.yaml/badge.svg)](https://github.com/one-acre-fund/oaf-public-charts/actions/workflows/helm-release.yaml)

A collection of useful Helm charts used at [One Acre Fund](https://oneacrefund.org/).

## Installation

```sh
helm repo add one-acre-fund https://one-acre-fund.github.io/oaf-public-charts
```

## Included Charts

* [Apicurio Studio](https://www.apicur.io/studio/)
* [Flagsmith](https://flagsmith.com/)
* [GrowthBook](https://growthbook.io/)
* [KoboToolbox](https://www.kobotoolbox.org/)
* [Kutt](https://kutt.it/)
* [Mautic](https://www.mautic.org/)
* [n8n](https://n8n.io/)
* [Nocodb](https://www.nocodb.com/)
* [PgBouncer](https://www.pgbouncer.org/)
* [Sydent](https://github.com/matrix-org/sydent)
* [Uptime Wrapper](https://uptime-kuma-api.readthedocs.io/en/latest)

## How to contribute

This repository has the following CI workflows:

* Every PR will lint and test all updated charts using [chart-testing](https://github.com/helm/chart-testing)
  * __Note__: this will fail if any chart is updated without bumping its version - so that published versions remain immutable
* Every merge to `main` branch will publish all updated charts using [chart-releaser](https://github.com/helm/chart-releaser)
* a pre-commit hook is configured to auto-generate each chart's README from the annotations in their `values.yaml`.
  * This requires contributors to install [pre-commit](https://pre-commit.com/)
    and set up the hook (`pre-commit install && pre-commit install-hooks`).
    Otherwise linting will fail at CI time if any discrepancy is detected between `values.yaml` and `README`.

# PromLens

![Version: 0.2.2](https://img.shields.io/badge/Version-0.2.2-informational?style=flat-square) ![Release Status](https://github.com/ricardo-ch/helm-charts/workflows/Release%20Charts/badge.svg)

This chart installs [PromLens](https://promlens.com/) from [PromLabs](https://promlabs.com/).

PromLens is a tool that makes learning and using PromQL easier and more productive. It integrates a visual query builder with explanation and visualization features.

## Helm Chart

This is an initial release, based on the Helm chart we are using to deploy the tool internally. Currently, there are multiple features of PromLens that this Chart doesn't provide. If something is missing, feel free to open and issue or submit a Pull Request.

### How To Install

Simply add this Chart repository to Helm:

```sh
➜ helm repo add ricardo https://ricardo-ch.github.io/helm-charts/
"ricardo" has been added to your repositories
```

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| config.gcs_sa | string | `""` | Google Cloud Storage Account |
| config.grafana_api_key | string | `""` | Grafana API Key, see https://grafana.com/docs/grafana/latest/http_api/auth/ |
| config.grafana_url | string | `""` | Grafana URL |
| config.license | string | `""` | PromLens License |
| config.shared_links_bucket_name | string | `"promlens"` | Bucket Name in Storage Account |
| deployment.image | string | `"promlabs/promlens"` | PromLens Conatiner Image |
| deployment.replicas | int | `1` | Number of replicas |
| deployment.version | string | `"latest"` | PromLens Container Image Version |

## Source Code

* <https://github.com/ricardo-ch/helm-charts/tree/main/charts/promlens>

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.3.0](https://github.com/norwoodj/helm-docs/releases/v1.3.0)
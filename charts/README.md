# respondnow

![Version: 0.1.2](https://img.shields.io/badge/Version-0.1.2-informational?style=flat-square) ![AppVersion: 1.0](https://img.shields.io/badge/AppVersion-1.0-informational?style=flat-square)

Helm chart for RespondNow services

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| imrajdas | <rajbabu.das@harness.io> |  |
| sagarkrsd | <sagar.kumar@harness.io> |  |
| ksatchit | <karthik.s@harness.io> |  |

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | mongodb | 15.6.21 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| mongodb.auth.database | string | `"respondnow"` |  |
| mongodb.auth.enabled | bool | `true` |  |
| mongodb.auth.password | string | `"1234"` |  |
| mongodb.auth.rootPassword | string | `"1234"` |  |
| mongodb.auth.username | string | `"root"` |  |
| mongodb.nameOverride | string | `"mongodb"` |  |
| mongodb.persistence.enabled | bool | `true` |  |
| mongodb.persistence.size | string | `"3Gi"` |  |
| mongodb.replicaSet.enabled | bool | `false` |  |
| mongodb.service.port | int | `27017` |  |
| portal.annotations | object | `{}` |  |
| portal.image.pullPolicy | string | `"Always"` |  |
| portal.image.repository | string | `"ghcr.io/respondnow/respondnow-portal"` |  |
| portal.image.tag | string | `"0.1.0"` |  |
| portal.ingress.annotations | object | `{}` |  |
| portal.ingress.enabled | bool | `true` |  |
| portal.ingress.hosts[0].host | string | `"server.example.com"` |  |
| portal.ingress.hosts[0].paths[0] | string | `"/"` |  |
| portal.ingress.tls | list | `[]` |  |
| portal.labels.app | string | `"respondnow-portal"` |  |
| portal.name | string | `"respondnow-portal"` |  |
| portal.nodeSelector | object | `{}` |  |
| portal.probes.livenessProbe.failureThreshold | int | `3` |  |
| portal.probes.livenessProbe.httpGet.path | string | `"/healthz"` |  |
| portal.probes.livenessProbe.httpGet.port | int | `8191` |  |
| portal.probes.livenessProbe.initialDelaySeconds | int | `30` |  |
| portal.probes.livenessProbe.periodSeconds | int | `10` |  |
| portal.probes.livenessProbe.successThreshold | int | `1` |  |
| portal.probes.livenessProbe.timeoutSeconds | int | `5` |  |
| portal.probes.readinessProbe.failureThreshold | int | `3` |  |
| portal.probes.readinessProbe.httpGet.path | string | `"/"` |  |
| portal.probes.readinessProbe.httpGet.port | int | `8191` |  |
| portal.probes.readinessProbe.initialDelaySeconds | int | `15` |  |
| portal.probes.readinessProbe.periodSeconds | int | `5` |  |
| portal.probes.readinessProbe.successThreshold | int | `1` |  |
| portal.probes.readinessProbe.timeoutSeconds | int | `3` |  |
| portal.replicaCount | int | `1` |  |
| portal.resources | object | `{}` |  |
| portal.service.port | int | `8191` |  |
| portal.service.type | string | `"LoadBalancer"` |  |
| server.annotations | object | `{}` |  |
| server.configMap.data.DEFAULT_USER_EMAIL | string | `"admin@respondnow.io"` |  |
| server.configMap.data.DEFAULT_USER_NAME | string | `"Admin"` |  |
| server.configMap.data.DEFAULT_USER_PASSWORD | string | `"respondnow"` |  |
| server.configMap.data.MONGO_DATABASE | string | `"respondnow"` |  |
| server.configMap.data.SLACK_INCIDENT_CHANNEL_ID | string | `""` |  |
| server.image.pullPolicy | string | `"Always"` |  |
| server.image.repository | string | `"ghcr.io/respondnow/respondnow-server"` |  |
| server.image.tag | string | `"0.1.0"` |  |
| server.ingress.annotations | object | `{}` |  |
| server.ingress.enabled | bool | `true` |  |
| server.ingress.hosts[0].host | string | `"server.example.com"` |  |
| server.ingress.hosts[0].paths[0] | string | `"/"` |  |
| server.ingress.tls | list | `[]` |  |
| server.labels.app | string | `"respondnow-server"` |  |
| server.name | string | `"respondnow-server"` |  |
| server.nodeSelector | object | `{}` |  |
| server.probes.livenessProbe.failureThreshold | int | `3` |  |
| server.probes.livenessProbe.httpGet.path | string | `"/status"` |  |
| server.probes.livenessProbe.httpGet.port | int | `8080` |  |
| server.probes.livenessProbe.initialDelaySeconds | int | `30` |  |
| server.probes.livenessProbe.periodSeconds | int | `10` |  |
| server.probes.livenessProbe.successThreshold | int | `1` |  |
| server.probes.livenessProbe.timeoutSeconds | int | `5` |  |
| server.probes.readinessProbe.failureThreshold | int | `3` |  |
| server.probes.readinessProbe.httpGet.path | string | `"/status"` |  |
| server.probes.readinessProbe.httpGet.port | int | `8080` |  |
| server.probes.readinessProbe.initialDelaySeconds | int | `15` |  |
| server.probes.readinessProbe.periodSeconds | int | `5` |  |
| server.probes.readinessProbe.successThreshold | int | `1` |  |
| server.probes.readinessProbe.timeoutSeconds | int | `3` |  |
| server.replicaCount | int | `1` |  |
| server.resources | object | `{}` |  |
| server.secret.data.JWT_SECRET | string | `"3iMkWJA5hD4DA7Nqe3GNOc1GfMtEsHyRiJcQdsxB2mc8JhySOUeBVYNRxfqBtijQ"` |  |
| server.secret.data.MONGO_URI | string | `"mongodb://root:1234@respondnow-mongodb:27017"` |  |
| server.secret.data.SLACK_APP_TOKEN | string | `""` |  |
| server.secret.data.SLACK_BOT_TOKEN | string | `""` |  |
| server.service.port | int | `8080` |  |
| server.service.type | string | `"ClusterIP"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)

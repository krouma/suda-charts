# documentserver

![Version: 7.0.1](https://img.shields.io/badge/Version-7.0.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 7.0.0](https://img.shields.io/badge/AppVersion-7.0.0-informational?style=flat-square)

Helm chart for installing ONLYOFFICE Docs in Kubernetes

**Homepage:** <https://github.com/suda/charts/tree/main/charts/documentserver>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| suda | admin@suda.pl | https://suda.pl |

## Source Code

* <https://github.com/suda/charts/tree/main/charts/documentserver>

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| connections.amqpHost | string | `"rabbitmq"` |  |
| connections.amqpPasswordSecret | string | `""` |  |
| connections.amqpProto | string | `"amqp"` |  |
| connections.amqpUser | string | `"user"` |  |
| connections.dbHost | string | `"postgresql"` |  |
| connections.dbPasswordSecret | string | `""` |  |
| connections.dbPort | string | `"5432"` |  |
| connections.dbUser | string | `"postgres"` |  |
| connections.redisHost | string | `"redis-master"` |  |
| converter.containerImage | string | `"onlyoffice/docs-converter-de:7.0.0.132"` |  |
| converter.replicas | int | `1` |  |
| converter.resources | object | `{}` |  |
| docservice.containerImage | string | `"onlyoffice/docs-docservice-de:7.0.0.132"` |  |
| docservice.livenessProbe.failureThreshold | int | `5` |  |
| docservice.livenessProbe.httpGet.path | string | `"/index.html"` |  |
| docservice.livenessProbe.httpGet.port | int | `8000` |  |
| docservice.livenessProbe.periodSeconds | int | `10` |  |
| docservice.livenessProbe.successThreshold | int | `1` |  |
| docservice.livenessProbe.timeoutSeconds | int | `3` |  |
| docservice.livenessProbeEnabled | bool | `false` |  |
| docservice.readinessProbe.failureThreshold | int | `2` |  |
| docservice.readinessProbe.httpGet.path | string | `"/index.html"` |  |
| docservice.readinessProbe.httpGet.port | int | `8000` |  |
| docservice.readinessProbe.periodSeconds | int | `10` |  |
| docservice.readinessProbe.successThreshold | int | `1` |  |
| docservice.readinessProbe.timeoutSeconds | int | `3` |  |
| docservice.readinessProbeEnabled | bool | `false` |  |
| docservice.replicas | int | `1` |  |
| docservice.resources | object | `{}` |  |
| docservice.startupProbe.failureThreshold | int | `30` |  |
| docservice.startupProbe.httpGet.path | string | `"/index.html"` |  |
| docservice.startupProbe.httpGet.port | int | `8000` |  |
| docservice.startupProbe.periodSeconds | int | `10` |  |
| docservice.startupProbeEnabled | bool | `false` |  |
| example.containerImage | string | `"onlyoffice/docs-example:7.0.0.132"` |  |
| example.enabled | bool | `false` |  |
| grafana_ingress.enabled | bool | `false` |  |
| ingress.enabled | bool | `false` |  |
| ingress.ssl.enabled | bool | `false` |  |
| ingress.ssl.host | string | `"example.com"` |  |
| ingress.ssl.secret | string | `"tls"` |  |
| jwt.enabled | bool | `true` |  |
| jwt.secret | string | `"MYSECRET"` |  |
| metrics.enabled | bool | `false` |  |
| persistence.enabled | bool | `false` |  |
| persistence.size | string | `"8Gi"` |  |
| persistence.storageClass | string | `""` |  |
| product.name | string | `"onlyoffice"` |  |
| proxy.livenessProbe.failureThreshold | int | `3` |  |
| proxy.livenessProbe.httpGet.path | string | `"/index.html"` |  |
| proxy.livenessProbe.httpGet.port | int | `8888` |  |
| proxy.livenessProbe.periodSeconds | int | `10` |  |
| proxy.livenessProbe.successThreshold | int | `1` |  |
| proxy.livenessProbe.timeoutSeconds | int | `3` |  |
| proxy.livenessProbeEnabled | bool | `false` |  |
| proxy.proxyContainerImage | string | `"onlyoffice/docs-proxy-de:7.0.0.132"` |  |
| proxy.resources | object | `{}` |  |
| proxy.startupProbe.failureThreshold | int | `30` |  |
| proxy.startupProbe.httpGet.path | string | `"/index.html"` |  |
| proxy.startupProbe.httpGet.port | int | `8888` |  |
| proxy.startupProbe.periodSeconds | int | `10` |  |
| proxy.startupProbeEnabled | bool | `false` |  |
| service.port | int | `8888` |  |
| service.type | string | `"ClusterIP"` |  |
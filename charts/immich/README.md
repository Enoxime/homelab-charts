# immich

![Version: 0.2.0](https://img.shields.io/badge/Version-0.2.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: v2.4.1](https://img.shields.io/badge/AppVersion-v2.4.1-informational?style=flat-square)

A Helm chart for Kubernetes

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| ai.image.pullPolicy | string | `"IfNotPresent"` |  |
| ai.image.repository | string | `"ghcr.io/immich-app/immich-machine-learning"` |  |
| ai.image.tag | string | `""` |  |
| ai.nodeSelector | object | `{}` |  |
| ai.podSecurityContext | object | `{}` |  |
| ai.replicaCount | int | `1` |  |
| ai.resources | object | `{}` |  |
| ai.runtimeClass.enabled | bool | `false` |  |
| ai.runtimeClass.name | string | `""` |  |
| ai.securityContext | object | `{}` |  |
| ai.service.port | int | `3003` |  |
| ai.service.type | string | `"ClusterIP"` |  |
| ai.tolerations | list | `[]` |  |
| ai.volumeMounts | list | `[]` |  |
| ai.volumes | list | `[]` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| fullnameOverride | string | `""` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"ghcr.io/immich-app/immich-server"` |  |
| image.tag | string | `""` | Overrides the image tag whose default is the chart appVersion. |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | object | `{}` |  |
| ingress.className | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hosts[0].host | string | `"chart-example.local"` |  |
| ingress.hosts[0].paths[0].path | string | `"/"` |  |
| ingress.hosts[0].paths[0].pathType | string | `"Prefix"` |  |
| ingress.tls | list | `[]` |  |
| ipp | object | `{"config":{"allowDownloadAll":1,"downloadOriginalPhoto":true,"enabled":false,"singleImageGallery":false},"enabled":false,"image":{"pullPolicy":"IfNotPresent","repository":"alangrainger/immich-public-proxy","tag":"1.14.2"},"podSecurityContext":{},"publicBaseUrl":{"enabled":false,"url":""},"resources":{},"securityContext":{},"service":{"port":3000,"type":"ClusterIP"},"volumeMounts":[],"volumes":[]}` | Activate immich-public-proxy |
| ipp.publicBaseUrl.url | string | `""` | http(s)?://public-domain.com |
| microservices.nodeSelector | object | `{}` |  |
| microservices.resources | object | `{}` |  |
| microservices.runtimeClass.enabled | bool | `false` |  |
| microservices.runtimeClass.name | string | `""` |  |
| microservices.tolerations | list | `[]` |  |
| microservices.volumeMounts | list | `[]` |  |
| microservices.volumes | list | `[]` |  |
| nameOverride | string | `""` |  |
| nodeSelector | object | `{}` |  |
| persistence.enabled | bool | `false` |  |
| persistence.library.enabled | bool | `false` |  |
| persistence.library.existingClaim.name | string | `""` |  |
| persistence.library.size | string | `"15Gi"` |  |
| persistence.storageClassName | string | `""` |  |
| persistence.upload.enabled | bool | `false` |  |
| persistence.upload.existingClaim.name | string | `""` |  |
| persistence.upload.size | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podLabels | object | `{}` |  |
| podSecurityContext.fsGroup | int | `65532` |  |
| postgresql.databaseName | string | `"immich"` |  |
| postgresql.hostname | string | `"database"` |  |
| postgresql.password.key | string | `""` |  |
| postgresql.password.name | string | `""` |  |
| postgresql.port | int | `5432` |  |
| postgresql.skipMigrations | bool | `false` |  |
| postgresql.sslMode | string | `"disable"` |  |
| postgresql.url | string | `""` |  |
| postgresql.username | string | `"postgres"` |  |
| postgresql.vectorExtension | string | `""` |  |
| redis.hostname | string | `""` |  |
| redis.password.key | string | `""` |  |
| redis.password.name | string | `""` |  |
| redis.port | string | `""` |  |
| redis.socket | string | `""` |  |
| redis.url | string | `""` |  |
| redis.username | string | `""` |  |
| replicaCount | int | `1` | Number of replica. Not tested above 1 |
| resources | object | `{}` |  |
| securityContext | object | `{}` |  |
| server.service.port | int | `2283` |  |
| server.service.type | string | `"ClusterIP"` |  |
| server.trustedProxies | string | `""` |  |
| server.volumeMounts | list | `[]` |  |
| server.volumes | list | `[]` |  |
| serviceAccount.annotations | object | `{}` | Annotations to add to the service account |
| serviceAccount.automount | bool | `true` | Automatically mount a ServiceAccount's API credentials? |
| serviceAccount.create | bool | `false` | Specifies whether a service account should be created |
| serviceAccount.name | string | `""` | The name of the service account to use. If not set and create is true, a name is generated using the fullname template |
| timezone | string | `"*1"` |  |
| tolerations | list | `[]` |  |
| volumeMounts | list | `[]` | Additional volumeMounts on the output Deployment definition. |
| volumes | list | `[]` | Additional volumes on the output Deployment definition. |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.14.2](https://github.com/norwoodj/helm-docs/releases/v1.14.2)

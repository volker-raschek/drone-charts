# drone-charts

[![Build Status](https://drone.cryptic.systems/api/badges/volker.raschek/drone-charts/status.svg)](https://drone.cryptic.systems/volker.raschek/drone-charts)
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/volker-raschek)](https://artifacthub.io/packages/search?repo=volker-raschek)

This is an inofficial helm chart for [drone](https://github.com/drone/drone) and
should replace the official unmainted helm chart
[repository](https://github.com/drone/charts). The official does not support
version `v2` of drone.

This helm chart can be found on [artifacthub.io](https://artifacthub.io/) and
can be installed via helm.

```bash
helm repo add volker.raschek https://charts.cryptic.systems/volker.raschek
helm install drone volker.raschek/drone
```

## Customization

All [configuration options](https://docs.drone.io/server/reference/) can be
defined in the `values.yml` file below the `config` section. Alternatively can
be the options passed via the `--set` flag of the `helm install` command.

| value                                                   | reference                                                                                 |
| ------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| `config.DRONE_BITBUCKET_CLIENT_ID`                      | [Documentation](https://docs.drone.io/server/reference/drone-bitbucket-client-id/)        |
| `config.DRONE_BITBUCKET_CLIENT_SECRET`                  | [Documentation](https://docs.drone.io/server/reference/drone-bitbucket-client-secret/)    |
| `config.DRONE_BITBUCKET_DEBUG`                          | [Documentation](https://docs.drone.io/server/reference/drone-bitbucket-debug)             |
| `config.DRONE_CLEANUP_DEADLINE_PENDING`                 | [Documentation](https://docs.drone.io/server/reference/drone-cleanup-deadline-pending)    |
| `config.DRONE_CLEANUP_DEADLINE_RUNNING`                 | [Documentation](https://docs.drone.io/server/reference/drone-cleanup-deadline-running)    |
| `config.DRONE_CLEANUP_DISABLED`                         | [Documentation](https://docs.drone.io/server/reference/config.drone-cleanup-disabled)     |
| `config.DRONE_CLEANUP_INTERVAL`                         | [Documentation](https://docs.drone.io/server/reference/drone-cleanup-interval)            |
| `config.DRONE_CONVERT_PLUGIN_ENDPOINT`                  | [Documentation](https://docs.drone.io/server/reference/drone-convert-plugin-endpoint)     |
| `config.DRONE_CONVERT_PLUGIN_EXTENSION`                 | [Documentation](https://docs.drone.io/server/reference/drone-convert-plugin-extension )   |
| `config.DRONE_CONVERT_PLUGIN_SECRET`                    | [Documentation](https://docs.drone.io/server/reference/drone-convert-plugin-secret)       |
| `config.DRONE_CONVERT_PLUGIN_SKIP_VERIFY`               | [Documentation](https://docs.drone.io/server/reference/drone-convert-plugin-skip-verify)  |
| `config.DRONE_COOKIE_SECRET`                            | [Documentation](https://docs.drone.io/server/reference/drone-cookie-secret)               |
| `config.DRONE_COOKIE_TIMEOUT`                           | [Documentation](https://docs.drone.io/server/reference/drone-cookie-timeout)              |
| `config.DRONE_CRON_DISABLED`                            | [Documentation](https://docs.drone.io/server/reference/drone-cron-disabled)               |
| `config.DRONE_CRON_INTERVAL`                            | [Documentation](https://docs.drone.io/server/reference/drone-cron-interval)               |
| `config.DRONE_DATABASE_DATASOURCE`                      | [Documentation](https://docs.drone.io/server/reference/drone-database-datasource)         |
| `config.DRONE_DATABASE_DRIVER`                          | [Documentation](https://docs.drone.io/server/reference/drone-database-driver)             |
| `config.DRONE_DATABASE_SECRET`                          | [Documentation](https://docs.drone.io/server/reference/drone-database-secret)             |
| `config.DRONE_GIT_ALWAYS_AUTH`                          | [Documentation](https://docs.drone.io/server/reference/drone-git-always-auth)             |
| `config.DRONE_GIT_PASSWORD`                             | [Documentation](https://docs.drone.io/server/reference/drone-git-password)                |
| `config.DRONE_GIT_USERNAME`                             | [Documentation](https://docs.drone.io/server/reference/drone-git-username)                |
| `config.DRONE_GITEA_CLIENT_ID`                          | [Documentation](https://docs.drone.io/server/reference/drone-gitea-client-id)             |
| `config.DRONE_GITEA_CLIENT_SECRET`                      | [Documentation](https://docs.drone.io/server/reference/drone-gitea-client-secret)         |
| `config.DRONE_GITEA_SERVER`                             | [Documentation](https://docs.drone.io/server/reference/drone-gitea-server)                |
| `config.DRONE_GITEA_SKIP_VERIFY`                        | [Documentation](https://docs.drone.io/server/reference/drone-gitea-skip-verify)           |
| `config.DRONE_GITHUB_CLIENT_SECRET`                     | [Documentation](https://docs.drone.io/server/reference/drone-github-client-secret)        |
| `config.DRONE_GITHUB_SCOPE`                             | [Documentation](https://docs.drone.io/server/reference/drone-github-scope)                |
| `config.DRONE_GITHUB_SERVER`                            | [Documentation](https://docs.drone.io/server/reference/drone-github-server)               |
| `config.DRONE_GITHUB_SKIP_VERIFY`                       | [Documentation](https://docs.drone.io/server/reference/drone-github-skip-verify)          |
| `config.DRONE_GITLAB_CLIENT_ID`                         | [Documentation](https://docs.drone.io/server/reference/drone-gitlab-client-id)            |
| `config.DRONE_GITLAB_CLIENT_SECRET`                     | [Documentation](https://docs.drone.io/server/reference/drone-gitlab-client-secret)        |
| `config.DRONE_GITLAB_SERVER`                            | [Documentation](https://docs.drone.io/server/reference/drone-gitlab-server)               |
| `config.DRONE_GITLAB_SKIP_VERIFY`                       | [Documentation](https://docs.drone.io/server/reference/drone-gitlab-skip-verify)          |
| `config.DRONE_GOGS_SERVER`                              | [Documentation](https://docs.drone.io/server/reference/drone-gogs-server)                 |
| `config.DRONE_GOGS_SKIP_VERIFY`                         | [Documentation](https://docs.drone.io/server/reference/drone-gogs-skip-verify )           |
| `config.DRONE_JSONNET_ENABLED`                          | [Documentation](https://docs.drone.io/server/reference/drone-jsonnet-enabled)             |
| `config.DRONE_LICENSE`                                  | [Documentation](https://docs.drone.io/server/reference/drone-license)                     |
| `config.DRONE_LOGS_COLOR`                               | [Documentation](https://docs.drone.io/server/reference/drone-logs-color)                  |
| `config.DRONE_LOGS_DEBUG`                               | [Documentation](https://docs.drone.io/server/reference/drone-logs-debug)                  |
| `config.DRONE_LOGS_PRETTY`                              | [Documentation](https://docs.drone.io/server/reference/drone-logs-pretty)                 |
| `config.DRONE_LOGS_TRACE`                               | [Documentation](https://docs.drone.io/server/reference/drone-logs-trace )                 |
| `config.DRONE_PROMETHEUS_ANONYMOUS_ACCESS`              | [Documentation](https://docs.drone.io/server/reference/drone-prometheus-anonymous-access) |
| `config.DRONE_REGISTRATION_CLOSED`                      | [Documentation](https://docs.drone.io/server/reference/drone-registration-closed)         |
| `config.DRONE_REPOSITORY_FILTER`                        | [Documentation](https://docs.drone.io/server/reference/drone-repository-filter)           |
| `config.DRONE_RPC_SECRET`                               | [Documentation](https://docs.drone.io/server/reference/drone-rpc-secret)                  |
| `config.DRONE_S3_BUCKET`                                | [Documentation](https://docs.drone.io/server/reference/drone-s3-bucket)                   |
| `config.DRONE_S3_ENDPOINT`                              | [Documentation](https://docs.drone.io/server/reference/drone-s3-endpoint)                 |
| `config.DRONE_S3_PATH_STYLE`                            | [Documentation](https://docs.drone.io/server/reference/drone-s3-path-style)               |
| `config.DRONE_S3_PREFIX`                                | [Documentation](https://docs.drone.io/server/reference/drone-s3-prefix)                   |
| `config.DRONE_SERVER_HOST`                              | [Documentation](https://docs.drone.io/server/reference/drone-server-host)                 |
| `config.DRONE_SERVER_PROTO`                             | [Documentation](https://docs.drone.io/server/reference/drone-server-proto)                |
| `config.DRONE_SERVER_PROXY_HOST`                        | [Documentation](https://docs.drone.io/server/reference/drone-server-proxy-host)           |
| `config.DRONE_SERVER_PROXY_PROTO`                       | [Documentation](https://docs.drone.io/server/reference/drone-server-proxy-proto)          |
| `config.DRONE_STARLARK_ENABLED`                         | [Documentation](https://docs.drone.io/server/reference/drone-starlark-enabled)            |
| `config.DRONE_STASH_CONSUMER_KEY`                       | [Documentation](https://docs.drone.io/server/reference/drone-stash-consumer-key)          |
| `config.DRONE_STASH_PRIVATE_KEY`                        | [Documentation](https://docs.drone.io/server/reference/drone-stash-private-key)           |
| `config.DRONE_STASH_SERVER`                             | [Documentation](https://docs.drone.io/server/reference/drone-stash-server)                |
| `config.DRONE_STASH_SKIP_VERIFY`                        | [Documentation](https://docs.drone.io/server/reference/drone-stash-skip-verify)           |
| `config.DRONE_STATUS_DISABLED`                          | [Documentation](https://docs.drone.io/server/reference/drone-status-disabled  )           |
| `config.DRONE_STATUS_NAME`                              | [Documentation](https://docs.drone.io/server/reference/drone-status-name)                 |
| `config.DRONE_TLS_AUTOCERT`                             | [Documentation](https://docs.drone.io/server/reference/drone-tls-autocert)                |
| `config.DRONE_TLS_CERT`                                 | [Documentation](https://docs.drone.io/server/reference/drone-tls-cert)                    |
| `config.DRONE_TLS_KEY`                                  | [Documentation](https://docs.drone.io/server/reference/drone-tls-key)                     |
| `config.DRONE_USER_CREATE`                              | [Documentation](https://docs.drone.io/server/reference/drone-user-create)                 |
| `config.DRONE_VALIDATE_PLUGIN_ENDPOINT`                 | [Documentation](https://docs.drone.io/server/reference/drone-validate-plugin-endpoint)    |
| `config.DRONE_VALIDATE_PLUGIN_SECRET`                   | [Documentation](https://docs.drone.io/server/reference/drone-validate-plugin-secret)      |
| `config.DRONE_VALIDATE_PLUGIN_SKIP_VERIFY`              | [Documentation](https://docs.drone.io/server/reference/drone-validate-plugin-skip-verify) |
| `config.DRONE_WEBHOOK_ENDPOINT`                         | [Documentation](https://docs.drone.io/server/reference/drone-webhook-endpoint)            |
| `config.DRONE_WEBHOOK_EVENTS`                           | [Documentation](https://docs.drone.io/server/reference/drone-webhook-events)              |
| `config.DRONE_WEBHOOK_SECRET`                           | [Documentation](https://docs.drone.io/server/reference/drone-webhook-secret)              |
| `config.DRONE_WEBHOOK_SKIP_VERIFY`                      | [Documentation](https://docs.drone.io/server/reference/drone-webhook-skip-verify)         |

## Missing features

1. Support postgres, maria and mysql database directly as helm dependency if as
   `DATABASE_DRIVER` an other instead of `sqlite` has been selected.
   Alternatively can be passed a completely custom string to establish a
   database connection, when the database is running outside the cluster.

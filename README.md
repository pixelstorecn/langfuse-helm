Langfuse Kubernetes Helm
==========

Langfuse Kubernetes Helm repository provides ways to install and configure Langfuse in a Kubernetes cluster.
The scripts are written in Helm 3.

# Chart Detailed Configuration

There are required values that you may need set explicitly when deploying Langfuse. You can change it in values.yaml when you need.

| Parameter | Description | Example |
| --------- | ----------- | ------- |
| `configMap.NODE_ENV` | run environment | `development`, `test`, `production` |
| `configMap.DATABASE_URL.USERNAME` | database username | `postgres` |
| `configMap.DATABASE_URL.PASSWORD` | database pasword | `postgres` |
| `configMap.DATABASE_URL.ADDRESS` | database address | `localhost`, etc |
| `configMap.DATABASE_URL.PORT` | database port | `5432` |
| `configMap.DATABASE_URL.DBNAME` | database name | `postgres` |
| `configMap.NEXTAUTH_URL` | redirect url when new user signed up, need to change to your langfuse url or what you need | `http://localhost:3000` |
| `configMap.NEXTAUTH_SECRET` | nextauth secret | `mysecret` |
| `configMap.SALT` | salt for API key hashing | `mysalt` |
| `configMap.TELEMETRY_ENABLED` | telemetry service for Docker deployments | `true`, `false` |
| `configMap.NEXT_PUBLIC_SIGN_UP_DISABLED` | if new user can sign up by themself | `true`, `false` |
| `INGRESS.ENABLE` | set this to true if you need to setup ingress rule for langfuse | `true`, `false` |
| `INGRESS.HOSTS.HOST` | change this value when you set ingress.enable to true | `langfuse.example.com`, etc |

## Install released version using Docker Helm repository (>= 4.3.0)

```shell
helm install langfuse oci://registry-1.docker.io/pixelstorecn/langfuse-helm --version <langfuse vserion you want> -n <namespace> --set fullnameOverride=langfuse 
```
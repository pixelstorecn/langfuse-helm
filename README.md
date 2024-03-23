Langfuse Kubernetes Helm
==========

Langfuse Kubernetes Helm repository provides ways to install and configure Langfuse in a Kubernetes cluster.
The scripts are written in Helm 3.

# Chart Detailed Configuration

There are required values that you may need set explicitly when deploying Langfuse. You can change it in values.yaml when you need.

| name | description | example |
| ---- | ----------- | ------- |
| `NODE_ENV` | run environment | `development`, `test`, `production` |
| `DATABASE_URL.USERNAME` | database username | `postgres` |
| `DATABASE_URL.PASSWORD` | database pasword | `postgres` |
| `DATABASE_URL.ADDRESS` | database address | `localhost`, etc |
| `DATABASE_URL.PORT` | database port | `5432` |
| `DATABASE_URL.DBNAME` | database name | `postgres` |
| `NEXTAUTH_URL` | redirect url when new user signed up, need to change to your langfuse url or what you need | `http://localhost:3000` |
| `NEXTAUTH_SECRET` | nextauth secret | `mysecret` |
| `SALT` | salt for API key hashing | `mysalt` |
| `TELEMETRY_ENABLED` | telemetry service for Docker deployments | `true`, `false` |
| `NEXT_PUBLIC_SIGN_UP_DISABLED` | if new user can sign up by themself | `true`, `false` |
| `LANGFUSE_ENABLE_EXPERIMENTAL_FEATURES` | experimental features switch | `true`, `false` |
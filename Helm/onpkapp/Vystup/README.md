
# Helm Chart for ONPK Application

This Helm chart is designed to deploy the **ONPK Application**, consisting of a frontend and backend microservice along with a MongoDB database.

## Features

- Configurable number of replicas for both frontend and backend services.
- Environment variable support for customizing application behavior.
- Service and Ingress configuration for external access.
- MongoDB integration as a subchart with support for initialization scripts.

## Requirements

- Kubernetes 1.20+
- Helm 3+
- MongoDB Helm chart from [Bitnami](https://github.com/bitnami/charts/tree/main/bitnami/mongodb)

## Values

The chart allows the following values to be configured:

### Frontend

| Key                     | Description                     | Default                      |
|--------------------------|--------------------------------|------------------------------|
| `frontend.replicas`      | Number of frontend replicas    | `1`                          |
| `frontend.env`           | Environment variables          | `[REACT_APP_APIHOSTPORT]`    |
| `frontend.service.type`  | Type of frontend service       | `ClusterIP`                  |
| `frontend.service.port`  | Port for frontend service      | `8080`                       |
| `frontend.ingress.hosts` | Hosts for ingress              | `["onpkapp.mydomain.local"]` |

### Backend

| Key                     | Description                           | Default               |
|--------------------------|--------------------------------------|-----------------------|
| `backend.replicas`       | Number of backend replicas           | `1`                   |
| `backend.env`            | Environment variables                | `[MONGO_CONN_STR      |
                                                                  |   MONGO_AUTH_SOURCE   |
                                                                  |   MONGO_USERNAME      |
                                                                  |   MONGO_PASSWORD]`    |
| `backend.service.type`   | Type of backend service              | `ClusterIP`           |
| `backend.service.port`   | Port for backend service             | `9080`                |

### MongoDB

| Key                     | Description                           | Default               |
|--------------------------|--------------------------------------|-----------------------|
| `mongodb.auth.enabled`   | Enable authentication for MongoDB    | `true`                |
| `mongodb.auth.username`  | MongoDB username                     | `admin`               |
| `mongodb.auth.password`  | MongoDB password                     | `password`            |
| `mongodb.initdb.scripts` | MongoDB initialization scripts       | `[init.js]`           |
## Usage

1. Install the Helm chart:
   
   helm upgrade --install onpkapp . --values values-onpkapp.yaml --wait --namespace onpkapp --create-namespace
   

2. Uninstall the Helm chart:
   
   helm uninstall onpkapp
   

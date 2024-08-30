# RespondNow

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Helm Charts for the RespondNow Application

## Overview

RespondNow is an open-source incident management application. It integrates with MongoDB and Slack to help teams track and respond to incidents efficiently.

## Prerequisites

- Helm 3.x or above
- Kubernetes 1.22+

## Installation

### Step 1: Add the RespondNow Helm Repository

```bash
helm repo add respondnow https://respondnow.github.io/respondnow-helm
helm repo update
```

### Step 2: Install RespondNow

```bash
helm install respondnow respondnow/respondnow \
--namespace=respondnow --create-namespace \
--set server.configMap.data.ENABLE_SLACK_CLIENT=true \
--set server.configMap.data.INCIDENT_CHANNEL_ID="FILL-YOUR-SLACK-INCIDENT-CHANNEL-ID" \
--set server.secret.data.SLACK_APP_TOKEN="FILL-YOUR-SLACK-APP-TOKEN" \
--set server.secret.data.SLACK_BOT_TOKEN="FILL-YOUR-SLACK-BOT-TOKEN"
```

### Step 3: Access the Application

Use the service URL for the respondnow-portal service (modify service type as needed) to access the portal. <br/> Default admin credentials are `admin@respondnow.io` and `respondnow`.

`Alternative`: Port Forwarding
If you prefer, you can access the RespondNow portal via port forwarding:

```bash
kubectl port-forward svc/respondnow-portal 8191:8191 --namespace=respondnow
```

## Uninstallation

```bash
helm uninstall respondnow --namespace=respondnow
```

### License
This project is licensed under the [Apache 2.0 License](https://opensource.org/licenses/Apache-2.0).




# Azure Billing Archival Solution

## Overview
Hot-Cold data tiering to reduce Cosmos DB costs:
- Hot (<=90 days): Cosmos DB
- Cold (>90 days): Azure Blob Storage (JSON)

Transparent routing via Azure Function API gateway.

## Architecture
See `architecture.png`.

## Setup

### 1. Provision infra:
```bash
bash infrastructure/storage-setup.sh
az deployment group create \
  --resource-group myrg \
  --template-file infrastructure/function-app-deploy.bicep# Santhosh-Bolusani
DevOps assignment Symplique Solutions

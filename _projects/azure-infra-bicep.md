---
layout: default
title: Azure Infrastructure with Bicep Project
permalink: /projects/azure-infra-bicep.html
---

# Azure Infrastructure Deployment using Bicep

## 🔍 Project Overview
This project uses **Azure Bicep**, a declarative infrastructure-as-code language, to provision cloud resources on Microsoft Azure. It demonstrates modular deployments and best practices in resource grouping, naming, and reuse.

## 🧰 Tools & Technologies
- **Azure Bicep**
- **Azure CLI**
- **Resource Groups, VMs, VNets, NSGs, Storage Accounts**
- **Visual Studio Code + Bicep Extension**

## 📷 Architecture Diagram
![Azure Architecture](../assets/azure-bicep-diagram-placeholder.png)

## 📁 Repository
- GitHub: [azure-infra-bicep](https://github.com/fernandezdelpeloso/azure-infra-bicep)

## ⚙️ Main Features
- Modular Bicep files for reuse (e.g., `network.bicep`, `vm.bicep`)
- Parameterized deployment using `*.parameters.json`
- Output values for automated chaining
- Role-based access control (RBAC) via ARM bindings

## 🚀 Deployment Instructions
1. Log in to Azure and set subscription:
```bash
az login
az account set --subscription "<Your Subscription Name>"
```
2. Deploy main Bicep file:
```bash
az deployment sub create \
  --location westeurope \
  --template-file main.bicep \
  --parameters main.parameters.json
```

## 🧪 Sample Resources Deployed
- Resource Group: `rg-demo-devops`
- Virtual Network: `vnet-demo`
- Subnets: `web`, `db`
- Linux VM: `vm-devops`
- Storage Account: `storagedemobicep`

## 📦 Bicep Structure Example
```
project-root/
├── main.bicep
├── modules/
│   ├── network.bicep
│   └── vm.bicep
├── parameters/
│   └── main.parameters.json
```

## 🧠 Lessons Learned
- Benefits of modularization for enterprise scaling
- Parameter validation for robust deployments
- Differences in resource scoping (tenant vs subscription vs RG)
- JSON parameter templating for CI/CD integration

## 📌 Next Steps
- Implement CI/CD deployment via GitHub Actions
- Extend modules for Windows-based infrastructure
- Add monitoring with Azure Monitor and Log Analytics

---

**Back to [Home](../index.html)**

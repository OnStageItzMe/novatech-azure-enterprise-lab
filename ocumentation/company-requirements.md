# NovaTech Solutions

## Company Overview

**Company Name:** NovaTech Solutions
**Industry:** Technology and Business Services
**Headquarters:** New York City
**Company Size:** 150 employees
**Cloud Platform:** Microsoft Azure
**Environment:** Cloud-first with Production and Development environments

NovaTech Solutions provides technology and business services to clients. The company is expanding and needs a centralized Azure environment for employee access, applications, storage, security, monitoring, and backup.

## Departments

| Department      | Total Employees | Azure Test Users |
| --------------- | --------------: | ---------------: |
| IT              |              10 |                2 |
| Human Resources |              15 |                2 |
| Finance         |              20 |                2 |
| Sales           |              40 |                2 |
| Marketing       |              25 |                2 |
| Operations      |              40 |                2 |
| **Total**       |         **150** |           **12** |

## Azure Test Users

### IT

* Marcus Reed
* Olivia Chen

### Human Resources

* Sarah Jones
* Daniel Brooks

### Finance

* Michael Brown
* Jasmine Patel

### Sales

* Ashley Davis
* Kevin Wilson

### Marketing

* Emily Carter
* Noah Martinez

### Operations

* Sophia Lewis
* Ethan Robinson

## Entra ID Groups

* `GRP-NovaTech-IT`
* `GRP-NovaTech-HR`
* `GRP-NovaTech-Finance`
* `GRP-NovaTech-Sales`
* `GRP-NovaTech-Marketing`
* `GRP-NovaTech-Operations`
* `GRP-NovaTech-AVD-Users`
* `GRP-NovaTech-Backup-Admins`

## Azure Requirements

NovaTech requires the following Azure services and resources:

### Identity

* Microsoft Entra ID users
* Department security groups
* Role-Based Access Control
* Multi-Factor Authentication

### Networking

* Production VNet
* Development VNet
* Multiple subnets
* Network Security Groups
* VNet peering
* Route tables
* NAT Gateway
* Azure Bastion
* Network Watcher

### Compute

* Windows Server virtual machines
* Linux virtual machines
* Web servers
* Application server
* Database server
* Management server

### Web Infrastructure

* Azure Application Gateway
* Azure Load Balancer
* Public IP address

### Storage

* Azure Storage Account
* Azure Files
* Blob Storage
* Department file shares

### Virtual Desktop

* Azure Virtual Desktop
* Host pool
* Workspace
* Application group
* Session hosts

### Security

* Microsoft Defender for Cloud
* Azure Key Vault
* NSGs
* RBAC
* Resource Locks
* Managed Identities

### Monitoring

* Azure Monitor
* Log Analytics Workspace
* Alerts
* Application Insights

### Backup

* Recovery Services Vault
* Virtual machine backups
* Backup policies
* Restore points

## Resource Groups

### Production

* `rg-novatech-network-prod`
* `rg-novatech-compute-prod`
* `rg-novatech-storage-prod`
* `rg-novatech-monitoring-prod`
* `rg-novatech-backup-prod`

### Development

* `rg-novatech-network-dev`
* `rg-novatech-compute-dev`

## Production Network

**VNet:** `vnet-novatech-prod`
**Address Space:** `10.10.0.0/16`

| Subnet               | Address Range  |
| -------------------- | -------------- |
| `snet-web`           | `10.10.1.0/24` |
| `snet-app`           | `10.10.2.0/24` |
| `snet-database`      | `10.10.3.0/24` |
| `snet-management`    | `10.10.4.0/24` |
| `snet-avd`           | `10.10.5.0/24` |
| `AzureBastionSubnet` | `10.10.6.0/26` |

## Development Network

**VNet:** `vnet-novatech-dev`
**Address Space:** `10.20.0.0/16`

| Subnet         | Address Range  |
| -------------- | -------------- |
| `snet-dev-web` | `10.20.1.0/24` |
| `snet-dev-app` | `10.20.2.0/24` |

## Virtual Machines

* `vm-mgmt-01` — Windows Server
* `vm-web-01` — Ubuntu
* `vm-web-02` — Ubuntu
* `vm-app-01` — Windows Server
* `vm-db-01` — Windows Server
* `avd-sh-01` — Azure Virtual Desktop Session Host
* `avd-sh-02` — Azure Virtual Desktop Session Host

## Storage

**Storage Account:** `stnovatechprod01`

### Azure File Shares

* `company-shared`
* `finance`
* `hr`
* `it`
* `operations`

### Blob Containers

* `documents`
* `logs`
* `images`
* `archive`

## Monitoring

**Log Analytics Workspace:** `law-novatech-prod`

**Application Insights:** `appi-novatech-web`

Example alerts:

* VM CPU above 80%
* VM unavailable
* Low disk space
* Application Gateway unhealthy backend
* Backup failure

## Backup

**Recovery Services Vault:** `rsv-novatech-prod`

Protected workloads:

* `vm-mgmt-01`
* `vm-app-01`
* `vm-db-01`

## Key Vault

**Key Vault:** `kv-novatech-prod`

Example stored secrets:

* Database password
* Application API secret
* Application certificate

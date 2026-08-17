# Storage Account

This folder contains screenshots and documentation for the **Azure Storage** portion of my **Novatech Azure Enterprise Lab**.

## Storage Components

The environment includes:

* Azure Storage Accounts
* Azure Files
* File Shares
* Blob Storage
* Private Endpoints
* Private network access
* Role-Based Access Control (RBAC)
* SMB file sharing
* Storage permissions

## Purpose

The storage environment was created to simulate how a company can securely store and share files across departments.

Azure Files was used to create shared folders that users can access similarly to a traditional network drive.

## Azure Files

Department file shares were created so users could store and access shared company files.

Examples include:

* Human Resources file shares
* Department-specific shared folders
* Shared company storage

Azure Files uses the **SMB protocol**, allowing Windows devices to map the file share as a network drive.

Example:

`\\storageaccount.file.core.windows.net\fileshare`

## Access Control

Access to storage resources is controlled using:

* Microsoft Entra ID
* Azure RBAC
* Storage-specific roles
* Group-based permissions

Users are assigned to groups based on their department, and permissions can be granted to the group instead of managing each user individually.

This makes access easier to manage as the company grows.

## Private Access

Private Endpoints were used to provide storage services with a **private IP address inside the Azure virtual network**.

This allows resources inside the VNet to access the storage account privately instead of relying on public internet access.

Public access can also be restricted to improve security.

## Network Drive Mapping

Azure File Shares can be mapped on Windows systems as network drives.

For example:

`Z:` → Human Resources File Share

This allows employees to access Azure-hosted files through File Explorer similar to an on-premises company file server.

## Security

The storage design focuses on:

* Least privilege access
* Department-based permissions
* Private network connectivity
* Reduced public exposure
* Centralized file storage
* Secure authentication

## Skills Demonstrated

This portion of the project demonstrates hands-on experience with:

* Azure Storage Accounts
* Azure Files
* SMB file sharing
* File share creation
* Network drive mapping
* Microsoft Entra ID integration
* Azure RBAC
* Group-based access control
* Private Endpoints
* Storage networking
* Secure cloud file storage

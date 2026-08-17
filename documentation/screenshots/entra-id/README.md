# Microsoft Entra ID

This folder contains screenshots and documentation for the **Microsoft Entra ID** portion of my **Novatech Azure Enterprise Lab**.

## Identity Components

The environment includes:

* Microsoft Entra ID users
* Security groups
* Department-based groups
* Role-Based Access Control (RBAC)
* Group-based permissions
* Azure resource access
* Identity and access management

## Purpose

Microsoft Entra ID was used to manage employee identities and control access to Azure resources.

Instead of assigning permissions individually to every user, users were organized into groups based on their department or job function.

This makes identity management easier to scale and maintain.

## Users

Employee accounts were created in Microsoft Entra ID to simulate a real company environment.

Each user represents an employee who may need access to resources such as:

* Azure File Shares
* Virtual machines
* Azure Virtual Desktop
* Storage resources
* Department-specific resources

## Groups

Security groups were created to organize users by department.

Examples include:

* Human Resources
* IT
* Finance
* Management

Users can be added or removed from these groups as their job role changes.

## Group-Based Access

Permissions were assigned to groups instead of individual users whenever possible.

For example:

`Sarah Jones → Human Resources Group → HR File Share Access`

This allows administrators to manage access by simply changing group membership.

## Role-Based Access Control

Azure RBAC was used to determine what users and groups are allowed to do with Azure resources.

Examples of permissions include:

* Read resources
* Manage resources
* Access Azure File Shares
* Upload and modify files
* Administer specific Azure services

RBAC helps follow the principle of least privilege by granting users only the permissions required for their job.

## Identity Lifecycle

A typical employee access process in this environment would be:

`Create User → Add User to Department Group → Assign Group Permissions → User Accesses Authorized Resources`

If an employee changes departments, access can be updated by changing their group membership.

If an employee leaves the company, their account can be disabled or removed to prevent further access.

## Security

The identity design focuses on:

* Least privilege
* Centralized identity management
* Group-based access control
* Reduced individual permission assignments
* Easier employee onboarding and offboarding
* Controlled access to Azure resources

## Skills Demonstrated

This portion of the project demonstrates hands-on experience with:

* Microsoft Entra ID
* User account creation
* Security group management
* Group membership
* Azure RBAC
* Identity and access management
* Department-based access control
* Least privilege
* User onboarding and offboarding
* Enterprise identity administration

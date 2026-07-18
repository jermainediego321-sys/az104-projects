# Lab 05 - Monitoring and Backup

## Objective

The purpose of this lab is to understand how Azure monitoring, alerts, Log Analytics, and backup services are used to track resource health, performance, availability, and recovery.

This section forms part of my AZ-104 Microsoft Azure Administrator learning journey.

## Topics Covered

- Azure Monitor
- Metrics
- Activity Logs
- Log Analytics Workspace
- Alerts
- Action Groups
- Recovery Services Vault
- Azure Backup
- Backup Policies
- Resource Health

## Environment

- Azure Free Account
- Azure Portal
- Azure Cloud Shell
- Azure CLI

## Lab Activities

### 1. Azure Monitor

In this section, I explored Azure Monitor to understand how Azure collects and displays monitoring data for resources.

Key areas reviewed:

- Metrics
- Activity Log
- Resource Health
- Alerts
- Diagnostic settings

### 2. Log Analytics Workspace

In this section, I created or reviewed a Log Analytics Workspace and explored how logs can be collected and queried.

Key areas reviewed:

- Workspace overview
- Logs
- Tables
- Basic KQL queries
- Diagnostic settings connection

### 3. Alerts and Action Groups

In this section, I explored how alerts can be created to notify administrators when specific conditions are met.

Examples:

- CPU threshold alert
- Storage account activity alert
- Virtual machine availability alert

Key areas reviewed:

- Alert rules
- Conditions
- Severity levels
- Action groups
- Email notifications

### 4. Recovery Services Vault

In this section, I explored how Recovery Services Vaults are used for backup and recovery.

Key areas reviewed:

- Vault creation
- Backup configuration
- Backup policies
- Retention settings
- Protected items

### 5. Azure Backup

In this section, I reviewed how Azure Backup helps protect Azure resources and supports recovery if data or services are lost.

Key areas reviewed:

- Backup policies
- Backup schedules
- Retention periods
- Restore options
- Backup jobs

## Azure CLI Commands

```bash
# Create a resource group
az group create \
  --name az104-monitoring-rg \
  --location southafricanorth

# Create a Log Analytics Workspace
az monitor log-analytics workspace create \
  --resource-group az104-monitoring-rg \
  --workspace-name az104-law-001 \
  --location southafricanorth

# List Log Analytics Workspaces
az monitor log-analytics workspace list \
  --output table

# Create an Action Group
az monitor action-group create \
  --name az104-actiongroup \
  --resource-group az104-monitoring-rg \
  --short-name az104ag

# View activity logs
az monitor activity-log list \
  --resource-group az104-monitoring-rg \
  --output table
``

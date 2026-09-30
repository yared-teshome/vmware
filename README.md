# VCF PowerCLI Administration Reference

## Purpose

This repository provides a maintained PowerShell command reference for
common VMware vSphere and VMware Cloud Foundation administrative,
inventory, monitoring, and troubleshooting operations using PowerCLI.

The reference is intended for Systems Administrators who need commonly
used PowerCLI commands in a standardized and documented location.

The repository includes commands for:

- vCenter Server connectivity
- Virtual machine inventory
- VM power-state review
- Guest operating system information
- Virtual disks
- VM network configuration
- VM snapshots
- ESXi host inventory
- Cluster inventory
- Resource pools
- Datastore capacity
- CPU and memory performance statistics
- Recent and failed tasks
- VM power operations
- PowerCLI command discovery

## Read-Only vs. Change Operations

Commands are intentionally divided into two categories.

### READ-ONLY

These commands retrieve information without intentionally changing
vSphere configuration or VM power state.

Examples include:

- Get-VM
- Get-VMHost
- Get-Cluster
- Get-Datastore
- Get-HardDisk
- Get-NetworkAdapter
- Get-VMGuest
- Get-Snapshot
- Get-Stat
- Get-Task

### CHANGE

These commands can affect virtual machine state and should be reviewed
before execution.

Examples include:

- Start-VM
- Stop-VMGuest
- Stop-VM
- Restart-VMGuest

Change commands are commented out by default in the reference script.

## Credentials

Credentials must not be stored directly in the repository.

Interactive credential collection should be used when appropriate:

    $Credential = Get-Credential

Credentials, passwords, API tokens, certificates, and other secrets
must not be committed to source control.

## Installation

Current Broadcom documentation refers to the product as VCF PowerCLI.

Example:

    Install-Module -Name VCF.PowerCLI -Scope CurrentUser

Legacy environments may contain VMware.PowerCLI.

Module installation changes the administrator workstation and is
therefore documented separately from read-only vSphere commands.

## Important

Always confirm the target vCenter Server, virtual machine, host,
cluster, datastore, or other infrastructure object before executing
a command that changes state.

This repository is a command reference and does not replace normal
change-management, security, access-control, or operational procedures.

## Version

Initial archived baseline:

v1.0.0

## Maintainer

Systems Administration

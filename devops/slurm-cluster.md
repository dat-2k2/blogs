---
layout: default
title: Slurm Cluster configuration
parent: devops
nav_order: 1
permarlink: /build-a-slurm-cluster-on-virtual-box
---
# Build a Slurm Cluster on Virtual Box

## Prequisitions
- Create a virtual machine on Virtual Box.
- What is a NAT network?
- Create and configure NAT network on Virtual Box.

## Hardware properties
Host:
- Windows 11
- Oracle VirtualBox 7.1.4
Nodes:
- Ubuntu Server 22.04

## Goals
We need to create and configure a cluster with 3 nodes, managed by Slurm Workload Manager.

In a cluster, we want to establish not only connection between nodes but also connection from outside. 
## Create VM machine


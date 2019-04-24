---
layout: layout.pug
title: Creating DC/OS Clusters
navigationTitle: Installing DC/OS
menuWeight: 5
excerpt: Creating and maintaining your DC/OS clusters.
---
# Understanding Clusters and SRE


# Overview of the DC/OS installation process
DC/OS is installed in your environment by using a dynamically generated configuration file. This file is generated by using specific parameters that are set during configuration. This installation file contains a Bash install script and a Docker container that is loaded with everything you need to deploy a customized DC/OS build. The Docker container contains all of the elements for DC/OS so it can be used for offline installation.

The DC/OS installation process requires a cluster of nodes to install DC/OS onto and a single node to run the DC/OS installation from. For fully functional clusters on any infrastructure including on-premise, public or private clouds, follow the On-Prem installation instructions. The On-Prem installation method was previously called Custom installation.

The production installation method is used to install production-ready DC/OS that can be upgraded. Using this method, you can package the DC/OS distribution and connect to every node manually to run the DC/OS installation commands. This installation method is recommended if you want to integrate with an existing system or if you do not have SSH access to your cluster.

The DC/OS installation process requires a bootstrap node, master node, public agent node, and a private agent node. You can view the [nodes](/1.13/overview/concepts/#node) documentation for more information.

# On-Prem Installation

The [On-Prem Installation](/1.13/installing/production/) is used to install production-ready DC/OS for datacenters. This method was previously called custom installation.

## Installing DC/OS
The following steps are required to install DC/OS clusters:

*   Configure bootstrap node
*   Install DC/OS on master node
*   Install DC/OS on agent node

![Production Installation Process](/1.13/img/advanced-installer.png)

Figure 1. The production installation process


This installation method requires that:

*   The bootstrap node must be network accessible from the cluster nodes.
*   The bootstrap node must have the HTTP(S) ports open from the cluster nodes.
# Access DC/OS Configuration File

- For installing DC/OS Enterprise Edition contact your sales representative or <sales@mesosphere.io>. You can access the DC/OS Enterprise configuration file from the [support website](https://support.mesosphere.com/s/downloads) using a [login credential](https://support.mesosphere.com/s/login/). [enterprise type="inline" size="small" /]

- You can download the most recent, stable, open source DC/OS generation configuration file [here](https://downloads.dcos.io/dcos/stable/dcos_generate_config.sh) or find older versions of the file on the [open source project website](https://dcos.io/releases/). [oss type="inline" size="small" /]
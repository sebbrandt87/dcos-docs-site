---
layout: layout.pug
title: Universal Installer
navigationTitle: DC/OS with Universal Installer
menuWeight: 25
excerpt: The Universal Installer terraform modules provide best-practice infrastructure and cluster management.
---
(overview page of the modules, development and notes)

## Introducing the Mesosphere Universal Installer

The Mesosphere Universal Installer is now the supported installation method for DC/OS on AWS, Azure and GCP. The cloud installation guide starts with a short demo to get your first cluster up and running. From there, you can easily start modifying your demo installation into a production cluster - all from the very same setup.


##### Jump to the getting started guide for your cloud provider:

#### [Amazon Web Services](/1.13/installing/evaluation/aws/)

#### [Azure Resource Manager](/1.13/installing/evaluation/azure/)

#### [Google Cloud Platform](/1.13/installing/evaluation/gcp/)


## About the Mesosphere Universal Installer

Use the [Mesosphere Universal Installer](/1.13/installing/evaluation/)  to deploy DC/OS on Amazon Web Services (AWS), Azure Resource Manager (AzureRM), and Google Cloud Platform (GCP). The Mesosphere Universal Installer is built on top of Terraform, an open source infrastructure automation tool which uses templates to manage infrastructure for multiple public cloud providers, service providers, and on-premises solutions. Through the Mesosphere Universal Installer you can quickly and easily create your infrastructure, configures resources, and manage communication between agents. Operations such as scaling a cluster or upgrading to a newer version of DC/OS are now incredibly easy. Getting started templates allow for a quick installation of DC/OS, yet can be expanded into a full production environment including upgrades, without ever taking down your cluster.
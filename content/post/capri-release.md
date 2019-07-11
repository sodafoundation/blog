+++
showonlyimage = true
draft = false
image = "img/default-bg-wide.jpg"
date = "2019-06-17T10:29:23+05:30"
title = "OpenSDS Capri Released"
description = "Capri Release Notes"
writer = "Sanil Kumar D."
categories = [ "Release", "Announcements"]
tags = ["capri"]
# weight = 1
+++

It took a lot of effort but it is finally here! OpenSDS Capri is now released. Loads of new features with current use cases in mind and some experimental features. Check out the full list below.
<!--more-->

This is an incremental stable release after Bali(0.4.0). Basic tests on all features done; encouraged to do integration trials; not yet production ready. [Please contact us for product integration, we are happy to support]


# New Features:

* Telemetry
    * Integrate with Prometheus and Grafana, and collecting metrics from storage backends.
    * Metrics driver for LVM, Ceph, and OceanStor V3/V5.
* Anomaly detection
    * Detect anomalous data points based on metrics collected from Telemetry.
    * Limitations: 
       * Alert generation is not done.
       * E2E testing is not done.
* Automation and orchestration
    * Design orchestration workflow using StackStorm.   
    * Use case includes provisioning storage with hooks to add custom actions.
    * Supported workflows include volume provisioning, bucket migration, and user defined workflows.
* Multi-cloud
    * GCP object store backend
    * IBM Cloud object store backend
    * Signature identification with AK/SK
* Object Lifecycle management
    * Provide object lifecycle management mechanism that allows tenants to manage lifecycle configuration policies through APIs.
    * Support migration between on-premise object storage (Ceph or Fusion Storage) and cloud storage (AWS S3, Azure Blob, GCS, Huawei OBS).
    * Support default OpenSDS storage tiers.  User defined rules is not supported in Capri.
    * Restore for Glacier is not supported.
    * Support non-versioned bucket only in Capri.
* File share support
    * Profiles design based on Swordfish
    * NFS driver, Manila driver
* Volume Drivers
    * NVMeoF driver (support LVM)
    * HPE Nimble driver  
    * Scutech Cloud Migration System (CMS) host-based replication driver
* CSI 1.1.0 support
    * Raw block support
    * Topology support 
    * Multi-attach support
    * NVMe TCP support
    * CSI driver support for shared file systems (through file share APIs)
* Installer
    * Enable multi-dock/multi-node and multi-backend installation with Ansible
    * Helm installation with Ceph
    * Salt installer
* Thin OpenSDS (Experimental, documentation pending, Refer PR #888 and branch thin-opensds)
   * A light-weight OpenSDS to serve Cloud Native environment

# Overall Testing:
* All features tested at module and integration with other  features
* E2E Usecases testing 
* Performance and negative tests are not done much (improving)
* UT (coverage improving)

*Note: Only for integration trials with products. Not yet production ready. If you want to deploy along with product, please contact us, we can help to make it production ready.*

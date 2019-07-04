+++
showonlyimage = false
draft = false
image = ""
date = "2018-12-17T10:29:23+05:30"
title = "OpenSDS Bali Released"
description = "Bali Release Notes"
writer = "Sean McGinnis"
categories = [ "Release", "Announcements"]
tags = ["bali"]
# weight = 1
+++

Wrapping up right on time, the team completed the Bali development cycle last week. This release brings a lot of great new functionality. Really an impressive accomplishment by all involved.
<!--more-->

The Capri release will get underway shortly, but it's a perfect time of the year to take a break and look back at all that was done over the last year.  
Truly impressive!

### Bali Updates

The Bali release adds the following functionality:

* Introduced management of multiple OpenStack deployments
* Expanded the OpenSDS standard RESTful API
* Multi-Cloud support
   - S3 API support with AWS, Azure, Huawei Cloud, and local Ceph object store and Fusion Storage backends.
   - Manual and basic policy based migration for AWS, Azure, Huawei Cloud, Ceph, and Fusion Storage.
* Dashboard UI interface has been broken out into separately installed component and integrated with multicloud support.
* Added ability to upload/download snapshot to/from cloud storage
* Updated support for the Container Storage Interface (CSI) v1.0 specification
   - Added support to create snapshot and create volume from snapshot
   - Added support for NodeStageVolume and NodeUnstageVolume.
* Support to provision replicated volumes using OpenSDS CSI plugin
* CSI plugin refactoring and FC support
* Southbound Fusion Storage and OceanStor V3/V5 volume drivers
* Integrated profiles properties definition and selector filtering.
* Support external volumes for VMs or baremetal.
* Add API support for AvailabilityZone.
* Installation with Helm (tested with LVM)

The OpenSDS controller (Hotpot), the north bound plugins (Sushi), the UI dashboard (opensds-dashboard), the multi-cloud management support, and the installer can be downloaded from here:

[Hotpot](https://github.com/opensds/opensds/releases/tag/v0.4.0)
[Sushi](https://github.com/opensds/nbp/releases/tag/v0.4.0)
[OpenSDS-Dashboard](https://github.com/opensds/opensds-dashboard/releases/tag/v0.4.0)
[Multi-Cloud](https://github.com/opensds/multi-cloud/releases/tag/v0.4.0)
[Installer](https://github.com/opensds/opensds-installer/releases/tag/v0.4.0)

### On to Capri

We are working on finalizing the Capri development cycle schedule now. Expect that to show up on [releases.opensds.io](https://releases.opensds.io/) very soon!

We have a lot of really good plans for Capri shaping up and are excited to see where things go from here.

A huge thank you to everyone that has been involved in the development, support, and feedback that has helped shape OpenSDS so far!

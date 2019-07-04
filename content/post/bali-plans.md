+++
showonlyimage = false
draft = false
image = ""
date = "2018-07-31T10:29:23+05:30"
title = "What's Coming in OpenSDS Bali Release"
description = "Bali Release Plans"
writer = "Xing Yang"
categories = [ "Release", "Announcements"]
tags = ["bali"]
# weight = 1
+++

After wrapping up the Aruba release at the end of June, the OpenSDS development team has started working for the Bali release.
<!--more-->
There are a lot of new features targeted for the Bali release:

* S3 support
* Multi-cloud data engine
* Multi-OpenStack
* Array-based migration
* Host-based migration
* NVMeoF
* Group snapshots and group replication
* Monitoring

S3 support would allow data to be stored in an S3 compatible object store locally, i.e., Ceph.

For the multi-cloud data engine, the team is designing an architecture that provides the ability to migrate data across multiple clouds. This could involve a public cloud such as AWS or Azure or a private cloud.

Multi-OpenStack would allow OpenSDS to manage storage in multiple OpenStack deployments, leveraging Federated Keystone or Shared Keystone.

Array-based and host-based migration support would allow data to be migrated across homogeneous and heterogeneous storage platforms. 

NVMeoF would allow storage managed by OpenSDS to support NVMe over Fabrics.

Basic volume group support was added to the Aruba release. In the Bali release, the plan is to add support for taking a snapshot and doing replication of a group of volumes.

The plan for monitoring is to start with volume metrics reporting through Prometheus integration.

There are a lot to be done. As always, we look for help from the community to accomplish the goal. Please join us if you are interested in OpenSDS and help us make a successful Bali release!

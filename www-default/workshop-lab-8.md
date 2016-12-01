---
layout: lab
title: Explore Cloud Instances
subtitle:
html_title:
categories: [lab, providers, ops]
next: workshop-lab-9.html
previous: workshop-lab-7.html
---


### What Are Cloud Instances?

In Red Hat CloudForms,

### Explore Cloud Instances

> Select Compute → Clouds → Instances.

**[INSERT_IMAGE_HERE]**

A list of your public and private cloud instances appears.

### Explore the Virtual Thumbnail for Cloud Instances

The web interface uses virtual thumbnails to represent providers. Each thumbnail contains four quadrants by default, which display basic information about each provider.

**[INSERT_IMAGE_HERE]**

* The top left quadrant shows the operating system running on the instance.
* The top right quadrant shows status of the instance.
* The image in the bottom left quadrant represents the type of provider the instance is running on (Amazon EC2 or OpenStack).
* The bottom right quadrant shows the number of snapshots for this instance.
*  A <i class="fa fa-shield fa-lg" aria-hidden="true"></i> (**Policy**) in the center indicates that this host has one or more policies applied.

> In the top right corner of the window, click <i class="fa fa-th fa-lg" aria-hidden="true"></i> <i class="fa fa-th-large fa-lg" aria-hidden="true"></i> <i class="fa fa-list fa-lg" aria-hidden="true"></i> to toggle between **Grid**, **Tile**, and **List** views.

**[INSERT_IMAGE_HERE]**

> Click <i class="fa fa-download fa-lg" aria-hidden="true"></i> (**Download**) to download a list of Cloud Instances.

**[INSERT_IMAGE_HERE]**

### Explore Cloud Instance Details

> Click the Instances by Provider accordion.

**[INSERT_IMAGE_HERE]**

> Select any instance and observe the following on the resulting screen.

**[INSERT_IMAGE_HERE]**

1. The Properties section shows detailed information about the instance.
2. The Lifecycle section shows when this instance was discovered, when it was most recently analyzed, and when it is scheduled for retirement.
3. The Relationships section shows the related cloud provider, availability zone, flavor, and drift and analysis histories for this instance.

Click these relationships to review how this instance relates to all of its resources.

> When you have finished looking at the related resources, click  (Back) at the top left—not the browser’s back arrow.

**[INSERT_IMAGE_HERE]**

1. The Compliance section shows whether the instance is compliant with its applied policies.
2. The Power Management section shows the instance’s current power state, most recent boot time, and most recent date that the power state changed.
3. The Security section lists users, groups, and key pairs.
4. The Configuration section lists applications/packages, initialization processes, files, and other operating system configuration-related information.
5. The Diagnostics section shows any running processes and event logs for this instance.
6. The Smart Management section shows tags you can use in policies and other CloudForms functions.

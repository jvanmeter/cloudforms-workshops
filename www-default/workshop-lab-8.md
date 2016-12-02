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

> Select **Compute** → **Clouds** → **Instances**.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-cloud-instances.png" /><br/>
*Cloud Instances*

A list of your public and private cloud instances appears.

### Explore the Virtual Thumbnail for Cloud Instances

The web interface uses virtual thumbnails to represent providers. Each thumbnail contains four quadrants by default, which display basic information about each provider.

<img alt="CloudForms Example Virtual Thumbnail" src="{{ site.baseurl }}/www-default/screenshots/cfme-virt-thumbnail-instances.png"/><br/>
*Example Virtual Thumbnail*

* The top left quadrant shows the operating system running on the instance.
* The top right quadrant shows status of the instance.
* The image in the bottom left quadrant represents the type of provider the instance is running on (Amazon EC2 or OpenStack).
* The bottom right quadrant shows the number of snapshots for this instance.
*  A <i class="fa fa-shield fa-lg" aria-hidden="true"></i> (**Policy**) in the center indicates that this host has one or more policies applied.

> In the top right corner of the window, click <i class="fa fa-th fa-lg" aria-hidden="true"></i> <i class="fa fa-th-large fa-lg" aria-hidden="true"></i> <i class="fa fa-list fa-lg" aria-hidden="true"></i> to toggle between **Grid**, **Tile**, and **List** views.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-grid-title-list-infra-instances.png"/><br/>
*Top Window Navigation*

> Click <i class="fa fa-download fa-lg" aria-hidden="true"></i> (**Download**) to download a list of Cloud Instances.

<img alt="CloudForms Download VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-download-infra-instances.png"/><br/>
*Download Instances*

### Explore Cloud Instance Details

> Click the **Instances by Provider** accordion.

<img alt="CloudForms Dashboard CF41_OpenStack1 VM" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-instances-provider.png"/><br/>
*Provider Accordion*

> Select any instance and observe the following on the resulting screen.

<img alt="CloudForms Dashboard CF41_OpenStack1 VM" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-instances.png"/><br/>
*Instance Provider*

1. The **Properties** section shows detailed information about the instance.
2. The **Lifecycle** section shows when this instance was discovered, when it was most recently analyzed, and when it is scheduled for retirement.
3. The **Relationships** section shows the related cloud provider, availability zone, flavor, and drift and analysis histories for this instance.
  * Click these relationships to review how this instance relates to all of its resources.
4. The **Compliance** section shows whether the instance is compliant with its applied policies.
5. The **Power Management** section shows the instance’s current power state, most recent boot time, and most recent date that the power state changed.
6. The **Security** section lists users, groups, and key pairs.
7. The **Configuration** section lists applications/packages, initialization processes, files, and other operating system configuration-related information.
8. The **Diagnostics** section shows any running processes and event logs for this instance.
9. The **Smart Management** section shows tags you can use in policies and other CloudForms functions.

:information_source: When you have finished looking at the related resources, click <i class="fa fa-caret-left fa-lg" aria-hidden="true"></i> (**Back**) at the top left—not the browser’s back arrow.

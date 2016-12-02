---
layout: lab
title: Explore Cloud Providers
subtitle: Amazon EC2, OpenStack, Microsoft Azure, & Google Compute Engine (GCE)
html_title: Amazon EC2, OpenStack, Microsoft Azure, & Google Compute Engine (GCE)
categories: [lab, providers, ops]
next: workshop-lab-8.html
previous: workshop-lab-6.html
---


### What's A Cloud Provider?

In Red Hat CloudForms, a cloud provider is a computing platform that manages instances and allows building of multi-tenant infrastructure services independent from underlying hypervisors.

### Explore Cloud Providers

> Select **Compute** → **Clouds** → **Providers**.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-cloud-providers.png" /><br/>
*Cloud Providers*

A list of your private and public cloud providers, such as OpenStack and Amazon EC2, appears.

To add Amazon EC2 or Microsoft Azure as a provider, use either <i class="fa fa-cog fa-lg" aria-hidden="true"></i> (**Configuration**) and <i class="fa fa-search fa-lg" aria-hidden="true"></i>
 (**Discover**) or <i class="fa fa-cog fa-lg" aria-hidden="true"></i> (**Configuration**) and <i class="fa fa-plus-circle fa-lg" aria-hidden="true"></i> (Add).

To add OpenStack or Google Compute Engine as a provider, you must use  (Configuration) and (Add).

### Explore the Virtual Thumbnail for Cloud Providers

The web interface uses virtual thumbnails to represent providers. Each thumbnail contains four quadrants by default, which display basic information about each provider.

<img alt="CloudForms Example Virtual Thumbnail" src="{{ site.baseurl }}/www-default/screenshots/cfme-virt-thumbnail-cloud.png"/><br/>
*Example Virtual Thumbnail*

* The top left quadrant shows the number of instances defined in the provider.
* The top right quadrant shows the number of images available in the provider.
* The image in the bottom left quadrant represents the type of provider (only Amazon EC2 or OpenStack are shown).
* The bottom right quadrant shows the status of the provider.
* A <i class="fa fa-shield fa-lg" aria-hidden="true"></i> (**Policy**) in the center indicates that this host has one or more policies applied.

> In the top right corner of the window, click <i class="fa fa-th fa-lg" aria-hidden="true"></i> <i class="fa fa-th-large fa-lg" aria-hidden="true"></i> <i class="fa fa-list fa-lg" aria-hidden="true"></i> to toggle between **Grid**, **Tile**, and **List** views.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-grid-title-list-infra-cloud.png"/><br/>
*Top Window Navigation*

> Click <i class="fa fa-download fa-lg" aria-hidden="true"></i> (**Download**) to download a list of Cloud Proviers.

<img alt="CloudForms Download VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-download-infra-cloud.png"/><br/>
*Download Cloud*

> Select the `Amazon (US West 2)` Amazon EC2 cloud provider.

<img alt="CloudForms Dashboard CF41_OpenStack1 VM" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-cloud.png"/><br/>
*Cloud Dashboard*

> Click the **Relationships** tab and review the kind of information CloudForms gathers from a provider.

<img alt="CloudForms Dashboard CF41_OpenStack1 VM" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-cloud-relation.png"/><br/>
*Cloud Relationships*

:information_source: The screen shows this provider’s relationships with its components, such as availability zones, flavors, security groups, instances, and images.

Return to the list of **Cloud Providers…**  Select the **OpenStack** cloud provider and click the relationships to review the gathered information.

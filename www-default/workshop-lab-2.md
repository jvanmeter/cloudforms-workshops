---
layout: lab
title: Explore Your First Provider
subtitle: Introducing Infrastructure Providers
html_title: Introducing Infrastructure Providers
categories: [lab, providers, ops]
previous: workshop-lab-1.html
next: workshop-lab-3.html
---

### What's a Provider?

In Red Hat CloudForms, an infrastructure provider is a virtual infrastructure environment that you can add to a Red Hat CloudForms appliance to manage and interact with the resources in that environment. This lab describes the different types of infrastructure providers that you can add to Red Hat CloudForms, and how to manage them.

### Explore Infrastructure Providers

> Navigate to Compute → Infrastructure → Providers.

<img alt="CloudForms Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-providers.png" width="600"/><br/>
*Infrastructure Providers*

A list of your datacenter infrastructure providers appears, such as VMware vCenter and Red Hat Enterprise Virtualization.

### Discover New Infrastructure Providers

In very large environments, you can discover new infrastructure providers.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-search" aria-hidden="true"></i> (**Discover**).

<img alt="CloudForms Discover Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-discover-infra-providers.png"/><br/>
*Discover Providers*

Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

<img alt="CloudForms Discover Infrastructure Providers Cancel" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-discover-infra-providers-cancel.png"/><br/>
*Cancel Discovery*

You can also add infrastructure providers, if known.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-plus-circle" aria-hidden="true"></i> (**Add**).

Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

### Explore the Virtual Thumbnail for Infrastructure Providers

The web interface uses virtual thumbnails to represent providers. Each thumbnail contains four quadrants by default, which display basic information about each provider.

> Example CloudForms Virtual Thumbnail.

<img alt="CloudForms Virtual Thumbnail" src="{{ site.baseurl }}/www-default/screenshots/cfme-virt-thumbnail.png"/><br/>
*Virtual Thumbnail*

1. Number of hosts
2. Management system software
3. Currently unused
4. Authentication status

In the Virtual Thumbnail below, note the **[INSERT_IMAGE_HERE]**. This demo is disconnected from the providers, so the exclamation point indicates the status as not connected.

**[INSERT_IMAGE_HERE]**

When connected to providers, such as in a actual deployment, the **[INSERT_IMAGE_HERE]** is replaced with a **[INSERT_IMAGE_HERE]**.

A <i class="fa fa-shield" aria-hidden="true"></i> (**Policy**) in the center of the virtual thumbnail indicates that this provider has one or more policies applied. There are no policies configured in this exercise, so the shield does not appear.

In the top right corner of the window, click **[INSERT_IMAGE_HERE]** to toggle between Grid, Tile, and List views.

Click **[INSERT_IMAGE_HERE]** (**Download**) for a list of providers in TXT, CSV, or PDF formats.

Click any infrastructure provider and observe the following details on the resulting screen:
* The **Properties** section lists the aggregate host resources for the provider.
* CloudForms can communicate with the provider in the **Authentication Status** section.
* The **Relationships** section lists related clusters, hosts, datastores, VMs, and templates for this provider. Click these relationships to see the type of information CloudForms gathers from a provider.
* The **Smart Management** section shows if this provider has any smart tags applied. You learn more about smart tagging later in the lab.

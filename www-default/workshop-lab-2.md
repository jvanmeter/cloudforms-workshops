---
layout: lab
title: Explore Your First Provider
subtitle: Infrastructure Providers
html_title: Infrastructure Providers
categories: [lab, providers, ops]
previous: workshop-lab-1.html
next: workshop-lab-3.html
---

### What's an Infrastructure Provider?

In Red Hat CloudForms, an infrastructure provider is a virtual infrastructure environment that you can add to a Red Hat CloudForms appliance to manage and interact with the resources in that environment.

### Explore Infrastructure Providers

> Select Compute → Infrastructure → Providers.

<img alt="CloudForms Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-providers.png" width="600"/><br/>
*Infrastructure Providers*

A list of your datacenter infrastructure providers appears, such as VMware vCenter and Red Hat Enterprise Virtualization.

### Discover Infrastructure Providers

In very large environments, you can discover new infrastructure providers.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-search" aria-hidden="true"></i> (**Discover**).

<img alt="CloudForms Discover Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-discover-infra-providers.png"/><br/>
*Discover Providers*

:warning: Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

<img alt="CloudForms Discover Infrastructure Providers Cancel" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-discover-infra-providers-cancel.png"/><br/>
*Cancel Discovery*

### Add Infrastructure Providers

You can also add infrastructure providers, if known.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-plus-circle" aria-hidden="true"></i> (**Add**).

<img alt="CloudForms Add Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-add-infra-providers.png"/><br/>
*Add Providers*

Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

<img alt="CloudForms Add Infrastructure Providers Cancel" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-add-infra-providers-cancel.png"/><br/>
*Cancel Add*

### Explore the Virtual Thumbnail for Infrastructure Providers

The web interface uses virtual thumbnails to represent providers. Each thumbnail contains four quadrants by default, which display basic information about each provider.

<img alt="CloudForms Example Virtual Thumbnail" src="{{ site.baseurl }}/www-default/screenshots/cfme-virt-thumbnail.png"/><br/>
*Example Virtual Thumbnail*

1. Number of hosts
2. Management system software
3. Currently unused
4. Authentication status

In the Virtual Thumbnail below, note the <i class="fa fa-exclamation-circle fa-lg" aria-hidden="true"></i>. This demo is disconnected from the providers, so if you ever encounter the exclamation point, it indicates the status as not connected.

<img alt="CloudForms Virtual Thumbnail Disconnected" src="{{ site.baseurl }}/www-default/screenshots/cfme-virt-thumbnail-disconnected.png"/><br/>
*Virtual Thumbnail Disconnected*

When connected to providers, such as in a actual deployment, the <i class="fa fa-exclamation-circle fa-lg" aria-hidden="true"></i> is replaced with a <i class="fa fa-check-circle-o fa-lg" aria-hidden="true"></i>.

A <i class="fa fa-shield fa-lg" aria-hidden="true"></i> (**Policy**) in the center of the virtual thumbnail indicates that this provider has one or more policies applied. There are no policies configured in this exercise, so the shield does not appear.

> In the top right corner of the window, click <i class="fa fa-th" aria-hidden="true"></i> <i class="fa fa-th-large" aria-hidden="true"></i> <i class="fa fa-list" aria-hidden="true"></i> to toggle between **Grid**, **Tile**, and **List** views.

<img alt="CloudForms Top Window Navigation Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-grid-title-list-infra-providers.png"/><br/>
*Top Window Navigation*

> Click <i class="fa fa-download fa-lg" aria-hidden="true"></i> (**Download**) for a list of providers in TXT, CSV, or PDF formats.

 <img alt="CloudForms Download Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-download-infra-providers.png"/><br/>
 *Download Provider*

> Click any infrastructure provider and observe the following details on the resulting screen:

 <img alt="CloudForms Dashboard Infrastructure Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-providers.png"/><br/>
 *Provider Dashboard*

1. The **Properties** section lists the aggregate host resources for the provider.
2. CloudForms can communicate with the provider in the **Authentication Status** section.
3. The **Relationships** section lists related clusters, hosts, datastores, VMs, and templates for this provider.
  * Click these relationships to see the type of information CloudForms gathers from a provider.
4. The **Smart Management** section shows if this provider has any smart tags applied. You learn more about smart tagging later in the lab.

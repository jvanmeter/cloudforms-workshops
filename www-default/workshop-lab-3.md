---
layout: lab
title: Discovering Host Systems
subtitle: Infrastructure Hosts
html_title: Infrastructure Hosts
categories: [lab, providers, ops]
next: workshop-lab-4.html
previous: workshop-lab-2.html
---

### What's An Infrastructure Host?

In Red Hat CloudForms, hosts are hypervisors running on physical hardware providing virtual machines and infrastructure.

The CloudForms Management Engine automatically adds hosts from discovered providers. However, you can also discover hosts directly if not using a provider. Discovering hosts is only supported for standalone VMware ESX servers.

### Explore Infrastructure Hosts

> Select Compute → Infrastructure → Hosts.

<img alt="CloudForms Infrastructure Hosts" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-hosts.png" /><br/>
*Infrastructure Hosts*

A list of your private datacenter infrastructure hosts appears, such as VMware ESXi and Red Hat Enterprise Virtualization managed hosts (Red Hat Enterprise Linux or Red Hat Enterprise Virtualization Hypervisor).

:information_source: You can discover hosts independently from an infrastructure provider, but this is not recommended because you do not see the relationship between hosts and providers.

### Discover Infrastructure Hosts

In very large environments, you can discover new hosts directly.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-search" aria-hidden="true"></i> (**Discover items**).

<img alt="CloudForms Discover Infrastructure Hosts" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-discover-infra-hosts.png"/><br/>
*Discover Items*

Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

<img alt="CloudForms Discover Infrastructure Hosts Cancel" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-discover-infra-hosts-cancel.png"/><br/>
*Cancel Discovery*

### Add Infrastructure Hosts

You can also add infrastructure hosts, if they are known.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-plus-circle fa-lg" aria-hidden="true"></i> (**Add**).

<img alt="CloudForms Add Infrastructure Hosts" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-add-infra-hosts.png"/><br/>
*Add Hosts*

Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

<img alt="CloudForms Add Infrastructure Hosts Cancel" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-add-infra-hosts-cancel.png"/><br/>
*Cancel Add*

### Explore the Virtual Thumbnail for Infrastructure Hosts

The web interface uses virtual thumbnails to represent providers. Each thumbnail contains four quadrants by default, which display basic information about each provider.

<img alt="CloudForms Example Virtual Thumbnail" src="{{ site.baseurl }}/www-default/screenshots/cfme-virt-thumbnail-hosts.png"/><br/>
*Example Virtual Thumbnail*

* The top left quadrant shows the number of VMs running on the host.
* The top right quadrant shows the power state of the host.
* The image in the bottom left quadrant represents the type of host, such as ESXi and Red Hat Enterprise Virtualization.
* The bottom right quadrant shows the status of the host.
* A <i class="fa fa-shield fa-lg" aria-hidden="true"></i> (**Policy**) in the center indicates that this host has one or more policies applied.

> To download the list of hosts, click <i class="fa fa-download fa-lg" aria-hidden="true"></i> (**Download**) next to <i class="fa fa-power-off" aria-hidden="true"></i> (**Power**).

<img alt="CloudForms Download Host Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-download-infra-hosts.png"/><br/>
*Download Host*

> In the top right corner of the window, click <i class="fa fa-th fa-lg" aria-hidden="true"></i> <i class="fa fa-th-large fa-lg" aria-hidden="true"></i> <i class="fa fa-list fa-lg" aria-hidden="true"></i> to toggle between **Grid**, **Tile**, and **List** views.

<img alt="CloudForms Top Window Navigation Host Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-grid-title-list-infra-hosts.png"/><br/>
*Top Window Navigation*

> Select the infrastructure host named `esxi3` with VMware and 20 VMs, and observe the following details on the resulting screen:

<img alt="CloudForms Dashboard ESXI3 Host" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-hosts.png"/><br/>
*Hosts Dashboard*

1. The **Properties** section displays detailed information about the host.
  * Observe these parts of the **Properties** details to see how this host relates to its resources in the provider.
2. The **Compliance** section shows whether the host is compliant with its applied policies.
3. The **Smart Management** section shows that this provider is tagged as existing at a specific location, as well as its provisioning scope.
4. The **Authentication** status section shows whether or not CloudForms can log in to the host.
5. The **Security** section lists users, groups, patches, firewall rules, and other operating system security-related information.
6. The **Configuration** section lists packages, services, and other operating system configuration-related information.

### Explore Host Drift History

> In the Relationships section, click Drift History.

<img alt="CloudForms Dashboard ESXI3 Host Drift Tab" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-infra-hosts-drift-1.png"/><br/>
*Hosts Drift History Tab*

:information_source: The **Relationships** section is an accordion tab nested within the host named `esxi3`.

On the resulting screen, check at least two of the available dates.

> Click <img alt="CloudForms Drift Icon" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-drift-icon.png"/> (**Drift**) above the list of timestamps.

<img alt="CloudForms Dashboard ESXI3 Host Drift Detail" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-infra-hosts-drift-2.png"/><br/>
*Hosts Drift History Detail*

On the next screen, do not uncheck Properties, but check Security and Configuration.

> Click Apply.

<img alt="CloudForms Dashboard ESXI3 Host Drift Section Detail" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-infra-hosts-drift-3.png"/><br/>
*Hosts Drift Section Detail*

If the host changes between the various points in time, it appears here. Can you see what’s changed over time?

Try using the <img alt="CloudForms Drift Icon" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-drift-filter-icon.png"/> (**Filters Buttons**) to see which changes have occurred.

<img alt="CloudForms Dashboard ESXI3 Host Drift Filter Detail" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-infra-hosts-drift-4.png"/><br/>
*Hosts Drift Filter Detail*

:information_source: You will likely need to click the little <i class="fa fa-angle-right fa-lg" aria-hidden="true"></i> mark next to the `Host Properties` section to expand and see the details of what’s changed.

### Explore Infrastructure Host Utilization

> Click `esxi3 (Summary)` to select the host named `esxi3` from the **Drift Analysis** page.

<img alt="CloudForms Dashboard ESXI3" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-esxi3-from-drift.png"/><br/>
*Navigate Hosts Dashboard*

> Click <img alt="CloudForms Monitor Icon" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-monitor-icon.png"/> (**Monitor**) and then select <img alt="CloudForms Utilization Icon" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-utilization-icon.png"/> (**Utilization**).

<img alt="CloudForms Dashboard Hosts Monitor" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-monitor-infra-hosts.png"/><br/>
*Navigate Hosts Monitor Utilization*

> Try changing the **Interval** to **Hourly**.

<img alt="CloudForms Dashboard Monitor Utilization Interval" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-infra-hosts-util-interval.png"/><br/>
*Hosts Monitor Utilization Interval*

Examine the screen that appears, showing a detailed report of CPU, memory, disk I/O, network, and running VMs.

* To see a specific data point, hover over any chart.
* To zoom in on a chart, click <i class="fa fa-search-plus fa-lg" aria-hidden="true"></i> (Zoom In).
* To modify the timeframe displayed in the report, select the date range at the top of the screen.

:warning: The data in this demo is stagnant, so do not go beyond August 7, 2013.

### Explore Infrastructure Host Power State Control

Return to the list of Compute Hosts (eg, click the **Hosts** link in the navigation breadcrumbs at the top of the page).

<img alt="CloudForms Infrastructure Hosts Breadcrumb" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-hosts-breadcrumb.png" /><br/>
*Infrastructure Hosts Breadcrumb*

Check the box next to any host, but do not select the host.

Note that the <img alt="CloudForms Power Icon" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-power-icon.png"/> (**Power**), located above the list of hosts, is now active due to a host being selected.

> Observe the available power states that you can set for this host.

<img alt="CloudForms Infrastructure Hosts  Power States" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-hosts-power-states.png" /><br/>
*Infrastructure Hosts Power States*

:warning: This demo environment is not connected to any real hosts, so changing the power state here does not affect any hosts.

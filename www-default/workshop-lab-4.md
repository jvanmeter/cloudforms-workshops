---
layout: lab
title: Discovering VM Systems
subtitle: Infrastructure VMs
html_title: Infrastructure VMs
categories: [lab, providers, ops]
next: workshop-lab-5.html
previous: workshop-lab-3.html
---

### What's An Infrastructure VM?

In Red Hat CloudForms,

### Explore Infrastructure VMs

> Select Compute → Infrastructure → Virtual Machines.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-vms.png" width="600"/><br/>
*Infrastructure VMs*

A list of your private datacenter’s infrastructure virtual machines appears.

### Explore the Virtual Thumbnail for Infrastructure VMs

The web interface uses virtual thumbnails to represent providers. Each thumbnail contains four quadrants by default, which display basic information about each provider.

<img alt="CloudForms Example Virtual Thumbnail" src="{{ site.baseurl }}/www-default/screenshots/cfme-virt-thumbnail-vms.png"/><br/>
*Example Virtual Thumbnail*

* The top left quadrant shows the operating system running on the VM.
* The top right quadrant shows the status of the VM.
* The image in the bottom left quadrant represents the type of host the VM is running on, such as ESXi or Red Hat Enterprise Virtualization.
* The bottom right quadrant shows the number of snapshots of this VM.
* A <i class="fa fa-shield fa-lg" aria-hidden="true"></i> (**Policy**) in the center indicates that this host has one or more policies applied.

> In the top right corner of the window, click <i class="fa fa-th fa-lg" aria-hidden="true"></i> <i class="fa fa-th-large fa-lg" aria-hidden="true"></i> <i class="fa fa-list fa-lg" aria-hidden="true"></i> to toggle between **Grid**, **Tile**, and **List** views.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-grid-title-list-infra-vms.png"/><br/>
*Top Window Navigation*

> Click <i class="fa fa-download fa-lg" aria-hidden="true"></i> (**Download**) to download a list of VMs.

<img alt="CloudForms Download VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-download-infra-vm.png"/><br/>
*Download VM*

> Select the VM named `CF41_OpenStack1`, and examine the following details:

<img alt="CloudForms Dashboard CF41_OpenStack1 VM" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-vms.png"/><br/>
*VMs Dashboard*

1. The **Properties** section shows detailed information about the VM.
2. The **Lifecycle** section shows when this VM was discovered, when it was most recently analyzed, and when it is scheduled for retirement.
3. The **Relationships** section shows the related infrastructure provider, cluster, host, datastore, resource pool, parent VM, and drift and analysis histories for this VM.
4. The **Normal Operating Ranges** section shows the VM’s average CPU and memory utilization.
5. The **Compliance** section shows whether the VM is compliant with its applied policies.
6. The **Power Management** section shows the VM’s current power state, last boot time, and date of its most recent change in power state.
7. The **Security** section lists users, groups, patches, firewall rules, and other operating system security-related information.
8. The **Configuration** section lists applications/packages, services, and other operating system configuration information.
9. The **Datastore Allocation** section shows the number of virtual disks in this VM—if the disks are aligned and if it is thin-provisioned—as well as the amount of space allocated.
10. The **Datastore Actual Usage Summary** section shows how much actual disk space the VM is using.
11. The **Diagnostics** section shows running processes and event logs for the VM.
12. The **Smart Management** section shows that this host is tagged as existing at a specific location, as well as other tags that you can use in policies and other functions within CloudForms.

> Click **Users** (under the **Security** section) to see a detailed list of user information.

<img alt="CloudForms Dashboard CF41_OpenStack1 VM" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-vms-users.png"/><br/>
*VMs Dashboard Users*

> Click **Packages** (under the **Configuration** section) to view details of packages installed on this VM.

<img alt="CloudForms Dashboard CF41_OpenStack1 VM" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-infra-vms-packages.png"/><br/>
*VMs Dashboard Packages*

### Explore Infrastructure VM Utilization

We will continue using the `CF41_OpenStack1` VM.  If needed, find it by returning to the list of all VMs  (eg, Compute → Infrastructure → Virtual Machines → VMs → All VMs).

**[INSERT_IMAGE_HERE]**

> Click <img alt="CloudForms Monitor Icon" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-monitor-icon.png"/> (**Monitor**) and then select <img alt="CloudForms Utilization Icon" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-utilization-icon.png"/> (**Utilization**).

**[INSERT_IMAGE_HERE]**

> Try changing the **Interval** to **Daily**.

**[INSERT_IMAGE_HERE]**

Examine the screen that appears, showing a detailed report of CPU, memory, disk I/O, and network.
* To see a specific data point, hover over any chart.
* To zoom in on a chart, click  (Zoom In) in the lower left corner of the chart.
* To modify the timeframe displayed in the report, select the date range at the top of the screen.

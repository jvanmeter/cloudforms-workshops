---
layout: lab
title: Discovering Hosts
subtitle: Introducing Infrastructure Hosts
html_title: Introducing Infrastructure Hosts
categories: [lab, providers, ops]
previous: workshop-lab-2.html
---

### Viewing Infrastructure Hosts

> Select Compute → Infrastructure → Hosts.

**[INSERT_IMAGE_HERE]**
*Infrastructure Hosts*

A list of your private datacenter infrastructure hosts appears, such as VMware ESXi and Red Hat Enterprise Virtualization managed hosts (Red Hat Enterprise Linux or Red Hat Enterprise Virtualization Hypervisor).

:information_source: You can discover hosts independently from an infrastructure provider, but this is not recommended because you do not see the relationship between hosts and providers.

In very large environments, you can discover new hosts directly.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-search" aria-hidden="true"></i> (**Discover**).

**[INSERT_IMAGE_HERE]**
*Discover Items*

Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

**[INSERT_IMAGE_HERE]**

You can also add infrastructure hosts, if they are known.

> Click <i class="fa fa-cog" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-plus-circle" aria-hidden="true"></i> (**Add**).

**[INSERT_IMAGE_HERE]**

Review the data entry screen, but do not enter any information.

>  Click **Cancel** to return to the previous screen.

**[INSERT_IMAGE_HERE]**

Explore the **Virtual Thumbnail** for the infrastructure hosts.

**[INSERT_IMAGE_HERE]**

All infrastructure hosts have a four-quadrant Virtual Thumbnail.
* The top left quadrant shows the number of VMs running on the host.
* The top right quadrant shows the power state of the host.
* The image in the bottom left quadrant represents the type of host, such as ESXi and Red Hat Enterprise Virtualization.
* The bottom right quadrant shows the status of the host.
* A <i class="fa fa-shield" aria-hidden="true"></i> (**Policy**) in the center indicates that this host has one or more policies applied.

To download the list of hosts, click <i class="fa fa-download" aria-hidden="true"></i> (**Download**) next to <i class="fa fa-power-off" aria-hidden="true"></i> (**Power**).

In the top right corner of the window, click <i class="fa fa-th fa-lg" aria-hidden="true"></i> <i class="fa fa-th-large fa-lg" aria-hidden="true"></i> <i class="fa fa-list fa-lg" aria-hidden="true"></i> to toggle between **Grid**, **Tile**, and **List** views.

Click <i class="fa fa-download fa-lg" aria-hidden="true"></i> (**Download**) to download a list of hosts.

Select the infrastructure host named `esxi3` with VMware and 20 VMs, and observe the following details on the resulting screen:

**[INSERT_IMAGE_HERE]**

1. The **Properties** section displays detailed information about the host.
2. Observe these parts of the **Properties** details to see how this host relates to its resources in the provider:
  * The **Compliance** section shows whether the host is compliant with its applied policies.
  * The **Smart Management** section shows that this provider is tagged as existing at a specific location, as well as its provisioning scope.
  * The **Authentication** status section shows whether or not CloudForms can log in to the host.
3. The **Security** section lists users, groups, patches, firewall rules, and other operating system security-related information.
4. The **Configuration** section lists packages, services, and other operating system configuration-related information.

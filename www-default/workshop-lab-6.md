---
layout: lab
title: Examine Infrastructure Provisioning
subtitle:
html_title:
categories: [lab, providers, ops]
next: workshop-lab-7.html
previous: workshop-lab-5.html
---

### What's Infrastructure Provisioning?

In Red Hat CloudForms, when a virtual machine or cloud instance is provisioned, it goes through multiple phases. First, the request must be made. The request includes ownership information, tags, virtual hardware requirements, the operating system, and any customization of the request. Second, the request must go through an approval phase, either automatic or manual. Finally, the request is executed.

Execution consists of pre-processing and post-processing. Pre-processing acquires IP addresses for the user, creates VMDB instances, and creates the virtual machine based on information in the request. Post-processing activates the VMDB instance.

<img alt="CloudForms Discover Infrastructure Hosts" src="{{ site.baseurl }}/www-default/screenshots/cfme-provision-vm-workflow.png"/><br/>
*Provision VM Workflow*

### Examine Infrastructure Provisioning

> Select **Compute** → **Infrastructure** → **Virtual Machines**.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-vms.png" /><br/>
*Infrastructure VMs*

On the left, in the **VMs** accordion, select **All VMs & Templates**.

On the right, click <img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-lifecycle-icon.png" /> (**Lifecycle**).

> Select <i class="fa fa-plus-circle fa-lg" aria-hidden="true"></i> (Provision VMs), and observe the following.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-compute-infra-vms-all-lifecycle.png" /><br/>
*Provision VMs*

You are provided with a list of templates.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-provision-vm-1.png" /><br/>
*Template List*

The **Provider** column shows some templates are from Red Hat Enterprise Virtualization Manager and others are from VMware.

> Select any template and click **Continue**.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-provision-vm-2.png" /><br/>
*Template Continue*

On the resulting page, perform the step indicated below for each tab and look at the data requested.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-provision-vm-3.png" /><br/>
*Provision Virtual Machines*

* In the **Request** tab, fill out all the fields.
* In the **Catalog** tab, set the VM Name.
* In the **Environment** tab, check **Choose Automatically**.
* In the **Network** tab, choose a **vLan**.
* Click **Submit**.

:warning: Because you are working in a lab environment, nothing happens after these steps.

On the resulting screen, observe that your provision request appears in a list. If you are in an environment with real infrastructure, you can monitor this area for the status of the VM build.

<img alt="CloudForms Infrastructure VMs" src="{{ site.baseurl }}/www-default/screenshots/cfme-provision-vm-4.png" /><br/>
*Provision Request*

:information_source: You can also arrive at this screen by clicking **Services** → **Requests**.

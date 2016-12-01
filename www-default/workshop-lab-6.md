---
layout: lab
title: Examine Infrastructure Provisioning
subtitle:
html_title:
categories: [lab, providers, ops]
previous: workshop-lab-5.html
---

### What's Infrastructure Provisioning?

In Red Hat CloudForms, when a virtual machine or cloud instance is provisioned, it goes through multiple phases. First, the request must be made. The request includes ownership information, tags, virtual hardware requirements, the operating system, and any customization of the request. Second, the request must go through an approval phase, either automatic or manual. Finally, the request is executed.

Execution consists of pre-processing and post-processing. Pre-processing acquires IP addresses for the user, creates VMDB instances, and creates the virtual machine based on information in the request. Post-processing activates the VMDB instance.

<img alt="CloudForms Discover Infrastructure Hosts" src="{{ site.baseurl }}/www-default/screenshots/cfme-provision-vm-workflow.png"/><br/>
*Provision VM Workflow*

---
layout: lab
title: Explore Chargeback
subtitle: Calculate VM Charges
html_title: Calculate VM Charges
categories: [lab, providers, ops]
next: workshop-lab-13.html
previous: workshop-lab-11.html
---

### What Is Chargeback?

In Red Hat CloudForms, the chargeback feature of CloudForms Management Engine (CFME) allows you to calculate monetary virtual machine charges based on owner or company tag.

### Explore Chargeback

> Select **Cloud Intel** → **Chargeback**.

<img alt="CloudForms Chargeback" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback.png"/><br/>
*Chargeback*

#### Explore Reports

> Select the **Reports** accordion.

<img alt="CloudForms Chargeback Reports" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-reports.png"/><br/>
*Chargeback Reports*

> Select **Saved Chargeback Reports** → **Chargeback (Admin)**

<img alt="CloudForms Chargeback Reports Admin" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-reports-admin.png"/><br/>
*Chargeback (Admin)*

Select any of the reports shown and note how each instance is charged by resources consumed.

### Explore Rates

> Select the **Rates** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-rates.png"/><br/>
*Chargeback Rates*

> Select **Rates** → **Compute** → **Default**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-rates-compute-default.png"/><br/>
*Chargeback Compute Default*

Observe how rates are assigned to each resource.

> Click <i class="fa fa-cog fa-lg" aria-hidden="true"></i> (**Configuration**) and select <i class="fa fa-files-o" aria-hidden="true"></i> (**Copy this Chargeback Rate**).

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-rates-compute-default-copy.png"/><br/>
*Chargeback Compute Copy*

Edit this chargeback rate, note the possible settings, and then click **Cancel** to discard your changes.

Repeat steps for **Rates** → **Storage** → **Default**.

### Explore Assignments

> Select the **Assignments** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-assignments.png"/><br/>
*Chargeback Assignments*

> Select **Assignments** → **Compute**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-assignments-compute.png"/><br/>
*Chargeback Assignments Compute*

Observe that the computed rate assignments are configured for the entire enterprise using the default rates from the previous accordion.

> Select **Assignments** → **Storage**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-chargeback-assignments-storage.png"/><br/>
*Chargeback Assignments Storage*

Observe that the computed rate assignments are configured for the entire enterprise using the default rates from the previous accordion.

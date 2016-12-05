---
layout: lab
title: Examine Policies
subtitle:
html_title:
categories: [lab, providers, ops]
next: workshop-lab-16.html
previous: workshop-lab-14.html
---

### What Are Policies?

In Red Hat CloudForms, Policy profiles are groupings of policies that you can apply to entities within CloudForms. Compliance policies check for a certain state in a host or VM. Control policies control a host or VM depending on certain criteria.

### Examine Policies

> Select **Control** → **Explorer**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-control-explorer.png"/><br/>
*Control Explorer*

> Select the **Policy Profiles** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-policy-profile-accordion.png"/><br/>
*Policy Profile Accordion*

> Select **All Policy Profiles** → **Linux Compliance Check** → **VM and Instance Compliance: Shell-Shock Vulnerability** → **Vulnerable bash Package (ShellShock)**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-shell-shock.png"/><br/>
*Shell-Shock Vulnerability*

On the right, observe the Expression used for this policy.

### Explore Events

> Select the **Events** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-events-accordion.png"/><br/>
*Events Accordion*

> Select **All Events** → **Container Image Discovered**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-container-image-discovered.png"/><br/>
*Container Image Discovered*

Observe that the imported policy shows up as assigned.

### Explore Conditions

> Select the **Conditions** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-conditions-accordion.png"/><br/>
*Conditions Accordion*

> Select **All Conditions** → **All VM and Instance Conditions** → **Vulnerable bash Package (ShellShock)**

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-conditions-shellshock.png"/><br/>
*Conditions ShellShock*

Examine the **Expression**.

### Explore Actions

> Select the **Actions** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-actions-accordion.png"/><br/>
*Actions Accordion*

> Select **All Actions** → **Send Email to Security Team**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-actions-send-email.png"/><br/>
*Send Email*

Observe what this action does and the policies to which it is assigned.

Examine other actions and results.

### Explore Alerts

> Select the **Alerts** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-alerts-accordion.png"/><br/>
*Alerts Accordion*

> Select **All Alerts** → **VM Memory was decreased**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-alerts-vm-decrease.png"/><br/>
*VM Memory Alerts*

Review the **Hardware Reconfigured Parameters** section to see what this alert monitors.

### Explore Alert Profiles

> Select the **Alert Profiles** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-alert-profile.png"/><br/>
*Alerts Profile Accordion*

> Select **All Alert Profiles** → **VM and Instance Alert Profiles**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-alert-profile-vm-instance.png"/><br/>
*All VM and Instance Alert Profiles*

Add an alert profile:

1. Click  (Configuration) → Add a New VM and Instance Alert Profile.
2. Enter VM Memory Decrease for Description.
3. In Alert Selection, select VM Memory was decreased and click .
4. Click Add.

**[INSERT_IMAGE_HERE]**

You cannot assign an alert directly to an entity; you must put alerts into an alert profile as you did here.

:information_source: An alert profile can contain many alerts or just one.

Assign your alert profile:

1. Select the new alert profile you just created.
2. Click  (Configuration) → Edit assignments for this Alert Profile.
3. Choose Selected Cluster/Deployment Roles for Assign To.
4. Check the Raleigh box.
5. Click Save.

**[INSERT_IMAGE_HERE]**

You have now assigned this alert to any VM in the Raleigh cluster.

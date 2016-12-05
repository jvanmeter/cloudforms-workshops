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

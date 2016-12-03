---
layout: lab
title: Explore Alerts
subtitle:
html_title:
categories: [lab, providers, ops]
next: workshop-lab-20.html
previous: workshop-lab-18.html
---
### What Are Alerts?

### Explore Alerts

> Select Control → Explorer.

**[INSERT_IMAGE_HERE]**

> Select the Alerts accordion.

**[INSERT_IMAGE_HERE]**

> Select All Alerts → VM Memory was decreased.

**[INSERT_IMAGE_HERE]**

Review the Hardware Reconfigured Parameters section to see what this alert monitors.

### Explore Alert Profiles

> Select the Alert Profiles accordion.

**[INSERT_IMAGE_HERE]**

> Select All Alert Profiles → VM and Instance Alert Profiles.

**[INSERT_IMAGE_HERE]**

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

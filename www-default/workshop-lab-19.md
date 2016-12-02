---
layout: lab
title: Explore Alerts
subtitle:
html_title:
categories: [lab, providers, ops]
next: workshop-lab-20.html
previous: workshop-lab-18.html
---

Select Control → Explorer.
Select the Alerts accordion.
Select All Alerts → VM Memory was decreased.
Review the Hardware Reconfigured Parameters section to see what this alert monitors.
Select the Alert Profiles accordion.
Select All Alert Profiles → VM and Instance Alert Profiles.
Add an alert profile:
Click  (Configuration) → Add a New VM and Instance Alert Profile.
Enter VM Memory Decrease for Description.
In Alert Selection, select VM Memory was decreased and click .
Click Add.
You cannot assign an alert directly to an entity; you must put alerts into an alert profile as you did here.
An alert profile can contain many alerts or just one.
Assign your alert profile:
Select the new alert profile you just created.
Click  (Configuration) → Edit assignments for this Alert Profile.
Choose Selected Cluster/Deployment Roles for Assign To.
Check the Raleigh box.
Click Save.
You have now assigned this alert to any VM in the Raleigh cluster.

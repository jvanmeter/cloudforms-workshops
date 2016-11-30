---
layout: lab
title: A Guided Tour of CloudForms
subtitle: Welcome to CloudForms
html_title: Welcome to CloudForms
categories: [lab, intro, welcome, developers, ops]
next: workshop-lab-2.html
previous: workshop-lab-0.html
---

### Welcome to CloudForms
This lab provides a quick tour of the console to help you get familiar with the user interface along with some key terminology we will use in subsequent lab content.  If you are already familiar with the basics of CloudForms you can skip this lab — after making sure you can login.

### Key Terms
We will be using the following terms throughout the workshop labs so here are some basic definitions you should be familiar with.  And you'll learn more terms along the way, but these are the basics to get you started.

* Container - Your software wrapped in a complete filesystem containing everything it needs to run
* Image - We are talking about Docker images; read-only and used to create containers

### Accessing CloudForms
CloudForms provides a web console that allow you to perform various tasks via a web browser. Let's get started by logging into this and checking the status of the platform.

### Let's Login

In this section, you log in to the CloudForms Management Engine web interface.

> Navigate to the URI provided by your instructor and login with the user/password provided (if there's an icon on the Desktop, just double click that).

<!-- ### Credentials

| User | Password | Description |
| ------ | ------------ | ----------- |
| admin | smartvm | CloudForms Management Console |
| clouduser | Redhat1! |  CloudForms Management Console |
| cloudops | Redhat1! |  CloudForms Management Console | -->

:information_source: Accept any warnings regarding the SSL certificate.

<img alt="CloudForms Console Login" src="{{ site.baseurl }}/www-default/screenshots/cfme-login.png" width="600"/><br/>
*Login Webpage*

Once logged in you should see the **Cloud Intelligence** dashboard. This customized dashboard shows four (or more) widgets.

<img alt="CloudForms Cloud Intelligence Dashboard" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-cloud-intel.png" width="600"/><br/>
*Cloud Intel Dashboard*

### Explore Cloud Intel Dashboard

Go ahead and explore the data in each of the widgets:
- Vendor and Guest OS Chart
- Guest OS Information
- Virtual Infrastructure Platforms
- CloudForms Status

Feel free to zoom in, download, open in a new window, minimize, and then minimize it in the dashboard (you also can remove the data from the dashboard, but do not do this now).

To return to this screen, select Cloud Intel → Dashboard.

Lastly, experiment with dragging widgets to tailor the view.

### Summary
You should now be ready to get hands-on with our workshop labs.

---
layout: lab
title: Examine Catalog Provisioning
subtitle:
html_title:
categories: [lab, providers, ops]
next: workshop-lab-11.html
previous: workshop-lab-9.html
---

:warning: The following is run as a customer (not admin) account.

### Explore Catalog Configuration

> Select **Services** → **Catalogs**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-services-catalog.png"/><br/>
*Services Catalog*

> On the right, select the catalog item called **Deploy Ticket Monster on VMware**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-ticket-monster.png"/><br/>
*Ticket Monster*

> Click **Order** to order the service.

Enter values for **DBName** and **App Server Name** and click **Submit**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-ticket-monster-submit.png"/><br/>
*Ticket Monster Submit*

:information_source: The request is submitted in a similar way to provisioning as admin, but with fewer choices.

### Verify Catalog Configuration

Log out of the `consumer` account and log in to the `admin` account.

> Select **Services** → **Requests**.

**[INSERT_IMAGE_HERE]**

Click the request you just made.

:information_source: On the request screen, review the request that was just generated.  In this demo environment, the system does not actually build, so continue to the next section.

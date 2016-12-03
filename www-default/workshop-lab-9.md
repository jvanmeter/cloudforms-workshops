---
layout: lab
title: Add New Role, Group, & User
subtitle: Access Control
html_title: Access Control
categories: [lab, providers, ops]
next: workshop-lab-10.html
previous: workshop-lab-8.html
---

### Explore Access Control

> Go to **Settings** → **Configuration** and select the **Access Control** accordion.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-settings-configuration-1.png"/><br/>
*Configuration Dashboard*

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-dashboard-settings-configuration-2.png"/><br/>
*Access Control*

Add a role by modifying a copy of an existing role:

> Select **Roles** → `EvmRole-user`.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-evmrole-role.png"/><br/>
*EvmRole-user Role*

> Click <i class="fa fa-cog fa-lg" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-files-o fa-lg" aria-hidden="true"></i> (**Copy**).

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-evmrole-role-copy.png"/><br/>
*EvmRole-user Copy Role*

1. For Name, enter `Consumer1-Role`.
2. On the right, expand **Services** → **Catalogs Explorer** → **Service Catalogs**.
3. Check the **Modify** box and click **Add**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-evmrole-user-role-add.png"/><br/>
*EvmRole-user Add Role*

Add a group:

1. Select **Groups**.
2. Click <i class="fa fa-cog fa-lg" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-plus-circle fa-lg" aria-hidden="true"></i> (**Add**).
3. For **Description**, enter `Consumer1-Group`.
4. For **Role**, select `Consumer-Role`.
5. For **Project/Tenant**, select `Red Hat`.
6. Click **Add**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-add-group.png"/><br/>
*Add Group*

Add a user:

1. Select Users.
2. Click <i class="fa fa-cog fa-lg" aria-hidden="true"></i> (**Configuration**), then click <i class="fa fa-plus-circle fa-lg" aria-hidden="true"></i> (**Add**).
  * Fill out the resulting form with `consumer` as the username and a password of your choosing.
3. Select **Consumer-Group** for Group and click Add.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-add-user.png"/><br/>
*Add User*

### Account Verification
> In the top right corner, click `Administrator | EVM` and select Logout.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-logout.png"/><br/>
*Logout*

:information_source: Instead of logging in and out of the `admin` account to do this, you can open a new browser or a "private" or "incognito" window in the same browser.

1. Log in to CloudForms as the consumer user with the password you set.
2. Observe that the default dashboard is different from the administrator dashboard.
3. This dashboard has a different set of widgets and fewer selections in the left bar (**Cloud Intelligence**, **Services**, **Compute**, and **Settings**).
4. Explore the data provided.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-test-user.png"/><br/>
*Customer-Group User*

:information_source: This data is more specific and targeted to end users.

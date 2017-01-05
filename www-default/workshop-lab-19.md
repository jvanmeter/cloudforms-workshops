---
layout: lab
title: “Hello, World!” Automation Script
subtitle: Writing and Running Our Own Automation Scripts
html_title: Writing and Running Our Own Automation Scripts
categories: [lab, script, automation, ops]
next: workshop-finally.html
previous: workshop-lab-18.html
---

Let’s jump right in and start writing our first automation script. In time-honored fashion we’ll write “Hello, World!” to the Automate Engine logfile.

Before we do anything, we need to ensure that the Automation Engine server role is selected on our CloudForms appliance. We do this from the **Configure** → **Configuration** menu, selecting the CloudForms server in the Settings accordion.

:information_source: The Automation Engine server role is now enabled by default in CloudForms 4.0, but it’s still worthwhile to check that this role is set on our CloudForms appliance.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-settings-configure-automation-engine.png"/><br/>
*Setting the Automation Engine server role*

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingOne">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
          The Automation Engine Role
        </a>
      </div>
    </div>
    <div id="collapseOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingOne">
      <div class="panel-body">
        Setting the Automation Engine role is necessary to be able to run <i>queued</i> Automate tasks. Automate actions initiated directly from the WebUI—such as running instances from Simulation, or processing methods to populate dynamic dialogs—are run on the WebUI appliance itself, regardless of whether it has the Automation Engine role enabled. <br/><br/>
      </div>
    </div>
  </div>
</div>

### Creating the Environment

Before we create our first automation script, we need to put some things in place. We’ll begin by adding a new domain called _ACME_. We’ll add all of our automation code into this new domain.

> Goto **Automate** → **Explorer**, then **<i class="fa fa-cog fa-lg" aria-hidden="true"></i> Configuration** → **<i class="fa fa-plus-circle fa-lg" aria-hidden="true"></i> Add a New Domain**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-domain.png"/><br/>
*Adding a new domain*

We’ll give the domain the name **ACME**, give it the description **ACME Corp.**, and ensure that the Enabled checkbox is selected.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-domain-acme.png"/><br/>
*ACME Domain*

### Adding a Namespace

Now we’ll add a namespace into this domain, called **General**. Highlight the ACME domain icon in the sidebar, and click **Configuration** → **Add a New Namespace**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-domain-namespace.png"/><br/>
*Adding a new namespace*

Give the namespace the name **General** and the description **General Content**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-domain-namespace-general.png"/><br/>
*General namespace*

### Adding a Class

Now we’ll add a new class, called _Methods_.

:information_source: Naming a class Methods may seem somewhat confusing, but many of the generic classes in the ManageIQ and RedHat domains in the Automate Datastore are called Methods to signify their general-purpose nature.

Highlight the General domain icon in the sidebar, and click **Configuration** → **Add a New Class**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-namespace-class.png"/><br/>
*Adding a new class*

Give the class the name **Methods** and the description **General Instances and Methods**. We’ll leave the display name empty for this example.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-namespace-class-methods.png"/><br/>
*Methods class*

### Editing the Schema

Now we’ll create a simple schema. Click the Schema tab for the _Methods_ class, and click **Configuration** → **Edit selected Schema**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-schema.png"/><br/>
*Editing the schema*

Click New Field, and add a single field with name **execute**, type **Method**, and data type **String**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-schema-field.png"/><br/>
*Adding a new schema field*

Click the checkmark in the lefthand column to save the field entry, and click the **Save** button to save the schema. We now have our generic class definition called _Methods_ set up, with a simple schema that executes a single method.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-schema-field-save.png"/><br/>
*Save schema field*

### Hello, World!

Our first Automate method is very simple; we’ll write an entry to the _automation.log_ file using this two-line script:

```
$evm.log(:info, "Hello, World!")
exit MIQ_OK
```
### Adding a New Instance

First we need to create an instance from our class. In the Instances tab of the new _Methods_ class, select **Configuration** → **Add a New Instance**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-instance.png"/><br/>
*Adding a new instance to our class*

We’ll call the instance **HelloWorld**, and it’ll run (execute) a method called _hello_world_.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-instance-helloworld.png"/><br/>
*Entering the instance details*

Click the **Add** button.

### Adding a New Method

In the Methods tab of the new _Methods_ class, select **Configuration** → **Add a New Method**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-method.png"/><br/>
*Adding a new method to our class*

Name the method **hello_world**, and paste our two lines of code into the Data window.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-add-new-method-helloworld.png"/><br/>
*Entering the method details*

Click **Validate** and then **Add**.

:information_source: Get into the habit of using the Validate button; it can save you a lot of time catching Ruby syntactical typos when you develop more complex scripts.

### Running the Instance

We’ll run our new instance using the _Simulation_ functionality of Automate, but before we do that, log in to CloudForms again from another browser or a private browsing tab, and navigate to **Automate** → **Log**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-log.png"/><br/>
*Automate log file*

:information_source: The CloudForms WebUI uses browser session cookies, so if we want two or more concurrent login sessions (particularly as different users), it helps to use different web browsers or private/incognito windows.

Alternatively, ssh into the CloudForms appliance as root and enter:
```
tail -f /var/www/miq/vmdb/log/automation.log
```

In the simulation, we actually run an instance called Call_Instance in the _/System/Request/_ namespace of the _ManageIQ_ domain, and this in turn calls our _HelloWorld_
instance using the namespace, class, and instance attribute/value pairs that we pass to it.

From the **Automate** → **Simulation** menu, complete the details.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-simulation-helloworld.png"/><br/>
*Completing the Simulation details*

Click **Submit**.

If all went well, we should see our “Hello, World!” message appear in the _automation.log_ file:

```
Invoking [inline] method [/ACME/General/Methods/hello_world] with inputs [{}]
<AEMethod [/ACME/General/Methods/hello_world]> Starting
<AEMethod hello_world> Hello, World!
<AEMethod [/ACME/General/Methods/hello_world]> Ending
Method exited with rc=MIQ_OK
```

Success!

### Exit Status Codes

In our example we used an exit status code of MIQ_OK . Although with simple methods such as this we don’t strictly need to specify an exit code, it’s good practice to do so. When we build more advanced multimethod classes and state machines, an exit code can signal an error condition to the Automation Engine so that action can be taken.

There are four exit codes that we can use:

```
MIQ_OK (0)
  Continues normal processing. This is logged to automation.log as:
  Method exited with rc=MIQ_OK
MIQ_WARN(4)
  Warning message, continues processing. This is logged to automation.log as:
  Method exited with rc=MIQ_WARN
MIQ_ERROR / MIQ_STOP (8)
  Stops processing current object. This is logged to automation.log as:
  Stopping instantiation because [Method exited with rc=MIQ_STOP]
MIQ_ABORT (16)
  Aborts entire automation instantiation. This is logged to automation.log as:
  Aborting instantiation because [Method exited with rc=MIQ_ABORT]
```

:information_source: The difference between `MIQ_STOP` and `MIQ_ABORT` is subtle but comes into play as we develop more advanced Automate workflows.

`MIQ_STOP` stops the currently running instance, but if this instance was called via a reference from another “parent” instance, the subsequent steps in the parent instance would still complete.

`MIQ_ABORT` stops the currently running instance and any parent instance that called it, thereby terminating the Automate task altogether.

### Summary

In this exercise we’ve seen how simple it is to create our own domain, namespace, class, instance, and method, and run our script from Simulation. These are the fundamental techniques that we use for all of automation scripts!

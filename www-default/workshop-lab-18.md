---
layout: lab
title: Introduction to the Automate Datastore
subtitle: Key Terminology for Writing Our Own Automation Script
html_title: Key Terminology for Writing Our Own Automation Script
categories: [lab, script, automation, ops]
next: workshop-lab-19.html
previous: workshop-lab-17.html
---

### What Is CloudForms Automate?

When we use the Automate capability of CloudForms, we write scripts in the Ruby language and use objects that the CloudForms Automation Engine makes available to us.

### Explore Automate

> Go to **Automate** → **Explorer**.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate.png"/><br/>
*Automate Navigation*

The first menu item that we see takes us to the Explorer. This is our visual interface into the Automate Datastore, and it contains the various kinds of Automate objects that we’ll use throughout this lab.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-explorer.png"/><br/>
*Automate Explorer*

Before we start our journey into learning CloudForms Automate, we’ll take a tour of the Automate Datastore to familiarize ourselves with the objects that we’ll find there.

### The Automate Datastore

The Automate Datastore has a directory-like structure, consisting of several types of organizational units arranged in a hierarchy:

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-datastore.png"/><br/>
*Automate Datastore*

Next, we’ll look at each type of object in more detail.

### Domains

A _domain_ is a collection of namespaces, classes, instances, and methods. The ManageIQ project provides a single _ManageIQ_ domain for all supplied automation code, while Red Hat adds the supplemental RedHat domain containing added-value code for the CloudForms product. Both the _ManageIQ_ and _RedHat_ domains are locked, indicating their read-only nature, but we can create new domains for our own custom automation code.

:information_source: Organizing our own code into custom domains greatly simplifies the task of exporting and importing code (simplifying code portability and reuse). It also leaves ManageIQ or Red Hat free to update the locked domains through minor releases without fear of overwriting our customizations.

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingOne">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
          Domain Priority
        </a>
      </div>
    </div>
    <div id="collapseOne" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingOne">
      <div class="panel-body">
        User-added domains can be individually enabled or disabled and can be ordered by priority such that if code exists in the same path in multiple domains (for example, /Cloud/VM/Provisioning/StateMachines), the code in the highest-priority enabled domain will be executed. We can change the priority order of our user-added domains using the

        <blockquote>
          <b>Configuration</b> → <b>Edit Priority Order of Domains</b> menu
        </blockquote>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-datastore-conf-priority.png"/><br/>
        <i>Edit priority</i><br/><br/>

        <blockquote>
          Try using the up and down arrows to switch the priority of a domain, then save.
        </blockquote>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-datastore-conf-priority-save.png"/><br/>
        <i>Save priority</i>
      </div>
    </div>
  </div>
</div>


<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingTwo">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo" aria-expanded="true" aria-controls="collapseTwo">
          Importing/Exporting Domains
        </a>
      </div>
    </div>
    <div id="collapseTwo" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingTwo">
      <div class="panel-body">

        We can export domains using rake from the command line and import them either using rake or from the WebUI. (Using rake enables us to specify more import and export options) A typical rake import line is as follows:

        <blockquote>
          $ bin/rake evm:automate:import YAML_FILE=bit63.yaml IMPORT_AS=Bit63 \
                                       SYSTEM=false ENABLED=true DOMAIN=Export PREVIEW=false
        </blockquote>
      </div>
    </div>
  </div>
</div>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingThree">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseThree" aria-expanded="true" aria-controls="collapseThree">
          Copying Objects Between Domains
        </a>
      </div>
    </div>
    <div id="collapseThree" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingThree">
      <div class="panel-body">
        We frequently need to customize code in the locked RedHat or ManageIQ domains — for example, when implementing our own custom VM placement method. Fortunately, we can easily copy any object from the locked domains into our own, using
        <blockquote>
          <b>Configuration</b> → <b>Copy this...</b>
        </blockquote>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-copy-object.png"/><br/>
        <i>Copying a class</i><br/><br/>

        When we copy an object such as a class, we are prompted for the From and To domains. We can optionally deselect “Copy to same path” and specify our own destination path for the object.<br/><br/>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-copy-object-class.png"/><br/>
        <i>Specifying the destination domain and path</i>
      </div>
    </div>
  </div>
</div>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingFour">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFour" aria-expanded="true" aria-controls="collapseFour">
          Importing Old Format Exports
        </a>
      </div>
    </div>
    <div id="collapseFour" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFour">
      <div class="panel-body">
        Domains were a new feature of the Automate Datastore in CloudForms 3.1. Prior to this release, all factory-supplied and user-created automation code was contained in a common structure, which made updates difficult when any user-added code was introduced (the user-supplied modifications needed exporting and reimporting/merging whenever an automation update was released). <br/><br/>

        To import a Datastore backup from a CloudForms 3.0 and prior format Datastore, we must convert it to the new Datastore format first, like so:

        <blockquote>
          $ cd /var/www/miq/vmdb <br/>
          $ bin/rake evm:automate:convert FILE=database.xml DOMAIN=SAMPLE \
                                          ZIP_FILE=/tmp/sample_converted.zip
        </blockquote>
      </div>
    </div>
  </div>
</div>

### Namespaces

A _namespace_ is a folder-like container for classes, instances, and methods, and is used purely for organizational purposes. We create namespaces to arrange our code logically, and namespaces often contain other namespaces.

<img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-namespaces.png"/><br/>
*Namespaces*

### Classes

A _class_ is similar to a template: it contains a generic definition for a set of automation operations. Each class has a _schema_ that defines the variables, states, relationships, or methods that instances of the class will use.

:information_source: The Automate Datastore uses object-oriented terminology for these objects. A _class_ is a generic definition for a set of automation
operations, and these classes are _instantiated_ as specific instances. The classes that we work with in the Automate Datastore are not the same as Ruby classes that we work with in our automation scripts.

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingFive">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseFive" aria-expanded="true" aria-controls="collapseFive">
          Schemas
        </a>
      </div>
    </div>
    <div id="collapseFive" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingFive">
      <div class="panel-body">
        A <i>schema</i> is made up of a number of elements, or <i>fields</i>, that describe the properties of the class. A schema often has just one entry—to run a single method—but in many cases it has several components. The following shows the schema for a <i>placement</i> class, which has several different field types.<br/><br/>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-schemas.png"/><br/>
        <i>A more complex schema</i>
      </div>
    </div>
  </div>
</div>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingSix">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseSix" aria-expanded="true" aria-controls="collapseSix">
          Adding or Editing a Schema
        </a>
      </div>
    </div>
    <div id="collapseSix" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingSix">
      <div class="panel-body">
        <blockquote>
          Go to <b><i class="fa fa-cog fa-lg" aria-hidden="true"></i> Configuration</b> → <b><i class="fa fa-pencil fa-lg" aria-hidden="true"></i> Edit selected schema</b>.
        </blockquote>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-schemas-edit.png"/><br/>
        <i>Edit selected schema</i><br/><br/>

        We add or edit each schema field in the schema editor by specifying the field type from a drop-down list.<br/><br/>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-schemas-edit-field.png"/><br/>
        <i>Edit field</i><br/><br/>

        Each field type has an associated data type, which is also selectable from a drop-down list.<br/><br/>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-schemas-edit-field-type.png"/><br/>
        <i>Edit field type</i><br/><br/>

        We can define default values for fields in a class schema. These will be inherited by all instances created from the class but can be optionally overridden in the schema of any particular instance.
      </div>
    </div>
  </div>
</div>

<div class="panel-group" id="accordion" role="tablist" aria-multiselectable="true">
  <div class="panel panel-default">
    <div class="panel-heading" role="tab" id="headingSeven">
      <div class="panel-title">
        <a role="button" data-toggle="collapse" data-parent="#accordion" href="#collapseSeven" aria-expanded="true" aria-controls="collapseSeven">
          Relationships
        </a>
      </div>
    </div>
    <div id="collapseSeven" class="panel-collapse collapse" role="tabpanel" aria-labelledby="headingSeven">
      <div class="panel-body">
        One of the schema field types is a <i>relationship</i>, which links to other instances elsewhere in the Automate Datastore. We often use relationships as a way of chaining instances together, and relationship values can accept variable substitutions for flexibility.<br/><br/>

        <img alt="CloudForms Top Window Navigation VM Providers" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-schemas-field-type-relationship.png"/><br/>
        <i>Relationship fields showing variable substitutions</i>
      </div>
    </div>
  </div>
</div>

### Instances

An _instance_ is a specific _instantiation_ or “clone” of the generic class and is the entity run by the Automation Engine. An instance contains a copy of the class schema but with actual values of the fields filled in.

<img alt="" src="{{ site.baseurl }}/www-default/screenshots/cfme-nav-automate-instances.png"/><br/>
*Single class definition with three instances*

### Methods

A _method_ is a self-contained block of Ruby code that gets executed when we run any automation operation. A typical method looks like this:

```
#
# Description: This method checks to see if the VM has been powered off or suspended.
#

# Get vm from root object
vm = $evm.root['vm']

if vm
  power_state = vm.attributes['power_state']
  ems = vm.ext_management_system
  $evm.log('info', "VM:<#{vm.name}> on provider:<#{ems.try(:name)} has Power \
           State:<#{power_state}>")

  # If VM is powered off or suspended exit
  if %w(off suspended).include?(power_state)
    # Bump State
    $evm.root['ae_result']         = 'ok'
  elsif power_state == "never"
    # If never then this VM is a template so exit the retirement state machine
    $evm.root['ae_result']         = 'error'
  else
    $evm.root['ae_result']         = 'retry'
    $evm.root['ae_retry_interval'] = '60.seconds'
  end
end
```

Methods can have one of three _location_ values: _inline_, _built-in_, or _URI_. In practice most of the methods that we create are inline methods, which means they run as a separate Ruby process outside of Rails.

### Summary

In this lab exercise we’ve learned about the fundamental objects or organizational units that we work with in the Automate Datastore: domains, namespaces, classes, instances, and methods.

We are now ready to use this information to write our first automation script!

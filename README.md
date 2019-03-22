## What is this?

The Private Data System is very important in the ClusterApps realm of idea. This is the playbook that uses all of the roles in to deploy a complete system. You will be able to pick and choose the software deployments and identity management. 

## How to use this

* Download this repo
* Copy inventory/hosts.example to inventory/hosts
* Copy secrets.example.yml to secrets.yml
* Update the group_vars as needed
* Run the site.yml playbook for a complete system 
* Run playbooks/install-name.yml for deploying a specific service.

## Dependencies

There are a lot of dependancies. It is best to use galaxy to insure you have all of the requirements.

`ansible-galaxy install -r requirements.yml -p roles`

## Major Role Variables

Each role has serveral variables that will allow you to deploy for your environment. Review each role you plan to deploy for specific details. 

When running this playbook from the command line, rename the ./inventory/hosts.example to ./inventory/hosts. Configure the variables for your environment. 

When running from AWX or Tower, use inventories and groups to define variables. Review the inventory folder for group lvel variables.


## Things to keep in mind.

The majority of the systems will be deployed to CentOS to keep compatibility with Red Hat Enterprise Linux. Some applications, like Evergreen ILS,  were developed to run on Debian based systems. Where possible, applications were deployed to CentOS. BookStack is an example of a package that most instructions only focus on Ubuntu, but for RHEL comaptibility is has been deployed to CentOS. 

As RHEL8 become availible, the systems will be redeployed here. Future deployments will see most of these applications moved to containers. The containers will be able to be deployed to almost any Kubernetes or OpenShift PaaS. 

## More Information

A complete set of manuals and guides is avalible at [ClusterApps](https://clusterapps.com) 

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.

Pull requests are also very welcome. The best way to submit a PR is by first creating a fork of this project, then creating a topic branch for the suggested change and pushing that branch to your own fork. Git can then easily create a PR based on that branch. Don't forget to add your name to the contributor list below!


## Contributors
- [Michael Cleary](https://clusterapps.com)

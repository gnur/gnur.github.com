---
layout: post
title: "Fix puppet enterprise 3.2 installation on ubuntu 12.04.4"
description: "A short how to for fixing the failing installation on Ubuntu 12.04 (.4)"
category:
tags: ["puppet", "puppet enterprise", "ubuntu", "fix"]
---
{% include JB/setup %}

# Fix puppet enterprise 3.2 installation on ubuntu 12.04

While trying to setup a clean Puppet Enterprise installation on Ubuntu 12.04 I came across the error:

    Error: No such file or directory - /opt/puppet/share/puppet/modules/firewall/spec/acceptance/nodesets/default.yml

After a quick search I found [this article](https://tickets.puppetlabs.com/browse/ENTERPRISE-88) on the subject with a hint of how to fix it.

Fixing it turned out to be really simple:

- Do a uninstall _./puppet-enterprise-uninstaller -p_ (I am not sure wether this is 100% needed, but I like to start over before I retry something)
- Go to the [firewall page](https://forge.puppetlabs.com/puppetlabs/firewall) on the Puppet labs forge
- Copy the _Download as a .tar.gz_ url
- On the machine you are trying to install Puppet Enterprise, cd to the modules directory that you extracted from the tarbal
- wget the url you just copied (currently: https://forgeapi.puppetlabs.com/v3/files/puppetlabs-firewall-1.0.2.tar.gz)
- Do a __rm -rf puppetlabs-firewall-1.0.0.tar.gz__
- Restart the installation

# bosh-dev-env

Everything needed for a local bosh development environment.  
This can be operated in one of two modes.

1. A BOSH director in a local Virtualbox with NAT only networking
2. A BOSH director in Virtualbox bridged to the LAN

There is two example settings.yml files in this repo.

This repo compliments [bosh-deployment](https://github.com/cloudfoundry/bosh-deployment) to make it easier to have a local bosh development environment.  

## TL;DR

``` bash
git clone git@github.com:cloudfoundry/bosh-deployment.git ~/src/bosh-deployment
git clone git@github.com:aussielunix/bosh-dev-env.git ~/workspace/bosh/bosh-dev-env
cd ~/workspace/bosh/bosh-dev-env
direnv allow
vim vbox/settings.yml # tune based on one of two examples
boshdev up
# Follow post up messages
```

## Tutorial

I have published a [tutorial](http://aussie.lunix.com.au/tutorial/bosh/bosh_localdev/) that walks you through getting a local bosh development environment complete with installing virtualbox, bosh cli, deploying a bosh director and a vagrant like workflow.



<table>
  <tr>
    <th>Author</th><td>Mick Pollard (aussielunix at g mail dot com)</td>
  </tr>
  <tr>
    <th>Copyright</th><td>Copyright (c) 2018 by Mick Pollard</td>
  </tr>
  <tr>
    <th>License</th><td>Distributed under the MIT License, see <a href="https://github.com/aussielunix/bosh-dev-env/blob/master/LICENSE">LICENSE</a></td>
  </tr>
  <tr>
    <th>twitter </th><td>@aussielunix</td>
  </tr>
</table>

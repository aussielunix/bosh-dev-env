# bosh-dev-env

Bootstrap a BOSH development environment in Virtualbox.  
At the end of this you will have a BOSH director, UAA and Credhub.

This can be operated in one of two modes.

1. A BOSH director in a local Virtualbox with NAT only networking
2. A BOSH director in Virtualbox bridged to the LAN

There is two example settings.yml files in this repo.


## TL;DR

``` bash
git clone git@github.com:cloudfoundry/bosh-deployment.git ~/src/bosh-deployment
git clone git@github.com:aussielunix/bosh-dev-env.git ~/workspace/bosh/bosh-dev-env
cd ~/workspace/bosh/bosh-dev-env
vim .envrc #tune based on example
direnv allow
vim config/settings.yml # tune based on one of two examples
boshdev up
# Follow post up messages
```

<table>
  <tr>
    <th>Author</th><td>Mick Pollard (aussielunix at g mail dot com)</td>
  </tr>
  <tr>
    <th>Copyright</th><td>Copyright (c) 2019 by Mick Pollard</td>
  </tr>
  <tr>
    <th>License</th><td>Distributed under the MIT License, see <a href="https://github.com/aussielunix/bosh-dev-env/blob/master/LICENSE">LICENSE</a></td>
  </tr>
  <tr>
    <th>twitter </th><td>@aussielunix</td>
  </tr>
</table>

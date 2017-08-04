# bosh-dev-env

Everything needed for a local bosh development environment.  

This repo compliments [bosh-deployment](https://github.com/cloudfoundry/bosh-deployment) to make it easier to have a local bosh development environment.  

## TL;DR

``` bash
git clone git@github.com:cloudfoundry/bosh-deployment.git ~/src/bosh-deployment
git clone git@github.com:aussielunix/bosh-dev-env.git ~/workspace/bosh/bosh-dev-env
cd ~/workspace/bosh/bosh-dev-env
direnv allow (optional)
boshdev up
bosh -e 192.168.50.6 --ca-cert <(bosh int ${BOSHLITE_MINE}/vbox/creds.yml --path /director_ssl/ca) alias-env vbox
bosh -e vbox login
bosh -e vbox us artifacts/bosh-warden-boshlite-ubuntu-trusty-go_agent.tar.gz
bosh -e vbox ur artifacts/garden-runc-release.tar.gz
bosh -e vbox ur artifacts/concourse.tar.gz
bosh -e vbox deploy -d concourse concourseci/manifest.yml
```

## Tutorial

I have published a [tutorial](http://aussie.lunix.com.au/tutorial/bosh/bosh_localdev/) that walks you through getting a local bosh development environment complete with installing virtualbox, bosh cli, deploying a bosh director, Concourse CI and vagrant like workflow.



<table>
  <tr>
    <th>Author</th><td>Mick Pollard (aussielunix at g mail dot com)</td>
  </tr>
  <tr>
    <th>Copyright</th><td>Copyright (c) 2017 by Mick Pollard</td>
  </tr>
  <tr>
    <th>License</th><td>Distributed under the MIT License, see <a href="https://github.com/aussielunix/bosh-dev-env/blob/master/LICENSE">LICENSE</a></td>
  </tr>
  <tr>
    <th>twitter </th><td>@aussielunix</td>
  </tr>
</table>

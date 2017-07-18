## Deploy ConcourseCI with bosh

This assumes you already have a bosh director [deployed locally with virtualbox](http://www.starkandwayne.com/blog/bosh-lite-on-virtualbox-with-bosh2/) and the default [cloud-config](https://github.com/cloudfoundry/bosh-deployment/blob/master/warden/cloud-config.yml) loaded.  

* upload stemcell
  ```
  bosh -e vbox upload-stemcell --version=latest https://bosh.io/d/stemcells/bosh-warden-boshlite-ubuntu-trusty-go_agent
  bosh -e vbox stemcells
  ```
* upload latest concourse release
  ```
  bosh -e vbox ur --version=latest --name=concourse https://bosh.io/d/github.com/concourse/concourse
  ```

* upload latest garden-runc release
  ```
  bosh -e vbox ur --version=latest --name=garden-runc https://bosh.io/d/github.com/cloudfoundry/garden-runc-release
  ```
* check you now have two releases uploaded to the bosh director
  ```
  bosh -e vbox releases
  ```
* Tune the deployment manifest (optional)
* Deploy ConcourseCI
  ```
  bosh -e vbox -d concourse deploy manifest.yml
  ```
* Check it deployed the various VMs ok
  ```
  bosh -e vbox -d concourse vms
  ```
* Surf to http://10.244.0.101:8080/ and you should get a ConcourseCI home page !

Kemukins: Demo Jenkins Configuration
====================================

Deployment pipeline skeleton with [Jenkins](http://jenkins-ci.org/) for Wakame CI

Features
--------

+ `/var/lib/jenkins` under version control
+ [wakame-vdc](https://github.com/axsh/wakame-vdc) rpmbuild job demo
+ deployment pipeline skeleton

Installation
------------

```
$ su - jenkins
```

```
$ umask 077
```

```
$ git clone https://github.com/wakameci/kemukins-jenkins-demo.git /var/tmp/kemukins-jenkins-demo
$ rsync -ax /var/tmp/kemukins-jenkins-demo/.git /var/lib/jenkins
$ cd /var/lib/jenkins
$ git checkout .
```

Files
-----

### Jenkins master

+ `config.xml` core config.xml
+ `buildstep-config-files.xml` managed scripts plugin
+ `jobs/` config.xml for each job

### Jekins cluster

Using ssh with no pass pharse key pair

+ ssh_config
  + `.ssh/config`
+ ssh key pair
  + `.ssh/kemukins-demo` private key
  + `.ssh/kemukins-demo.pub` public key

Build Tool
----------

+ [kemumaki](https://github.com/axsh/kemumaki)

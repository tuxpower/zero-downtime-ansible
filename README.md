# Intro

This is the starting point for the tutorial "Zero Downtime Deployment with Ansible" where you will learn how to provision Linux servers with a web-proxy, a database and automate zero downtime deployment of a Java application to a load balanced environment.

## Requirements

### Install Ansible

#### Mac:

Install Python setuptools: https://pypi.python.org/pypi/setuptools#installation-instructions

If you prefer not to install packages to your global `site-packages` you can install and use virtualenv: http://virtualenv.readthedocs.org/en/latest/

```sudo easy_install pip```

```sudo pip install paramiko PyYAML jinja2 passlib```

```sudo pip install ansible```

Then, if you're going to update ansible later, just do:

```sudo pip install ansible --upgrade```

#### Other:

http://docs.ansible.com/ansible/intro_installation.html#installing-the-control-machine

### Install VirtualBox and Extension Pack

https://www.virtualbox.org/wiki/Downloads

### Install Vagrant

http://docs.vagrantup.com/v2/installation/

Install [vagrant-cachier plugin](https://github.com/fgrehm/vagrant-cachier) to speed up apt with a shared cache between boxes:

```vagrant plugin install vagrant-cachier```

Install [vagrant-hostmanager plugin](https://github.com/smdahlen/vagrant-hostmanager) to manage the /etc/hosts file on guest machines and the host:

```vagrant plugin install vagrant-hostmanager```

Clone this repo, and start the virtual machines:

```
git clone https://github.com/steinim/zero-downtime-ansible.git
cd zero-downtime-ansible
vagrant up
```

### Provision with Ansible

```ansible-playbook site.yml```

### Install Java and Maven (Optional)

http://www.oracle.com/technetwork/articles/javase/index-jsp-138363.html

http://maven.apache.org/download.cgi

### Build the Java app

```cd helloworld-java-app```

```mvn clean install```

### Getting started

http://docs.ansible.com/ansible/intro_getting_started.html

### Ansible Modules

http://docs.ansible.com/ansible/list_of_all_modules.html

# About

The first time I a held the tutorial was at the [Velocity Conference in Barcelona 2014](http://conferences.oreilly.com/velocity/velocityeu2014/).

* [Velocity Abstract](http://velocityconf.com/velocityeu2014/public/schedule/detail/37017)
* [Velocity Tutorial slides](http://steinim.github.io/slides/zero-downtime-ansible)

I also did a talk on the same subject at [DevOpsCon Berlin 2016](http://devopsconference.de/),

* [DevOpsCon Abstract](http://devopsconference.de/session/zero-downtime-deployment-with-ansible/)
* [DevOpsCon Slides](http://steinim.github.io/slides/devopscon/zero-downtime-ansible/)
* [DevOpsCon Full tutorial](http://steinim.github.io/slides/devopscon/zero-downtime-ansible/tutorial.html)

and at [DevOps Pro in Moscow 2016](http://www.devopspro.ru/).

* [DevOps Pro Abstract](http://www.devopspro.ru/stein-inge-morisbak/)
* [DevOps Pro Slides](http://steinim.github.io/slides/devopspro/zero-downtime-ansible/)
* [DevOps Pro Full tutorial](http://steinim.github.io/slides/devopspro/zero-downtime-ansible/tutorial.html)

and at [DevOpsCon in Munich 2017](https://devopsconference.de).

* [DevOpsCon Abstract](https://devopsconference.de/continuous-delivery/zero-downtime-deployment-with-ansible/)
* [DevOpsCon Tutorial](http://steinim.github.io/slides/devopscon-munich/zero-downtime-ansible/)

and at [FOSDEM in Brussels 2018](https://fosdem.org/2018/)

* [FOSDEM Abstract](https://fosdem.org/2018/schedule/event/zero_downtime_deployments_ansible/)
* [FOSDEM Slides](http://steinim.github.io/slides/fosdem/zero-downtime-ansible/)

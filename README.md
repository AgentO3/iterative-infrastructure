Iterative Infrastructure
========================

### How to effectively iterate on your Ansible Playbooks using Vagrant and Docker.

I have been using Ansible for some time now to manage my companies infrastructure. Ansible is super flexible, we use it in a number of different scenarios such as building, deployment, and configuration management. The infrastructure consists of many servers running many different types of applications. With this type of architecture it's easy to run a segment of the system locally, but trying to run the whole thing is a different story. If you have ever tried running more than a couple of Vagrant vms at one time on your laptop you will see why. To be sure your infrastructure is repeatable you need to be able to completely destroy it and bring it backup again from scratch. Unless you can efficiently simulate the whole infrastructure on your laptop you won't be able to verify the repeatability of your Playbooks locally before pushing it to staging or production. You won’t discover issues until they are deployed against real server. This all makes the build, test, learn loop very slow.

Don't worry, there is hope, Docker is here to help. With a single Vagrant image and Docker you can efficiently emulate you full infrastructure on your laptop. By running multiple Docker containers inside that single Vagrant vm you can efficiently iterate on your Ansible Playbooks. In this talk I will go over how to setup Vagrant and configure your Docker containers so that you can access them with Ansible. Next I will go over my build, test, learn loop to quickly iterate my Ansible Playbooks until they are ready for production use.


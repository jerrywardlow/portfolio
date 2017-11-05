# Selected projects by Jerry Wardlow

## Table of Contents
* [Item Catalog](#item-catalog-)
* [Cascadia Cookbooks](#cascadia-cookbooks)
    * [Mage2 Terraform - AWS](#user-content-mage2tfaws)
    * [Mage2 Terraform - DigitalOcean](#user-content-mage2tfdo)
    * [Magento 2 Starter](#user-content-mage2sstarter)
    * [Cron Chef cookbook](#user-content-cascron)
    * [Magento Chef cookbook](#user-content-casmagento)
    * [Robots.txt Chef cookbook](#user-content-casrobots)
* [Copious Chef Cookbooks](#copious-cookbooks)
    * [Magento](#user-content-copmagento)
    * [Users](#user-content-copusers)
    * [Keepalived](#user-content-copkeepalived)
* [Dreadnought](#dreadnought)
* [Wordpress on AWS](#wordpress-on-amazon-web-services-)
* [Ansible config for VanillaPHP](#ansible-configuration-for-vanilla-forums-)
* [Docker](#docker)
    * [Python on Alpine Linux](#user-content-dockalp)
    * [LAMP/phpMyAdmin](#user-content-docklamp)
    * [Python App](#user-content-dockcatalog)
    * [Express App](#user-content-dockexpress)
* [Ansible Playbooks](#ansible)
    * [Magento](#user-content-ansmagento)
    * [Joomla](#user-content-ansjoomla)
    * [MEAN Stack](#user-content-ansmean)
    * [Linux Config](#user-content-ansp5)
* [Google App Engine](#conference-central-)

***
[Item Catalog ](https://github.com/jerrywardlow/p3catalog)
---
A RESTful web application built on the Python Flask framework.
This project uses a PostgreSQL database to store information about items and the categories to which they belong.
Users are authenticated with OAuth2 and allowed to update and delete items and categories that they have created.
In addition to the web app, multiple deployment and configuration options are presented as well.

* **Docker** - A [Dockerfile](https://github.com/jerrywardlow/p3catalog/blob/master/Dockerfile) is available which can be used in conjunction with Docker Compose to run two linked containers, one with the Catalog web app and another with a database containing sample data.
* **Vagrant** - Using the included [Vagrantfile](https://github.com/jerrywardlow/p3catalog/blob/master/Vagrantfile) will spin up an application server and a PostgreSQL database in VirtualBox for local testing and development.
* **Ansible** - [Playbooks](https://github.com/jerrywardlow/p3catalog/tree/master/provision/ansible) are provided to configure both the web server and database.
* **Packer** - Using [Packer](https://github.com/jerrywardlow/p3catalog/tree/master/provision/packer), artifacts can be generated for use with Amazon Web Services, Digital Ocean, and Google Compute Engine.
* **Terraform (WIP)** - [Configurations](https://github.com/jerrywardlow/p3catalog/tree/master/provision/terraform) to launch AWS and Digital Ocean infrastructure.
* **Shell Script** - Application server and database [shell scripts](https://github.com/jerrywardlow/p3catalog/tree/master/provision/shell)

[![Item Catalog](/assets/item_catalog/catalog1_s.png)](https://raw.githubusercontent.com/jerrywardlow/portfolio/master/assets/item_catalog/catalog1.PNG) [![Item Catalog](/assets/item_catalog/catalog2_s.png)](https://raw.githubusercontent.com/jerrywardlow/portfolio/master/assets/item_catalog/catalog2.PNG)

***
[Cascadia Cookbooks](https://github.com/cascadia-cookbooks)
---
Open source cookbooks and templates covering a range of services, applications, infrastructures, and providers. Intended to be a stepping off point for collaboration across organizations without the limitations or associations of any single for profit group.

[Magento 2 Terraform Reference - AWS](https://github.com/cascadia-cookbooks/magento2-terraform-aws)<a name="mage2tfaws"></a> - Large scale highly available infrastructure reference for the Magento 2 ecommerce application. Includes configuration for EC2 auto scaling groups, EFS file system, RDS database, security groups, and more. Use as a module allows for convenience and reapatibility across multiple environments (preview, staging, production, etc.).

[Magento 2 Terraform Reference - DigitalOcean](https://github.com/cascadia-cookbooks/magento2-terraform-digitalocean)<a name="mage2tfdo"></a> - Basic configuration of DigitalOcean resources for a low cost, low complexity alternative to managed hosting providers. Intended for use as a module to provision application and database droplets. Includes example of module usage for reference.

[Magento 2 Starter](https://github.com/cascadia-cookbooks/magento2-starter)<a name="mage2starter"></a> - Work in progress. Starter project for the Magento 2 ecommerce application. Intended as a "fork-and-go" for anyone looking for a quickstart into a highly customizable deployment of Magento 2. Includes configuration management for multiple environments (local, staging, production) utilizing strictly open source Chef cookbooks.

[Cron Chef cookbook](https://github.com/cascadia-cookbooks/cron)<a name="cascron"></a> - Chef cookbook for management of the cron daemon and creation of cron jobs.

[Magento Chef cookbook](https://github.com/cascadia-cookbooks/magento)<a name="casmagento"></a> - Work in progress. Chef cookbook for the pre-deployment configuration of a Magento 2 environment.

[Robots.txt Chef cookbook](https://github.com/cascadia-cookbooks/robots)<a name="casrobots"></a> - Chef cookbook for the management of a site's `robots.txt`.

[![Doug](/assets/cascadia/doug.png)](https://en.wikipedia.org/wiki/Doug_flag) &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; [![Chef](/assets/cascadia/chef.png)](https://www.chef.io/) &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; &#8291; [![Terraform](/assets/cascadia/terraform.png)](https://www.terraform.io/) 

***
[Copious Cookbooks](https://github.com/copious-cookbooks)
---
A sample of public [Chef](https://www.chef.io/chef/) cookbooks developed for [Copious](https://github.com/copious).

[magento](https://github.com/copious-cookbooks/magento)<a name="copmagento"></a> - Installation and configuration of [Magento 2](http://devdocs.magento.com/) ecommerce platform.

[users](https://github.com/copious-cookbooks/users)<a name="copusers"></a> - Creation and management of Linux system users.

[keepalived](https://github.com/copious-cookbooks/keepalived)<a name="copkeepalived"></a> - Management of the `keepalived` service for Ubuntu, RHEL/CentOS, and Debian platforms

***
[Dreadnought](https://github.com/jerrywardlow/devops-playground/tree/master/dreadnought)
---
A reference project using HAProxy to route requests via host headers to a variety of web applications. Presently, the project consists of a `Vagrantfile` which provisions five virtual machines, of which both Ubuntu and CentOS are present. Configuration management was originally handled by shell scripts, but has been updated to Ansible roles. Includes roles for HAProxy, Wordpress, Magento, NodeBB, ELK, and others.

[![Dreadnought](/assets/dreadnought/dreadnought_s.png)](https://raw.githubusercontent.com/jerrywardlow/portfolio/master/assets/dreadnought/dreadnought.png)

***
[Wordpress on Amazon Web Services ](https://github.com/jerrywardlow/devops-playground/tree/master/terraform-wordpress-cloud)
---
A demonstration of Amazon Web Services technologies focused around using [Terraform](https://www.terraform.io/) to implement infrastructure as code. EC2 application servers running Wordpress are isolated in private subnets across multiple availability zones, accessed through an Elastic Load Balancer. Data is stored in a Relational Database Service MySQL instance and cached with ElastiCache/Redis. Static content is uploaded to S3 and CloudFront is used as a CDN.

Packer is used in conjunction with a shell script to generate an AMI which may be used with Terraform to stand up rapidly deployed EC2 servers. Future improvements include implementing auto-scaling groups for the web servers and using OpsWorks for configuration management.

[![Terraform](/assets/twc/twc_s.png)](https://raw.githubusercontent.com/jerrywardlow/portfolio/master/assets/twc/twc.png)

***
[Ansible Configuration for Vanilla Forums ](https://github.com/jerrywardlow/vanilla-qa)
---
Ansible playbooks to install and configure the Vanilla Forums PHP web application. Playbook functionality includes configuration of a MySQL database, installation and configuration of Vanilla on application servers, and a HAProxy load balancer. Planned additions include replication of the MySQL database across additional slave servers. An included Vagrantfile brings up local virtual machines for testing.
***
Docker
---

[Alpine Catalog](https://github.com/jerrywardlow/docker-playground/blob/master/alpine-catalog/Dockerfile)<a name="dockalp"></a> - An incredibly lightweight and irresponsible containerized implementation of the aforementioned Item Catalog on Alpine Linux. PostgreSQL and Gunicorn are left behind in exchange for SQLite and the builtin Flask server.

[Wordpress/PHPMyAdmin/MariaDB](https://github.com/jerrywardlow/docker-playground/blob/master/wppma/docker-compose.yml)<a name="docklamp"></a> - Docker Compose is used to bring up linked containers for Wordpress and MariaDB. A third container running PHPMyAdmin is presented as a convenience.

[Item Catalog](https://hub.docker.com/r/jerrywardlow/p3catalog/)<a name="dockcatalog"></a> - Docker image for [Item Catalog](https://github.com/jerrywardlow/p3catalog) hosted on Docker Hub and automatically built/updated from the source repository.

[Express](https://hub.docker.com/r/jerrywardlow/express-catalog/)<a name="dockexpress"></a> - Docker Hub container image automatically built from source repository for a basic MEAN stack catalog.
***
Ansible
---

[Magento](https://github.com/jerrywardlow/devops-playground/tree/master/ansible-magento)<a name="ansmagento"></a> - Deployment of Magento 2 artifact generated via CircleCI.

[Joomla](https://github.com/jerrywardlow/devops-playground/tree/master/ansible-joomla)<a name="ansjoomla"></a> - Configuration for Joomla CMS and associated PostgreSQL database.

[MEAN catalog](https://github.com/jerrywardlow/meansible)<a name="ansmean"></a> - Example configuration for a MEAN stack application. Includes playbooks for NGINX, NodeJS, and MongoDB, as well as general Linux housekeeping.

[p5linux](https://github.com/jerrywardlow/p5linux)<a name="ansp5"></a> - Ansible playbook for Project 5 of the Udacity Full Stack Web Developer Nanodegree. Implements basic Linux chores like user creation, firewalling, SSH lockdown, and deployment of a Python web app behind Gunicorn and Apache.
***
[Conference Central ](https://github.com/jerrywardlow/p4conference)
---

A Google App Engine project implementing a RESTful API server. OAuth2 is used to authenticate users and grant access to API functions. A basic front end is provided for convenient access to the API. This project was built for the Udacity Full Stack Web Developer Nanodegree.

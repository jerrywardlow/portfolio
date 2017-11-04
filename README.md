# Selected projects by Jerry Wardlow


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

[![Item Catalog](/assets/item_catalog/catalog1_s.png)](/assets/item_catalog/catalog1.PNG) [![Item Catalog](/assets/item_catalog/catalog2_s.png)](/assets/item_catalog/catalog2.PNG)

***
[Cascadia Cookbooks](https://github.com/cascadia-cookbooks)
---
Open source cookbooks and templates covering a range of services, applications, infrastructures, and providers. Intended to be a stepping off point for collaboration across organizations without the limitations or associations of any single for profit group.

[Magento 2 Terraform Reference - AWS](https://github.com/cascadia-cookbooks/magento2-terraform-aws) - Large scale highly available infrastructure reference for the Magento 2 ecommerce application. Includes configuration for EC2 auto scaling groups, EFS file system, RDS database, security groups, and more. Use as a module allows for convenience and reapatibility across multiple environments (preview, staging, production, etc.).

[Magento 2 Terraform Reference - DigitalOcean](https://github.com/cascadia-cookbooks/magento2-terraform-digitalocean) - Basic configuration of DigitalOcean resources for a low cost, low complexity alternative to managed hosting providers. Intended for use as a module to provision application and database droplets. Includes example of module usage for reference.

[Magento 2 Starter](https://github.com/cascadia-cookbooks/magento2-starter) - Work in progress. Starter project for the Magento 2 ecommerce application. Intended as a "fork-and-go" for anyone looking for a quickstart into a highly customizable deployment of Magento 2. Includes configuration management for multiple environments (local, staging, production) utilizing strictly open source Chef cookbooks.

[Magento Chef cookbook](https://github.com/cascadia-cookbooks/magento) - Work in progress. Chef cookbook for the pre-deployment configuration of a Magento 2 environment.

[Robots.txt Chef cookbook](https://github.com/cascadia-cookbooks/robots) - Chef cookbook for the management of a site's `robots.txt`.

***
[Copious Cookbooks](https://github.com/copious-cookbooks)
---
A sample of public [Chef](https://www.chef.io/chef/) cookbooks developed for [Copious](https://github.com/copious) with a 'tests first' strategy.

[magento](https://github.com/copious-cookbooks/magento) - Installation and configuration of [Magento 2](http://devdocs.magento.com/) ecommerce platform.

[users](https://github.com/copious-cookbooks/users) - Creation and management of Linux system users.

[keepalived](https://github.com/copious-cookbooks/keepalived) - Management of the `keepalived` service for Ubuntu, RHEL/CentOS, and Debian platforms

***
[Dreadnought](https://github.com/jerrywardlow/devops-playground/tree/master/dreadnought)
---
A reference project using HAProxy to route requests via host headers to a variety of web applications. Presently, the project consists of a `Vagrantfile` which provisions five virtual machines, of which both Ubuntu and CentOS are present. Configuration management was originally handled by shell scripts, but has been updated to Ansible roles. Includes roles for HAProxy, Wordpress, Magento, NodeBB, ELK, and others.

***
[Wordpress on Amazon Web Services ](https://github.com/jerrywardlow/devops-playground/tree/master/terraform-wordpress-cloud)
---
A demonstration of Amazon Web Services technologies focused around using [Terraform](https://www.terraform.io/) to implement infrastructure as code. EC2 application servers running Wordpress are isolated in private subnets across multiple availability zones, accessed through an Elastic Load Balancer. Data is stored in a Relational Database Service MySQL instance and cached with ElastiCache/Redis. Static content is uploaded to S3 and CloudFront is used as a CDN.

Packer is used in conjunction with a shell script to generate an AMI which may be used with Terraform to stand up rapidly deployed EC2 servers. Future improvements include implementing auto-scaling groups for the web servers and using OpsWorks for configuration management.
***
[Ansible Configuration for Vanilla Forums ](https://github.com/jerrywardlow/vanilla-qa)
---
Ansible playbooks to install and configure the Vanilla Forums PHP web application. Playbook functionality includes configuration of a MySQL database, installation and configuration of Vanilla on application servers, and a HAProxy load balancer. Planned additions include replication of the MySQL database across additional slave servers. An included Vagrantfile brings up local virtual machines for testing.
***
Docker
---

[Alpine Catalog](https://github.com/jerrywardlow/docker-playground/blob/master/alpine-catalog/Dockerfile) - An incredibly lightweight and irresponsible containerized implementation of the aforementioned Item Catalog on Alpine Linux. PostgreSQL and Gunicorn are left behind in exchange for SQLite and the builtin Flask server.

[Wordpress/PHPMyAdmin/MariaDB](https://github.com/jerrywardlow/docker-playground/blob/master/wppma/docker-compose.yml) - Docker Compose is used to bring up linked containers for Wordpress and MariaDB. A third container running PHPMyAdmin is presented as a convenience.

[Item Catalog](https://hub.docker.com/r/jerrywardlow/p3catalog/) - Docker image for [Item Catalog](https://github.com/jerrywardlow/p3catalog) hosted on Docker Hub and automatically built/updated from the source repository.

[Express](https://hub.docker.com/r/jerrywardlow/express-catalog/) - Docker Hub container image automatically built from source repository for a basic MEAN stack catalog.
***
Ansible
---

[Magento](https://github.com/jerrywardlow/devops-playground/tree/master/ansible-magento) - Deployment of Magento 2 artifact generated via CircleCI.

[Joomla](https://github.com/jerrywardlow/devops-playground/tree/master/ansible-joomla) - Configuration for Joomla CMS and associated PostgreSQL database.

[MEAN catalog](https://github.com/jerrywardlow/meansible) - Example configuration for a MEAN stack application. Includes playbooks for NGINX, NodeJS, and MongoDB, as well as general Linux housekeeping.

[p5linux](https://github.com/jerrywardlow/p5linux) - Ansible playbook for Project 5 of the Udacity Full Stack Web Developer Nanodegree. Implements basic Linux chores like user creation, firewalling, SSH lockdown, and deployment of a Python web app behind Gunicorn and Apache.
***
[Conference Central ](https://github.com/jerrywardlow/p4conference)
---

A Google App Engine project implementing a RESTful API server. OAuth2 is used to authenticate users and grant access to API functions. A basic front end is provided for convenient access to the API. This project was built for the Udacity Full Stack Web Developer Nanodegree.

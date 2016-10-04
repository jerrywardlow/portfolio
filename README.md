# Selected portfolio pieces by Jerry Wardlow
***

### [Item Catalog](https://github.com/jerrywardlow/p3catalog)
A RESTful web application built on the Python Flask framework.
This project uses a PostgreSQL database to store information about items and the categories to which they belong.
Users are authenticated with OAuth2 and allowed to update and delete items and categories that they have created.
In addition to the web app, multiple deployment and configuration options are presented as well.

* **Docker** - A [Dockerfile](https://github.com/jerrywardlow/p3catalog/blob/master/Dockerfile) is available which can be used in conjunction with Docker Compose to run two linkeed containers, one with the Catalog web app and another with a database containing sample data.
* **Vagrant** - Using the included [Vagrantfile](https://github.com/jerrywardlow/p3catalog/blob/master/Vagrantfile) will spin up an application server and a PostgreSQL database in VirtualBox for local testing and development.
* **Ansible** - [Playbooks](https://github.com/jerrywardlow/p3catalog/tree/master/provision/ansible) are provided to configure both the web server and database.
* **Packer** - Using [Packer](https://github.com/jerrywardlow/p3catalog/tree/master/provision/packer), artifacts can be generated for use with Amazon Web Services, Digital Ocean, and Google Compute Engine.
* **Terraform (WIP)** - [Configurations](https://github.com/jerrywardlow/p3catalog/tree/master/provision/terraform) to launch AWS and Digital Ocean infrastructure.
* **Shell Script** - Application server and database [shell scripts](https://github.com/jerrywardlow/p3catalog/tree/master/provision/shell)

### [Wordpress on Amazon Web Services](https://github.com/jerrywardlow/devops-playground/tree/master/wordpress-cloud)
A demonstration of Amazon Web Services technologies focused around using [Terraform](https://www.terraform.io/) to implement infrastructure as code. EC2 application servers running Wordpress are isolated in private subnets across multiple availability zones, accessed through an Elastic Load Balancer. Data is stored in a Relational Database Service MySQL instance and cached with ElastiCache/Redis. Static content is uploaded to S3 and CloudFront is used as a CDN.

Packer is used in conjunction with a shell script to generate an AMI which may be used with Terraform to stand up rapidly deployed EC2 servers. Future improvements include implementing auto-scaling groups for the web servers and using OpsWorks for configuration management.

### [Ansible Configuration for Vanilla Forums](https://github.com/jerrywardlow/vanilla-qa)
Ansible playbooks to install and configure the Vanilla Forums PHP web application. Playbook functionality includes configuration of a MySQL database, installation and configuration of Vanilla on application servers, and a HAProxy load balancer. Planned additions include replication of the MySQL database across additional slave servers. An included Vagrantfile brings up local virtual machines for testing.

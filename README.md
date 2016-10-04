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

### Wordpress

### Ansible

### Python

### Ruby

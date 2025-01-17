## Ansible Project for PHP Application Deployment

This repository provides an automated setup for deploying a PHP application using Ansible. The configuration includes setting up the application on Apache2, configuring a PostgreSQL database, and provisioning virtual machines using Vagrant.

## Project Overview

- **Application**: [Practical-DevOps/app-for-devops](https://github.com/Practical-DevOps/app-for-devops)
- **Configuration Tools**: Ansible roles
- **Provisioning**: Vagrant for local virtual machine creation.

## Features

#### Server Role:

- Installs Node.js
- Installs and configures Apache2.
- Ensures necessary PHP extensions are installed.
- Deploys the PHP + Vite application from the GitHub repository.

#### Database Role:

- Installs and configures PostgreSQL.
- Creates a database and user for the application.
- Applies necessary permissions.

#### Vagrant Integration:

- Provides a Vagrantfile to create virtual machines for the application

## Usage

- **Clone the Repository**

```bash
  git clone https://github.com/mariansmolii/ansible-project.git
  cd ansible-project
```

- **Start Virtual Machines**

```bash
  cd vagrant
  vagrant up
```

- **Run the Playbook**

```bash
  ansible-playbook main.yaml --extra-vars="db_name=app_db db_user=app_user db_pass=app_pass"
```

- **Access the Application**

```
  http://192.168.50.20/
```

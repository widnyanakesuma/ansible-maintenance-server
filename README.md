# Ansible Server Maintenance Project

This project automates server maintenance using [Ansible](https://www.ansible.com/). It focuses on upgrading essential dependencies, like Nginx, and performing other routine maintenance tasks to keep the server up-to-date and secure.

## Project Overview

- **Purpose**: Automate server maintenance tasks.
- **Scope**: Upgrade dependencies such as Nginx, system packages, and other components as required.
- **Tools**: Ansible is used to manage configuration and deployment across multiple servers.
- **Ongoing Maintenance**: The project will be updated to include new roles for additional packages as needed.

## Getting Started

### Prerequisites

Ensure you have the following installed:
- [Python 3](https://www.python.org/downloads/) (Version 3.6 or higher)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) (Version 9 or higher is recommended)

### Installation

1. **Clone the repository**:

    ```bash
    git clone <your-repository-url>
    cd <your-project-directory>
    ```

2. **Install dependencies**:

    First, create a virtual environment (recommended) and activate it:

    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

    Then, install the required Python packages for Ansible and other dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. **Configure your inventory file**:

    First, copy `inventory/hosts.yml.example` to `inventory/hosts.yml` using

    ```bash
    cp inventory/hosts.yml.example inventory/hosts.yml
    ```

    Then, edit `inventory/hosts.yml` with the IPs or hostnames of the servers to manage.

4. **Update Ansible configuration** as needed in `ansible.cfg`.

### Usage

To run the main playbook for dependency upgrades, execute:

```bash
ansible-playbook -i inventory/hosts.yml main.yml

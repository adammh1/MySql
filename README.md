# MySQL 5.6 Installation Playbook

This Ansible playbook installs MySQL 5.6 on a Ubuntu Server 24.04 LTS along with necessary dependencies.

## Requirements

- Ansible 2.9 or higher
- Target host with Ubuntu 24.04

## Usage

1. **Update the inventory file:**

    Modify the `hosts` file to include the target host information.

2. **Run the playbook:**
    ```sh
    ansible-playbook -i inventory playbook.yaml --ask-become-pass
    ```

## Playbook Tasks

- **Unarchive the MySQL package:**
    - Unarchives the MySQL 5.6 package to the specified directory.

- **Install Dependencies:**
    - Downloads and installs `libaio1`.
    - Downloads and installs `libtinfo5`.
    - Downloads and installs `libncurses5`.

- **Install MySQL 5.6:**
    - Installs `mysql-common`, `mysql-community-client`, `mysql-client`, `mysql-community-server`, `mysql-server`, and `libmysqlclient18`.

- **Start MySQL Service:**
    - Starts and enables the MySQL service to run on system boot.




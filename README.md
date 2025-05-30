# OpenStack Prerequisites Automated Installation

This repository contains Ansible playbooks for automating the installation and configuration of OpenStack prerequisites on Ubuntu servers. It streamlines the setup process for OpenStack deployment by handling all necessary dependencies and services.

## 🚀 Features

- Automated installation of all OpenStack prerequisites
- Configurable deployment for controller nodes
- Handles multiple essential services:
  - NTP (Network Time Protocol)
  - SQL Database
  - Message Queue (RabbitMQ)
  - Memcached
  - etcd
  - OpenStack base components

## 📋 Prerequisites

- Ubuntu server(s)
- Ansible installed on the control machine
- SSH access to target servers
- Sudo privileges on target servers

## 🗂️ Project Structure

```
.
├── ansible.cfg         # Ansible configuration file
├── config.yml         # Main playbook configuration
├── inventory          # Inventory file for target hosts
└── roles/            # Ansible roles for different components
    ├── ETCD/         # etcd installation and configuration
    ├── MEMCACHED/    # Memcached service setup
    ├── MSGQ/         # Message Queue (RabbitMQ) configuration
    ├── NTP/          # Network Time Protocol setup
    ├── OPENSTACK/    # OpenStack base components
    └── SQL/          # SQL database installation
```

## 🛠️ Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/[your-username]/OpenStack-Prerequisite-Installation.git
   cd OpenStack-Prerequisite-Installation
   ```

2. Update the inventory file with your target hosts:
   ```bash
   nano inventory
   ```

3. Run the playbook:
   ```bash
   ansible-playbook -i inventory config.yml
   ```

## ⚙️ Configuration

The main configuration is handled through `config.yml`. The playbook performs the following tasks:
- Fixes any broken package installations
- Updates and upgrades the system packages
- Installs and configures all prerequisite services

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## ✨ Acknowledgments

- OpenStack community
- Ansible community

## 📞 Support

For support, please open an issue in the GitHub repository.

# Jenkins Provisioning with Vagrant & Ansible

This repository provides a simple, reproducible environment to quickly install a Jenkins server on a virtual machine using Vagrant and Ansible. The VM is based on **Ubuntu 24** and the configuration is fully automated.

## Features

- **Automated Setup:** Uses Ansible to install and configure Jenkins.
- **Vagrant-Based Environment:** Easily spin up a virtual machine running Ubuntu 24.
- **Quick Deployment:** Get your Jenkins server up and running fast for development, testing, or CI/CD experiments.

## Prerequisites

Before getting started, ensure you have the following installed on your host machine:

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) (or another supported provider)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Getting Started

Follow these steps to set up your Jenkins server:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com:Anthony-Ucci/Snippets-Quick_Jenkins.git
   cd your-repository
   ```

2. **Start the Virtual Machine:**

   Run the following command to create the VM and trigger the Ansible playbook for provisioning:

   ```
   vagrant up
   ```

   This command will:
   - Download the Ubuntu 24 box (if not already available)
   - Boot up the VM
   - Execute the Ansible playbook to install and configure Jenkins

3. **Access Jenkins:**

   Once provisioning is complete, open your browser and navigate to:

   ```
   http://vm_ip_addr:8080
   ```

   You should see the Jenkins interface ready for use.

## Project Structure

- **Vagrantfile:** Configures the virtual machine and defines the provisioning steps.
- **jenkins/**: Contains the Ansible playbook(s) used to install Jenkins.
- **README.md:** This documentation file.

## Customization

Feel free to modify the Vagrantfile and Ansible playbooks to suit your needs. You can:
- Adjust VM specifications (e.g., memory, CPU cores)
- Update Jenkins configurations and plugins
- Extend the playbooks to install additional software

## Contributing

Contributions are welcome! If you have suggestions, improvements, or encounter any issues, please open an issue or submit a pull request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgments

- [Jenkins](https://www.jenkins.io/)
- [Vagrant](https://www.vagrantup.com/)
- [Ansible](https://www.ansible.com/)
- [Ubuntu](https://ubuntu.com/)

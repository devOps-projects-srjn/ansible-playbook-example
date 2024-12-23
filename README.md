# Ansible EC2 Configuration Setup

################

*This repository demonstrates the setup and configuration of two EC2 machines using Ansible. The steps below outline the process of establishing communication with the EC2 machines, running ad-hoc commands, and executing an Ansible playbook for configuration management.
*
################

Steps Followed

1. Establish Communication with EC2 Machines
    Password-less Authentication:
    To enable secure and password-less communication between the development machine and the target EC2 instances, SSH key-based authentication was configured using ssh-keygen.

    The public RSA key was copied to the ~/.ssh/authorized_keys file of the target EC2 instances to allow secure SSH access.


2. Set Up the Inventory File
    An inventory file was created to specify the target EC2 instances.
    The file contains the IP addresses of the two EC2 machines under the [webservers] group, making them available for configuration through Ansible.
3. Run Ad-Hoc Commands
    To familiarize with Ansible, simple ad-hoc commands were executed on the target EC2 machines to understand the basic configuration management concepts.
        Example ad-hoc command:
            # ansible -i inventory -m shell -a "nproc"


4. Create and Test the Ansible Playbook
    After validating the ad-hoc commands, a comprehensive Ansible playbook was created to automate the configuration of the EC2 machines.
    The playbook includes tasks such as installing packages, starting services, and configuring settings on both EC2 instances.
5. Execute the Playbook and Verify
    The playbook was successfully executed on the EC2 machines.
    After execution, each task was verified on both target EC2 machines to ensure the desired configurations were applied.
6. Next Steps: Advanced Ansible Usage
    The next phase will focus on exploring advanced Ansible features such as:
    Using Ansible roles for better task organization
    Implementing playbook conditionals, loops, and templates
    Automating EC2 instance provisioning with dynamic inventories
    Leveraging Ansible Vault for securing sensitive data
    Enhancing automation with Ansible Tower or AWX

###################
    
This project demonstrates a basic configuration management setup using Ansible to automate the configuration of EC2 machines. Future enhancements will include more advanced Ansible techniques and improved automation workflows.

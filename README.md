## Purpose

This AMI Builder example, creates a new AMI out of the latest Amazon Ubuntu AMI.

## Source code structure

```bash
├── roles                              <-- Roles used
│    ├── requirements.yml              <-- Ansible galaxy file with roles to import
│    ├── common                        <-- Application code
│    │    ├── handlers
│    │    │    └── main.yml            <-- Ansible file for handlers
│    │    ├── tasks
│    │    │    └── main.yml            <-- Ansible file for tasks
│    │    ├── templates
│    │    │    └── main.yml            <-- Ansible Jinja2 templates
│    │    └── vars
│    │         └── main.yml            <-- Ansible file for vars
│    ├── apache-php                    <-- Install apache & php packages
│    │    └── ...
│    └── agora                         <-- Install and configure application
│         └── ...
├── sic
│    └── aca.yml                       <-- Main configuration SIC
├── ansible-playbook.yml               <-- Wordpress ansible playbook file
├── ansible.cfg                        <-- Ansible config
├── aws-wordpress.yml                  <-- Wordpress packer configuration file
├── ...                         	   <-- ...
└── README.md
```

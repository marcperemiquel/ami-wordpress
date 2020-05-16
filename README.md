## Wordpress AMI

This AMI Builder, creates a new Agora Wordpress AMI out of the latest Amazon Ubuntu AMI.

## Source code structure

```bash
├── roles                              <-- Roles used
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
│    │    └── ...
│    └── aws-configs                   <-- Install and configure aws configurations
│         └── ...
├── sic
│    └── aca.yml                       <-- Main configuration SIC
├── ansible-playbook.yml               <-- Moodle ansible playbook file
├── ansible.cfg                        <-- Ansible config
├── aws-moodle.yml                     <-- Moodle packer configuration file
├── ...                         	     <-- ...
└── README.md
```

## Locally run

Test with Vagrant

```bash
vagrant up
```

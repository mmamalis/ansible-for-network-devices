################################################################################
#### 
#### Testing Ansible for network devices 
#### 
################################################################################

The first playbook is used to produce a new configuration for a new VPN service.
The new configuration gathers all required variables from the YAML file located
under the group_vars folder. 
This YAML file is used to describe the specifics of a service we want to deploy.

RUN: ansible-playbook create_mdvpn_configuration.yml

The second playbook can be used to upload configuration to the network by 
using ansible-junos-stdlib modules.

RUN: ansible-playbook upload_configuration_and_commit.yml

The configurations are gathered under the ./generated_configs folder.

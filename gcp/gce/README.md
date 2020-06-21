This module creates VPC, Subnet, Firewall, Routing and VMs

Reference: https://docs.ansible.com/ansible/latest/scenario_guides/guide_gce.html

Requisites
The GCP modules require both the requests and the google-auth libraries to be installed.

$ pip install requests google-auth
Alternatively for RHEL / CentOS, the python-requests package is also available to satisfy requests libraries.

$ yum install python-requests


Credentials
- Service Accounts (Recommended): Use JSON service accounts with specific permissions.
- Machine Accounts: Use the permissions associated with the GCP Instance you’re using Ansible on.

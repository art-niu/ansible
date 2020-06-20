Problem:
"msg": "Please install the google-auth library"

Env:
macOS Catalina, v 10.15.4

Solution:
$ pip3 uninstall ansible

$ sudo pip3 install ansible

Problem:
'errors': [{'message': \"The resource 'projects/hello-world' was not found

Solution:
Use gcp project id other than project name, and change dynamic inventory file name to <project-id>.gcp.yml

      gcp_project: <project id>

Problem:
Cannot connect to vm with ssh

Solution:
The vm was created on different network.

Temporarily, use default network by setting network to null

        network_interfaces:
          - network: null

Problem:
'resource.sourceImage': 'projects/ubuntu-os-cloud/global/licenses/ubuntu-1910'. Unexpected resource collection 'licenses'

Solution:
In Equivalent REST response window, choose the value of selfLink other than the one in licenses list.
"selfLink": "projects/ubuntu-os-cloud/global/images/ubuntu-1910-eoan-v20200529",

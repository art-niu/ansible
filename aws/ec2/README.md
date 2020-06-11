Authentication

- Option 1:

  $ aws configure
  AWS Access Key ID   [****************36CA]: 
  AWS Secret Access Key   [****************sOIf]: 
  Default region name [us-east-1]: 
  Default output format [json]: 
  
Option 2:

  $ export AWS_ACCESS_KEY_ID='AK123'
  
  $ export AWS_SECRET_ACCESS_KEY='abc123'
  
Customization

To run the code, you have to customze roles/global/vars/main.yml. 

  key_pair_to_login_ec2: <You Key Pair to login the targets you created>
  target_region: <The region you plan to create ec2 in>
  ami_name: <The ami name you plan to use>
  
Reference
  https://docs.ansible.com/ansible/latest/scenario_guides/guide_aws.html
#  LAMP Stack Deployment Automation 
This is a Ansible Playbook to deploy a LAMP Stack infrastructure on ubuntu/debian hosts. 
Mail realy role also available which install postfix with amazon ses support.

### Stack -
* apache2
* mysql 
* php
* postfix-ses
### Pre-requisites 
You must have Ansible version greater or similar to  2.6 installed.

### Setup
* Add host in /etc/ansible/hosts file. See the given hosts file to add hosts.  
* Run command `sudo ansible-playbook lamp-playbook.yml`


### Variable  Configuration
* `USERNAME`: root
* `PASSWORD`: [update the variable "mysql_root_password" in lamp-playbook.yml]
* `http_host`: your domain name.
* `http_conf`: the name of the configuration file that will be created within Apache.
* `http_port`: HTTP port, default is 80.
* `disable_default`: whether or not to disable the default Apache website. When set to true, your new virtualhost should be used as default website. Default is true.
*   `postfix_aliases`:
       - user: root
         alias: ashish@devopsunification.com
*    `postfix_relayhost`: 
*    ` postfix_relaytls`: true
    # AWS IAM SES credentials (not access key):
*    `postfix_sasl_user`: 
*    `postfix_sasl_password`: 





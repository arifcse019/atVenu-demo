Usage:

1. Create four vms
     - Docker based configuration server
     - HAproxy instance
     - Two rails instances

 Make sure you have keys setup in these vms and have sudo/root access

2. Update environments/demo/hosts file with their public ip addresses

4. Store your encrypted dockerhub credential in roles/docker-setup/vars/vault_dockerhub_demo.yml

3.  Setup the demo environment

ansible-playbook -i environments/demo atVenu-config-server-setup.yml -v --ask-vault-pass

This will first create the docker based configuration server and from there a docker image will be configuring the other three servers

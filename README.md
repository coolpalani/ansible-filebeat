# ansible-filebeat

Require Ansible >= 1.2

## How to use :

in this example i have 50 hosts and i want to ship their logs in ELK, i need to deploy the client filebeat & configuration files.
So to do it we use ansible :

1. Add ip address of all hosts who you want to deply filebeat in /etc/ansible/hosts and name the hosts-group "[Filebeat-Client]" (or in you working directory but use '-i' argument to specify the location of you hosts file) 

2. Edit the template configuration file as you want in template/filebeat.yml & specify the IP Adress of you elasticsearch

3. Specify authentificaion method in test/test.yml (private key, user/password ...)

4. launch the playbook with  the command "ansible-playbook test/test.yml" or "ansible-playbook -i hosts_file_location test/test.yml



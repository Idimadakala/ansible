#session-20

Ansible is a Automation Engine that runs Ansible playbooks
Why Ansible ?
-> Declarative
-> user-friendly: we can define all the steps in yamls
-> more readable
-> orchestrate the app lifecycle
-> Agenetless: push based CM server. No Agent installation required. Ansible CM Server pushes the changes to the client.

syntax to run ansible-playbook
---------------------------
insllation of ansible: sudo dnf install ansible -y

ssh ec2-user@<ip-addr>
ssh ec2-user@<ip-addr> "echo "hello ansible" >> /tmp/hello-ansible.txt"

ansible all -i ansible-node.jsprajampeta.org -e ansible_user= -e ansible_password= -m ping
ansible all -i 3.88.24.223 -e ansible_user= -e ansible_password= -m ping
ansible all -i 172.31.40.165, -e ansible_user= -e ansible_password= -m ping


ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password= 01-playbook.yaml

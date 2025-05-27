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

-- dnf: value of state must be one of: absent, installed, latest, present, removed, got: started

ansible all -b -i ansible-node.jsprajampeta.org, -e ansible_user=ec2-user -e ansible_password=DevOps321 -m dnf -a "name=nginx state=installed"

-- service: "value of state must be one of: reloaded, restarted, started, stopped, got: removed"
ansible all -b -i ansible-node.jsprajampeta.org, -e ansible_user=ec2-user -e ansible_password=DevOps321 -m service -a "name=nginx state=started"

--dnf

 ansible all -b -i ansible-node.jsprajampeta.org, -e ansible_user=ec2-user -e ansible_password=DevOps321 -m dnf -a "name=nginx state=removed"





ansible-playbook -i inventory.ini -e ansible_user=ec2-user -e ansible_password= 01-playbook.yaml

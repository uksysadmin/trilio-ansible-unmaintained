# trilio-ansible
Set of Ansible Roles and Playbooks for Trilio Cloud-Native Intelligent Recovery products

# Examples

ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml<br>
<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "auth"<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "check"<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "backup"<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "smoketest"<br>

Authors: Kevin Jackson <kevin.jackson at trilio io>
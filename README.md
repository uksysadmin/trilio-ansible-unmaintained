# trilio-ansible
Set of Ansible Playbooks for Trilio Cloud-Native Intelligent Recovery products

# Examples

ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-check.yaml<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-create-target.yaml<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-create-backup.yaml<br>
<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-smoktest.yaml --tags "auth"<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-smoktest.yaml --tags "check"<br>
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-smoktest.yaml --tags "auth,smoketest"<br>

Authors: Kevin Jackson <kevin.jackson at trilio io>
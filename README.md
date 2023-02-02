# trilio-ansible
Set of Ansible Playbooks for Trilio Cloud-Native Intelligent Recovery products

*Examples*

ansible-playbook -e @secrets.env -e @auth.enc --vault-ask-pass tvk-check.yaml
ansible-playbook -e @secrets.env -e @auth.enc --vault-ask-pass tvk-smoktest.yaml
ansible-playbook -e @secrets.env -e @auth.enc --vault-ask-pass tvk-create-target.yaml
ansible-playbook -e @secrets.env -e @auth.enc --vault-ask-pass tvk-create-backup.yaml

Authors: Kevin Jackson <kevin.jackson at trilio io>
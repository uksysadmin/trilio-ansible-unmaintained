# trilio-ansible
Set of Ansible Roles and Playbooks for Trilio Cloud-Native Intelligent Recovery products

# Examples

``` bash
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml
```

```bash
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "auth"
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "check"
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "backup"
ansible-playbook -e @secrets.enc -e @auth.enc --vault-ask-pass tvk-utility.yaml --tags "smoketest"
```

# Configuration
Configuration is done in *tvk-config.yaml* to allow for automation.<br>

To create S3 based Trilio for Kubernetes Targets, a secret is used. This Play can create secrets from an encrypted vault with the following structure:

``` yaml
secrets:
  - name: s3-access-secret
    type: generic
    data:
      - key: accessKey
        value: YOURACCESSKEY
      - key: secretKey
        value: YOURSECRETKEY
```
Create this in a file called *secrets.enc* then encrypt with<br>
``` bash
ansible-vault encrypt secrets.enc
```
You would then specify this on the command line with<br>
``` bash
ansible-playbook -e @secrets.enc --vault-ask-pass tvk-utility.yaml
```

Authors: Kevin Jackson <kevin.jackson at trilio io>
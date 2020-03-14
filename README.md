# Openshift Drools Hacep automation

Ansible and scripts to automate openshift-drools-hacep-automation with just one command line.

CRC setup must be previously executed with your key from https://cloud.redhat.com/openshift/install/crc/installer-provisioned
```sh
crc setup
```

#### Fedora

Create from scratch
```sh
ansible-playbook fedora/playbook_create.yaml
```

#### Ubuntu

Create from scratch
```sh
ansible-playbook fedora/playbook_create.yaml
```
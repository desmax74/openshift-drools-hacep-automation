# Openshift Drools Hacep automation

Ansible and scripts to automate openshift-drools-hacep-automation with just one command line.

CRC, Git, Java and Maven must be installed, and Ansible of course.

#### Fedora

Create from scratch the crc setup, kafka cluster, topics and namespace
```sh
ansible-playbook fedora/playbook_create.yaml
```

Simple start after the create from scratch
```sh
ansible-playbook fedora/playbook_start.yaml
```

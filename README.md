# Openshift Drools Hacep automation

Ansible and scripts to automate openshift-drools-hacep-automation with just one command line.

Git, Java 1.8, Maven 3.6.3 and Ansible of course, must be installed.

note:In the kubernetes folder is present the deployment.yaml without the usual placeholders,
feel free to change your image name and tag before to run ansible

### Create an account on cloud.redhat.com
https://cloud.redhat.com/openshift/install and download or copy your Pull secret from the the laptop installation https://cloud.redhat.com/openshift/install/crc/installer-provisioned

#### Ansible commands

On Debian/Ubuntu only:
```sh
ansible-playbook ./playbook_libs.yaml
```

Download and copy CRC in the user's path (2GB),
change the kafka namespace (my-cluster-kafka) and app_name (my-kafka-project) in the file if you want different names
```sh
ansible-playbook ./playbook_crc.yaml
```

Configure etc/hosts
```sh
sudo ansible-playbook ./playbook_etc_hosts.yaml
```

Create from scratch the crc setup, kafka cluster, topics and namespace
```sh
ansible-playbook ./playbook_create.yaml
```
Note: The CRC setup spent 10 minute, cut to 1 minute in the video recording

[![asciicast](https://asciinema.org/a/311642.png)](https://asciinema.org/a/311642)

Simple start after the create from scratch
```sh
ansible-playbook ./playbook_start.yaml
```
[![asciicast](https://asciinema.org/a/311654.png)](https://asciinema.org/a/311654)
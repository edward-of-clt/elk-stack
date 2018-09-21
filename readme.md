# Local ELK Stack

## What to Expect:

> You can add (or remove) hosts in the Vagrantfile.

1. 3 Elasticsearch Nodes
1. 2 Kibana Nodes
1. 1 Logstash Node

## Spin Up Your Cluster

> Before running vagrant up, ensure you have a SSH key located at ~/.ssh/id_rsa

```shell
vagrant up
```

> The `all.yml` playbook will cycle through the `docker.yml`, `elastic.yml`, `logstash.yml`, and `kibana.yml` plays.

```shell
ansible-playbook -i playbooks/tmp_inv/ playbooks/all.yml
```
> Note: After running `all.yml` it may take a few minutes for Kibana to respond.


## Destroy Cluster

```shell
vagrant destroy
```

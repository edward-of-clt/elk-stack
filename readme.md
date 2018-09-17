# Local ELK Stack

## What to Expect:

> You can add (or remove) hosts in the Vagrantfile.

1. 3 Elasticsearch Nodes
1. 2 Kibana Nodes
1. 1 Logstash Node

## Spin Up Your Cluster

```shell
vagrant up
```

```shell
ansible-playbook -i playbooks/tmp_inv/ playbooks/all.yml
```

> The `all.yml` playbook will cycle through the `docker.yml`, `elastic.yml`, `logstash.yml`, and `kibana.yml` plays.

## Destroy Cluster

```shell
vagrant destroy
```

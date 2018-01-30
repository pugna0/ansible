## Description

Redis cluster twin instance running on a host listened on 7000 and 7001. Cluster is running in master-slave model consisted of at least three pair of master-slave(6 nodes). In this project, we use [Telegraf](https://github.com/influxdata/telegraf "click please") as monitor to collect system basic inforimation and redis status information.
______

## Check syntax and predict result

ansible-playbook -i inventories/test -t redis-cluster site.yml -C 

## How to run deployment

ansible-playbook -i inventories/test -t redis-cluster site.yml

```bash
    -i dynamically handle inventory

    -t dynamically limit playbook file, by default, site.yml file will contain all the playbook file.
```

## About monitoring outputs

By default, we enable prometheus output plugin listened on :9273/metrics.


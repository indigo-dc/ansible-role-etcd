Etcd Role
=========

Configure and start etcd in a docker container using the image `quay.io/coreos/etcd:latest`. 

This role has been specifically developed to be used for the deployment of calico in the framework of INDIGO-DataCloud project.

Role Variables
--------------
- `etcd_peers` (optional): list of etcd nodes - alternatively, you can use a proper inventory file specifying the hosts group [etcd_servers]

Dependencies
------------

- `indigo-dc.docker`

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: indigo-dc.etcd, etcd_peers: ["10.10.10.1", "10.10.10.2", "10.10.10.3"] }

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0


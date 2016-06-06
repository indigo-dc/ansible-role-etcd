Zookeeper Role
=========

Configure and start etcd in a docker container using the image `indigodatacloud/zookeeper:latest`. 

This role has been specifically developed to be used for the deployment of calico in the framework of INDIGO-DataCloud project.

Role Variables
--------------


Dependencies
------------

- `indigo-dc.docker`

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: indigo-dc.etcd }

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0


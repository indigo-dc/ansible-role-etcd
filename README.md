Etcd Role
=========

[![Build Status](https://travis-ci.org/sochoa/ansible-role-etcd.svg?branch=master)](https://travis-ci.org/sochoa/ansible-role-etcd)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-sochoa.etcd-blue.svg)](https://galaxy.ansible.com/sochoa/etcd/)
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/sochoa/ansible-role-etcd.svg)](http://isitmaintained.com/project/sochoa/ansible-role-etcd "Average time to resolve an issue")
[![Percentage of issues still open](http://isitmaintained.com/badge/open/sochoa/ansible-role-etcd.svg)](http://isitmaintained.com/project/sochoa/ansible-role-etcd "Percentage of issues still open")

Configure and start an Etcd cluster via docker.

Links
-----

* [EtcD Docker Image](https://quay.io/repository/coreos/etcd)
* [EtcD Documentation](https://coreos.com/etcd/docs/latest)
* [EtcD Clustering Guide](https://coreos.com/etcd/docs/latest/clustering.html)
* [EtcD Cluster Tuning](https://coreos.com/etcd/docs/latest/clustering.html)

Role Variables
--------------

- `etcd_peers` (optional): list of etcd nodes - Alternatively, you can use a proper inventory file specifying a host group titled `etcd_peers`.

Dependencies
------------

- **Docker**:  It is recommend a widely used Ansible Galaxy role for docker such as [dochang.docker](https://galaxy.ansible.com/dochang/docker) which has been successfully managing docker on modern Ubuntu and modern RHEL.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: indigo-dc.etcd
           etcd_peers:
             - 10.10.10.1
             - 10.10.10.2
             - 10.10.10.3

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0

Contributors
------------

- [Marica Antonacci](https://github.com/indigo-dc) - Initial creator and Jinja master

- [Sean Ochoa](https://github.com/sochoa) - Contributor testing on RHEL and uplifting to use `docker_container`

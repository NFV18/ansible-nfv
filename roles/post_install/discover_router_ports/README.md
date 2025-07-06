# Discover Instance Ports

## Description

The following role attempts to discover the ports attached to routers.

* Query OpenStack APIs
    * Discover attached ports to routers

## Role Variables

Virtual environment to use
(OpenStack Ansible modules require to have OpenStack python SDK installed)
(Leverages the task `setup_openstack_env` from `roles/post_install/openstack_tasks`)
```
venv_path: '/tmp/ansible_venv'
```

Name of cloud to be queried via OpenStack Ansible modules
(Requires `clouds.yaml` to be present, refer to [documentation](https://docs.openstack.org/python-openstackclient/pike/configuration/index.html))
(Leverages the task `setup_openstack_env` from `roles/post_install/openstack_tasks`)
```
query_cloud: 'overcloud'
```

Validate HTTPS certificates when using APIs:
```
cloud_validate_certs: False
```

## Returns

A list of list containing ports attached to routers.

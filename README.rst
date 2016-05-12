OpenStack-Ansible Sahara 
########################
:tags: openstack, sahara, cloud, ansible
:category: \*nix

This Ansible role installs and configures OpenStack sahara and sahara
engine.

This role will install the following Upstart services:
    * sahara-api
    * sahara-engine

.. code-block:: yaml

    - name: Install sahara server
      hosts: sahara_all
      user: root
      roles:
        - { role: "os_sahara", tags: [ "os-sahara" ] }
      vars:
        external_lb_vip_address: 172.16.24.1
        internal_lb_vip_address: 192.168.0.1
        sahara_galera_address: "{{ internal_lb_vip_address }}"

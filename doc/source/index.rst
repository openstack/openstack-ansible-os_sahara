=============================
OpenStack-Ansible sahara role
=============================

.. toctree::
   :maxdepth: 2

   configure-sahara.rst

This role installs the following Upstart services:

    * sahara-api
    * sahara-engine

Default variables
~~~~~~~~~~~~~~~~~

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.

Required variables
~~~~~~~~~~~~~~~~~~

.. code-block:: yaml

    sahara_galera_address
    sahara_container_mysql_password
    sahara_service_password
    sahara_rabbitmq_password

Example playbook
~~~~~~~~~~~~~~~~

.. literalinclude:: ../../examples/playbook.yml
   :language: yaml

Tags
~~~~

This role supports two tags: ``sahara-install`` and ``sahara-config``.
The ``sahara-install`` tag can be used to install and upgrade. The
``sahara-config`` tag can be used to manage configuration.

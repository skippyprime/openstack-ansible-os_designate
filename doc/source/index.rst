====================================
Designate role for OpenStack-Ansible
====================================

This Ansible role installs and configures OpenStack Designate.

This role will install the following services:
    * designate-api
    * designate-central
    * designate-pool-manager
    * designate-zone-manager
    * designate-mdns
    * designate-sink

Default variables
~~~~~~~~~~~~~~~~~

.. literalinclude:: ../../defaults/main.yml
   :language: yaml
   :start-after: under the License.

Required variables
~~~~~~~~~~~~~~~~~~

.. code-block:: yaml

    designate_galera_address
    designate_galera_password
    designate_pool_manager_galera_password
    designate_service_password
    designate_rabbitmq_password

Example playbook
~~~~~~~~~~~~~~~~

.. literalinclude:: ../../examples/playbook.yml
   :language: yaml

Tags
^^^^

This role supports two tags: ``designate-install`` and ``designate-config``.
The ``designate-install`` tag can be used to install and upgrade. The
``designate-config`` tag can be used to maintain configuration of the service.


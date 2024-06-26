========================
Ansible 10 Release Notes
========================

This changelog describes changes since Ansible 9.0.0.

.. contents::
  :depth: 2

v10.0.0a1
=========

.. contents::
  :local:
  :depth: 2

Release Summary
---------------

Release Date: 2024-04-09

`Porting Guide <https://docs.ansible.com/ansible/devel/porting_guides.html>`_

Removed Collections
-------------------

- community.azure (previously included version: 2.0.0)
- community.sap (previously included version: 2.0.0)
- gluster.gluster (previously included version: 1.0.2)
- hpe.nimble (previously included version: 1.1.4)
- netapp.aws (previously included version: 21.7.1)
- netapp.azure (previously included version: 21.10.1)
- netapp.elementsw (previously included version: 21.7.0)
- netapp.um_info (previously included version: 21.8.1)
- purestorage.fusion (previously included version: 1.6.0)

Added Collections
-----------------

- community.library_inventory_filtering_v1 (version 1.0.0)

Ansible-core
------------

Ansible 10.0.0a1 contains ansible-core version 2.17.0b1.
This is a newer version than version 2.16.0 contained in the previous Ansible release.

The changes are reported in the combined changelog below.

Included Collections
--------------------

If not mentioned explicitly, the changes are reported in the combined changelog below.

+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| Collection                               | Ansible 9.0.0 | Ansible 10.0.0a1 | Notes                                                                                                                        |
+==========================================+===============+==================+==============================================================================================================================+
| amazon.aws                               | 7.0.0         | 7.5.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| ansible.netcommon                        | 5.3.0         | 6.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| ansible.utils                            | 2.11.0        | 4.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| ansible.windows                          | 2.1.0         | 2.3.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| arista.eos                               | 6.2.1         | 8.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| awx.awx                                  | 23.3.1        | 24.1.0           | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| azure.azcollection                       | 1.19.0        | 2.3.0            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| check_point.mgmt                         | 5.1.1         | 5.2.3            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.aci                                | 2.8.0         | 2.9.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.asa                                | 4.0.3         | 5.0.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.dnac                               | 6.7.6         | 6.13.2           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.intersight                         | 2.0.3         | 2.0.8            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.ios                                | 5.2.0         | 7.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.iosxr                              | 6.1.0         | 8.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.ise                                | 2.5.16        | 2.8.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.meraki                             | 2.16.14       | 2.18.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.mso                                | 2.5.0         | 2.6.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cisco.nxos                               | 5.2.1         | 7.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cloud.common                             | 2.1.4         | 3.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.aws                            | 7.0.0         | 7.2.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.ciscosmb                       | 1.0.7         | 1.0.8            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.crypto                         | 2.16.0        | 2.18.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.digitalocean                   | 1.24.0        | 1.26.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.dns                            | 2.6.3         | 2.8.3            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.docker                         | 3.4.11        | 3.8.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.general                        | 8.0.2         | 8.5.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.grafana                        | 1.6.1         | 1.8.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.hashi_vault                    | 6.0.0         | 6.2.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.hrobot                         | 1.8.2         | 1.9.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.library_inventory_filtering_v1 |               | 1.0.0            | The collection was added to Ansible                                                                                          |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.mongodb                        | 1.6.3         | 1.7.3            | There are no changes recorded in the changelog.                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.mysql                          | 3.8.0         | 3.9.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.okd                            | 2.3.0         | 3.0.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.postgresql                     | 3.2.0         | 3.4.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.rabbitmq                       | 1.2.3         | 1.3.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.routeros                       | 2.10.0        | 2.14.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.sap_libs                       | 1.4.1         | 1.4.2            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.vmware                         | 4.0.0         | 4.2.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.windows                        | 2.0.0         | 2.2.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| community.zabbix                         | 2.1.0         | 2.3.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| containers.podman                        | 1.11.0        | 1.12.1           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| cyberark.pas                             | 1.0.23        | 1.0.25           | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| dellemc.enterprise_sonic                 | 2.2.0         | 2.4.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| dellemc.openmanage                       | 8.4.0         | 9.1.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| dellemc.powerflex                        | 2.0.1         | 2.3.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| dellemc.unity                            | 1.7.1         | 2.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| f5networks.f5_modules                    | 1.27.0        | 1.28.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| fortinet.fortimanager                    | 2.3.0         | 2.4.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| fortinet.fortios                         | 2.3.4         | 2.3.6            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| google.cloud                             | 1.2.0         | 1.3.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| grafana.grafana                          | 2.2.3         | 3.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| hetzner.hcloud                           | 2.3.0         | 3.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| ibm.qradar                               | 2.1.0         | 3.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| ibm.storage_virtualize                   | 2.1.0         | 2.3.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| infinidat.infinibox                      | 1.3.12        | 1.4.3            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| infoblox.nios_modules                    | 1.5.0         | 1.6.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| inspur.ispim                             | 2.1.0         | 2.2.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| junipernetworks.junos                    | 5.3.0         | 7.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| kubernetes.core                          | 2.4.0         | 3.0.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| lowlydba.sqlserver                       | 2.2.2         | 2.3.2            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| microsoft.ad                             | 1.3.0         | 1.5.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| netapp.ontap                             | 22.8.2        | 22.10.0          |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| netapp.storagegrid                       | 21.11.1       | 21.12.0          |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| netbox.netbox                            | 3.15.0        | 3.17.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| openstack.cloud                          | 2.1.0         | 2.2.0            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| purestorage.flasharray                   | 1.22.0        | 1.27.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| purestorage.flashblade                   | 1.14.0        | 1.17.0           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| splunk.es                                | 2.1.0         | 3.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| telekom_mms.icinga_director              | 1.34.1        | 2.1.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| theforeman.foreman                       | 3.14.0        | 4.0.0            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| vmware.vmware_rest                       | 2.3.1         | 3.0.1            |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+
| vultr.cloud                              | 1.10.0        | 1.12.1           |                                                                                                                              |
+------------------------------------------+---------------+------------------+------------------------------------------------------------------------------------------------------------------------------+

Major Changes
-------------

Ansible-core
~~~~~~~~~~~~

- urls.py - Removed support for Python 2

ansible.netcommon
~~~~~~~~~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.

ansible.utils
~~~~~~~~~~~~~

- Bumping `netaddr` to `>=0.10.1`, means that starting from this release, the minimum `netaddr` version this collection requires is `>=0.10.1`.
- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.
- This release mainly addresses the breaking changes in the `netaddr` library.
- With the new release of `netaddr` 1.0.0, the `IPAddress.is_private()` method has been removed and instead, the `IPAddress.is_global()` method has been extended to support the same functionality. This change has been reflected in the `ipaddr` filter plugin.

arista.eos
~~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.
- This release removes previously deprecated modules and attributes from this collection. Please refer to the **Removed Features** section for details.

cisco.asa
~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.

cisco.ios
~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.
- ios_ntp - Remove deprecated ntp legacy module

cisco.iosxr
~~~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.
- This release removes previously deprecated module and attributes from this collection. Please refer to the **Removed Features** section for details.

cisco.nxos
~~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.
- This release removes four previously deprecated modules from this collection. Please refer to the **Removed Features** section for details.

community.docker
~~~~~~~~~~~~~~~~

- The ``community.docker`` collection now depends on the ``community.library_inventory_filtering_v1`` collection. This utility collection provides host filtering functionality for inventory plugins. If you use the Ansible community package, both collections are included and you do not have to do anything special. If you install the collection with ``ansible-galaxy collection install``, it will be installed automatically. If you install the collection by copying the files of the collection to a place where ansible-core can find it, for example by cloning the git repository, you need to make sure that you also have to install the dependency if you are using the inventory plugins (https://github.com/ansible-collections/community.docker/pull/698).

community.hashi_vault
~~~~~~~~~~~~~~~~~~~~~

- requirements - the ``requests`` package which is required by ``hvac`` now has a more restrictive range for this collection in certain use cases due to breaking security changes in ``ansible-core`` that were backported (https://github.com/ansible-collections/community.hashi_vault/pull/416).

community.mysql
~~~~~~~~~~~~~~~

- Collection version 2.*.* is EOL, no more bugfixes will be backported. Please consider upgrading to the latest version.

dellemc.openmanage
~~~~~~~~~~~~~~~~~~

- All OME modules are enhanced to support the environment variables `OME_USERNAME` and `OME_PASSWORD` as fallback for credentials.
- All iDRAC and Redfish modules are enhanced to support the environment variables `IDRAC_USERNAME` and `IDRAC_PASSWORD` as fallback for credentials.
- idrac_certificates - The module is enhanced to support the import and export of `CUSTOMCERTIFICATE`.
- idrac_diagnostics - The module is introduced to run and export diagnostics on iDRAC.
- idrac_gather_facts - This role is enhanced to support secure boot.
- idrac_license - The module is introduced to configure iDRAC licenses.
- idrac_user - This role is introduced to manage local users of iDRAC.

dellemc.unity
~~~~~~~~~~~~~

- Adding support for Unity Puffin v5.4.

fortinet.fortios
~~~~~~~~~~~~~~~~

- Add notes for backup modules in the documentation in both monitor and monitor_fact modules.
- Supported new FOS versions 7.4.2 and 7.4.3, and support data type mac_address in the collection.
- Update all the boolean values to true/false in the documents and examples.
- Update the document of log_fact.
- Update the documentation for the supported versions from latest to a fix version number.
- Update the mismatched version message with version ranges.
- Update the required ansible version to 2.14.
- Update the required ansible version to 2.15.
- Update the supported version ranges instead of concrete version numbers to reduce the collection size.

grafana.grafana
~~~~~~~~~~~~~~~

- Add an Ansible role for OpenTelemetry Collector by @ishanjainn in https://github.com/grafana/grafana-ansible-collection/pull/138

ibm.qradar
~~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.

infoblox.nios_modules
~~~~~~~~~~~~~~~~~~~~~

- Upgrade Ansible version support from 2.13 to 2.16.
- Upgrade Python version support from 3.8 to 3.10.

junipernetworks.junos
~~~~~~~~~~~~~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.
- This release removes previously deprecated modules from this collection. Please refer to the **Removed Features** section for details.

splunk.es
~~~~~~~~~

- Bumping `requires_ansible` to `>=2.14.0`, since previous ansible-core versions are EoL now.

Minor Changes
-------------

Ansible-core
~~~~~~~~~~~~

- Add ``dump`` and ``passno`` mount information to facts component (https://github.com/ansible/ansible/issues/80478)
- Added MIRACLE LINUX 9.2 in RedHat OS Family.
- Interpreter Discovery - Remove hardcoded references to specific python interpreters to use for certain distro versions, and modify logic for python3 to become the default.
- Use Python's built-in ``functools.update_wrapper`` instead an inline copy from Python 3.7.
- User can now set ansible.log to record higher verbosity than what is specified for display via new configuration item LOG_VERBOSITY.
- ``DEFAULT_PRIVATE_ROLE_VARS`` is now overridden by explicit setting of ``public`` for ``include_roles`` and ``import_roles``.
- ``ansible-galaxy role|collection init`` - accept ``--extra-vars`` to supplement/override the variables ``ansible-galaxy`` injects for templating ``.j2`` files in the skeleton.
- ``import_role`` action now also gets a ``public`` option that controls variable exports,  default depending on ``DEFAULT_PRIVATE_ROLE_VARS`` (if using defaults equates to ``public=True``).
- added configuration item ``TARGET_LOG_INFO`` that allows the user/author to add an information string to the log output on targets.
- ansible-doc - treat double newlines in documentation strings as paragraph breaks. This is useful to create multi-paragraph notes in module/plugin documentation (https://github.com/ansible/ansible/pull/82465).
- ansible-doc output has been revamped to make it more visually pleasing when going to a terminal, also more concise, use -v to show extra information.
- ansible-galaxy - Started normalizing build directory with a trailing separator when building collections, internally. (https://github.com/ansible/ansible/pull/81619).
- ansible-galaxy dependency resolution messages have changed the unexplained 'virtual' collection for the specific type ('scm', 'dir', etc) that is more user friendly
- ansible-test - Add Alpine 3.19 container.
- ansible-test - Add Alpine 3.19 to remotes.
- ansible-test - Add Fedora 39 container.
- ansible-test - Add Fedora 39 remote.
- ansible-test - Add a work-around for permission denied errors when using ``pytest >= 8`` on multi-user systems with an installed version of ``ansible-test``.
- ansible-test - Add support for RHEL 9.3 remotes.
- ansible-test - Added a macOS 14.3 remote VM.
- ansible-test - Bump the ``nios-test-container`` from version 2.0.0 to version 3.0.0.
- ansible-test - Containers and remotes managed by ansible-test will have their Python ``EXTERNALLY-MANAGED`` marker (PEP668) removed. This provides backwards compatibility for existing tests running in newer environments which mark their Python as externally managed. A future version of ansible-test may change this behavior, requiring tests to be adapted to such environments.
- ansible-test - Make Python 3.12 the default version used in the ``base`` and ``default`` containers.
- ansible-test - Remove Alpine 3(.18) container.
- ansible-test - Remove Alpine 3.18 from remotes.
- ansible-test - Remove Fedora 38 remote support.
- ansible-test - Remove Fedora 38 test container.
- ansible-test - Remove rhel/9.2 test remote
- ansible-test - Remove the FreeBSD 13.2 remote.
- ansible-test - Removed fallback to ``virtualenv`` when ``-m venv`` is non-functional.
- ansible-test - Removed test remotes: macos/13.2
- ansible-test - Removed the ``no-basestring`` sanity test. The test is no longer necessary now that Python 3 is required.
- ansible-test - Removed the ``no-dict-iteritems``, ``no-dict-iterkeys`` and ``no-dict-itervalues`` sanity tests. The tests are no longer necessary since Python 3 is required.
- ansible-test - Removed the ``no-main-display`` sanity test. The unwanted pattern is unlikely to occur, since the test has existed since Ansible 2.8.
- ansible-test - Removed the ``no-unicode-literals`` sanity test. The test is unnecessary now that Python 3 is required and the ``unicode_literals`` feature has no effect.
- ansible-test - Special handling for installation of ``cryptography`` has been removed, as it is no longer necessary.
- ansible-test - The ``shellcheck`` sanity test no longer disables the ``SC2164`` check. In most cases, seeing this error means the script is missing ``set -e``.
- ansible-test - The ``unidiomatic-typecheck`` rule has been enabled in the ``pylint`` sanity test.
- ansible-test - The ``unidiomatic-typecheck`` rule has been removed from the ``validate-modules`` sanity test.
- ansible-test - Update the base and default containers to use Ubuntu 22.04 for the base image. This also updates PowerShell to version 7.4.0 with .NET 8.0.0 and ShellCheck to version 0.8.0.
- ansible-test - Updated the CloudStack test container to version 1.7.0.
- ansible-test - Updated the distro test containers to version 6.3.0 to include coverage 7.3.2 for Python 3.8+. The alpine3 container is now based on 3.18 instead of 3.17 and includes Python 3.11 instead of Python 3.10.
- ansible-test - Updated the distro test containers to version 7.1.0.
- ansible-test - When ansible-test installs requirements, it now instructs pip to allow installs on externally managed environments as defined by PEP 668. This only occurs in ephemeral environments managed by ansible-test, such as containers, or when the `--requirements` option is used.
- ansible-test - When invoking ``sleep`` in containers during container setup, the ``env`` command is used to avoid invoking the shell builtin, if present.
- ansible-test - document block name now included in error message for YAML parsing errors (https://github.com/ansible/ansible/issues/82353).
- ansible-test - sanity test allows ``EXAMPLES`` to be multi-document YAML (https://github.com/ansible/ansible/issues/82353).
- ansible-test now has FreeBSD 13.3 and 14.0 support
- ansible.builtin.user - Remove user not found warning (https://github.com/ansible/ansible/issues/80267)
- apt_repository.py - use api.launchpad.net endpoint instead of launchpad.net/api
- async tasks can now also support check mode at the same time.
- async_status now supports check mode.
- constructed inventory plugin - Adding a note that only group_vars of explicit groups are loaded (https://github.com/ansible/ansible/pull/82580).
- csvfile - add a keycol parameter to specify in which column to search.
- dnf - add the ``best`` option
- dnf5 - add the ``best`` option
- filter plugin - Add the count and mandatory_count parameters in the regex_replace filter
- find - add a encoding parameter to specify which encoding of the files to be searched.
- git module - gpg_allowlist name was added in 2.17 and we will eventually deprecate the gpg_whitelist alias.
- import_role - allow subdirectories with ``_from`` options for parity with ``include_role`` (https://github.com/ansible/ansible/issues/82584).
- module argument spec - Allow module authors to include arbitrary additional context in the argument spec, by making use of a new top level key called ``context``. This key should be a dict type. This allows for users to customize what they place in the argument spec, without having to ignore sanity tests that validate the schema.
- modules - Add the ability for an action plugin to call ``self._execute_module(*, ignore_unknown_opts=True)`` to execute a module with options that may not be supported for the version being called. This tells the module basic wrapper to ignore validating the options provided match the arg spec.
- package action now has a configuration that overrides the detected package manager, it is still overridden itself by the use option.
- py3compat - Remove ``ansible.utils.py3compat`` as it is no longer necessary
- removed the unused argument ``create_new_password`` from ``CLI.build_vault_ids`` (https://github.com/ansible/ansible/pull/82066).
- urls - Add support for TLS 1.3 post handshake certificate authentication - https://github.com/ansible/ansible/issues/81782
- urls - reduce complexity of ``Request.open``
- user - accept yescrypt hash as user password
- validate-modules tests now correctly handles ``choices`` in dictionary format.

amazon.aws
~~~~~~~~~~

- AnsibeAWSModule - added ``fail_json_aws_error()`` as a wrapper for ``fail_json()`` and ``fail_json_aws()`` when passed an ``AnsibleAWSError`` exception (https://github.com/ansible-collections/amazon.aws/pull/1997).
- autoscaling_group - minor PEP8 whitespace sanity fixes (https://github.com/ansible-collections/amazon.aws/pull/1846).
- backup_plan - Let user to set ``schedule_expression_timezone`` for backup plan rules when when using botocore >= 1.31.36 (https://github.com/ansible-collections/amazon.aws/issues/1952).
- ec2_ami_info - simplify parameters to ``get_image_attribute`` to only pass ID of image (https://github.com/ansible-collections/amazon.aws/pull/1846).
- ec2_eip - use ``ResourceTags`` to set initial tags upon creation (https://github.com/ansible-collections/amazon.aws/issues/1843)
- ec2_instance - Add support for modifying metadata options of an existing instance (https://github.com/ansible-collections/amazon.aws/pull/1918).
- ec2_instance - add support for AdditionalInfo option when creating an instance (https://github.com/ansible-collections/amazon.aws/pull/1828).
- ec2_security_group - use ``ResourceTags`` to set initial tags upon creation (https://github.com/ansible-collections/amazon.aws/pull/1844)
- ec2_vpc_igw - use ``ResourceTags`` to set initial tags upon creation (https://github.com/ansible-collections/amazon.aws/issues/1843)
- ec2_vpc_route_table - use ``ResourceTags`` to set initial tags upon creation (https://github.com/ansible-collections/amazon.aws/issues/1843)
- ec2_vpc_subnet - the default value for ``tags`` has been changed from ``{}`` to ``None``, to remove tags from a subnet an empty map must be explicitly passed to the module (https://github.com/ansible-collections/amazon.aws/pull/1876).
- ec2_vpc_subnet - use ``ResourceTags`` to set initial tags upon creation (https://github.com/ansible-collections/amazon.aws/issues/1843)
- ec2_vpc_subnet - use ``wait_timeout`` to also control maximum time to wait for initial creation of subnets (https://github.com/ansible-collections/amazon.aws/pull/1848).
- iam_access_key - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_access_key_info - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_group - Basic testing of ``name`` and ``path`` has been added to improve error messages (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_group - ``group_name`` has been added as an alias to ``name`` for consistency with other IAM modules (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_group - add support for setting group path (https://github.com/ansible-collections/amazon.aws/pull/1892).
- iam_group - adds attached_policies return value (https://github.com/ansible-collections/amazon.aws/pull/1892).
- iam_group - code refactored to avoid single long function (https://github.com/ansible-collections/amazon.aws/pull/1892).
- iam_group - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_instance_profile - Basic testing of ``name`` and ``path`` has been added to improve error messages (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_instance_profile - attempting to change the ``path`` for an existing profile will now generate a warning, previously this was silently ignored (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_instance_profile - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_instance_profile - the ``prefix`` parameter has been renamed ``path`` for consistency with other IAM modules, ``prefix`` remains as an alias. No change to playbooks is required (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_instance_profile - the default value for ``path`` has been removed.  New instances will still be created with a default path of ``/``. No change to playbooks is required (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_instance_profile_info - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_managed_policy - Basic testing of ``name`` and ``path`` has been added to improve error messages (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_managed_policy - ``description`` attempting to update the description now results in a warning, previously it was simply ignored (https://github.com/ansible-collections/amazon.aws/pull/1936).
- iam_managed_policy - ``policy`` is no longer a required parameter (https://github.com/ansible-collections/amazon.aws/pull/1936).
- iam_managed_policy - added support for tagging managed policies (https://github.com/ansible-collections/amazon.aws/pull/1936).
- iam_managed_policy - more consistently perform retries on rate limiting errors (https://github.com/ansible-collections/amazon.aws/pull/1936).
- iam_managed_policy - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_managed_policy - support for setting ``path`` (https://github.com/ansible-collections/amazon.aws/pull/1936).
- iam_managed_policy - the ``policy_description`` parameter has been renamed ``description`` for consistency with other IAM modules, ``policy_description`` remains as an alias. No change to playbooks is required (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_managed_policy - the ``policy_name`` parameter has been renamed ``name`` for consistency with other IAM modules, ``policy_name`` remains as an alias. No change to playbooks is required (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_mfa_device_info - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_role - Basic testing of ``name`` and ``path`` has been added to improve error messages (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_role - ``prefix`` and ``path_prefix`` have been added as aliases to ``path`` for consistency with other IAM modules (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_role - ``role_name`` has been added as an alias to ``name`` for consistency with other IAM modules (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_role - attempting to change the ``path`` for an existing profile will now generate a warning, previously this was silently ignored (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_role - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_role - the default value for ``path`` has been removed.  New roles will still be created with a default path of ``/``. No change to playbooks is required (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_role_info - ``path`` and ``prefix`` have been added as aliases to ``path_prefix`` for consistency with other IAM modules (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_role_info - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_user - Basic testing of ``name`` and ``path`` has been added to improve error messages (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_user - ``user_name`` has been added as an alias to ``name`` for consistency with other IAM modules (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_user - add ``boundary`` parameter to support managing boundary policy on users (https://github.com/ansible-collections/amazon.aws/pull/1912).
- iam_user - add ``path`` parameter to support managing user path (https://github.com/ansible-collections/amazon.aws/pull/1912).
- iam_user - added ``attached_policies`` to return value (https://github.com/ansible-collections/amazon.aws/pull/1912).
- iam_user - refactored code to reduce complexity (https://github.com/ansible-collections/amazon.aws/pull/1912).
- iam_user - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_user - refactored error handling to use a decorator (https://github.com/ansible-collections/amazon.aws/pull/1951).
- iam_user_info - Add ``login_profile`` to return info that is get from a user, to know if they can login from AWS console (https://github.com/ansible-collections/amazon.aws/pull/2012).
- iam_user_info - ``prefix`` has been added as an alias to ``path_prefix`` for consistency with other IAM modules (https://github.com/ansible-collections/amazon.aws/pull/1933).
- iam_user_info - refactored code to use ``AnsibleIAMError`` and ``IAMErrorHandler`` as well as moving shared code into module_utils.iam (https://github.com/ansible-collections/amazon.aws/pull/1998).
- iam_user_info - the ``path`` parameter has been renamed ``path_prefix`` for consistency with other IAM modules, ``path`` remains as an alias. No change to playbooks is required (https://github.com/ansible-collections/amazon.aws/pull/1933).
- lambda - added support for using ECR images for the function (https://github.com/ansible-collections/amazon.aws/pull/1939).
- module_utils.errors - added a basic error handler decorator (https://github.com/ansible-collections/amazon.aws/pull/1951).
- module_utils.iam - refactored normalization functions to use ``boto3_resource_to_ansible_dict()`` and ``boto3_resource_list_to_ansible_dict()`` (https://github.com/ansible-collections/amazon.aws/pull/2006).
- module_utils.transformations - add ``boto3_resource_to_ansible_dict()`` and ``boto3_resource_list_to_ansible_dict()`` helpers (https://github.com/ansible-collections/amazon.aws/pull/2006).
- rds_cluster - Add support for ServerlessV2ScalingConfiguration to create and modify cluster operations (https://github.com/ansible-collections/amazon.aws/pull/1839).
- rds_instance_snapshot - minor PEP8 whitespace sanity fixes (https://github.com/ansible-collections/amazon.aws/pull/1846).
- s3_bucket_info - add parameter ``bucket_versioning`` to return the versioning state of a bucket (https://github.com/ansible-collections/amazon.aws/pull/1919).
- s3_object_info - fix exception raised when listing objects from empty bucket (https://github.com/ansible-collections/amazon.aws/pull/1919).

ansible.utils
~~~~~~~~~~~~~

- Add support in fact_diff filter plugin to show common lines.(https://github.com/ansible-collections/ansible.utils/issues/311)
- Fact_diff filter plugin - Add fact_diff filter plugin. (https://github.com/ansible-collections/ansible.utils/issues/78).

ansible.windows
~~~~~~~~~~~~~~~

- Set minimum supported Ansible version to 2.14 to align with the versions still supported by Ansible.
- win_share - Added a new param called ``scope_name`` that allows file shares to be scoped for Windows Server failover cluster roles.
- win_uri - Max depth for json object conversion used to be 2. Can now send json objects with up to 20 levels of nesting

check_point.mgmt
~~~~~~~~~~~~~~~~

- New resource modules for R81.20 JHF Take 43
- meta/runtime.yml - update minimum Ansible version required to 2.14.0.

cisco.aci
~~~~~~~~~

- Add Authentification option for EIGRP interface profile.
- Add L3out Floating SVI modules (aci_l3out_floating_svi, aci_l3out_floating_svi_path, aci_l3out_floating_svi_path_secondary_ip and aci_l3out_floating_svi_secondary_ip) (#478)
- Add No-verification flag option to reduce the number of API calls. If true, a verifying GET will not be sent after a POST update to APIC
- Add access spine interface selector and port block binding in aci_access_port_block_to_access_port
- Add aci_access_spine_interface_selector module
- Add aci_action_rule_additional_communities module
- Add aci_action_rule_set_as_path and aci_action_rule_set_as_path_asn modules
- Add aci_bgp_peer_prefix_policy, aci_bgp_route_summarization_policy and aci_bgp_address_family_context_policy modules
- Add aci_fabric_pod, aci_fabric_pod_external_tep, aci_fabric_pod_profile, aci_fabric_pod_remote_pool modules (#558)
- Add aci_hsrp_interface_policy, aci_l3out_hsrp_group, aci_l3out_hsrp_interface_profile and aci_l3out_hsrp_secondary_vip modules (#505)
- Add aci_interface_policy_eigrp (class:eigrpIfPol) module
- Add aci_interface_policy_pim module
- Add aci_interface_policy_storm_control module
- Add aci_keychain_policy and aci_key_policy modules
- Add aci_l3out_bfd_multihop_interface_profile, aci_l3out_bfd_interface_profile, aci_interface_policy_bfd_multihop, aci_interface_policy_bfd and aci_bfd_multihop_node_policy modules (#492)
- Add aci_l3out_dhcp_relay_label, aci_dhcp_option_policy and aci_dhcp_option modules
- Add aci_l3out_eigrp_interface_profile module
- Add aci_listify filter plugin to flattens nested dictionaries
- Add aci_netflow_exporter_policy module
- Add aci_netflow_monitor_policy and aci_netflow_record_policy modules
- Add aci_netflow_monitor_to_exporter module
- Add aci_node_block module
- Add aci_pim_route_map_policy and aci_pim_route_map_entry modules
- Add aci_qos_custom_policy and aci_qos_dscp_class modules
- Add aci_qos_dot1p_class module
- Add action rules attributes to aci_tenant_action_rule_profile.
- Add auto to speed attribute options in aci_interface_policy_link_level module (#577)
- Add missing options to aci_bd module
- Add modules aci_bd_to_netflow_monitor_policy and aci_bd_rogue_exception_mac (#600)
- Add modules for Fabric External Connection Policies and its childs
- Add option to set delimiter to  _  in aci_epg_to_domain module
- Add qos_custom_policy, pim_interface_policy and igmp_interface_policy as new child_classes for aci_l3out_logical_interface_profile.
- Add support for annotation in aci_rest module (#437)
- Add support for block statements in useg attributes with the aci_epg_useg_attribute_block_statement module
- Add support for configuration of access switch policy groups with aci_access_switch_policy_group module
- Add support for configuration of certificate authorities in aci_aaa_certificate_authority
- Add support for configuration of fabric management access policies in aci_fabric_management_access
- Add support for configuration of vrf multicast with aci_vrf_multicast module
- Add support for configuring Azure cloud subnets using the aci_cloud_subnet module
- Add support for encap scope in aci_l3out_interface
- Add support for https ssl cipher configuration in aci_fabric_management_access_https_cipher
- Add support for infra l3out nodes bgp-evpn loopback, mpls transport loopback and segment id in aci_l3out_logical_node
- Add support for infra sr mpls micro bfd in aci_l3out_interface
- Add support for intra epg, taboo, and contract interface in aci_epg_to_contract
- Add support for key ring configuration in aci_aaa_key_ring
- Add support for mac and description in aci_l3out_interface
- Add support for mpls custom qos policy for infra sr mpls l3outs node profiles in aci_l3out_logical_node_profile
- Add support for security default settings configuration in aci_aaa_security_default_settings
- Add support for simple statements in useg attributes with the aci_epg_useg_attribute_simple_statement module
- Add support for sr-mpls bgpInfraPeerP and bgp_password in aci_l3out_bgp_peer module (#543)
- Add support for sr-mpls in aci_l3out module
- Add support for sr-mpls l3out to infra l3out in aci_l3out_to_sr_mpls_infra_l3out
- Add support for subject labels for EPG, EPG Contract, ESG, Contract Subject, L2Out External EPG, L3out External EPG, and L3out External EPG Contract with the aci_subject_label module
- Add support for taboo contract, contract interface and intra_epg contract in aci_l3out_extepg_to_contract
- Add support for useg default block statement configuration for useg epg in aci_epg
- Modify child class node block conditions to be optional in aci_switch_leaf_selector

cisco.dnac
~~~~~~~~~~

- Added a method to validate IP addresses.
- Added attributes 'dnac_api_task_timeout' and 'dnac_task_poll_interval' in intent and workflow_manager modules.
- Added the op_modifies=True when calling SDK APIs in the workflow manager modules.
- Addressed image un-tagging issues in inherited site settings.
- Changes the minimum supported version from Ansible v2.9.10 to v2.14.0
- Corrected site creation issues in the site module when optional parameters are missing.
- Fixed a minor issue in the site workflow manager module.
- Fixed management IP updates for devices on SNMP version v2.
- Introduced sample playbooks for the discovery module.
- Provided documentation for EWLC templates in Cisco Catalyst Center version 2.3.7.x.
- Resolved a 'NoneType' error in discovery module credentials.
- Updating galaxy.yml ansible.utils dependencies.
- inventory_workflow_manager - Added attributes 'add_user_defined_field', 'update_interface_details', 'export_device_list' and 'admin_status'
- inventory_workflow_manager - Removed attributes 'provision_wireless_device', 'reprovision_wired_device'

cisco.ios
~~~~~~~~~

- Added ios_evpn_evi resource module.
- Added ios_evpn_global resource module.
- Added ios_vxlan_vtep resource module.
- Fixed ios_evpn_evi resource module integration test failure - code to remove VLAN config.
- ios_bgp_address_family - Fixed an issue with inherit peer-policy CLI
- ios_bgp_address_family - added 'advertise' key
- ios_bgp_global - added 'bgp.default.ipv4_unicast' and 'bgp.default.route_target.filter' key
- ios_l3_interfaces - added 'autostate', 'mac_address', 'ipv4.source_interface', and 'ipv6.enable' key
- ios_vlans - Add purged state to deal with toplevel vlan and vlan configuration config.
- ios_vlans - added vlan config CLI feature.
- ios_vrf - added MDT related keys

cisco.iosxr
~~~~~~~~~~~

- Add missing options in afi and safi in address-family of bgp_templates RM.
- iosxr_facts - Add cdp neighbors in ansible_net_neighbors dictionary (https://github.com/ansible-collections/cisco.iosxr/pull/457).

cisco.ise
~~~~~~~~~

- Changes the minimum supported version from Ansible v2.9.10 to v2.14.0
- Services included configuration, edda, dataconnect_services, subscriber.
- cisco.ise collection now supports ansible.utils v3

cisco.meraki
~~~~~~~~~~~~

- Adding support to ansible.utils ">=2.0.0, <4.00".
- Ansible collection now support v1.44.1 of Dashboard Api.
- administered_licensing_subscription_entitlements_info - new plugin.
- administered_licensing_subscription_subscriptions_bind - new plugin.
- administered_licensing_subscription_subscriptions_claim - new plugin.
- administered_licensing_subscription_subscriptions_claim_key_validate - new plugin.
- administered_licensing_subscription_subscriptions_compliance_statuses_info - new plugin.
- administered_licensing_subscription_subscriptions_info - new plugin.
- devices_appliance_radio_settings - new plugin.
- devices_appliance_radio_settings_info - new plugin.
- devices_live_tools_arp_table - new plugin.
- devices_live_tools_arp_table_info - new plugin.
- devices_live_tools_cable_test - new plugin.
- devices_live_tools_cable_test_info - new plugin.
- devices_live_tools_throughput_test - new plugin.
- devices_live_tools_throughput_test_info - new plugin.
- devices_live_tools_wake_on_lan - new plugin.
- devices_live_tools_wake_on_lan_info - new plugin.
- devices_wireless_alternate_management_interface_ipv6 - new plugin.
- networks_appliance_rf_profiles - new plugin.
- networks_appliance_rf_profiles_info - new plugin.
- networks_appliance_traffic_shaping_vpn_exclusions - new plugin.
- networks_sm_devices_install_apps - new plugin.
- networks_sm_devices_reboot - new plugin.
- networks_sm_devices_shutdown - new plugin.
- networks_sm_devices_uninstall_apps - new plugin.
- networks_vlan_profiles - new plugin.
- networks_vlan_profiles_assignments_by_device_info - new plugin.
- networks_vlan_profiles_assignments_reassign - new plugin.
- networks_vlan_profiles_info - new plugin.
- networks_wireless_ethernet_ports_profiles - new plugin.
- networks_wireless_ethernet_ports_profiles_assign - new plugin.
- networks_wireless_ethernet_ports_profiles_info - new plugin.
- networks_wireless_ethernet_ports_profiles_set_default - new plugin.
- organizations_appliance_traffic_shaping_vpn_exclusions_by_network_info - new plugin.
- organizations_appliance_uplinks_statuses_overview_info - new plugin.
- organizations_appliance_uplinks_usage_by_network_info - new plugin.
- organizations_camera_boundaries_areas_by_device_info - new plugin.
- organizations_camera_boundaries_lines_by_device_info - new plugin.
- organizations_camera_detections_history_by_boundary_by_interval_info - new plugin.
- organizations_camera_permissions_info - new plugin.
- organizations_camera_roles - new plugin.
- organizations_camera_roles_info - new plugin.
- organizations_devices_availabilities_change_history_info - new plugin.
- organizations_devices_boots_history_info - new plugin.
- organizations_sm_admins_roles - new plugin.
- organizations_sm_admins_roles_info - new plugin.
- organizations_sm_sentry_policies_assignments - new plugin.
- organizations_sm_sentry_policies_assignments_by_network_info - new plugin.
- organizations_summary_top_networks_by_status_info - new plugin.
- organizations_webhooks_callbacks_statuses_info - new plugin.
- organizations_wireless_devices_channel_utilization_by_device_info - new plugin.
- organizations_wireless_devices_channel_utilization_by_network_info - new plugin.
- organizations_wireless_devices_channel_utilization_history_by_device_by_interval_info - new plugin.
- organizations_wireless_devices_channel_utilization_history_by_network_by_interval_info - new plugin.
- organizations_wireless_devices_packet_loss_by_client_info - new plugin.
- organizations_wireless_devices_packet_loss_by_device_info - new plugin.
- organizations_wireless_devices_packet_loss_by_network_info - new plugin.

cisco.mso
~~~~~~~~~

- Add Azure Cloud site support to mso_schema_site_contract_service_graph
- Add Azure Cloud site support to mso_schema_site_service_graph
- Add functionality to resolve same name in remote and local user.
- Add l3out_template and l3out_schema arguments to mso_schema_site_external_epg (#394)
- Add mso_schema_site_contract_service_graph module to manage site contract service graph
- Add mso_schema_site_contract_service_graph_listener module to manage Azure site contract service graph listeners and update other modules
- Add new parameter remote_user to add multiple remote users associated with multiple login domains
- Add support for replacing all existing contracts with new provided contracts in a single operation with one request and adding/removing multiple contracts in multiple operations with a single request in mso_schema_template_anp_epg_contract module
- Add support for replacing all existing static ports with new provided static ports in a single operation with one request and adding/removing multiple static ports in multiple operations with a single request in mso_schema_template_anp_epg_staticport module
- Add support for required attributes introduced in NDO 4.2 for mso_schema_site_anp_epg_domain
- Support for creation of schemas without templates with the mso_schema module

cisco.nxos
~~~~~~~~~~

- nxos_config - Relax restrictions on I(src) parameter so it can be used more like I(lines). (https://github.com/ansible-collections/cisco.nxos/issues/89).

community.aws
~~~~~~~~~~~~~

- aws_ssm - Updated the documentation to explicitly state that an S3 bucket is required, the behavior of the files in that bucket, and requirements around that. (https://github.com/ansible-collections/community.aws/issues/1775).
- cloudfront_distribution - added support for ``cache_policy_id`` and ``origin_request_policy_id`` for behaviors (https://github.com/ansible-collections/community.aws/pull/1589)
- glue_job - add support for 2 new instance types which are G.4X and G.8X (https://github.com/ansible-collections/community.aws/pull/2048).
- mq_broker - add support to wait for broker state via ``wait`` and ``wait_timeout`` parameter values (https://github.com/ansible-collections/community.aws/pull/1879).
- msk_cluster - Support for additional ``m5`` and ``m7g`` types of MSK clusters (https://github.com/ansible-collections/community.aws/pull/1947).

community.ciscosmb
~~~~~~~~~~~~~~~~~~

- docs - addeed info about SG-250 support and testing

community.crypto
~~~~~~~~~~~~~~~~

- luks_device - add allow discards option (https://github.com/ansible-collections/community.crypto/pull/693).
- x509_crl - the new option ``serial_numbers`` allow to configure in which format serial numbers can be provided to ``revoked_certificates[].serial_number``. The default is as integers (``serial_numbers=integer``) for backwards compatibility; setting ``serial_numbers=hex-octets`` allows to specify colon-separated hex octet strings like ``00:11:22:FF`` (https://github.com/ansible-collections/community.crypto/issues/687, https://github.com/ansible-collections/community.crypto/pull/715).

community.digitalocean
~~~~~~~~~~~~~~~~~~~~~~

- digital_ocean_kubernetes - add project_name parameter (https://github.com/ansible-collections/community.digitalocean/issues/264).
- fix sanity tests (https://github.com/ansible-collections/community.digitalocean/issues/323).

community.dns
~~~~~~~~~~~~~

- hetzner_dns_records and hosttech_dns_records inventory plugins - the ``filters`` option has been renamed to ``simple_filters``. The old name still works until community.hrobot 2.0.0. Then it will change to allow more complex filtering with the ``community.library_inventory_filtering_v1`` collection's functionality (https://github.com/ansible-collections/community.dns/pull/181).
- nameserver_info and nameserver_record_info - add ``server`` parameter to specify custom DNS servers (https://github.com/ansible-collections/community.dns/pull/168, https://github.com/ansible-collections/community.dns/pull/178).
- wait_for_txt - add ``server`` parameter to specify custom DNS servers (https://github.com/ansible-collections/community.dns/pull/178).

community.docker
~~~~~~~~~~~~~~~~

- The ``ca_cert`` option available to almost all modules and plugins has been renamed to ``ca_path``. The name ``ca_path`` is also used for similar options in ansible-core and other collections. The old name has been added as an alias and can still be used (https://github.com/ansible-collections/community.docker/pull/744).
- The ``docker_stack*`` modules now use the common CLI-based module code added for the ``docker_image_build`` and ``docker_compose_v2`` modules. This means that the modules now have various more configuration options with respect to talking to the Docker Daemon, and now also are part of the ``community.docker.docker`` and ``docker`` module default groups (https://github.com/ansible-collections/community.docker/pull/745).
- docker_compose_v2 - add ``scale`` option to allow to explicitly scale services (https://github.com/ansible-collections/community.docker/pull/776).
- docker_compose_v2 - allow to wait until containers are running/health when running ``docker compose up`` with the new ``wait`` option (https://github.com/ansible-collections/community.docker/issues/794, https://github.com/ansible-collections/community.docker/pull/796).
- docker_compose_v2, docker_compose_v2_pull - support ``files`` parameter to specify multiple Compose files (https://github.com/ansible-collections/community.docker/issues/772, https://github.com/ansible-collections/community.docker/pull/775).
- docker_container - add ``networks[].mac_address`` option for Docker API 1.44+. Note that Docker API 1.44 no longer uses the global ``mac_address`` option, this new option is the only way to set the MAC address for a container (https://github.com/ansible-collections/community.docker/pull/763).
- docker_container - implement better ``platform`` string comparisons to improve idempotency (https://github.com/ansible-collections/community.docker/issues/654, https://github.com/ansible-collections/community.docker/pull/705).
- docker_container - internal refactorings which allow comparisons to use more information like details of the current image or the Docker host config (https://github.com/ansible-collections/community.docker/pull/713).
- docker_container - the ``pull_check_mode_behavior`` option now allows to control the module's behavior in check mode when ``pull=always`` (https://github.com/ansible-collections/community.docker/issues/792, https://github.com/ansible-collections/community.docker/pull/797).
- docker_container - the ``pull`` option now accepts the three values ``never``, ``missing_image`` (default), and ``never``, next to the previously valid values ``true`` (equivalent to ``always``) and ``false`` (equivalent to ``missing_image``). This allows the equivalent to ``--pull=never`` from the Docker command line (https://github.com/ansible-collections/community.docker/issues/783, https://github.com/ansible-collections/community.docker/pull/797).
- docker_image - allow to specify labels and ``/dev/shm`` size when building images (https://github.com/ansible-collections/community.docker/issues/726, https://github.com/ansible-collections/community.docker/pull/727).
- docker_image - allow to specify memory size and swap memory size in other units than bytes (https://github.com/ansible-collections/community.docker/pull/727).
- inventory plugins - add ``filter`` option which allows to include and exclude hosts based on Jinja2 conditions (https://github.com/ansible-collections/community.docker/pull/698, https://github.com/ansible-collections/community.docker/issues/610).

community.general
~~~~~~~~~~~~~~~~~

- bitwarden lookup plugin - add ``bw_session`` option, to pass session key instead of reading from env (https://github.com/ansible-collections/community.general/pull/7994).
- bitwarden lookup plugin - allows to fetch all records of a given collection ID, by allowing to pass an empty value for ``search_value`` when ``collection_id`` is provided (https://github.com/ansible-collections/community.general/pull/8013).
- bitwarden lookup plugin - when looking for items using an item ID, the item is now accessed directly with ``bw get item`` instead of searching through all items. This doubles the lookup speed (https://github.com/ansible-collections/community.general/pull/7468).
- consul_auth_method, consul_binding_rule, consul_policy, consul_role, consul_session, consul_token - added action group ``community.general.consul`` (https://github.com/ansible-collections/community.general/pull/7897).
- consul_policy - added support for diff and check mode (https://github.com/ansible-collections/community.general/pull/7878).
- consul_policy, consul_role, consul_session - removed dependency on ``requests`` and factored out common parts (https://github.com/ansible-collections/community.general/pull/7826, https://github.com/ansible-collections/community.general/pull/7878).
- consul_role - ``node_identities`` now expects a ``node_name`` option to match the Consul API, the old ``name`` is still supported as alias (https://github.com/ansible-collections/community.general/pull/7878).
- consul_role - ``service_identities`` now expects a ``service_name`` option to match the Consul API, the old ``name`` is still supported as alias (https://github.com/ansible-collections/community.general/pull/7878).
- consul_role - added support for diff mode (https://github.com/ansible-collections/community.general/pull/7878).
- consul_role - added support for templated policies (https://github.com/ansible-collections/community.general/pull/7878).
- elastic callback plugin - close elastic client to not leak resources (https://github.com/ansible-collections/community.general/pull/7517).
- git_config - allow multiple git configs for the same name with the new ``add_mode`` option (https://github.com/ansible-collections/community.general/pull/7260).
- git_config - the ``after`` and ``before`` fields in the ``diff`` of the return value can be a list instead of a string in case more configs with the same key are affected (https://github.com/ansible-collections/community.general/pull/7260).
- git_config - when a value is unset, all configs with the same key are unset (https://github.com/ansible-collections/community.general/pull/7260).
- gitlab modules - add ``ca_path`` option (https://github.com/ansible-collections/community.general/pull/7472).
- gitlab modules - remove duplicate ``gitlab`` package check (https://github.com/ansible-collections/community.general/pull/7486).
- gitlab_deploy_key, gitlab_group_members, gitlab_group_variable, gitlab_hook, gitlab_instance_variable, gitlab_project_badge, gitlab_project_variable, gitlab_user - improve API pagination and compatibility with different versions of ``python-gitlab`` (https://github.com/ansible-collections/community.general/pull/7790).
- gitlab_hook - adds ``releases_events`` parameter for supporting Releases events triggers on GitLab hooks (https://github.com/ansible-collections/community.general/pull/7956).
- gitlab_runner - add support for new runner creation workflow (https://github.com/ansible-collections/community.general/pull/7199).
- icinga2 inventory plugin - add Jinja2 templating support to ``url``, ``user``, and ``password`` paramenters (https://github.com/ansible-collections/community.general/issues/7074, https://github.com/ansible-collections/community.general/pull/7996).
- icinga2 inventory plugin - adds new parameter ``group_by_hostgroups`` in order to make grouping by Icinga2 hostgroups optional (https://github.com/ansible-collections/community.general/pull/7998).
- ini_file - support optional spaces between section names and their surrounding brackets (https://github.com/ansible-collections/community.general/pull/8075).
- ipa_config - adds ``passkey`` choice to ``ipauserauthtype`` parameter's choices (https://github.com/ansible-collections/community.general/pull/7588).
- ipa_dnsrecord - adds ability to manage NS record types (https://github.com/ansible-collections/community.general/pull/7737).
- ipa_pwpolicy - refactor module and exchange a sequence ``if`` statements with a ``for`` loop (https://github.com/ansible-collections/community.general/pull/7723).
- ipa_pwpolicy - update module to support ``maxrepeat``, ``maxsequence``, ``dictcheck``, ``usercheck``, ``gracelimit`` parameters in FreeIPA password policies (https://github.com/ansible-collections/community.general/pull/7723).
- ipa_sudorule - adds options to include denied commands or command groups (https://github.com/ansible-collections/community.general/pull/7415).
- ipa_user - adds ``idp`` and ``passkey`` choice to ``ipauserauthtype`` parameter's choices (https://github.com/ansible-collections/community.general/pull/7589).
- irc - add ``validate_certs`` option, and rename ``use_ssl`` to ``use_tls``, while keeping ``use_ssl`` as an alias. The default value for ``validate_certs`` is ``false`` for backwards compatibility. We recommend to every user of this module to explicitly set ``use_tls=true`` and `validate_certs=true`` whenever possible, especially when communicating to IRC servers over the internet (https://github.com/ansible-collections/community.general/pull/7550).
- java_cert - enable ``owner``, ``group``, ``mode``, and other generic file arguments (https://github.com/ansible-collections/community.general/pull/8116).
- keycloak module utils - expose error message from Keycloak server for HTTP errors in some specific situations (https://github.com/ansible-collections/community.general/pull/7645).
- keycloak_realm_key - the ``config.algorithm`` option now supports 8 additional key algorithms (https://github.com/ansible-collections/community.general/pull/7698).
- keycloak_realm_key - the ``config.certificate`` option value is no longer defined with ``no_log=True`` (https://github.com/ansible-collections/community.general/pull/7698).
- keycloak_realm_key - the ``provider_id`` option now supports RSA encryption key usage (value ``rsa-enc``) (https://github.com/ansible-collections/community.general/pull/7698).
- keycloak_user_federation - add option for ``krbPrincipalAttribute`` (https://github.com/ansible-collections/community.general/pull/7538).
- keycloak_user_federation - allow custom user storage providers to be set through ``provider_id`` (https://github.com/ansible-collections/community.general/pull/7789).
- ldap_attrs - module now supports diff mode, showing which attributes are changed within an operation (https://github.com/ansible-collections/community.general/pull/8073).
- lvol - change ``pvs`` argument type to list of strings (https://github.com/ansible-collections/community.general/pull/7676, https://github.com/ansible-collections/community.general/issues/7504).
- lxd connection plugin - tighten the detection logic for lxd ``Instance not found`` errors, to avoid false detection on unrelated errors such as ``/usr/bin/python3: not found`` (https://github.com/ansible-collections/community.general/pull/7521).
- lxd_container - uses ``/1.0/instances`` API endpoint, if available. Falls back to ``/1.0/containers`` or ``/1.0/virtual-machines``. Fixes issue when using Incus or LXD 5.19 due to migrating to ``/1.0/instances`` endpoint (https://github.com/ansible-collections/community.general/pull/7980).
- mail - add ``Message-ID`` header; which is required by some mail servers (https://github.com/ansible-collections/community.general/pull/7740).
- mail module, mail callback plugin - allow to configure the domain name of the Message-ID header with a new ``message_id_domain`` option (https://github.com/ansible-collections/community.general/pull/7765).
- mssql_script - adds transactional (rollback/commit) support via optional boolean param ``transaction`` (https://github.com/ansible-collections/community.general/pull/7976).
- netcup_dns - adds support for record types ``OPENPGPKEY``, ``SMIMEA``, and ``SSHFP`` (https://github.com/ansible-collections/community.general/pull/7489).
- nmcli - add support for new connection type ``loopback`` (https://github.com/ansible-collections/community.general/issues/6572).
- nmcli - allow for ``infiniband`` slaves of ``bond`` interface types (https://github.com/ansible-collections/community.general/pull/7569).
- nmcli - allow for the setting of ``MTU`` for ``infiniband`` and ``bond`` interface types (https://github.com/ansible-collections/community.general/pull/7499).
- nmcli - allow setting ``MTU`` for ``bond-slave`` interface types (https://github.com/ansible-collections/community.general/pull/8118).
- onepassword lookup plugin - support 1Password Connect with the opv2 client by setting the connect_host and connect_token parameters (https://github.com/ansible-collections/community.general/pull/7116).
- onepassword_raw lookup plugin - support 1Password Connect with the opv2 client by setting the connect_host and connect_token parameters (https://github.com/ansible-collections/community.general/pull/7116)
- passwordstore - adds ``timestamp`` and ``preserve`` parameters to modify the stored password format (https://github.com/ansible-collections/community.general/pull/7426).
- proxmox - adds ``startup`` parameters to configure startup order, startup delay and shutdown delay (https://github.com/ansible-collections/community.general/pull/8038).
- proxmox - adds ``template`` value to the ``state`` parameter, allowing conversion of container to a template (https://github.com/ansible-collections/community.general/pull/7143).
- proxmox - adds ``update`` parameter, allowing update of an already existing containers configuration (https://github.com/ansible-collections/community.general/pull/7540).
- proxmox inventory plugin - adds an option to exclude nodes from the dynamic inventory generation. The new setting is optional, not using this option will behave as usual (https://github.com/ansible-collections/community.general/issues/6714, https://github.com/ansible-collections/community.general/pull/7461).
- proxmox_disk - add ability to manipulate CD-ROM drive (https://github.com/ansible-collections/community.general/pull/7495).
- proxmox_kvm - add parameter ``update_unsafe`` to avoid limitations when updating dangerous values (https://github.com/ansible-collections/community.general/pull/7843).
- proxmox_kvm - adds ``template`` value to the ``state`` parameter, allowing conversion of a VM to a template (https://github.com/ansible-collections/community.general/pull/7143).
- proxmox_kvm - support the ``hookscript`` parameter (https://github.com/ansible-collections/community.general/issues/7600).
- proxmox_ostype - it is now possible to specify the ``ostype`` when creating an LXC container (https://github.com/ansible-collections/community.general/pull/7462).
- proxmox_vm_info - add ability to retrieve configuration info (https://github.com/ansible-collections/community.general/pull/7485).
- redfish_config - add command ``SetServiceIdentification`` to set service identification (https://github.com/ansible-collections/community.general/issues/7916).
- redfish_info - add command ``GetServiceIdentification`` to get service identification (https://github.com/ansible-collections/community.general/issues/7882).
- redfish_info - adding the ``BootProgress`` property when getting ``Systems`` info (https://github.com/ansible-collections/community.general/pull/7626).
- revbitspss lookup plugin - removed a redundant unicode prefix. The prefix was not necessary for Python 3 and has been cleaned up to streamline the code (https://github.com/ansible-collections/community.general/pull/8087).
- ssh_config - adds ``controlmaster``, ``controlpath`` and ``controlpersist`` parameters (https://github.com/ansible-collections/community.general/pull/7456).
- ssh_config - new feature to set ``AddKeysToAgent`` option to ``yes`` or ``no`` (https://github.com/ansible-collections/community.general/pull/7703).
- ssh_config - new feature to set ``IdentitiesOnly`` option to ``yes`` or ``no`` (https://github.com/ansible-collections/community.general/pull/7704).
- sudoers - add support for the ``NOEXEC`` tag in sudoers rules (https://github.com/ansible-collections/community.general/pull/7983).
- terraform - add support for ``diff_mode`` for terraform resource_changes (https://github.com/ansible-collections/community.general/pull/7896).
- terraform - fix ``diff_mode`` in state ``absent`` and when terraform ``resource_changes`` does not exist (https://github.com/ansible-collections/community.general/pull/7963).
- xcc_redfish_command - added support for raw POSTs (``command=PostResource`` in ``category=Raw``) without a specific action info (https://github.com/ansible-collections/community.general/pull/7746).

community.grafana
~~~~~~~~~~~~~~~~~

- Add Quickwit search engine datasource (https://quickwit.io).
- Add parameter `org_name` to `grafana_dashboard`
- Add parameter `org_name` to `grafana_datasource`
- Add parameter `org_name` to `grafana_organization_user`
- Add support for Grafana Tempo datasource type (https://grafana.com/docs/grafana/latest/datasources/tempo/)
- Manage `grafana_folder` for organizations
- Merged ansible role telekom-mms/ansible-role-grafana into ansible-collections/community.grafana
- added `community.grafana.notification_channel` to role
- default to true/false in docs and code
- grafana_dashboard - add check_mode support

community.hashi_vault
~~~~~~~~~~~~~~~~~~~~~

- cert auth - add option to set the ``cert_auth_public_key`` and ``cert_auth_private_key`` parameters using the variables ``ansible_hashi_vault_cert_auth_public_key`` and ``ansible_hashi_vault_cert_auth_private_key`` (https://github.com/ansible-collections/community.hashi_vault/issues/428).

community.hrobot
~~~~~~~~~~~~~~~~

- robot inventory plugin - the ``filters`` option has been renamed to ``simple_filters``. The old name still works until community.hrobot 2.0.0. Then it will change to allow more complex filtering with the ``community.library_inventory_filtering_v1`` collection's functionality (https://github.com/ansible-collections/community.hrobot/pull/94).

community.mysql
~~~~~~~~~~~~~~~

- mysql_user - add the ``password_expire`` and ``password_expire_interval`` arguments to implement the password expiration management for mysql user (https://github.com/ansible-collections/community.mysql/pull/598).
- mysql_user - add user attribute support via the ``attributes`` parameter and return value (https://github.com/ansible-collections/community.mysql/pull/604).

community.postgresql
~~~~~~~~~~~~~~~~~~~~

- postgresql_db - add the ``comment`` argument (https://github.com/ansible-collections/community.postgresql/issues/614).
- postgresql_db - add the ``icu_locale`` argument (https://github.com/ansible-collections/community.postgresql/issues/666).
- postgresql_db - add the ``locale_provider`` argument (https://github.com/ansible-collections/community.postgresql/issues/666).
- postgresql_ext - add the ``comment`` argument (https://github.com/ansible-collections/community.postgresql/issues/354).
- postgresql_publication - add the ``comment`` argument (https://github.com/ansible-collections/community.postgresql/issues/354).
- postgresql_schema - add the ``comment`` argument (https://github.com/ansible-collections/community.postgresql/issues/354).
- postgresql_subscription - add the ``comment`` argument (https://github.com/ansible-collections/community.postgresql/issues/354).
- postgresql_tablespace - add the ``comment`` argument (https://github.com/ansible-collections/community.postgresql/issues/354).

community.rabbitmq
~~~~~~~~~~~~~~~~~~

- rabbitmq_user - add support to user manipulation through RabbitMQ API (https://github.com/ansible-collections/community.rabbitmq/issues/76)

community.routeros
~~~~~~~~~~~~~~~~~~

- api_info, api_modify - add ``interface ovpn-client`` path (https://github.com/ansible-collections/community.routeros/issues/242, https://github.com/ansible-collections/community.routeros/pull/244).
- api_info, api_modify - add ``radius`` path (https://github.com/ansible-collections/community.routeros/issues/241, https://github.com/ansible-collections/community.routeros/pull/245).
- api_info, api_modify - add ``routing rule`` path (https://github.com/ansible-collections/community.routeros/issues/162, https://github.com/ansible-collections/community.routeros/pull/246).
- api_info, api_modify - add missing DoH parameters ``doh-max-concurrent-queries``, ``doh-max-server-connections``, and ``doh-timeout`` to the ``ip dns`` path (https://github.com/ansible-collections/community.routeros/issues/230, https://github.com/ansible-collections/community.routeros/pull/235)
- api_info, api_modify - add missing parameters ``address-list``, ``address-list-timeout``, ``randomise-ports``, and ``realm`` to subpaths of the ``ip firewall`` path (https://github.com/ansible-collections/community.routeros/issues/236, https://github.com/ansible-collections/community.routeros/pull/237).
- api_info, api_modify - add missing path ``routing bgp template`` (https://github.com/ansible-collections/community.routeros/pull/243).
- api_info, api_modify - add read-only fields ``installed-version``, ``latest-version`` and ``status`` in ``system package update`` (https://github.com/ansible-collections/community.routeros/pull/263).
- api_info, api_modify - add support for the ``tx-power`` attribute in ``interface wireless`` (https://github.com/ansible-collections/community.routeros/pull/239).
- api_info, api_modify - added support for ``interface wifi`` and its sub-paths (https://github.com/ansible-collections/community.routeros/pull/266).
- api_info, api_modify - make path ``user group`` modifiable and add ``comment`` attribute (https://github.com/ansible-collections/community.routeros/issues/256, https://github.com/ansible-collections/community.routeros/pull/257).
- api_info, api_modify - mark the ``interface wireless`` parameter ``running`` as read-only (https://github.com/ansible-collections/community.routeros/pull/233).
- api_info, api_modify - remove default value for read-only ``running`` field in ``interface wireless`` (https://github.com/ansible-collections/community.routeros/pull/264).
- api_info, api_modify - removed ``host`` primary key in ``tool netwatch`` path (https://github.com/ansible-collections/community.routeros/pull/248).
- api_info, api_modify - set the default value to ``false`` for the  ``disabled`` parameter in some more paths where it can be seen in the documentation (https://github.com/ansible-collections/community.routeros/pull/237).
- api_modify - add missing ``comment`` attribute to ``/routing id`` (https://github.com/ansible-collections/community.routeros/pull/234).
- api_modify - add missing attributes to the ``routing bgp connection`` path (https://github.com/ansible-collections/community.routeros/pull/234).
- api_modify - add versioning to the ``/tool e-mail`` path (RouterOS 7.12 release) (https://github.com/ansible-collections/community.routeros/pull/234).
- api_modify - make ``/ip traffic-flow target`` a multiple value attribute (https://github.com/ansible-collections/community.routeros/pull/234).
- api_modify, api_info - add support for the ``ip vrf`` path in RouterOS 7  (https://github.com/ansible-collections/community.routeros/pull/259)
- api_modify, api_info - added support for ``interface wifiwave2`` (https://github.com/ansible-collections/community.routeros/pull/226).

community.vmware
~~~~~~~~~~~~~~~~

- Add standard function vmware_argument_spec() from module_utils for using default env fallback function. https://github.com/ansible-collections/community.vmware/issues/1977
- vmware_first_class_disk_info - Add a module to gather informations about first class disks. (https://github.com/ansible-collections/community.vmware/pull/1996). (https://github.com/ansible-collections/community.vmware/issues/1988).
- vmware_guest - Add IPv6 support for VM network interfaces (https://github.com/ansible-collections/community.vmware/pull/1937).
- vmware_guest_sendkey - Add Windows key (https://github.com/ansible-collections/community.vmware/issues/1959).
- vmware_guest_tools_upgrade - Add parameter `installer_options` to pass command line options to the installer to modify the installation procedure for tools (https://github.com/ansible-collections/community.vmware/pull/1059).
- vmware_host_facts - Add the possibility to get the related datacenter. (https://github.com/ansible-collections/community.vmware/pull/1994).
- vmware_vm_inventory - Add parameter `subproperties` (https://github.com/ansible-collections/community.vmware/pull/1972).
- vmware_vmkernel - Add the function to set the enable_backup_nfc setting (https://github.com/ansible-collections/community.vmware/pull/1978)
- vsphere_copy - Add parameter to tell vsphere_copy which diskformat is being uploaded (https://github.com/ansible-collections/community.vmware/pull/1995).

community.windows
~~~~~~~~~~~~~~~~~

- Set minimum supported Ansible version to 2.14 to align with the versions still supported by Ansible.
- win_regmerge - Add content 'content' parameter for specifying registry file contents directly

community.zabbix
~~~~~~~~~~~~~~~~

- Added zabbix_group_events_info module
- action module - Added notify_if_canceled property
- agent and proxy roles - Set default `zabbix_api_server_port` to 80 or 443 based on `zabbix_api_use_ssl`
- agent role - Removed duplicative Windows agent task
- agent role - Standardized default yum priority to 99
- all roles - Re-added ability to override Debian repo source
- all roles - Updated Debian repository format to 822 standard
- api_requests - Handled error from depricated CertificateError class
- multiple roles - Removed unneeded Apt Clean commands.
- proxy role - Updated MariaDB version for Centos 7 to 10.11
- various - updated testing modules
- various - updated to fully qualified module names
- zabbix agent - Added capability to add additional configuration includes
- zabbix web - Allowed the independent configuration of php-fpm without creating vhost.
- zabbix_api_info module added
- zabbix_host_info - added ability to get all the hosts configured in Zabbix
- zabbix_proxy role - Add variable zabbix_proxy_dbpassword_hash_method to control whether you want postgresql user password to be hashed with md5 or want to use db default. When zabbix_proxy_dbpassword_hash_method is set to anything other than md5 then do not hash the password with md5 so you could use postgresql scram-sha-256 hashing method.
- zabbix_server role - Add variable zabbix_server_dbpassword_hash_method to control whether you want postgresql user password to be hashed with md5 or want to use db default. When zabbix_server_dbpassword_hash_method is set to anything other than md5 then do not hash the password with md5 so you could use postgresql scram-sha-256 hashing method.
- zabbix_templategroup module added
- zabbix_user module - add current_passwd optional parameter to enable password updating of the currently logged in user (https://www.zabbix.com/documentation/6.4/en/manual/api/reference/user/update)

containers.podman
~~~~~~~~~~~~~~~~~

- Add log_opt and annotaion options to podman_play module
- Add option to parse CreateCommand easily for diff calc
- Add support for setting underlying interface in podman_network
- Alias generate systemd options stop_timeout and time
- CI - Fix rootfs test in CI
- CI - add custom podman path to tasks
- CI - add parametrized executables to tests
- Fix CI rootfs for podman_container
- Fix broken conmon version in CI install
- Improve security_opt comparison between existing container
- podman_container - Add new arguments to podman status commands
- podman_container - Add pasta as default network mode after v5
- podman_container - Update env_file to accept a list of files instead of a single file
- podman_container_exec - Return data for podman exec module
- podman_generate_systemd - Fix broken example for podman_generate_systemd (#708)
- podman_login - Update podman_login.py
- podman_play - Add support for kube yaml files with multi-documents (#724)
- podman_play - Update the logic for deleting pods/containers in podman_play
- podman_pod_info - handle return being list in Podman 5 (#713)
- podman_secret_info - Add secrets info module

dellemc.enterprise_sonic
~~~~~~~~~~~~~~~~~~~~~~~~

- sonic_aaa - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/304).
- sonic_aaa - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_acl_interfaces - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/306).
- sonic_acl_interfaces - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_bgp_as_paths - Add support for replaced and overridden states (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/290).
- sonic_bgp_communities - Add support for replaced and overridden states (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/251).
- sonic_bgp_ext_communities - Add support for replaced and overridden states (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/252).
- sonic_interfaces - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/301).
- sonic_interfaces - Add support for replaced and overridden states (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/314).
- sonic_interfaces - Change deleted design for interfaces module (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/310).
- sonic_interfaces - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_ip_neighbor - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/285).
- sonic_ip_neighbor - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_l2_acls - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/306).
- sonic_l2_acls - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_l2_interfaces - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/303).
- sonic_l2_interfaces - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_l3_acls - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/306).
- sonic_l3_acls - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_l3_interfaces - Add support for replaced and overridden states (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/241).
- sonic_lag_interfaces - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/303).
- sonic_lag_interfaces - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_logging - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/285).
- sonic_logging - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_mclag - Add VLAN range support for 'unique_ip' and 'peer_gateway' options (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/288).
- sonic_mclag - Add support for replaced and overridden states (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/288).
- sonic_ntp - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/281).
- sonic_ntp - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_port_breakout - Add Ansible support for all port breakout modes now allowed in Enterprise SONiC (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/276).
- sonic_port_breakout - Add support for replaced and overridden states (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/291).
- sonic_port_group - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/284).
- sonic_port_group - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_radius_server - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/279).
- sonic_radius_server - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_static_routes - Add playbook check and diff modes support for static routes resource module (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/313).
- sonic_static_routes - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_system - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/284).
- sonic_system - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_tacacs_server - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/281).
- sonic_tacacs_server - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_users - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/304).
- sonic_users - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_vlans - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/301).
- sonic_vlans - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- sonic_vrfs - Add mgmt VRF replaced state handling to sonic_vrfs module (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/298).
- sonic_vrfs - Add mgmt VRF support to sonic_vrfs module (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/293).
- sonic_vrfs - Add support for playbook check and diff modes (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/285).
- sonic_vrfs - Enhance config diff generation function (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/318).
- tests - Add UTs for BFD, COPP, and MAC modules (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/287).
- tests - Enable contiguous execution of all regression integration tests on an S5296f (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/277).
- tests - Fix the bgp CLI test base_cfg_path derivation of the bgp role_path by avoiding relative pathing from the possibly external playbook_dir (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/283).

dellemc.openmanage
~~~~~~~~~~~~~~~~~~

- Ansible lint issues are fixed for the collections.
- For idrac_certificate role, added support for import operation of `HTTPS` certificate with the SSL key.
- For idrac_certificates module, below enhancements are made: Added support for import operation of `HTTPS` certificate with the SSL key. The `email_address` has been made as an optional parameter.
- For idrac_gather_facts role, added storage controller details in the role output.
- Module ``redfish_storage_volume`` is enhanced to support reboot options and job tracking operation.
- redfish_storage_volume - This module is enhanced to support iDRAC8.

dellemc.powerflex
~~~~~~~~~~~~~~~~~

- Added support for PowerFlex Denver version(4.5.x) to TB and Config role.
- Added support for PowerFlex ansible modules and roles on Azure.
- Added support for resource group provisioning to validate, deploy, edit, add nodes and delete a resource group.
- The Info module is enhanced to list the firmware repositories.
- The Info module is enhanced to retrieve lists related to fault sets, service templates, deployments, and managed devices.
- The SDS module has been enhanced to facilitate SDS creation within a fault set.

f5networks.f5_modules
~~~~~~~~~~~~~~~~~~~~~

- bigiq_device_discovery - Changes in documentation related to Provider block

fortinet.fortimanager
~~~~~~~~~~~~~~~~~~~~~

- Added deprecated warning to invalid argument name, please change the invalid argument name such as "var-name", "var name" to "var_name".
- Supported fortimanager 7.4.2, 21 new modules.

google.cloud
~~~~~~~~~~~~

- anisble-test - integration tests are now run against 2.14.0 and 2.15.0
- ansible - 2.14.0 is now the minimum version supported
- ansible-lint - fixed over a thousand reported errors
- ansible-lint - upgraded to 6.22
- ansible-test - add support for GCP application default credentials (https://github.com/ansible-collections/google.cloud/issues/359).
- gcp_serviceusage_service - added backoff when checking for operation completion.
- gcp_serviceusage_service - use alloyb API for the integration test as spanner conflicts with other tests
- gcp_sql_ssl_cert - made sha1_fingerprint optional, which enables resource creation
- gcp_storage_default_object_acl - removed non-existent fields; the resource is not usable.

grafana.grafana
~~~~~~~~~~~~~~~

- Add 'run_once' to download&unzip tasks by @v-zhuravlev in https://github.com/grafana/grafana-ansible-collection/pull/136
- Adding `oauth_allow_insecure_email_lookup` to fix oauth user sync error by @hypery2k in https://github.com/grafana/grafana-ansible-collection/pull/132
- Bump ansible-core from 2.15.4 to 2.15.8 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/137
- Bump ansible-lint from 6.13.1 to 6.14.3 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/139
- Bump ansible-lint from 6.14.3 to 6.22.2 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/142
- Bump ansible-lint from 6.22.2 to 24.2.0 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/150
- Bump cryptography from 41.0.4 to 41.0.6 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/126
- Bump jinja2 from 3.1.2 to 3.1.3 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/129
- Bump pylint from 2.16.2 to 3.0.3 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/141
- Bump pylint from 3.0.3 to 3.1.0 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/158
- Bump pylint from 3.0.3 to 3.1.0 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/161
- Bump the pip group across 1 directories with 1 update by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/156
- Bump yamllint from 1.29.0 to 1.33.0 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/140
- Bump yamllint from 1.29.0 to 1.33.0 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/143
- Bump yamllint from 1.33.0 to 1.34.0 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/151
- Bump yamllint from 1.33.0 to 1.35.1 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/155
- Bump yamllint from 1.33.0 to 1.35.1 by @dependabot in https://github.com/grafana/grafana-ansible-collection/pull/159
- Change handler to systemd by @v-zhuravlev in https://github.com/grafana/grafana-ansible-collection/pull/135
- Drop curl check by @v-zhuravlev in https://github.com/grafana/grafana-ansible-collection/pull/120
- ExecStartPre and EnvironmentFile settings to system unit file by @fabiiw05 in https://github.com/grafana/grafana-ansible-collection/pull/157
- Fix check mode for grafana role by @Boschung-Mecatronic-AG-Infrastructure in https://github.com/grafana/grafana-ansible-collection/pull/125
- Fix check mode in Grafana Agent by @AmandaCameron in https://github.com/grafana/grafana-ansible-collection/pull/124
- Fix links in grafana_agent/defaults/main.yaml by @PabloCastellano in https://github.com/grafana/grafana-ansible-collection/pull/134
- Topic/grafana agent idempotency by @ohdearaugustin in https://github.com/grafana/grafana-ansible-collection/pull/147
- Update tags in README by @ishanjainn in https://github.com/grafana/grafana-ansible-collection/pull/121
- datasources url parameter fix by @dergudzon in https://github.com/grafana/grafana-ansible-collection/pull/162

hetzner.hcloud
~~~~~~~~~~~~~~

- Add the `hetzner.hcloud.all` group to configure all the modules using `module_defaults`.
- Allow to set the `api_endpoint` module argument using the `HCLOUD_ENDPOINT` environment variable.
- Removed the `hcloud_` prefix from all modules names, e.g. `hetzner.hcloud.hcloud_firewall` was renamed to `hetzner.hcloud.firewall`. Old module names will continue working.
- Renamed the `endpoint` module argument to `api_endpoint`, backward compatibility is maintained using an alias.
- Replace deprecated `ansible.netcommon` ip utils with python `ipaddress` module. The `ansible.netcommon` collection is no longer required by the collections.
- firewall - Allow forcing the deletion of firewalls that are still in use.
- firewall - Do not silence 'firewall still in use' delete failures.
- firewall - Return resources the firewall is `applied_to`.
- firewall_info - Add new `firewall_info` module to gather firewalls info.
- firewall_resource - Add new `firewall_resource` module to manage firewalls resources.
- hcloud inventory - Add the `api_endpoint` option.
- hcloud inventory - Deprecate the `api_token_env` option, suggest using a lookup plugin (`{{ lookup('ansible.builtin.env', 'YOUR_ENV_VAR') }}`) or use the well-known `HCLOUD_TOKEN` environment variable name.
- hcloud inventory - Rename the `token_env` option to `api_token_env`, use aliases for backward compatibility.
- hcloud inventory - Rename the `token` option to `api_token`, use aliases for backward compatibility.
- inventory - Add `hostname` option used to template the hostname of the instances.
- inventory - Add `hostvars_prefix` and hostvars_suffix` options to customize the inventory host variables keys.
- network - Allow renaming networks.

ibm.storage_virtualize
~~~~~~~~~~~~~~~~~~~~~~

- ibm_sv_manage_replication_policy - Added support to configure a 2-site-ha policy.
- ibm_sv_manage_snapshot - Added support to restore entire volumegroup from a snapshot of that volumegroup.
- ibm_sv_manage_snapshot - Added support to restore subset of volumes of a volumegroup from a snapshot
- ibm_svc_host - Added support to create nvmetcp host.
- ibm_svc_info - Added support to display information about partition, quorum, IO group, VG replication and enclosure, snmp server and ldap server
- ibm_svc_info - Added support to display information about thinclone/clone volumes and volumegroups.
- ibm_svc_manage_volume - Added support to create clone or thinclone from snapshot
- ibm_svc_manage_volumgroup - Added support to create clone or thinkclone volumegroup from snapshot from a subset of volumes
- ibm_svc_manage_volumgroup - Added support to delete volumegroups keeping volumes via 'evictvolumes'.

inspur.ispim
~~~~~~~~~~~~

- Modify edit_smtp_com and add description information.

kubernetes.core
~~~~~~~~~~~~~~~

- helm - add ``reuse_values`` and ``reset_values`` support to helm module (https://github.com/ansible-collections/kubernetes.core/issues/394).
- k8s - add new option ``delete_all`` to support deletion of all resources when state is set to ``absent``. (https://github.com/ansible-collections/kubernetes.core/issues/504)
- k8s, k8s_info - add a hidden_fields option to allow fields to be hidden in the results of k8s and k8s_info
- k8s_drain - add ability to filter the list of pods to be drained by a pod label selector (https://github.com/ansible-collections/kubernetes.core/issues/474).

lowlydba.sqlserver
~~~~~~~~~~~~~~~~~~

- Add ability to prevent changing login's password, even if password supplied.
- Add new input strings to be compatible with dbops v0.9.x (https://github.com/lowlydba/lowlydba.sqlserver/pull/231)

microsoft.ad
~~~~~~~~~~~~

- Added ``group/microsoft.ad.domain`` module defaults group for the ``computer``, ``group``, ``object_info``, ``object``, ``ou``, and ``user`` module. Users can use this defaults group to set common connection options for these modules such as the ``domain_server``, ``domain_username``, and ``domain_password`` options.
- Added support for Jinja2 templating in ldap inventory.
- Make ``name`` an optional parameter for the AD modules. Either ``name`` or ``identity`` needs to be set with their respective behaviours. If creating a new AD user and only ``identity`` is set, that will be the value used for the name of the object.
- Set minimum supported Ansible version to 2.14 to align with the versions still supported by Ansible.
- object_info - Add ActiveDirectory module import

netapp.ontap
~~~~~~~~~~~~

- na_ontap_cifs_server - new option `is_multichannel_enabled` added in REST, requires ONTAP 9.10 or later.
- na_ontap_cifs_server - new option `lm_compatibility_level` added in REST, requires ONTAP 9.8 or later.
- na_ontap_cluster - new option `certificate.uuid` added in REST, requires ONTAP 9.10 or later.
- na_ontap_cluster_peer - added REST only support for modifying remote intercluster addresses in cluster peer relation.
- na_ontap_ems_destination - new options `syslog`, `port`, `transport`, `message_format`, `timestamp_format_override` and `hostname_format_override` added in REST, requires ONTAP 9.12.1 or later.
- na_ontap_export_policy_rule - added `actions` and `modify` in module output.
- na_ontap_file_security_permissions_acl - added `actions` and `modify` in module output.
- na_ontap_igroup_initiator - added `actions` in module output.
- na_ontap_lun_map - added `actions` in module output.
- na_ontap_lun_map_reporting_nodes - added `actions` in module output.
- na_ontap_name_mappings - added `actions` and `modify` in module output.
- na_ontap_node - added `modify` in module output.
- na_ontap_rest_info - added warning message if given subset doesn't support option `owning_resource`.
- na_ontap_s3_services - create, modify S3 service returns `s3_service_info` in module output.
- na_ontap_snapmirror - updated resync and resume operation for synchronous snapmirror relationship in REST.
- na_ontap_storage_auto_giveback - added information on modified attributes in module output.
- na_ontap_vscan_scanner_pool - added REST support to Vscan Scanner Pools Configuration module, requires ONTAP 9.6 or later.

netapp.storagegrid
~~~~~~~~~~~~~~~~~~

- na_sg_grid_account - New option ``allow_select_object_content`` for enabling use of the S3 SelectObjectContent API.
- na_sg_grid_account - New option ``description`` for setting additional identifying information for the tenant account.

netbox.netbox
~~~~~~~~~~~~~

- CI - CI adjustments [#1154](https://github.com/netbox-community/ansible_modules/pull/1154) [#1155](https://github.com/netbox-community/ansible_modules/pull/1155) [#1157](https://github.com/netbox-community/ansible_modules/pull/1157)
- nb_inventory - Add facility group_by option [#1059](https://github.com/netbox-community/ansible_modules/pull/1059)
- nb_inventory - Enable ansible-vault strings in config-context data [#1114](https://github.com/netbox-community/ansible_modules/pull/1114)
- nb_lookup - Add new VPN endpoints for NetBox 3.7 support [#1162](https://github.com/netbox-community/ansible_modules/pull/1162)
- netbox_platform - Add config_template option to netbox_platform [#1119](https://github.com/netbox-community/ansible_modules/pull/1119)
- netbox_power_port_template - Add option module_type to netbox_power_port_template [#1105](https://github.com/netbox-community/ansible_modules/pull/1105)
- netbox_rack_role - Add description option [#1143](https://github.com/netbox-community/ansible_modules/pull/1143)
- netbox_virtual_disk - New module [#1153](https://github.com/netbox-community/ansible_modules/pull/1153)
- netbox_virtual_machine and netbox_device - Add option config_template [#1171](https://github.com/netbox-community/ansible_modules/pull/1171)

purestorage.flasharray
~~~~~~~~~~~~~~~~~~~~~~

- all - ``distro`` package added as a pre-requisite
- multiple - Remove packaging pre-requisite.
- multiple - Where only REST 2.x endpoints are used, convert to REST 2.x methodology.
- purefa_arrayname - Convert to REST v2
- purefa_dns - Added facility to add a CA certifcate to management DNS and check peer.
- purefa_eula - Only sign if not previously signed. From REST 2.30 name, title and company are no longer required
- purefa_info - Add NSID value for NVMe namespace in `hosts` response
- purefa_info - Add support for controller uptime from Purity//FA 6.6.3
- purefa_info - Expose NFS security flavor for policies
- purefa_info - Expose cloud capacity details if array is a Cloud Block Store.
- purefa_info - Subset `pgroups` now also provides a new dict called `deleted_pgroups`
- purefa_inventory - Convert to REST v2
- purefa_ntp - Convert to REST v2
- purefa_offload - Convert to REST v2
- purefa_offload - Remove `nfs` as an option when Purity//FA 6.6.0 or higher is detected
- purefa_pgsnap - Module now requires minimum FlashArray Purity//FA 6.1.0
- purefa_policy - Add SMB user based enumeration parameter
- purefa_policy - Added NFS security flavors for accessing files in the mount point.
- purefa_policy - Remove default setting for nfs_version to allow for change of version at policy level
- purefa_ra - Add ``present`` and ``absent`` as valid ``state`` options
- purefa_ra - Add connecting as valid status of RA to perform operations on
- purefa_ra - Convert to REST v2
- purefa_snap - Add support for suffix on remote offload snapshots
- purefa_syslog - ``name`` becomes a required parameter as module converts to full REST 2 support
- purefa_vnc - Convert to REST v2

purestorage.flashblade
~~~~~~~~~~~~~~~~~~~~~~

- purefb_bucket - Add support for public buckets
- purefb_bucket - Add support for strict 17a-4 WORM compliance.
- purefb_bucket - From REST 2.12 the `mode` parameter default changes to `multi-site-writable`.
- purefb_connect - Increase Fan-In and Fan-Out maximums
- purefb_ds - Add `force_bind_password` parameter to allow module to be idempotent.
- purefb_fs - Add ``group_ownership`` parameter from Purity//FB 4.4.0.
- purefb_fs - Added SMB Continuous Availability parameter. Requires REST 2.12 or higher.
- purefb_info - Added enhanced information for buckets, filesystems and snapshots, based on new features in REST 2.12
- purefb_info - Show array network access policy from Purity//FB 4.4.0
- purefb_policy - Add support for network access policies from Purity//FB 4.4.0
- purefb_s3acc - Add support for public buckets
- purefb_s3acc - Remove default requirements for ``hard_limit`` and ``default_hard_limit``

telekom_mms.icinga_director
~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Extended docs and examples for multiple assign_filter conditions (https://github.com/telekom-mms/ansible-collection-icinga-director/pull/227)
- Increase sleep to 5 seconds (https://github.com/telekom-mms/ansible-collection-icinga-director/pull/245)

theforeman.foreman
~~~~~~~~~~~~~~~~~~

- content_view_publish role - allow passing ``async`` and ``poll`` to the module (https://github.com/theforeman/foreman-ansible-modules/pull/1676)
- convert2rhel role - install ``convert2rhel`` from ``cdn-public.redhat.com``, dropping the requirement of a custom CA cert

vmware.vmware_rest
~~~~~~~~~~~~~~~~~~

- Add requires_ansible to manifest (https://github.com/ansible-community/ansible.content_builder/pull/76).
- Generate action_groups for the vmware.vmware_rest collection (https://github.com/ansible-community/ansible.content_builder/issues/75).
- Use 7.0 U3 API spec to build the modules (https://github.com/ansible-collections/vmware.vmware_rest/pull/449).
- Use folder attribute for host and dc module only (https://github.com/ansible-community/ansible.content_builder/pull/79).

vultr.cloud
~~~~~~~~~~~

- Added retry on HTTP 504 returned by the API (https://github.com/vultr/ansible-collection-vultr/pull/104).
- Implemented a feature to distinguish resources by region if available. This allows to have identical name per region e.g. a VPC named ``default`` in each region. (https://github.com/vultr/ansible-collection-vultr/pull/98).
- instance - Added a new param ``user_scheme`` to change user scheme to non-root on Linux while creating the instance (https://github.com/vultr/ansible-collection-vultr/issues/96).

Breaking Changes / Porting Guide
--------------------------------

Ansible-core
~~~~~~~~~~~~

- assert - Nested templating may result in an inability for the conditional to be evaluated. See the porting guide for more information.

cloud.common
~~~~~~~~~~~~

- Bump minimum Python supported version to 3.9.
- Remove support for ansible-core < 2.14.

community.ciscosmb
~~~~~~~~~~~~~~~~~~

- in facts of interface 'bandwith' changed to 'bandwidth'

community.okd
~~~~~~~~~~~~~

- Bump minimum Python suupported version to 3.9 (https://github.com/openshift/community.okd/pull/202).
- Remove support for ansible-core < 2.14 (https://github.com/openshift/community.okd/pull/202).

hetzner.hcloud
~~~~~~~~~~~~~~

- Drop support for ansible-core 2.13.
- certificate - The `not_valid_before` and `not_valid_after` values are now returned as ISO-8601 formatted strings.
- certificate_info - The `not_valid_before` and `not_valid_after` values are now returned as ISO-8601 formatted strings.
- inventory - Remove the deprecated `api_token_env` option, you may use the `ansible.builtin.env` lookup as alternative.
- iso_info - The `deprecated` value is now returned as ISO-8601 formatted strings.

kubernetes.core
~~~~~~~~~~~~~~~

- Remove support for ansible-core < 2.14
- Update python kubernetes library to 24.2.0, helm/kind-action to 1.8.0, kubernetes >= 1.24.

theforeman.foreman
~~~~~~~~~~~~~~~~~~

- content_view_filter - stop managing rules from this module, ``content_view_filter_rule`` should be used for that
- inventory plugin - do not default to ``http://localhost:3000`` as the Foreman URL, providing a URL is now mandatory

vmware.vmware_rest
~~~~~~~~~~~~~~~~~~

- Remove support for ansible-core < 2.14

Deprecated Features
-------------------

- The ``inspur.sm`` collection is considered unmaintained and will be removed from Ansible 11 if no one starts maintaining it again before Ansible 11. See `the removal process for details on how this works <https://github.com/ansible-collections/overview/blob/main/removal_from_ansible.rst#cancelling-removal-of-an-unmaintained-collection>`__ (https://forum.ansible.com/t/2854).
- The ``netapp.storagegrid`` collection is considered unmaintained and will be removed from Ansible 11 if no one starts maintaining it again before Ansible 11. See `the removal process for details on how this works <https://github.com/ansible-collections/overview/blob/main/removal_from_ansible.rst#cancelling-removal-of-an-unmaintained-collection>`__ (https://forum.ansible.com/t/2811).

Ansible-core
~~~~~~~~~~~~

- Old style vars plugins which use the entrypoints `get_host_vars` or `get_group_vars` are deprecated. The plugin should be updated to inherit from `BaseVarsPlugin` and define a `get_vars` method as the entrypoint.
- The 'required' parameter in 'ansible.module_utils.common.process.get_bin_path' API is deprecated (https://github.com/ansible/ansible/issues/82464).
- ``module_utils`` - importing the following convenience helpers from ``ansible.module_utils.basic`` has been deprecated: ``get_exception``, ``literal_eval``, ``_literal_eval``, ``datetime``, ``signal``, ``types``, ``chain``, ``repeat``, ``PY2``, ``PY3``, ``b``, ``binary_type``, ``integer_types``, ``iteritems``, ``string_types``, ``test_type``, ``map`` and ``shlex_quote``.
- ansible-doc - role entrypoint attributes are deprecated and eventually will no longer be shown in ansible-doc from ansible-core 2.20 on (https://github.com/ansible/ansible/issues/82639, https://github.com/ansible/ansible/pull/82678).
- paramiko connection plugin, configuration items in the global scope are being deprecated and will be removed in favor or the existing same options in the plugin itself. Users should not need to change anything (how to configure them are the same) but plugin authors using the global constants should move to using the plugin's get_option().

amazon.aws
~~~~~~~~~~

- iam_role_info - in a release after 2026-05-01 paths must begin and end with ``/`` (https://github.com/ansible-collections/amazon.aws/pull/1998).

community.crypto
~~~~~~~~~~~~~~~~

- openssl_csr_pipe, openssl_privatekey_pipe, x509_certificate_pipe - the current behavior of check mode is deprecated and will change in community.crypto 3.0.0. The current behavior is similar to the modules without ``_pipe``: if the object needs to be (re-)generated, only the ``changed`` status is set, but the object is not updated. From community.crypto 3.0.0 on, the modules will ignore check mode and always act as if check mode is not active. This behavior can already achieved now by adding ``check_mode: false`` to the task. If you think this breaks your use-case of this module, please `create an issue in the community.crypto repository <https://github.com/ansible-collections/community.crypto/issues/new/choose>`__ (https://github.com/ansible-collections/community.crypto/issues/712, https://github.com/ansible-collections/community.crypto/pull/714).

community.dns
~~~~~~~~~~~~~

- hetzner_dns_records and hosttech_dns_records inventory plugins - the ``filters`` option has been renamed to ``simple_filters``. The old name will stop working in community.hrobot 2.0.0 (https://github.com/ansible-collections/community.dns/pull/181).

community.docker
~~~~~~~~~~~~~~~~

- docker_container - the default ``ignore`` for the ``image_name_mismatch`` parameter has been deprecated and will switch to ``recreate`` in community.docker 4.0.0. A deprecation warning will be printed in situations where the default value is used and where a behavior would change once the default changes (https://github.com/ansible-collections/community.docker/pull/703).

community.general
~~~~~~~~~~~~~~~~~

- consul_acl - the module has been deprecated and will be removed in community.general 10.0.0. ``consul_token`` and ``consul_policy`` can be used instead (https://github.com/ansible-collections/community.general/pull/7901).

community.hrobot
~~~~~~~~~~~~~~~~

- robot inventory plugin - the ``filters`` option has been renamed to ``simple_filters``. The old name will stop working in community.hrobot 2.0.0 (https://github.com/ansible-collections/community.hrobot/pull/94).

community.okd
~~~~~~~~~~~~~

- openshift - the ``openshift`` inventory plugin has been deprecated and will be removed in release 4.0.0 (https://github.com/ansible-collections/kubernetes.core/issues/31).

dellemc.openmanage
~~~~~~~~~~~~~~~~~~

- The ``dellemc_idrac_storage_volume`` module is deprecated and replaced with ``idrac_storage_volume``.

kubernetes.core
~~~~~~~~~~~~~~~

- k8s - the ``k8s`` inventory plugin has been deprecated and will be removed in release 4.0.0 (https://github.com/ansible-collections/kubernetes.core/issues/31).

Removed Features (previously deprecated)
----------------------------------------

- The ``gluster.gluster`` collection was considered unmaintained and removed from Ansible 10 (https://github.com/ansible-community/community-topics/issues/225). Users can still install this collection with ``ansible-galaxy collection install gluster.gluster``.
- The ``hpe.nimble`` collection was considered unmaintained and removed from Ansible 10 (https://github.com/ansible-community/community-topics/issues/254). Users can still install this collection with ``ansible-galaxy collection install hpe.nimble``.
- The ``netapp.aws`` collection was considered unmaintained and removed from Ansible 10 (https://github.com/ansible-community/community-topics/issues/223). Users can still install this collection with ``ansible-galaxy collection install netapp.aws``.
- The ``netapp.azure`` collection was considered unmaintained and removed from Ansible 10 (https://github.com/ansible-community/community-topics/issues/234). Users can still install this collection with ``ansible-galaxy collection install netapp.azure``.
- The ``netapp.elementsw`` collection was considered unmaintained and removed from Ansible 10 (https://github.com/ansible-community/community-topics/issues/235). Users can still install this collection with ``ansible-galaxy collection install netapp.elementsw``.
- The ``netapp.um_info`` collection was considered unmaintained and removed from Ansible 10 (https://github.com/ansible-community/community-topics/issues/244). Users can still install this collection with ``ansible-galaxy collection install netapp.um_info``.
- The deprecated ``community.azure`` collection has been removed. There is a successor collection ``azure.azcollection`` in the community package which should cover the same functionality.
- The deprecated ``community.sap`` collection has been removed from Ansible 10 (https://github.com/ansible-community/community-topics/issues/247). There is a successor collection ``community.sap_libs`` in the community package which should cover the same functionality.
- The deprecated ``purestorage.fusion`` collection has been removed (https://forum.ansible.com/t/3712).

Ansible-core
~~~~~~~~~~~~

- Remove deprecated APIs from ansible-docs (https://github.com/ansible/ansible/issues/81716).
- Remove deprecated JINJA2_NATIVE_WARNING environment variable (https://github.com/ansible/ansible/issues/81714)
- Remove deprecated ``scp_if_ssh`` from ssh connection plugin (https://github.com/ansible/ansible/issues/81715).
- Remove deprecated crypt support from ansible.utils.encrypt (https://github.com/ansible/ansible/issues/81717)
- With the removal of Python 2 support, the yum module and yum action plugin are removed and redirected to ``dnf``.

arista.eos
~~~~~~~~~~

- Remove depreacted eos_bgp module which is replaced with eos_bgp_global and eos_bgp_address_family.
- Remove deprecated eos_logging module which is replaced with eos_logging_global resource module.
- Remove deprecated timers.throttle attribute.

cisco.ios
~~~~~~~~~

- Deprecated ios_ntp module in favor of ios_ntp_global.
- Removed previously deprecated ios_bgp module in favor of ios_bgp_global and ios_bgp_address_family.

cisco.iosxr
~~~~~~~~~~~

- Remove deprecated iosxr_logging module which is replaced with iosxr_logging_global resource module.

cisco.nxos
~~~~~~~~~~

- The nxos_logging module has been removed with this release.
- The nxos_ntp module has been removed with this release.
- The nxos_ntp_auth module has been removed with this release.
- The nxos_ntp_options module has been removed with this release.

junipernetworks.junos
~~~~~~~~~~~~~~~~~~~~~

- Remove deprected junos_logging module which is replaced by junos_logging_global resource module.

Security Fixes
--------------

Ansible-core
~~~~~~~~~~~~

- ANSIBLE_NO_LOG - Address issue where ANSIBLE_NO_LOG was ignored (CVE-2024-0690)
- ansible-galaxy - Prevent roles from using symlinks to overwrite files outside of the installation directory (CVE-2023-5115)
- templating - Address issues where internal templating can cause unsafe variables to lose their unsafe designation (CVE-2023-5764)

community.dns
~~~~~~~~~~~~~

- hosttech_dns_records and hetzner_dns_records inventory plugins - make sure all data received from the remote servers is marked as unsafe, so remote code execution by obtaining texts that can be evaluated as templates is not possible (https://www.die-welt.net/2024/03/remote-code-execution-in-ansible-dynamic-inventory-plugins/, https://github.com/ansible-collections/community.dns/pull/189).

community.docker
~~~~~~~~~~~~~~~~

- docker_containers, docker_machine, and docker_swarm inventory plugins - make sure all data received from the Docker daemon / Docker machine is marked as unsafe, so remote code execution by obtaining texts that can be evaluated as templates is not possible (https://www.die-welt.net/2024/03/remote-code-execution-in-ansible-dynamic-inventory-plugins/, https://github.com/ansible-collections/community.docker/pull/815).

community.general
~~~~~~~~~~~~~~~~~

- cobbler, gitlab_runners, icinga2, linode, lxd, nmap, online, opennebula, proxmox, scaleway, stackpath_compute, virtualbox, and xen_orchestra inventory plugin - make sure all data received from the remote servers is marked as unsafe, so remote code execution by obtaining texts that can be evaluated as templates is not possible (https://www.die-welt.net/2024/03/remote-code-execution-in-ansible-dynamic-inventory-plugins/, https://github.com/ansible-collections/community.general/pull/8098).

community.hrobot
~~~~~~~~~~~~~~~~

- robot inventory plugin - make sure all data received from the Hetzner robot service server is marked as unsafe, so remote code execution by obtaining texts that can be evaluated as templates is not possible (https://www.die-welt.net/2024/03/remote-code-execution-in-ansible-dynamic-inventory-plugins/, https://github.com/ansible-collections/community.hrobot/pull/99).

Bugfixes
--------

Ansible-core
~~~~~~~~~~~~

- All core lookups now use set_option(s) even when doing their own custom parsing. This ensures that the options are always the proper type.
- Allow for searching handler subdir for included task via include_role (https://github.com/ansible/ansible/issues/81722)
- AnsibleModule.atomic_move - fix preserving extended ACLs of the destination when it exists (https://github.com/ansible/ansible/issues/72929).
- Cache host_group_vars after instantiating it once and limit the amount of repetitive work it needs to do every time it runs.
- Call PluginLoader.all() once for vars plugins, and load vars plugins that run automatically or are enabled specifically by name subsequently.
- Consolidate systemd detection logic into one place (https://github.com/ansible/ansible/issues/80975).
- Consolidated the list of internal static vars, centralized them as constant and completed from some missing entries.
- Do not print undefined error message twice (https://github.com/ansible/ansible/issues/78703).
- Enable file cache for vaulted files during vars lookup to fix a strong performance penalty in huge and complex playbboks.
- Fix NEVRA parsing of package names that include digit(s) in them (https://github.com/ansible/ansible/issues/76463, https://github.com/ansible/ansible/issues/81018)
- Fix ``force_handlers`` not working with ``any_errors_fatal`` (https://github.com/ansible/ansible/issues/36308)
- Fix ``run_once`` being incorrectly interpreted on handlers (https://github.com/ansible/ansible/issues/81666)
- Fix an issue when setting a plugin name from an unsafe source resulted in ``ValueError: unmarshallable object`` (https://github.com/ansible/ansible/issues/82708)
- Fix check for missing _sub_plugin attribute in older connection plugins (https://github.com/ansible/ansible/pull/82954)
- Fix condition for unquoting configuration strings from ini files (https://github.com/ansible/ansible/issues/82387).
- Fix for when ``any_errors_fatal`` was ignored if error occurred in a block with always (https://github.com/ansible/ansible/issues/31543)
- Fix handling missing urls in ansible.module_utils.urls.fetch_file for Python 3.
- Fix issue where an ``include_tasks`` handler in a role was not able to locate a file in ``tasks/`` when ``tasks_from`` was used as a role entry point and ``main.yml`` was not present (https://github.com/ansible/ansible/issues/82241)
- Fix issues when tasks withing nested blocks wouldn't run when ``force_handlers`` is set (https://github.com/ansible/ansible/issues/81533)
- Fix loading vars_plugins in roles (https://github.com/ansible/ansible/issues/82239).
- Fix notifying role handlers by listen keyword topics with the "role_name : " prefix (https://github.com/ansible/ansible/issues/82849).
- Fix setting proper locale for git executable when running on non english systems, ensuring git output can always be parsed.
- Fix tasks in always section not being executed for nested blocks with ``any_errors_fatal`` (https://github.com/ansible/ansible/issues/73246)
- Fixes permission for cache json file from 600 to 644 (https://github.com/ansible/ansible/issues/82683).
- Give the tombstone error for ``include`` pre-fork like other tombstoned action/module plugins.
- Harden python templates for respawn and ansiballz around str literal quoting
- Include the task location when a module or action plugin is deprecated (https://github.com/ansible/ansible/issues/82450).
- Interpreter discovery - Add ``Amzn`` to ``OS_FAMILY_MAP`` for correct family fallback for interpreter discovery (https://github.com/ansible/ansible/issues/80882).
- Mirror the behavior of dnf on the command line when handling NEVRAs with omitted epoch (https://github.com/ansible/ansible/issues/71808)
- Plugin loader does not dedupe nor cache filter/test plugins by file basename, but full path name.
- Properly template tags in parent blocks (https://github.com/ansible/ansible/issues/81053)
- Provide additional information about the alternative plugin in the deprecation message (https://github.com/ansible/ansible/issues/80561).
- Remove the galaxy_info field ``platforms`` from the role templates (https://github.com/ansible/ansible/issues/82453).
- Restoring the ability of filters/tests can have same file base name but different tests/filters defined inside.
- Reword the error message when the module fails to parse parameters in JSON format (https://github.com/ansible/ansible/issues/81188).
- Reword warning if the reserved keyword _ansible_ used as a module parameter (https://github.com/ansible/ansible/issues/82514).
- Run all handlers with the same ``listen`` topic, even when notified from another handler (https://github.com/ansible/ansible/issues/82363).
- Slight optimization to hostvars (instantiate template only once per host, vs per call to var).
- Stopped misleadingly advertising ``async`` mode support in the ``reboot`` module (https://github.com/ansible/ansible/issues/71517).
- ``ansible-galaxy role import`` - fix using the ``role_name`` in a standalone role's ``galaxy_info`` metadata by disabling automatic removal of the ``ansible-role-`` prefix. This matches the behavior of the Galaxy UI which also no longer implicitly removes the ``ansible-role-`` prefix. Use the ``--role-name`` option or add a ``role_name`` to the ``galaxy_info`` dictionary in the role's ``meta/main.yml`` to use an alternate role name.
- ``ansible-test sanity --test runtime-metadata`` - add ``action_plugin`` as a valid field for modules in the schema (https://github.com/ansible/ansible/pull/82562).
- ``ansible.module_utils.service`` - ensure binary data transmission in ``daemonize()``
- ``any_errors_fatal`` should fail all hosts and rescue all of them when a ``rescue`` section is specified (https://github.com/ansible/ansible/issues/80981)
- ``include_role`` - properly execute ``v2_playbook_on_include`` and ``v2_runner_on_failed`` callbacks as well as increase ``ok`` and ``failed`` stats in the play recap, when appropriate (https://github.com/ansible/ansible/issues/77336)
- allow_duplicates - fix evaluating if the current role allows duplicates instead of using the initial value from the duplicate's cached role.
- ansible-config init will now dedupe ini entries from plugins.
- ansible-galaxy - Deprecate use of the Galaxy v2 API (https://github.com/ansible/ansible/issues/81781)
- ansible-galaxy - Provide a better error message when using a requirements file with an invalid format - https://github.com/ansible/ansible/issues/81901
- ansible-galaxy - Resolve issue with the dataclass used for galaxy.yml manifest caused by using future annotations
- ansible-galaxy - ensure path to ansible collection when installing or downloading doesn't have a backslash (https://github.com/ansible/ansible/pull/79705).
- ansible-galaxy - started allowing the use of pre-releases for collections that do not have any stable versions published. (https://github.com/ansible/ansible/pull/81606)
- ansible-galaxy - started allowing the use of pre-releases for dependencies on any level of the dependency tree that specifically demand exact pre-release versions of collections and not version ranges. (https://github.com/ansible/ansible/pull/81606)
- ansible-galaxy error on dependency resolution will not error itself due to 'virtual' collections not having a name/namespace.
- ansible-galaxy info - fix reporting no role found when lookup_role_by_name returns None.
- ansible-galaxy role import - exit with 1 when the import fails (https://github.com/ansible/ansible/issues/82175).
- ansible-galaxy role install - fix installing roles from Galaxy that have version ``None`` (https://github.com/ansible/ansible/issues/81832).
- ansible-galaxy role install - normalize tarfile paths and symlinks using ``ansible.utils.path.unfrackpath`` and consider them valid as long as the realpath is in the tarfile's role directory (https://github.com/ansible/ansible/issues/81965).
- ansible-inventory - index available_hosts for major performance boost when dumping large inventories
- ansible-pull now will expand relative paths for the ``-d|--directory`` option is now expanded before use.
- ansible-pull will now correctly handle become and connection password file options for ansible-playbook.
- ansible-test - Add a ``pylint`` plugin to work around a known issue on Python 3.12.
- ansible-test - Explicitly supply ``ControlPath=none`` when setting up port forwarding over SSH to address the scenario where the local ssh configuration uses ``ControlPath`` for all hosts, and would prevent ports to be forwarded after the initial connection to the host.
- ansible-test - Fix parsing of cgroup entries which contain a ``:`` in the path (https://github.com/ansible/ansible/issues/81977).
- ansible-test - Include missing ``pylint`` requirements for Python 3.10.
- ansible-test - Properly detect docker host when using ``ssh://`` protocol for connecting to the docker daemon.
- ansible-test - The ``libexpat`` package is automatically upgraded during remote bootstrapping to maintain compatibility with newer Python packages.
- ansible-test - The ``validate-modules`` sanity test no longer attempts to process files with unrecognized extensions as Python (resolves https://github.com/ansible/ansible/issues/82604).
- ansible-test - Update ``pylint`` to version 3.0.1.
- ansible-test ansible-doc sanity test - do not remove underscores from plugin names in collections before calling ``ansible-doc`` (https://github.com/ansible/ansible/pull/82574).
- ansible-test validate-modules sanity test - do not treat leading underscores for plugin names in collections as an attempted deprecation (https://github.com/ansible/ansible/pull/82575).
- ansible-test — Python 3.8–3.12 will use ``coverage`` v7.3.2.
- ansible.builtin.apt - calling clean = true does not properly clean certain cache files such as /var/cache/apt/pkgcache.bin and /var/cache/apt/pkgcache.bin (https://github.com/ansible/ansible/issues/82611)
- ansible.builtin.uri - the module was ignoring the ``force`` parameter and always requesting a cached copy (via the ``If-Modified-Since`` header) when downloading to an existing local file. Disable caching when ``force`` is ``true``, as documented (https://github.com/ansible/ansible/issues/82166).
- apt - honor install_recommends and dpkg_options while installing python3-apt library (https://github.com/ansible/ansible/issues/40608).
- apt - install recommended packages when installing package via deb file (https://github.com/ansible/ansible/issues/29726).
- apt_repository - do not modify repo files if the file is a symlink (https://github.com/ansible/ansible/issues/49809).
- apt_repository - update PPA URL to point to https URL (https://github.com/ansible/ansible/issues/82463).
- assemble - fixed missing parameter 'content' in _get_diff_data API (https://github.com/ansible/ansible/issues/82359).
- async - Fix bug that stopped running async task in ``--check`` when ``check_mode: False`` was set as a task attribute - https://github.com/ansible/ansible/issues/82811
- blockinfile - when ``create=true`` is used with a filename without path, the module crashed (https://github.com/ansible/ansible/pull/81638).
- check if there are attributes to set before attempting to set them (https://github.com/ansible/ansible/issues/76727)
- copy action now also generates temprary files as hidden ('.' prefixed) to avoid accidental pickup by running services that glob by extension.
- copy action now ensures that tempfiles use the same suffix as destination, to allow for ``validate`` to work with utilities that check extensions.
- deb822_repository - handle idempotency if the order of parameters is changed (https://github.com/ansible/ansible/issues/82454).
- debconf - allow user to specify a list for value when vtype is multiselect (https://github.com/ansible/ansible/issues/81345).
- delegate_to when set to an empty or undefined variable will now give a proper error.
- distribution.py - Recognize ALP-Dolomite as part of the SUSE OS family in Ansible, fixing its previous misidentification (https://github.com/ansible/ansible/pull/82496).
- distro - bump bundled distro version from 1.6.0 to 1.8.0 (https://github.com/ansible/ansible/issues/81713).
- dnf - fix an issue when cached RPMs were left in the cache directory even when the keepcache setting was unset (https://github.com/ansible/ansible/issues/81954)
- dnf - fix an issue when installing a package by specifying a file it provides could result in installing a different package providing the same file than the package already installed resulting in resolution failure (https://github.com/ansible/ansible/issues/82461)
- dnf - properly set gpg check options on enabled repositories according to the ``disable_gpg_check`` option (https://github.com/ansible/ansible/issues/80110)
- dnf - properly skip unavailable packages when ``skip_broken`` is enabled (https://github.com/ansible/ansible/issues/80590)
- dnf - the ``nobest`` option only overrides the distribution default when explicitly used, and is used for all supported operations (https://github.com/ansible/ansible/issues/82616)
- dnf5 - respect ``allow_downgrade`` when installing packages directly from rpm files
- dnf5 - the ``nobest`` option only overrides the distribution default when used
- dwim functions for lookups should be better at detectging role context even in abscense of tasks/main.
- expect - fix argument spec error using timeout=null (https://github.com/ansible/ansible/issues/80982).
- fact gathering on linux now handles thread count by using rounding vs dropping decimals, it should give slightly more accurate numbers.
- facts - detect VMware ESXi 8.0 virtualization by product name VMware20,1
- fetch - Do not calculate the file size for Windows fetch targets to improve performance.
- fetch - add error message when using ``dest`` with a trailing slash that becomes a local directory - https://github.com/ansible/ansible/issues/82878
- find - do not fail on Permission errors (https://github.com/ansible/ansible/issues/82027).
- first_found lookup now always returns a full (absolute) and normalized path
- first_found lookup now always takes into account k=v options
- flush_handlers - properly handle a handler failure in a nested block when ``force_handlers`` is set (http://github.com/ansible/ansible/issues/81532)
- galaxy - skip verification for unwanted Python compiled bytecode files (https://github.com/ansible/ansible/issues/81628).
- handle exception raised while validating with elements='int' and value is not within choices (https://github.com/ansible/ansible/issues/82776).
- include_tasks - include `ansible_loop_var` and `ansible_index_var` in a loop (https://github.com/ansible/ansible/issues/82655).
- include_vars - fix calculating ``depth`` relative to the root and ensure all files are included (https://github.com/ansible/ansible/issues/80987).
- interpreter_discovery - handle AnsibleError exception raised while interpreter discovery (https://github.com/ansible/ansible/issues/78264).
- iptables - add option choices 'src,src' and 'dst,dst' in match_set_flags (https://github.com/ansible/ansible/issues/81281).
- iptables - set jump to DSCP when set_dscp_mark or set_dscp_mark_class is set (https://github.com/ansible/ansible/issues/77077).
- known_hosts - Fix issue with `@cert-authority` entries in known_hosts incorrectly being removed.
- module no_log will no longer affect top level booleans, for example ``no_log_module_parameter='a'`` will no longer hide ``changed=False`` as a 'no log value' (matches 'a').
- moved assemble, raw, copy, fetch, reboot, script and wait_for_connection to query task instead of play_context ensuring they get the lastest and most correct data.
- reboot action now handles connections with 'timeout' vs only 'connection_timeout' settings.
- role params now have higher precedence than host facts again, matching documentation, this had unintentionally changed in 2.15.
- roles, code cleanup and performance optimization of dependencies, now cached,  and ``public`` setting is now determined once, at role instantiation.
- roles, the ``static`` property is now correctly set, this will fix issues with ``public`` and ``DEFAULT_PRIVATE_ROLE_VARS`` controls on exporting vars.
- set_option method for plugins to update config now properly passes through type casting and validation.
- ssh - add tests for the SSH connection plugin.
- support url-encoded credentials in URLs like http://x%40:%40@example.com (https://github.com/ansible/ansible/pull/82552)
- syslog - Handle ValueError exception raised when sending Null Characters to syslog with Python 3.12.
- systemd_services - update documentation regarding required_one_of and required_by parameters (https://github.com/ansible/ansible/issues/82914).
- template - Fix error when templating an unsafe string which corresponds to an invalid type in Python (https://github.com/ansible/ansible/issues/82600).
- template action will also inherit the behavior from copy (as it uses it internally).
- templating - ensure syntax errors originating from a template being compiled into Python code object result in a failure (https://github.com/ansible/ansible/issues/82606)
- unarchive - add support for 8 character permission strings for zip archives (https://github.com/ansible/ansible/pull/81705).
- unarchive - force unarchive if symlink target changes (https://github.com/ansible/ansible/issues/30420).
- unarchive modules now uses zipinfo options without relying on implementation defaults, making it more compatible with all OS/distributions.
- unsafe data - Address an incompatibility when iterating or getting a single index from ``AnsibleUnsafeBytes``
- unsafe data - Address an incompatibility with ``AnsibleUnsafeText`` and ``AnsibleUnsafeBytes`` when pickling with ``protocol=0``
- unsafe data - Enable directly using ``AnsibleUnsafeText`` with Python ``pathlib`` (https://github.com/ansible/ansible/issues/82414)
- uri action plugin now skipped during check mode (not supported) instead of even trying to execute the module, which already skipped, this does not really change the result, but returns much faster.
- vars - handle exception while combining VarsWithSources and dict (https://github.com/ansible/ansible/issues/81659).
- wait_for should not handle 'non mmapable files' again.
- winrm - Better handle send input failures when communicating with hosts under load
- winrm - Do not raise another exception during cleanup when a task is timed out - https://github.com/ansible/ansible/issues/81095
- winrm - does not hang when attempting to get process output when stdin write failed

amazon.aws
~~~~~~~~~~

- backup_plan - Fix idempotency issue when using botocore >= 1.31.36 (https://github.com/ansible-collections/amazon.aws/issues/1952).
- cloudwatchevent_rule - Fix to avoid adding quotes to JSON input for provided input_template (https://github.com/ansible-collections/amazon.aws/pull/1883).
- cloudwatchlogs_log_group_info - Implement exponential backoff when making API calls to prevent throttling exceptions (https://github.com/ansible-collections/amazon.aws/issues/2011).
- ec2_vpc_subnet - cleanly handle failure when subnet isn't created in time (https://github.com/ansible-collections/amazon.aws/pull/1848).
- iam_managed_policy - fixed an issue where only partial results were returned (https://github.com/ansible-collections/amazon.aws/pull/1936).
- lookup/secretsmanager_secret - fix the issue when the nested secret is missing and on_missing is set to warn, the lookup was raising an error instead of a warning message (https://github.com/ansible-collections/amazon.aws/issues/1781).
- module_utils/elbv2 - Fix issue when creating or modifying Load balancer rule type authenticate-oidc using ``ClientSecret`` parameter and ``UseExistingClientSecret=true`` (https://github.com/ansible-collections/amazon.aws/issues/1877).
- plugin_utils.inventory - Ensure templated options in lookup plugins are converted (https://github.com/ansible-collections/amazon.aws/issues/1955).
- plugins/inventory/aws_ec2 - Fix failure when retrieving information for more than 40 instances with use_ssm_inventory (https://github.com/ansible-collections/amazon.aws/issues/1713).
- s3_object - Fix the issue when copying an object with overriding metadata. (https://github.com/ansible-collections/amazon.aws/issues/1991).
- s3_object - Fix typo that caused false deprecation warning when setting ``overwrite=latest`` (https://github.com/ansible-collections/amazon.aws/pull/1847).
- s3_object - when doing a put and specifying ``Content-Type`` in metadata, this module (since 6.0.0) erroneously set the ``Content-Type`` to ``None`` causing the put to fail. Fix now correctly honours the specified ``Content-Type`` (https://github.com/ansible-collections/amazon.aws/issues/1881).

ansible.utils
~~~~~~~~~~~~~

- Avoid unnecessary use of persistent connection in `cli_parse`, `fact_diff`, `update_fact` and `validate` as this action does not require a connection.

ansible.windows
~~~~~~~~~~~~~~~

- Process.cs - Fix up the ``ProcessCreationFlags.CreateProtectedProcess`` typo in the enum name
- setup - Fix up typo ``collection -> collect`` when a timeout occurred during a fact subset
- win_acl - Fix broken path in case of volume junction
- win_get_url - Fix Tls1.3 getting removed from the list of security protocols
- win_powershell - Remove unecessary using in code causing stray error records in output - https://github.com/ansible-collections/ansible.windows/issues/571
- win_service_info - Warn and not fail if ERROR_FILE_NOT_FOUND when trying to query a service - https://github.com/ansible-collections/ansible.windows/issues/556
- win_updates - Fix up typo for Download progress event messages - https://github.com/ansible-collections/ansible.windows/issues/554

arista.eos
~~~~~~~~~~

- This fix is needed because static_routes and vlans are not returning anything when resources are not configured.
- This got noticed in this issue (https://github.com/network-automation/toolkit/issues/47)
- correct a missing whitespace and add 'auth' string.
- correct the parsing of the elements in 'name_servers' in 'eos_system' module.
- correct the reference of string attribute 'reference_bandwith'.
- when static_routes and vlans are not confirgured then return empty list.

check_point.mgmt
~~~~~~~~~~~~~~~~

- httpapi/checkpoint.py - Raise a fatal error if login wasn't successful.

cisco.aci
~~~~~~~~~

- Fix auto logout issue in aci connection plugin to keep connection active between tasks
- Fix idempotency for l3out configuration when l3protocol is used in aci_l3out
- Fix issues with new attributes in aci_interface_policy_leaf_policy_group module by adding conditions to include attributes in the payload only when they are specified by the user (#578)
- Fix query in aci_vmm_controller

cisco.asa
~~~~~~~~~

- Prevents module_defaults from were being incorrectly applied to the platform action, instead of the concerned module.

cisco.ios
~~~~~~~~~

- Prevents module_defaults from were being incorrectly applied to the platform action, instead of the concerned module.
- Updated the ios_ping ping module to support size param.
- ios_acls - Adds back existing remarks for an ace entry when updated with replaced or overridden state, as all remarks for a specific sequence gets removed when ace entry is updated.
- ios_acls - Fix replaced state to consider remarks and ace entries while comparing configuration.
- ios_acls - correctly match the different line for ACL without sequence number
- ios_acls - make sequence optional for rendering of standard acls.
- ios_acls - take correctly in case where we want to push an ACL from a different type
- ios_acls - update module to apply remarks entry with sequence numbers.
- ios_bgp_address_family - description attribute, evalutated as complex object casted to string.
- ios_bgp_global - Explicitly add neighbor address to every parser.
- ios_bgp_global - Shutdown attributes generates negate command on set as false.
- ios_bgp_global - description attribute, evalutated as complex object casted to string.
- ios_bgp_global - fix template attribute to generate configuration commands.
- ios_bgp_global - remote_as not mendatory for neighbors.
- ios_interfaces - description attribute, evalutated as complex object casted to string.
- ios_l3_interfaces - remove validation from ipv6 address parameter.
- ios_ospfv2 - Fix improper rendering of admin_distance attribute.
- ios_prefix_lists - description attribute, evalutated as complex object casted to string.
- ios_route_maps - description attribute, evalutated as complex object casted to string.
- ios_snmp_server - fix group and user IPv6 ACL commands.
- ios_snmp_server - fixed config issue with snmp user password update being idempotent on consecutive runs.
- ios_user - Fix configuration of hashed passwords and secrets.
- ios_user - fix configuration of user with hashed password.
- ios_user - fixed configuration removal of ssh users using purge.
- ios_vlans - Make behaviour of the action states consistent.
- ios_vlans - Top level configuration attribute is not required, the module works with vlan and vlan configuration both.
- ios_vlans - fixes behaviour of shutdown attribute with action states.
- ios_vrf - Update and add missing argspec keys that define the attributes.
- ios_vrf - added MDT related keys

cisco.iosxr
~~~~~~~~~~~

- Fix 'afi' value in bgp_templates RM to valid values.
- Fix issue in gathered state of interfaces and l3_interfaces RMs(https://github.com/ansible-collections/cisco.iosxr/issues/452, https://github.com/ansible-collections/cisco.iosxr/issues/451)

cisco.ise
~~~~~~~~~

- Added missing import re in endpoint module
- Updated to use ciscoisesdk v2.1.1 or newer fixing ciscoisesdk problem.
- ansible.utils changes to `">=2.0.0,<5.0"` in galaxy.yml dependencies.

cisco.meraki
~~~~~~~~~~~~

- Adding `network_clients_info` and `network_client_info`.
- Adding `platform_meraki.rst` to docs.
- Adding `product_types` for update request on networks.
- Adding `smartquotes = False` to `conf.py` and romoving `'` from rst files.
- Adding build_ignore property to galaxy file.
- Adding support to ansible.utils >=3.0
- Idempotency bugs fixed in devices_switch_ports.
- Parameter`organization_id` change to `organizationId` organizations_claim.
- Parameter`organization_id` change to `organizationId` organizations_clone.
- Parameter`organization_id` change to `organizationId` organizations_inventory_claim.
- Parameter`organization_id` change to `organizationId` organizations_inventory_onboarding_cloud_monitoring_export_events.
- Parameter`organization_id` change to `organizationId` organizations_inventory_onboarding_cloud_monitoring_prepare.
- Parameter`organization_id` change to `organizationId` organizations_inventory_release.
- Parameter`organization_id` change to `organizationId` organizations_licenses_assign_seats.
- Parameter`organization_id` change to `organizationId` organizations_licenses_move.
- Parameter`organization_id` change to `organizationId` organizations_licenses_move_seats.
- Parameter`organization_id` change to `organizationId` organizations_licenses_renew_seats.
- Parameter`organization_id` change to `organizationId` organizations_licensing_coterm_licenses_move.
- Parameter`organization_id` change to `organizationId` organizations_networks_combine.
- Parameter`organization_id` change to `organizationId` organizations_switch_devices_clone.
- Parameter`organization_id` change to `organizationId` organizations_users.
- Removing logs in meraki.py.
- networks_syslog_servers is now just an Update action to API.

cisco.mso
~~~~~~~~~

- Fix TypeError for iteration on NoneType in mso_schema_template
- Fixed the useg_subnet logic in mso_schema_template_anp_epg_useg_attribute

cisco.nxos
~~~~~~~~~~

- Prevents module_defaults from were being incorrectly applied to the platform action, instead of the concerned module.
- nxos_acls - Fix parsing of ace entries with range in it. (https://github.com/ansible-collections/cisco.nxos/issues/788)
- nxos_file_copy - correctly set file_pull_timeout/persistent_command_timeout value.
- nxos_interfaces - Correctly enable L3 interfaces on supported N3K platforms (https://github.com/ansible-collections/cisco.nxos/issues/749).

community.aws
~~~~~~~~~~~~~

- aws_ssm - disable ``enable-bracketed-paste`` to fix issue with amazon linux 2023 and other OSes (https://github.com/ansible-collections/community.aws/issues/1756)
- ssm(connection) - fix bucket region logic when region is ``us-east-1`` (https://github.com/ansible-collections/community.aws/pull/1908).

community.ciscosmb
~~~~~~~~~~~~~~~~~~

- issue
- solved issue

community.crypto
~~~~~~~~~~~~~~~~

- acme_* modules - also retry requests in case of socket errors, bad status lines, and unknown connection errors; improve error messages in these cases (https://github.com/ansible-collections/community.crypto/issues/680).
- acme_* modules - directly react on bad return data for account creation/retrieval/updating requests (https://github.com/ansible-collections/community.crypto/pull/682).
- acme_* modules - fix improved error reporting in case of socket errors, bad status lines, and unknown connection errors (https://github.com/ansible-collections/community.crypto/pull/684).
- acme_* modules - increase number of retries from 5 to 10 to increase stability with unstable ACME endpoints (https://github.com/ansible-collections/community.crypto/pull/685).
- acme_* modules - make account registration handling more flexible to accept 404 instead of 400 send by DigiCert's ACME endpoint when an account does not exist (https://github.com/ansible-collections/community.crypto/pull/681).
- luks_device - fixed module a bug that prevented using ``remove_keyslot`` with the value ``0`` (https://github.com/ansible-collections/community.crypto/pull/710).
- luks_device - fixed module falsely outputting ``changed=false`` when trying to add a new slot with a key that is already present in another slot. The module now rejects adding keys that are already present in another slot (https://github.com/ansible-collections/community.crypto/pull/710).
- luks_device - fixed testing of LUKS passphrases in when specifying a keyslot for cryptsetup version 2.0.3. The output of this cryptsetup version slightly differs from later versions (https://github.com/ansible-collections/community.crypto/pull/710).
- openssl_dhparam - was using an internal function instead of the public API to load DH param files when using the ``cryptography`` backend. The internal function was removed in cryptography 42.0.0. The module now uses the public API, which has been available since support for DH params was added to cryptography (https://github.com/ansible-collections/community.crypto/pull/698).
- openssl_privatekey_info - ``check_consistency=true`` no longer works for RSA keys with cryptography 42.0.0+ (https://github.com/ansible-collections/community.crypto/pull/701).
- openssl_privatekey_info - ``check_consistency=true`` now reports a warning if it cannot determine consistency (https://github.com/ansible-collections/community.crypto/pull/705).

community.digitalocean
~~~~~~~~~~~~~~~~~~~~~~

- The C(project_name) parameter for many modules was used by alias C(project) internally in the codebase, but to work properly C(project_name) must be used in the code. Replace self.module.params.get("project") with self.module.params.get("project_name") (https://github.com/ansible-collections/community.digitalocean/issues/326).
- digital_ocean_kubernetes - module didn't return kubeconfig properly, return documentation was invalid. Fixed version returns data with the same structure all the time, also it is aligned with M(community.digitalocean.digital_ocean_kubernetes_info) documentation return data now. (https://github.com/ansible-collections/community.digitalocean/issues/322).
- inventory plugin - restore reading auth token from env variables (https://github.com/ansible-collections/community.digitalocean/pull/315).

community.dns
~~~~~~~~~~~~~

- DNS record modules, inventory plugins - fix the TXT entry encoder to avoid splitting up escape sequences for quotes and backslashes over multiple TXT strings (https://github.com/ansible-collections/community.dns/issues/190, https://github.com/ansible-collections/community.dns/pull/191).
- Update Public Suffix List.
- nameserver_record_info - fix crash when more than one record is retrieved (https://github.com/ansible-collections/community.dns/pull/172).
- wait_for_txt, nameserver_info, nameserver_record_info - when looking up nameservers for a domain, do not treat ``NXDOMAIN`` as a fatal error (https://github.com/ansible-collections/community.dns/pull/177).

community.docker
~~~~~~~~~~~~~~~~

- Use ``unix:///var/run/docker.sock`` instead of the legacy ``unix://var/run/docker.sock`` as default for ``docker_host`` (https://github.com/ansible-collections/community.docker/pull/736).
- docker_compose_v2 - do not consider a ``Waiting`` event as an action/change (https://github.com/ansible-collections/community.docker/pull/804).
- docker_compose_v2 - do not fail when non-fatal errors occur. This can happen when pulling an image fails, but then the image can be built for another service. Docker Compose emits an error in that case, but ``docker compose up`` still completes successfully (https://github.com/ansible-collections/community.docker/issues/807, https://github.com/ansible-collections/community.docker/pull/810, https://github.com/ansible-collections/community.docker/pull/811).
- docker_compose_v2 - do not treat service-level pull events as changes to avoid incorrect ``changed=true`` return value of ``pull=always`` (https://github.com/ansible-collections/community.docker/issues/802, https://github.com/ansible-collections/community.docker/pull/803).
- docker_compose_v2 - properly parse dry-run build events from ``stderr`` (https://github.com/ansible-collections/community.docker/issues/778, https://github.com/ansible-collections/community.docker/pull/779).
- docker_compose_v2* modules - correctly parse ``Warning`` events emitted by Docker Compose (https://github.com/ansible-collections/community.docker/issues/807, https://github.com/ansible-collections/community.docker/pull/811).
- docker_compose_v2* modules - parse ``logfmt`` warnings emitted by Docker Compose (https://github.com/ansible-collections/community.docker/issues/787, https://github.com/ansible-collections/community.docker/pull/811).
- docker_compose_v2, docker_compose_v2_pull - fix parsing of pull messages for Docker Compose 2.20.0 (https://github.com/ansible-collections/community.docker/issues/785, https://github.com/ansible-collections/community.docker/pull/786).
- docker_compose_v2_pull - fixing idempotence by checking actual pull progress events instead of service-level pull request when ``policy=always``. This stops the module from reporting ``changed=true`` if no actual change happened when pulling. In check mode, it has to assume that a change happens though (https://github.com/ansible-collections/community.docker/issues/813, https://github.com/ansible-collections/community.docker/pull/814).
- docker_compose_v2_pull - the module was documented as part of the ``community.docker.docker`` action group, but was not actually part of it. That has now been fixed (https://github.com/ansible-collections/community.docker/pull/773).
- docker_image - fix archiving idempotency with Docker API 1.44 or later (https://github.com/ansible-collections/community.docker/pull/765).
- modules and plugins using the Docker SDK for Python - remove ``ssl_version`` from the parameters passed to Docker SDK for Python 7.0.0+. Explicitly fail with a nicer error message if it was explicitly set in this case (https://github.com/ansible-collections/community.docker/pull/715).
- modules and plugins using the Docker SDK for Python - remove ``tls_hostname`` from the parameters passed to Docker SDK for Python 7.0.0+. Explicitly fail with a nicer error message if it was explicitly set in this case (https://github.com/ansible-collections/community.docker/pull/721).
- vendored Docker SDK for Python - avoid passing on ``ssl_version`` and ``tls_hostname`` if they were not provided by the user. Remove dead code. (https://github.com/ansible-collections/community.docker/pull/722).

community.general
~~~~~~~~~~~~~~~~~

- aix_filesystem - fix issue with empty list items in crfs logic and option order (https://github.com/ansible-collections/community.general/pull/8052).
- apt-rpm - the module did not upgrade packages if a newer version exists. Now the package will be reinstalled if the candidate is newer than the installed version (https://github.com/ansible-collections/community.general/issues/7414).
- cargo - fix idempotency issues when using a custom installation path for packages (using the ``--path`` parameter). The initial installation runs fine, but subsequent runs use the ``get_installed()`` function which did not check the given installation location, before running ``cargo install``. This resulted in a false ``changed`` state. Also the removal of packeges using ``state: absent`` failed, as the installation check did not use the given parameter (https://github.com/ansible-collections/community.general/pull/7970).
- cloudflare_dns - fix Cloudflare lookup of SHFP records (https://github.com/ansible-collections/community.general/issues/7652).
- consul_token - fix token creation without ``accessor_id`` (https://github.com/ansible-collections/community.general/pull/8091).
- gitlab_issue - fix behavior to search GitLab issue, using ``search`` keyword instead of ``title`` (https://github.com/ansible-collections/community.general/issues/7846).
- gitlab_runner - fix pagination when checking for existing runners (https://github.com/ansible-collections/community.general/pull/7790).
- homebrew - detect already installed formulae and casks using JSON output from ``brew info`` (https://github.com/ansible-collections/community.general/issues/864).
- homebrew - error returned from brew command was ignored and tried to parse empty JSON. Fix now checks for an error and raises it to give accurate error message to users (https://github.com/ansible-collections/community.general/issues/8047).
- incus connection plugin - treats ``inventory_hostname`` as a variable instead of a literal in remote connections (https://github.com/ansible-collections/community.general/issues/7874).
- interface_files - also consider ``address_family`` when changing ``option=method`` (https://github.com/ansible-collections/community.general/issues/7610, https://github.com/ansible-collections/community.general/pull/7612).
- ipa_hbacrule - the module uses a string for ``ipaenabledflag`` for new FreeIPA versions while the returned value is a boolean (https://github.com/ansible-collections/community.general/pull/7880).
- ipa_otptoken - the module expect ``ipatokendisabled`` as string but the ``ipatokendisabled`` value is returned as a boolean (https://github.com/ansible-collections/community.general/pull/7795).
- ipa_sudorule - the module uses a string for ``ipaenabledflag`` for new FreeIPA versions while the returned value is a boolean (https://github.com/ansible-collections/community.general/pull/7880).
- iptables_state - fix idempotency issues when restoring incomplete iptables dumps (https://github.com/ansible-collections/community.general/issues/8029).
- irc - replace ``ssl.wrap_socket`` that was removed from Python 3.12 with code for creating a proper SSL context (https://github.com/ansible-collections/community.general/pull/7542).
- keycloak_* - fix Keycloak API client to quote ``/`` properly (https://github.com/ansible-collections/community.general/pull/7641).
- keycloak_authz_permission - resource payload variable for scope-based permission was constructed as a string, when it needs to be a list, even for a single item (https://github.com/ansible-collections/community.general/issues/7151).
- keycloak_client - fixes issue when metadata is provided in desired state when task is in check mode (https://github.com/ansible-collections/community.general/issues/1226, https://github.com/ansible-collections/community.general/pull/7881).
- keycloak_identity_provider - ``mappers`` processing was not idempotent if the mappers configuration list had not been sorted by name (in ascending order). Fix resolves the issue by sorting mappers in the desired state using the same key which is used for obtaining existing state (https://github.com/ansible-collections/community.general/pull/7418).
- keycloak_identity_provider - it was not possible to reconfigure (add, remove) ``mappers`` once they were created initially. Removal was ignored, adding new ones resulted in dropping the pre-existing unmodified mappers. Fix resolves the issue by supplying correct input to the internal update call (https://github.com/ansible-collections/community.general/pull/7418).
- keycloak_user - when ``force`` is set, but user does not exist, do not try to delete it (https://github.com/ansible-collections/community.general/pull/7696).
- ldap - previously the order number (if present) was expected to follow an equals sign in the DN. This makes it so the order number string is identified correctly anywhere within the DN (https://github.com/ansible-collections/community.general/issues/7646).
- linode inventory plugin - add descriptive error message for linode inventory plugin (https://github.com/ansible-collections/community.general/pull/8133).
- log_entries callback plugin - replace ``ssl.wrap_socket`` that was removed from Python 3.12 with code for creating a proper SSL context (https://github.com/ansible-collections/community.general/pull/7542).
- lvol - test for output messages in both ``stdout`` and ``stderr`` (https://github.com/ansible-collections/community.general/pull/7601, https://github.com/ansible-collections/community.general/issues/7182).
- modprobe - listing modules files or modprobe files could trigger a FileNotFoundError if ``/etc/modprobe.d`` or ``/etc/modules-load.d`` did not exist. Relevant functions now return empty lists if the directories do not exist to avoid crashing the module (https://github.com/ansible-collections/community.general/issues/7717).
- mssql_script - make the module work with Python 2 (https://github.com/ansible-collections/community.general/issues/7818, https://github.com/ansible-collections/community.general/pull/7821).
- nmcli - fix ``connection.slave-type`` wired to ``bond`` and not with parameter ``slave_type`` in case of connection type ``wifi`` (https://github.com/ansible-collections/community.general/issues/7389).
- onepassword lookup plugin - failed for fields that were in sections and had uppercase letters in the label/ID. Field lookups are now case insensitive in all cases (https://github.com/ansible-collections/community.general/pull/7919).
- onepassword lookup plugin - field and section titles are now case insensitive when using op CLI version two or later. This matches the behavior of version one (https://github.com/ansible-collections/community.general/pull/7564).
- pacemaker_cluster - actually implement check mode, which the module claims to support. This means that until now the module also did changes in check mode (https://github.com/ansible-collections/community.general/pull/8081).
- pam_limits - when the file does not exist, do not create it in check mode (https://github.com/ansible-collections/community.general/issues/8050, https://github.com/ansible-collections/community.general/pull/8057).
- pkgin - pkgin (pkgsrc package manager used by SmartOS) raises erratic exceptions and spurious ``changed=true`` (https://github.com/ansible-collections/community.general/pull/7971).
- proxmox - fix updating a container config if the setting does not already exist (https://github.com/ansible-collections/community.general/pull/7872).
- proxmox_kvm - fixed status check getting from node-specific API endpoint (https://github.com/ansible-collections/community.general/issues/7817).
- proxmox_kvm - running ``state=template`` will first check whether VM is already a template (https://github.com/ansible-collections/community.general/pull/7792).
- redfish_info - allow for a GET operation invoked by ``GetUpdateStatus`` to allow for an empty response body for cases where a service returns 204 No Content (https://github.com/ansible-collections/community.general/issues/8003).
- redfish_info - correct uncaught exception when attempting to retrieve ``Chassis`` information (https://github.com/ansible-collections/community.general/pull/7952).
- redhat_subscription - use the D-Bus registration on RHEL 7 only on 7.4 and
  greater; older versions of RHEL 7 do not have it
  (https://github.com/ansible-collections/community.general/issues/7622,
  https://github.com/ansible-collections/community.general/pull/7624).
- statusio_maintenance - fix error caused by incorrectly formed API data payload. Was raising "Failed to create maintenance HTTP Error 400 Bad Request" caused by bad data type for date/time and deprecated dict keys (https://github.com/ansible-collections/community.general/pull/7754).
- terraform - fix multiline string handling in complex variables (https://github.com/ansible-collections/community.general/pull/7535).

community.grafana
~~~~~~~~~~~~~~~~~

- Add `grafana_organiazion_user` to `action_groups.grafana`
- Fixed orgId handling in diff comparison for `grafana_datasource` if using org_name
- test: replace deprecated `TestCase.assertEquals` to support Python 3.12

community.mysql
~~~~~~~~~~~~~~~

- mysql_info - the ``slave_status`` filter was returning an empty list on MariaDB with multiple replication channels. It now returns all channels by running ``SHOW ALL SLAVES STATUS`` for MariaDB servers (https://github.com/ansible-collections/community.mysql/issues/603).

community.postgresql
~~~~~~~~~~~~~~~~~~~~

- postgresql_privs - fix a failure when altering privileges with ``grant_option: true`` (https://github.com/ansible-collections/community.postgresql/issues/668).
- postgresql_query - now reports not changed for queries starting with "SHOW" (https://github.com/ansible-collections/community.postgresql/pull/592).
- postgresql_user - module failed when running against an SQL_ASCII encoded database as the user's current password was returned as bytes as opposed to a str. Fix now checks for this case and decodes the bytes as an ascii encoded string. (https://github.com/ansible-collections/community.postgresql/issues/584).

community.routeros
~~~~~~~~~~~~~~~~~~

- facts - fix date not getting removed for idempotent config export (https://github.com/ansible-collections/community.routeros/pull/262).

community.sap_libs
~~~~~~~~~~~~~~~~~~

- fixes failures in sanity test for all modules

community.vmware
~~~~~~~~~~~~~~~~

- Fix InsecureRequestWarning for modules based on the VmwareRestClient module util when setting ``validate_certs`` to ``False`` (https://github.com/ansible-collections/community.vmware/pull/1969).
- module_utils/vmware.py - remove ssl.wrap_socet() function. Replaced for code based on ssl.get_server_certificate (https://github.com/ansible-collections/community.vmware/issues/1930).
- vmware_guest - Fix failure of vm reconfiguration with enabled virt_based_security (https://github.com/ansible-collections/community.vmware/pull/1848).
- vmware_vm_info - Fix an AttributeError when gathering network information (https://github.com/ansible-collections/community.vmware/pull/1919).

community.windows
~~~~~~~~~~~~~~~~~

- Remove some code which is no longer valid for dotnet 5+
- community.windows.win_psmodule_info - exception thrown when host has no Installed Module. Fix now checks that variable $installedModules is not null before calling the .Contains(..) function on it.
- win_format, win_partition - Add support for Windows failover cluster disks
- win_psmodule - Fix up error message with ``state=latest``
- win_rabbitmq_plugin - Avoid using ``Invoke-Expression`` when running external commands
- win_rds_rap - The module crashed when creating a RAP with Gateway Managed Computer Group (https://github.com/ansible-collections/community.windows/issues/184).
- win_robocopy - Fix up ``cmd`` return value to include the executable ``robocopy``

community.zabbix
~~~~~~~~~~~~~~~~

- Avoid to update user-directory configuration in dry run.
- api module - Fixed certificiate errors
- proxy and server roles - Defaulted location of fping and fping6 based on OS.
- proxy role - Removed requirement for mysql group definition.
- server role - typo in configuration var StasAllowedIP to StatsAllowedIP
- zabbix-{agent, javagateway, proxy, server, web} - support raspberry pi without repository url specification
- zabbix_inventory - fixed handeling of add_zabbix_groups option
- zabbix_template - fix template export when template's content has "error" word
- zabbix_web role - fix variable naming issues (undefined) to zabbix_web_version and zabbix_web_apt_repository

containers.podman
~~~~~~~~~~~~~~~~~

- Add idempotency for podman_secret module
- Catch exceptions when no JSON output in podman_image
- Fail if systemd generation failed and it's explicitly set
- Fix example name
- Fix idempotency for podman_network
- Fix idempotency when using 0.0.0.0 in ports
- Fix multi-image support for podman_save
- Fix volume inspection by name in podman_volume
- Recreate stopped containers if recreate flag is enabled
- podman_container - Add check and fixed for v5 network diff
- podman_container - Fix pasta networking idempotency for v5 (#728)
- podman_container_exec - Remove unnecessary quotes in podman_container_exec module
- podman_image_info - Fix wrong return data type in podman_image_info
- podman_play - Fix kube play annotations
- podman_pod - Fix broken info of pods in Podman v5
- podman_pod - Fix pod for Podman v5
- podman_pod - Fix podman pod v5 broken info issue

dellemc.enterprise_sonic
~~~~~~~~~~~~~~~~~~~~~~~~

- requirements - Update requires_ansible version in meta/runtime.yml to the oldest supported version (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/321).
- sonic_bgp_communities - Fix incorrect "facts" handling for parsing of a BGP community list configured with an empty "members" list (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/319).
- sonic_bgp_neighbors - Fix prefix-limit issue (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/289).
- sonic_interfaces - Add warnings when speed and auto_negotiate is configured at same time (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/314).
- sonic_interfaces - Fix support for standard naming interfaces (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/314).
- sonic_interfaces - Prevent configuring speed in port group interfaces (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/314).
- sonic_stp - Correct the commands list for STP delete state (https://github.com/ansible-collections/dellemc.enterprise_sonic/pull/302).

dellemc.openmanage
~~~~~~~~~~~~~~~~~~

- Added support for RAID creation using NVMe disks.(https://github.com/dell/dellemc-openmanage-ansible-modules/issues/635)
- Fixed the issue for ignoring the environment variable `NO_PROXY` earlier. (https://github.com/dell/dellemc-openmanage-ansible-modules/issues/554)
- For idrac_certificates module, the `email_address` has been made as an optional parameter. (https://github.com/dell/dellemc-openmanage-ansible-modules/issues/582).
- Issue is fixed for deploying a new configuration on quick deploy slot when IPv6 is disabled.(https://github.com/dell/dellemc-openmanage-ansible-modules/issues/533)
- idrac_network_attributes - Issue(279049) -  If unsupported values are provided for the parameter ``ome_network_attributes``, then this module does not provide a correct error message.
- ome_device_network_services - Issue(212681) - The module does not provide a proper error message if unsupported values are provided for the following parameters- port_number, community_name, max_sessions, max_auth_retries, and idle_timeout.
- ome_device_power_settings - Issue(212679) - The module displays the following message if the value provided for the parameter ``power_cap`` is not within the supported range of 0 to 32767, ``Unable to complete the request because PowerCap does not exist or is not applicable for the resource URI.``
- ome_inventory - The plugin returns 50 results when a group is specified. No results are shown when a group is not specified. (https://github.com/dell/dellemc-openmanage-ansible-modules/issues/575).
- redfish_storage_volume is enhanced to support iDRAC8.(https://github.com/dell/dellemc-openmanage-ansible-modules/issues/625)

f5networks.f5_modules
~~~~~~~~~~~~~~~~~~~~~

- bigip_gtm_monitor_bigip - fixed an issue where IP and port were not applied correctly when creating new monitor.
- bigip_gtm_monitor_firepass - fixed an issue where IP and port were not applied correctly when creating new monitor.
- bigip_gtm_monitor_http - fixed an issue where IP and port were not applied correctly when creating new monitor.
- bigip_gtm_monitor_https- fixed an issue where IP and port were not applied correctly when creating new monitor.
- bigip_gtm_monitor_tcp - fixed an issue where IP and port were not applied correctly when creating new monitor.
- bigip_gtm_monitor_tcp_half_open - fixed an issue where IP and port were not applied correctly when creating new monitor.
- bigip_gtm_topology_region - fixed an issue where if multiple states with spaces in values were defined, module would throw invalid command error
- bigip_gtm_topology_region - fixed an issue where states names that contained spaces caused the idempotency to break.
- bigip_ssl_key_cert - fixed an issue where the passphrase was not being properly send to the BIG-IP.

fortinet.fortimanager
~~~~~~~~~~~~~~~~~~~~~

- Added missing enum values for some arguments.
- Change minimum required ansible-core version to 2.14.0
- Changed revision to v_range to reduce the size of the code.
- Fixed a bug where ansible may skip update incorrectly.
- Fixed the behavior of module fmgr_firewall_internetservicecustom.
- Fixed the behavior of some modules that contain the argument policyid.
- Improved example ansible playbooks.
- Improved the logic of fmgr_fact, fmgr_clone, fmgr_rename, fmgr_move. Usage remains unchanged.
- Reduced the size of module_arg_spec in each module.
- Removed most of the sanity test ignores.
- Support FortiManager 7.0.10

fortinet.fortios
~~~~~~~~~~~~~~~~

- Fix the issue that ssl-certificate cannot be set in `fortios_firewall_vip` and `fortios_firewall_vip6`.
- Github issue
- mantis issue

hetzner.hcloud
~~~~~~~~~~~~~~

- hcloud inventory - Ensure the API client use a new cache for every *cached session*.
- load_balancer_info - Correctly return the `cookie_lifetime` value.
- load_balancer_service - Correctly return the `cookie_lifetime` value.

ibm.qradar
~~~~~~~~~~

- A bunch of ansible-lint and ansible-test sanity issues have been fixed.

ibm.storage_virtualize
~~~~~~~~~~~~~~~~~~~~~~

- ibm_svc_info - Command and release mapping to remove errors in gather_subset=all
- ibm_svc_info - Return error in listing entities that require object name

infoblox.nios_modules
~~~~~~~~~~~~~~~~~~~~~

- Fixes environment variable max_results using INFOBLOX_MAX_RESULTS `#209 <https://github.com/infobloxopen/infoblox-ansible/pull/209>`_
- Fixes index error for transform fields in DTC LBDN (auth_zone and Pool) and DTC POOL (servers and monitors) `#209 <https://github.com/infobloxopen/infoblox-ansible/pull/209>`_
- Fixes typo for environment variable INFOBLOX_WAPI_VERSION `#209 <https://github.com/infobloxopen/infoblox-ansible/pull/209>`_

junipernetworks.junos
~~~~~~~~~~~~~~~~~~~~~

- Fix the empty facts list placement
- Prevents module_defaults from were being incorrectly applied to the platform action, instead of the concerned module.
- acls
- fix to gather l2_interfaces facts with default port-mode access.
- initialize facts dictionary with empty containers for respective resources mentioned below
- lldp_global
- lldp_interfaces
- logging_global
- ntp_global
- ospf_interfaces
- ospfv2
- ospfv3
- prefix_lists
- routing_instances
- routing_options
- security_policies
- security_policies_global
- security_zones
- snmp_server
- static_routes
- vlans

kubernetes.core
~~~~~~~~~~~~~~~

- Resolve Collections util resource discovery fails when complex subresources present (https://github.com/ansible-collections/kubernetes.core/pull/676).
- align `helmdiff_check()` function commandline rendering with the `deploy()` function (https://github.com/ansible-collections/kubernetes.core/pull/670).
- helm - Put the chart_ref into quotes when running ``helm show chart``, ``helm upgrade`` and ``helm dependency update`` commands (https://github.com/ansible-collections/kubernetes.core/issues/653).
- helm - delete temporary file created when deploying chart with option ``release_values`` set (https://github.com/ansible-collections/kubernetes.core/issues/530).
- helm - fix issue occurring when uninstalling chart with statues others than ``deployed`` (https://github.com/ansible-collections/kubernetes.core/issues/319).
- helm - fix post_renderer argument breaking the helm deploy_command (https://github.com/ansible-collections/kubernetes.core/pull/586).
- helm - use ``reuse-values`` when running ``helm diff`` command (https://github.com/ansible-collections/kubernetes.core/issues/680).
- helm - use post_renderer when checking ``changed`` status for a helm release (https://github.com/ansible-collections/kubernetes.core/pull/588).
- integrations test helm_kubeconfig - set helm version to v3.10.3 to avoid incompatability with new bitnami charts (https://github.com/ansible-collections/kubernetes.core/pull/670).
- k8s_scale - clean handling of ResourceTimeout exception (https://github.com/ansible-collections/kubernetes.core/issues/583).
- k8s_scale - fix issue when scaling StatefulSets with ``updateStrategy=OnDelete`` (https://github.com/ansible-collections/kubernetes.core/issues/579).

lowlydba.sqlserver
~~~~~~~~~~~~~~~~~~

- Add ActiveStartDate to the compare properties so this item is marked accurately as changed.
- Fixed the formatting of the SPN by updating the backslash to a forward-slash for the $spn var (lowlydba.sqlserver.spn)
- Update documentation for agent_job_schedule to reflect proper input formatting. (https://github.com/lowlydba/lowlydba.sqlserver/pull/229)

microsoft.ad
~~~~~~~~~~~~

- debug_ldap_client - handle failures when attempting to get the krb5 context and default CCache rather than fail with a traceback
- microsoft.ad.group - Support membership lookup of groups that are longer than 20 characters long
- microsoft.ad.membership - Add helpful hint when the failure was due to a missing/invalid ``domain_ou_path`` - https://github.com/ansible-collections/microsoft.ad/issues/88

netapp.ontap
~~~~~~~~~~~~

- na_ontap_ems_destination - fix field error with `certificate.name` for ONTAP 9.11.1 or later in REST.
- na_ontap_igroup_initiator - fixed issue with idempotency.
- na_ontap_nfs - fix error with `windows` in REST for ONTAP 9.10 or earlier.
- na_ontap_security_certificates - fix error with ontap_info returned in module output in REST.
- na_ontap_snapshot_policy - fix issue with modifying snapshot policy in REST.
- na_ontap_volume - modified `type` to be case insensitive in REST.
- na_ontap_vserver_peer - fix issue with peering multiple clusters with same vserver name in REST.

netapp.storagegrid
~~~~~~~~~~~~~~~~~~

- Removed fetch limit in API request and implemented pagination.

netbox.netbox
~~~~~~~~~~~~~

- Improve error reporting for missing module [#1126](https://github.com/netbox-community/ansible_modules/pull/1126)
- nb_inventory - Fix API cache failure [#1111](https://github.com/netbox-community/ansible_modules/pull/1111)
- nb_lookup - Allow multiple IDs in nb_lookup [#1042](https://github.com/netbox-community/ansible_modules/pull/1042)
- netbox_vlan - Fix documentation of vlan_group [#1138](https://github.com/netbox-community/ansible_modules/pull/1138)

purestorage.flasharray
~~~~~~~~~~~~~~~~~~~~~~

- purefa_cert - Fixed issue where parts of the subject where not included in the CSR if they did not exist in the currently used cert.
- purefa_certs - Allow certificates of over 3000 characters to be imported.
- purefa_dns - Fixed attribute error on deletion of management DNS
- purefa_ds - Fix issue with SDK returning empty data for data directory services even when it does exist
- purefa_info - Resolved issue with KeyError when LACP bonds are in use
- purefa_inventory - Fix issue with iSCSI-only FlashArrays
- purefa_pg - Allows a protection group to be correctly created when `target` is specified as well as other objects, such as `volumes` or `hosts`
- purefa_pgsched - Fixed issue with disabling schedules
- purefa_pgsnap - Add support for restoring volumes connected to hosts in a host-based protection group and hosts in a hostgroup-based protection group.
- purefa_pgsnap - Fixed incorrect parameter name
- purefa_policy - Fix incorrect call of psot instead of patch for NFS policies

purestorage.flashblade
~~~~~~~~~~~~~~~~~~~~~~

- purefb_bucket - Changed logic to allow complex buckets to be created in a single call, rather than having to split into two tasks.
- purefb_info - Added missing object lock retention details if enabledd
- purefb_lag - Enable LAG port configuration with multi-chassis
- purefb_timeout - Fixed arithmetic error that resulted in module incorrectly reporting changed when no change was required.

splunk.es
~~~~~~~~~

- Fixed argspec validation for plugins with empty task attributes when run with Ansible 2.9.

telekom_mms.icinga_director
~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Fixes #190 - Workaround for service apply bug (https://github.com/telekom-mms/ansible-collection-icinga-director/pull/239)

theforeman.foreman
~~~~~~~~~~~~~~~~~~

- compute_profile, host - refer to VMware storage pods by name, not id (https://github.com/theforeman/foreman-ansible-modules/issues/1247)
- content_view_filter_rule - handle multiple rules for the same package but different architectures and versions correctly (https://bugzilla.redhat.com/show_bug.cgi?id=2189687)

vmware.vmware_rest
~~~~~~~~~~~~~~~~~~

- content_library_item_info - fixed error with unsupported property
- lookup plugins - Refactor to use native options configuration via doc_fragment, which ensures that vcenter_validate_certs=false is honored (https://github.com/ansible-collections/vmware.vmware_rest/issues/425).

vultr.cloud
~~~~~~~~~~~

- Fixed an error while waiting for a specific state and the API returns an empty response. (https://github.com/vultr/ansible-collection-vultr/issues/108).
- Fixed an issue with waiting for state (https://github.com/vultr/ansible-collection-vultr/pull/102).
- instance - Fixed an issue detecting the instance state returned by the API (https://github.com/vultr/ansible-collection-vultr/pull/89).
- instance_info - Fixed the alias ``name`` being was used on the wrong argument. (https://github.com/vultr/ansible-collection-vultr/issues/105).
- reserved_ip - Fixed an issue which caused the module to fail, also enabled integration tests (https://github.com/vultr/ansible-collection-vultr/issues/92).

Known Issues
------------

dellemc.openmanage
~~~~~~~~~~~~~~~~~~

- idrac_diagnostics - Issue(285322) - This module doesn't support export of diagnostics file to HTTP and HTTPS share via SOCKS proxy.
- idrac_firmware - Issue(279282) - This module does not support firmware update using HTTP, HTTPS, and FTP shares with authentication on iDRAC8.
- idrac_network_attributes - Issue(279049) -  If unsupported values are provided for the parameter ``ome_network_attributes``, then this module does not provide a correct error message.
- idrac_storage_volume - Issue(290766) - The module will report success instead of showing failure for new virtual creation on the BOSS-N1 controller if a virtual disk is already present on the same controller.
- ome_device_network_services - Issue(212681) - The module does not provide a proper error message if unsupported values are provided for the following parameters- port_number, community_name, max_sessions, max_auth_retries, and idle_timeout.
- ome_device_power_settings - Issue(212679) - The module displays the following message if the value provided for the parameter ``power_cap`` is not within the supported range of 0 to 32767, ``Unable to complete the request because PowerCap does not exist or is not applicable for the resource URI.``
- ome_device_quick_deploy - Issue(275231) - This module does not deploy a new configuration to a slot that has disabled IPv6.
- ome_diagnostics - Issue(279193) - Export of SupportAssist collection logs to the share location fails on OME version 4.0.0.
- ome_smart_fabric_uplink - Issue(186024) - The module supported by OpenManage Enterprise Modular, however it does not allow the creation of multiple uplinks of the same name. If an uplink is created using the same name as an existing uplink, then the existing uplink is modified.

New Plugins
-----------

Callback
~~~~~~~~

- community.general.default_without_diff - The default ansible callback without diff output

Connection
~~~~~~~~~~

- community.general.incus - Run tasks in Incus instances via the Incus CLI.

Filter
~~~~~~

- ansible.utils.fact_diff - Find the difference between currently set facts
- community.crypto.parse_serial - Convert a serial number as a colon-separated list of hex numbers to an integer
- community.crypto.to_serial - Convert an integer to a colon-separated list of hex numbers
- community.general.from_ini - Converts INI text input into a dictionary
- community.general.lists_difference - Difference of lists with a predictive order
- community.general.lists_intersect - Intersection of lists with a predictive order
- community.general.lists_symmetric_difference - Symmetric Difference of lists with a predictive order
- community.general.lists_union - Union of lists with a predictive order
- community.general.to_ini - Converts a dictionary to the INI file format
- microsoft.ad.dn_escape - Escape an LDAP DistinguishedName value string.
- microsoft.ad.parse_dn - Parses an LDAP DistinguishedName string into an object.

Lookup
~~~~~~

- community.general.github_app_access_token - Obtain short-lived Github App Access tokens
- community.general.onepassword_doc - Fetch documents stored in 1Password

Test
~~~~

- community.general.fqdn_valid - Validates fully-qualified domain names against RFC 1123

New Modules
-----------

check_point.mgmt
~~~~~~~~~~~~~~~~

- check_point.mgmt.cp_mgmt_add_central_license - Add central license.
- check_point.mgmt.cp_mgmt_central_license_facts - Get central-license objects facts on Checkpoint over Web Services API.
- check_point.mgmt.cp_mgmt_delete_central_license - Delete central license.
- check_point.mgmt.cp_mgmt_distribute_cloud_licenses - Distribute licenses to target CloudGuard gateways.
- check_point.mgmt.cp_mgmt_show_cloud_licenses_usage - Show attached licenses usage.
- check_point.mgmt.cp_mgmt_show_ha_status - Retrieve domain high availability status.

cisco.ios
~~~~~~~~~

- cisco.ios.ios_evpn_evi - Resource module to configure L2VPN EVPN EVI.
- cisco.ios.ios_evpn_global - Resource module to configure L2VPN EVPN.
- cisco.ios.ios_vxlan_vtep - Resource module to configure VXLAN VTEP interface.

community.aws
~~~~~~~~~~~~~

- community.aws.dynamodb_table_info - Returns information about a Dynamo DB table

community.digitalocean
~~~~~~~~~~~~~~~~~~~~~~

- community.digitalocean.digital_ocean_project_resource_info - Gather information about DigitalOcean Project Resources

community.docker
~~~~~~~~~~~~~~~~

- community.docker.docker_compose_v2 - Manage multi-container Docker applications with Docker Compose CLI plugin
- community.docker.docker_compose_v2_pull - Pull a Docker compose project
- community.docker.docker_image_build - Build Docker images using Docker buildx
- community.docker.docker_image_export - Export (archive) Docker images
- community.docker.docker_image_pull - Pull Docker images from registries
- community.docker.docker_image_push - Push Docker images to registries
- community.docker.docker_image_remove - Remove Docker images
- community.docker.docker_image_tag - Tag Docker images with new names and/or tags

community.general
~~~~~~~~~~~~~~~~~

- community.general.consul_acl_bootstrap - Bootstrap ACLs in Consul
- community.general.consul_auth_method - Manipulate Consul auth methods
- community.general.consul_binding_rule - Manipulate Consul binding rules
- community.general.consul_token - Manipulate Consul tokens
- community.general.dnf_config_manager - Enable or disable dnf repositories using config-manager
- community.general.git_config_info - Read git configuration
- community.general.gitlab_group_access_token - Manages GitLab group access tokens
- community.general.gitlab_issue - Create, update, or delete GitLab issues
- community.general.gitlab_label - Creates/updates/deletes GitLab Labels belonging to project or group.
- community.general.gitlab_milestone - Creates/updates/deletes GitLab Milestones belonging to project or group
- community.general.gitlab_project_access_token - Manages GitLab project access tokens
- community.general.keycloak_component_info - Retrive component info in Keycloak
- community.general.keycloak_realm_rolemapping - Allows administration of Keycloak realm role mappings into groups with the Keycloak API
- community.general.nomad_token - Manage Nomad ACL tokens
- community.general.proxmox_node_info - Retrieve information about one or more Proxmox VE nodes
- community.general.proxmox_storage_contents_info - List content from a Proxmox VE storage
- community.general.usb_facts - Allows listing information about USB devices

community.hashi_vault
~~~~~~~~~~~~~~~~~~~~~

- community.hashi_vault.vault_database_connection_configure - Configures the database engine
- community.hashi_vault.vault_database_connection_delete - Delete a Database Connection
- community.hashi_vault.vault_database_connection_read - Returns the configuration settings for a O(connection_name)
- community.hashi_vault.vault_database_connection_reset - Closes a O(connection_name) and its underlying plugin and restarts it with the configuration stored
- community.hashi_vault.vault_database_connections_list - Returns a list of available connections
- community.hashi_vault.vault_database_role_create - Creates or updates a (dynamic) role definition
- community.hashi_vault.vault_database_role_delete - Delete a role definition
- community.hashi_vault.vault_database_role_read - Queries a dynamic role definition
- community.hashi_vault.vault_database_roles_list - Returns a list of available (dynamic) roles
- community.hashi_vault.vault_database_rotate_root_credentials - Rotates the root credentials stored for the database connection. This user must have permissions to update its own password.
- community.hashi_vault.vault_database_static_role_create - Create or update a static role
- community.hashi_vault.vault_database_static_role_get_credentials - Returns the current credentials based on the named static role
- community.hashi_vault.vault_database_static_role_read - Queries a static role definition
- community.hashi_vault.vault_database_static_role_rotate_credentials - Trigger the credential rotation for a static role
- community.hashi_vault.vault_database_static_roles_list - Returns a list of available static roles

containers.podman
~~~~~~~~~~~~~~~~~

- containers.podman.podman_secret_info - Secrets info module

dellemc.enterprise_sonic
~~~~~~~~~~~~~~~~~~~~~~~~

- dellemc.enterprise_sonic.sonic_dhcp_snooping - Manage DHCP Snooping on SONiC
- dellemc.enterprise_sonic.sonic_pki - Manages PKI attributes of Enterprise Sonic
- dellemc.enterprise_sonic.sonic_stp - Manage STP configuration on SONiC

dellemc.openmanage
~~~~~~~~~~~~~~~~~~

- dellemc.openmanage.idrac_diagnostics - This module allows to run and export diagnostics on iDRAC.
- dellemc.openmanage.idrac_license - This module allows to import, export, and delete licenses on iDRAC.
- dellemc.openmanage.idrac_storage_volume - Configures the RAID configuration attributes.

dellemc.powerflex
~~~~~~~~~~~~~~~~~

- dellemc.powerflex.fault_set - Manage Fault Sets on Dell PowerFlex
- dellemc.powerflex.resource_group - Manage resource group deployments on Dell PowerFlex

fortinet.fortimanager
~~~~~~~~~~~~~~~~~~~~~

- fortinet.fortimanager.fmgr_diameterfilter_profile - Configure Diameter filter profiles.
- fortinet.fortimanager.fmgr_firewall_accessproxysshclientcert - Configure Access Proxy SSH client certificate.
- fortinet.fortimanager.fmgr_firewall_accessproxysshclientcert_certextension - Configure certificate extension for user certificate.
- fortinet.fortimanager.fmgr_firewall_vip6_quic - QUIC setting.
- fortinet.fortimanager.fmgr_firewall_vip_gslbpublicips - Publicly accessible IP addresses for the FortiGSLB service.
- fortinet.fortimanager.fmgr_sctpfilter_profile - Configure SCTP filter profiles.
- fortinet.fortimanager.fmgr_sctpfilter_profile_ppidfilters - PPID filters list.
- fortinet.fortimanager.fmgr_switchcontroller_managedswitch_vlan - Configure VLAN assignment priority.
- fortinet.fortimanager.fmgr_system_admin_profile_writepasswdprofiles - Profile list.
- fortinet.fortimanager.fmgr_system_admin_profile_writepasswduserlist - User list.
- fortinet.fortimanager.fmgr_system_npu_nputcam - Configure NPU TCAM policies.
- fortinet.fortimanager.fmgr_system_npu_nputcam_data - Data fields of TCAM.
- fortinet.fortimanager.fmgr_system_npu_nputcam_mask - Mask fields of TCAM.
- fortinet.fortimanager.fmgr_system_npu_nputcam_miract - Mirror action of TCAM.
- fortinet.fortimanager.fmgr_system_npu_nputcam_priact - Priority action of TCAM.
- fortinet.fortimanager.fmgr_system_npu_nputcam_sact - Source action of TCAM.
- fortinet.fortimanager.fmgr_system_npu_nputcam_tact - Target action of TCAM.
- fortinet.fortimanager.fmgr_videofilter_keyword - Configure video filter keywords.
- fortinet.fortimanager.fmgr_videofilter_keyword_word - List of keywords.
- fortinet.fortimanager.fmgr_videofilter_profile_filters - YouTube filter entries.
- fortinet.fortimanager.fmgr_videofilter_youtubekey - Configure YouTube API keys.

hetzner.hcloud
~~~~~~~~~~~~~~

- hetzner.hcloud.firewall_resource - Manage Resources a Hetzner Cloud Firewall is applied to.

infoblox.nios_modules
~~~~~~~~~~~~~~~~~~~~~

- infoblox.nios_modules.nios_dtc_monitor_http - Configures the Infoblox NIOS DTC HTTP monitor.
- infoblox.nios_modules.nios_dtc_monitor_icmp - Configures the Infoblox NIOS DTC ICMP monitor
- infoblox.nios_modules.nios_dtc_monitor_pdp - Configures the Infoblox NIOS DTC PDP monitor
- infoblox.nios_modules.nios_dtc_monitor_sip - Configures the Infoblox NIOS DTC SIP monitor
- infoblox.nios_modules.nios_dtc_monitor_snmp - Configures the Infoblox NIOS DTC SNMP monitor
- infoblox.nios_modules.nios_dtc_monitor_tcp - Configures the Infoblox NIOS DTC TCP monitor
- infoblox.nios_modules.nios_dtc_topology - Configures the Infoblox NIOS DTC Topology

netapp.ontap
~~~~~~~~~~~~

- netapp.ontap.na_ontap_cifs_unix_symlink_mapping - NetApp ONTAP module to manage UNIX symbolic link mapping for CIFS clients.
- netapp.ontap.na_ontap_cli_timeout - NetApp ONTAP module to set the CLI inactivity timeout value.
- netapp.ontap.na_ontap_snmp_config - NetApp ONTAP module to modify SNMP configuration.

netbox.netbox
~~~~~~~~~~~~~

- netbox.netbox.netbox_virtual_disk - Create, updates, or removes a disk from a Virtual Machine

purestorage.flasharray
~~~~~~~~~~~~~~~~~~~~~~

- purestorage.flasharray.purefa_hardware - Manage FlashArray Hardware Identification

purestorage.flashblade
~~~~~~~~~~~~~~~~~~~~~~

- purestorage.flashblade.purefb_hardware - Manage FlashBlade Hardware

theforeman.foreman
~~~~~~~~~~~~~~~~~~

- theforeman.foreman.registration_command - Manage Registration Command
- theforeman.foreman.webhook - Manage Webhooks

vultr.cloud
~~~~~~~~~~~

- vultr.cloud.object_storage - Manages object storages on Vultr

New Roles
---------

- dellemc.openmanage.idrac_user - Role to manage local users of iDRAC.

Unchanged Collections
---------------------

- ansible.posix (still version 1.5.4)
- chocolatey.chocolatey (still version 1.5.1)
- cisco.ucs (still version 1.10.0)
- cloudscale_ch.cloud (still version 2.3.1)
- community.libvirt (still version 1.3.0)
- community.network (still version 5.0.2)
- community.proxysql (still version 1.5.1)
- community.sops (still version 1.6.7)
- cyberark.conjur (still version 1.2.2)
- frr.frr (still version 2.0.2)
- ibm.spectrum_virtualize (still version 2.0.0)
- inspur.sm (still version 2.3.0)
- netapp.cloudmanager (still version 21.22.1)
- netapp_eseries.santricity (still version 1.4.0)
- ngine_io.cloudstack (still version 2.3.0)
- ngine_io.exoscale (still version 1.1.0)
- openvswitch.openvswitch (still version 2.1.1)
- ovirt.ovirt (still version 3.2.0)
- sensu.sensu_go (still version 1.14.0)
- t_systems_mms.icinga_director (still version 2.0.1)
- vyos.vyos (still version 4.1.0)
- wti.remote (still version 1.0.5)

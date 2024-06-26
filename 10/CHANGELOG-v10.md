# Ansible 10 Release Notes

This changelog describes changes since Ansible 9\.0\.0\.

- <a href="#v10-0-0a1">v10\.0\.0a1</a>
    - <a href="#release-summary">Release Summary</a>
    - <a href="#removed-collections">Removed Collections</a>
    - <a href="#added-collections">Added Collections</a>
    - <a href="#ansible-core">Ansible\-core</a>
    - <a href="#included-collections">Included Collections</a>
    - <a href="#major-changes">Major Changes</a>
    - <a href="#minor-changes">Minor Changes</a>
    - <a href="#breaking-changes--porting-guide">Breaking Changes / Porting Guide</a>
    - <a href="#deprecated-features">Deprecated Features</a>
    - <a href="#removed-features-previously-deprecated">Removed Features \(previously deprecated\)</a>
    - <a href="#security-fixes">Security Fixes</a>
    - <a href="#bugfixes">Bugfixes</a>
    - <a href="#known-issues">Known Issues</a>
    - <a href="#new-plugins">New Plugins</a>
    - <a href="#new-modules">New Modules</a>
    - <a href="#new-roles">New Roles</a>
    - <a href="#unchanged-collections">Unchanged Collections</a>

<a id="v10-0-0a1"></a>
## v10\.0\.0a1

- <a href="#release-summary">Release Summary</a>
- <a href="#removed-collections">Removed Collections</a>
- <a href="#added-collections">Added Collections</a>
- <a href="#ansible-core">Ansible\-core</a>
- <a href="#included-collections">Included Collections</a>
- <a href="#major-changes">Major Changes</a>
    - <a href="#ansible-core-1">Ansible\-core</a>
    - <a href="#ansible-netcommon">ansible\.netcommon</a>
    - <a href="#ansible-utils">ansible\.utils</a>
    - <a href="#arista-eos">arista\.eos</a>
    - <a href="#cisco-asa">cisco\.asa</a>
    - <a href="#cisco-ios">cisco\.ios</a>
    - <a href="#cisco-iosxr">cisco\.iosxr</a>
    - <a href="#cisco-nxos">cisco\.nxos</a>
    - <a href="#community-docker">community\.docker</a>
    - <a href="#community-hashi-vault">community\.hashi\_vault</a>
    - <a href="#community-mysql">community\.mysql</a>
    - <a href="#dellemc-openmanage">dellemc\.openmanage</a>
    - <a href="#dellemc-unity">dellemc\.unity</a>
    - <a href="#fortinet-fortios">fortinet\.fortios</a>
    - <a href="#grafana-grafana">grafana\.grafana</a>
    - <a href="#ibm-qradar">ibm\.qradar</a>
    - <a href="#infoblox-nios-modules">infoblox\.nios\_modules</a>
    - <a href="#junipernetworks-junos">junipernetworks\.junos</a>
    - <a href="#splunk-es">splunk\.es</a>
- <a href="#minor-changes">Minor Changes</a>
    - <a href="#ansible-core-2">Ansible\-core</a>
    - <a href="#amazon-aws">amazon\.aws</a>
    - <a href="#ansible-utils-1">ansible\.utils</a>
    - <a href="#ansible-windows">ansible\.windows</a>
    - <a href="#check-point-mgmt">check\_point\.mgmt</a>
    - <a href="#cisco-aci">cisco\.aci</a>
    - <a href="#cisco-dnac">cisco\.dnac</a>
    - <a href="#cisco-ios-1">cisco\.ios</a>
    - <a href="#cisco-iosxr-1">cisco\.iosxr</a>
    - <a href="#cisco-ise">cisco\.ise</a>
    - <a href="#cisco-meraki">cisco\.meraki</a>
    - <a href="#cisco-mso">cisco\.mso</a>
    - <a href="#cisco-nxos-1">cisco\.nxos</a>
    - <a href="#community-aws">community\.aws</a>
    - <a href="#community-ciscosmb">community\.ciscosmb</a>
    - <a href="#community-crypto">community\.crypto</a>
    - <a href="#community-digitalocean">community\.digitalocean</a>
    - <a href="#community-dns">community\.dns</a>
    - <a href="#community-docker-1">community\.docker</a>
    - <a href="#community-general">community\.general</a>
    - <a href="#community-grafana">community\.grafana</a>
    - <a href="#community-hashi-vault-1">community\.hashi\_vault</a>
    - <a href="#community-hrobot">community\.hrobot</a>
    - <a href="#community-mysql-1">community\.mysql</a>
    - <a href="#community-postgresql">community\.postgresql</a>
    - <a href="#community-rabbitmq">community\.rabbitmq</a>
    - <a href="#community-routeros">community\.routeros</a>
    - <a href="#community-vmware">community\.vmware</a>
    - <a href="#community-windows">community\.windows</a>
    - <a href="#community-zabbix">community\.zabbix</a>
    - <a href="#containers-podman">containers\.podman</a>
    - <a href="#dellemc-enterprise-sonic">dellemc\.enterprise\_sonic</a>
    - <a href="#dellemc-openmanage-1">dellemc\.openmanage</a>
    - <a href="#dellemc-powerflex">dellemc\.powerflex</a>
    - <a href="#f5networks-f5-modules">f5networks\.f5\_modules</a>
    - <a href="#fortinet-fortimanager">fortinet\.fortimanager</a>
    - <a href="#google-cloud">google\.cloud</a>
    - <a href="#grafana-grafana-1">grafana\.grafana</a>
    - <a href="#hetzner-hcloud">hetzner\.hcloud</a>
    - <a href="#ibm-storage-virtualize">ibm\.storage\_virtualize</a>
    - <a href="#inspur-ispim">inspur\.ispim</a>
    - <a href="#kubernetes-core">kubernetes\.core</a>
    - <a href="#lowlydba-sqlserver">lowlydba\.sqlserver</a>
    - <a href="#microsoft-ad">microsoft\.ad</a>
    - <a href="#netapp-ontap">netapp\.ontap</a>
    - <a href="#netapp-storagegrid">netapp\.storagegrid</a>
    - <a href="#netbox-netbox">netbox\.netbox</a>
    - <a href="#purestorage-flasharray">purestorage\.flasharray</a>
    - <a href="#purestorage-flashblade">purestorage\.flashblade</a>
    - <a href="#telekom-mms-icinga-director">telekom\_mms\.icinga\_director</a>
    - <a href="#theforeman-foreman">theforeman\.foreman</a>
    - <a href="#vmware-vmware-rest">vmware\.vmware\_rest</a>
    - <a href="#vultr-cloud">vultr\.cloud</a>
- <a href="#breaking-changes--porting-guide">Breaking Changes / Porting Guide</a>
    - <a href="#ansible-core-3">Ansible\-core</a>
    - <a href="#cloud-common">cloud\.common</a>
    - <a href="#community-ciscosmb-1">community\.ciscosmb</a>
    - <a href="#community-okd">community\.okd</a>
    - <a href="#hetzner-hcloud-1">hetzner\.hcloud</a>
    - <a href="#kubernetes-core-1">kubernetes\.core</a>
    - <a href="#theforeman-foreman-1">theforeman\.foreman</a>
    - <a href="#vmware-vmware-rest-1">vmware\.vmware\_rest</a>
- <a href="#deprecated-features">Deprecated Features</a>
    - <a href="#ansible-core-4">Ansible\-core</a>
    - <a href="#amazon-aws-1">amazon\.aws</a>
    - <a href="#community-crypto-1">community\.crypto</a>
    - <a href="#community-dns-1">community\.dns</a>
    - <a href="#community-docker-2">community\.docker</a>
    - <a href="#community-general-1">community\.general</a>
    - <a href="#community-hrobot-1">community\.hrobot</a>
    - <a href="#community-okd-1">community\.okd</a>
    - <a href="#dellemc-openmanage-2">dellemc\.openmanage</a>
    - <a href="#kubernetes-core-2">kubernetes\.core</a>
- <a href="#removed-features-previously-deprecated">Removed Features \(previously deprecated\)</a>
    - <a href="#ansible-core-5">Ansible\-core</a>
    - <a href="#arista-eos-1">arista\.eos</a>
    - <a href="#cisco-ios-2">cisco\.ios</a>
    - <a href="#cisco-iosxr-2">cisco\.iosxr</a>
    - <a href="#cisco-nxos-2">cisco\.nxos</a>
    - <a href="#junipernetworks-junos-1">junipernetworks\.junos</a>
- <a href="#security-fixes">Security Fixes</a>
    - <a href="#ansible-core-6">Ansible\-core</a>
    - <a href="#community-dns-2">community\.dns</a>
    - <a href="#community-docker-3">community\.docker</a>
    - <a href="#community-general-2">community\.general</a>
    - <a href="#community-hrobot-2">community\.hrobot</a>
- <a href="#bugfixes">Bugfixes</a>
    - <a href="#ansible-core-7">Ansible\-core</a>
    - <a href="#amazon-aws-2">amazon\.aws</a>
    - <a href="#ansible-utils-2">ansible\.utils</a>
    - <a href="#ansible-windows-1">ansible\.windows</a>
    - <a href="#arista-eos-2">arista\.eos</a>
    - <a href="#check-point-mgmt-1">check\_point\.mgmt</a>
    - <a href="#cisco-aci-1">cisco\.aci</a>
    - <a href="#cisco-asa-1">cisco\.asa</a>
    - <a href="#cisco-ios-3">cisco\.ios</a>
    - <a href="#cisco-iosxr-3">cisco\.iosxr</a>
    - <a href="#cisco-ise-1">cisco\.ise</a>
    - <a href="#cisco-meraki-1">cisco\.meraki</a>
    - <a href="#cisco-mso-1">cisco\.mso</a>
    - <a href="#cisco-nxos-3">cisco\.nxos</a>
    - <a href="#community-aws-1">community\.aws</a>
    - <a href="#community-ciscosmb-2">community\.ciscosmb</a>
    - <a href="#community-crypto-2">community\.crypto</a>
    - <a href="#community-digitalocean-1">community\.digitalocean</a>
    - <a href="#community-dns-3">community\.dns</a>
    - <a href="#community-docker-4">community\.docker</a>
    - <a href="#community-general-3">community\.general</a>
    - <a href="#community-grafana-1">community\.grafana</a>
    - <a href="#community-mysql-2">community\.mysql</a>
    - <a href="#community-postgresql-1">community\.postgresql</a>
    - <a href="#community-routeros-1">community\.routeros</a>
    - <a href="#community-sap-libs">community\.sap\_libs</a>
    - <a href="#community-vmware-1">community\.vmware</a>
    - <a href="#community-windows-1">community\.windows</a>
    - <a href="#community-zabbix-1">community\.zabbix</a>
    - <a href="#containers-podman-1">containers\.podman</a>
    - <a href="#dellemc-enterprise-sonic-1">dellemc\.enterprise\_sonic</a>
    - <a href="#dellemc-openmanage-3">dellemc\.openmanage</a>
    - <a href="#f5networks-f5-modules-1">f5networks\.f5\_modules</a>
    - <a href="#fortinet-fortimanager-1">fortinet\.fortimanager</a>
    - <a href="#fortinet-fortios-1">fortinet\.fortios</a>
    - <a href="#hetzner-hcloud-2">hetzner\.hcloud</a>
    - <a href="#ibm-qradar-1">ibm\.qradar</a>
    - <a href="#ibm-storage-virtualize-1">ibm\.storage\_virtualize</a>
    - <a href="#infoblox-nios-modules-1">infoblox\.nios\_modules</a>
    - <a href="#junipernetworks-junos-2">junipernetworks\.junos</a>
    - <a href="#kubernetes-core-3">kubernetes\.core</a>
    - <a href="#lowlydba-sqlserver-1">lowlydba\.sqlserver</a>
    - <a href="#microsoft-ad-1">microsoft\.ad</a>
    - <a href="#netapp-ontap-1">netapp\.ontap</a>
    - <a href="#netapp-storagegrid-1">netapp\.storagegrid</a>
    - <a href="#netbox-netbox-1">netbox\.netbox</a>
    - <a href="#purestorage-flasharray-1">purestorage\.flasharray</a>
    - <a href="#purestorage-flashblade-1">purestorage\.flashblade</a>
    - <a href="#splunk-es-1">splunk\.es</a>
    - <a href="#telekom-mms-icinga-director-1">telekom\_mms\.icinga\_director</a>
    - <a href="#theforeman-foreman-2">theforeman\.foreman</a>
    - <a href="#vmware-vmware-rest-2">vmware\.vmware\_rest</a>
    - <a href="#vultr-cloud-1">vultr\.cloud</a>
- <a href="#known-issues">Known Issues</a>
    - <a href="#dellemc-openmanage-4">dellemc\.openmanage</a>
- <a href="#new-plugins">New Plugins</a>
    - <a href="#callback">Callback</a>
    - <a href="#connection">Connection</a>
    - <a href="#filter">Filter</a>
    - <a href="#lookup">Lookup</a>
    - <a href="#test">Test</a>
- <a href="#new-modules">New Modules</a>
    - <a href="#check-point-mgmt-2">check\_point\.mgmt</a>
    - <a href="#cisco-ios-4">cisco\.ios</a>
    - <a href="#community-aws-2">community\.aws</a>
    - <a href="#community-digitalocean-2">community\.digitalocean</a>
    - <a href="#community-docker-5">community\.docker</a>
    - <a href="#community-general-4">community\.general</a>
    - <a href="#community-hashi-vault-2">community\.hashi\_vault</a>
    - <a href="#containers-podman-2">containers\.podman</a>
    - <a href="#dellemc-enterprise-sonic-2">dellemc\.enterprise\_sonic</a>
    - <a href="#dellemc-openmanage-5">dellemc\.openmanage</a>
    - <a href="#dellemc-powerflex-1">dellemc\.powerflex</a>
    - <a href="#fortinet-fortimanager-2">fortinet\.fortimanager</a>
    - <a href="#hetzner-hcloud-3">hetzner\.hcloud</a>
    - <a href="#infoblox-nios-modules-2">infoblox\.nios\_modules</a>
    - <a href="#netapp-ontap-2">netapp\.ontap</a>
    - <a href="#netbox-netbox-2">netbox\.netbox</a>
    - <a href="#purestorage-flasharray-2">purestorage\.flasharray</a>
    - <a href="#purestorage-flashblade-2">purestorage\.flashblade</a>
    - <a href="#theforeman-foreman-3">theforeman\.foreman</a>
    - <a href="#vultr-cloud-2">vultr\.cloud</a>
- <a href="#new-roles">New Roles</a>
- <a href="#unchanged-collections">Unchanged Collections</a>

<a id="release-summary"></a>
### Release Summary

Release Date\: 2024\-04\-09

[Porting Guide](https\://docs\.ansible\.com/ansible/devel/porting\_guides\.html)

<a id="removed-collections"></a>
### Removed Collections

* community\.azure \(previously included version\: 2\.0\.0\)
* community\.sap \(previously included version\: 2\.0\.0\)
* gluster\.gluster \(previously included version\: 1\.0\.2\)
* hpe\.nimble \(previously included version\: 1\.1\.4\)
* netapp\.aws \(previously included version\: 21\.7\.1\)
* netapp\.azure \(previously included version\: 21\.10\.1\)
* netapp\.elementsw \(previously included version\: 21\.7\.0\)
* netapp\.um\_info \(previously included version\: 21\.8\.1\)
* purestorage\.fusion \(previously included version\: 1\.6\.0\)

<a id="added-collections"></a>
### Added Collections

* community\.library\_inventory\_filtering\_v1 \(version 1\.0\.0\)

<a id="ansible-core"></a>
### Ansible\-core

Ansible 10\.0\.0a1 contains ansible\-core version 2\.17\.0b1\.
This is a newer version than version 2\.16\.0 contained in the previous Ansible release\.

The changes are reported in the combined changelog below\.

<a id="included-collections"></a>
### Included Collections

If not mentioned explicitly\, the changes are reported in the combined changelog below\.

| Collection                               | Ansible 9.0.0 | Ansible 10.0.0a1 | Notes                                                                                                                        |
| ---------------------------------------- | ------------- | ---------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| amazon.aws                               | 7.0.0         | 7.5.0            |                                                                                                                              |
| ansible.netcommon                        | 5.3.0         | 6.0.0            |                                                                                                                              |
| ansible.utils                            | 2.11.0        | 4.0.0            |                                                                                                                              |
| ansible.windows                          | 2.1.0         | 2.3.0            |                                                                                                                              |
| arista.eos                               | 6.2.1         | 8.0.0            |                                                                                                                              |
| awx.awx                                  | 23.3.1        | 24.1.0           | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
| azure.azcollection                       | 1.19.0        | 2.3.0            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
| check_point.mgmt                         | 5.1.1         | 5.2.3            |                                                                                                                              |
| cisco.aci                                | 2.8.0         | 2.9.0            |                                                                                                                              |
| cisco.asa                                | 4.0.3         | 5.0.1            |                                                                                                                              |
| cisco.dnac                               | 6.7.6         | 6.13.2           |                                                                                                                              |
| cisco.intersight                         | 2.0.3         | 2.0.8            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
| cisco.ios                                | 5.2.0         | 7.0.0            |                                                                                                                              |
| cisco.iosxr                              | 6.1.0         | 8.0.0            |                                                                                                                              |
| cisco.ise                                | 2.5.16        | 2.8.1            |                                                                                                                              |
| cisco.meraki                             | 2.16.14       | 2.18.0           |                                                                                                                              |
| cisco.mso                                | 2.5.0         | 2.6.0            |                                                                                                                              |
| cisco.nxos                               | 5.2.1         | 7.0.0            |                                                                                                                              |
| cloud.common                             | 2.1.4         | 3.0.0            |                                                                                                                              |
| community.aws                            | 7.0.0         | 7.2.0            |                                                                                                                              |
| community.ciscosmb                       | 1.0.7         | 1.0.8            |                                                                                                                              |
| community.crypto                         | 2.16.0        | 2.18.0           |                                                                                                                              |
| community.digitalocean                   | 1.24.0        | 1.26.0           |                                                                                                                              |
| community.dns                            | 2.6.3         | 2.8.3            |                                                                                                                              |
| community.docker                         | 3.4.11        | 3.8.1            |                                                                                                                              |
| community.general                        | 8.0.2         | 8.5.0            |                                                                                                                              |
| community.grafana                        | 1.6.1         | 1.8.0            |                                                                                                                              |
| community.hashi_vault                    | 6.0.0         | 6.2.0            |                                                                                                                              |
| community.hrobot                         | 1.8.2         | 1.9.1            |                                                                                                                              |
| community.library_inventory_filtering_v1 |               | 1.0.0            | The collection was added to Ansible                                                                                          |
| community.mongodb                        | 1.6.3         | 1.7.3            | There are no changes recorded in the changelog.                                                                              |
| community.mysql                          | 3.8.0         | 3.9.0            |                                                                                                                              |
| community.okd                            | 2.3.0         | 3.0.1            |                                                                                                                              |
| community.postgresql                     | 3.2.0         | 3.4.0            |                                                                                                                              |
| community.rabbitmq                       | 1.2.3         | 1.3.0            |                                                                                                                              |
| community.routeros                       | 2.10.0        | 2.14.0           |                                                                                                                              |
| community.sap_libs                       | 1.4.1         | 1.4.2            |                                                                                                                              |
| community.vmware                         | 4.0.0         | 4.2.0            |                                                                                                                              |
| community.windows                        | 2.0.0         | 2.2.0            |                                                                                                                              |
| community.zabbix                         | 2.1.0         | 2.3.1            |                                                                                                                              |
| containers.podman                        | 1.11.0        | 1.12.1           |                                                                                                                              |
| cyberark.pas                             | 1.0.23        | 1.0.25           | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
| dellemc.enterprise_sonic                 | 2.2.0         | 2.4.0            |                                                                                                                              |
| dellemc.openmanage                       | 8.4.0         | 9.1.0            |                                                                                                                              |
| dellemc.powerflex                        | 2.0.1         | 2.3.0            |                                                                                                                              |
| dellemc.unity                            | 1.7.1         | 2.0.0            |                                                                                                                              |
| f5networks.f5_modules                    | 1.27.0        | 1.28.0           |                                                                                                                              |
| fortinet.fortimanager                    | 2.3.0         | 2.4.0            |                                                                                                                              |
| fortinet.fortios                         | 2.3.4         | 2.3.6            |                                                                                                                              |
| google.cloud                             | 1.2.0         | 1.3.0            |                                                                                                                              |
| grafana.grafana                          | 2.2.3         | 3.0.0            |                                                                                                                              |
| hetzner.hcloud                           | 2.3.0         | 3.0.0            |                                                                                                                              |
| ibm.qradar                               | 2.1.0         | 3.0.0            |                                                                                                                              |
| ibm.storage_virtualize                   | 2.1.0         | 2.3.1            |                                                                                                                              |
| infinidat.infinibox                      | 1.3.12        | 1.4.3            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
| infoblox.nios_modules                    | 1.5.0         | 1.6.1            |                                                                                                                              |
| inspur.ispim                             | 2.1.0         | 2.2.0            |                                                                                                                              |
| junipernetworks.junos                    | 5.3.0         | 7.0.0            |                                                                                                                              |
| kubernetes.core                          | 2.4.0         | 3.0.1            |                                                                                                                              |
| lowlydba.sqlserver                       | 2.2.2         | 2.3.2            |                                                                                                                              |
| microsoft.ad                             | 1.3.0         | 1.5.0            |                                                                                                                              |
| netapp.ontap                             | 22.8.2        | 22.10.0          |                                                                                                                              |
| netapp.storagegrid                       | 21.11.1       | 21.12.0          |                                                                                                                              |
| netbox.netbox                            | 3.15.0        | 3.17.0           |                                                                                                                              |
| openstack.cloud                          | 2.1.0         | 2.2.0            | Unfortunately, this collection does not provide changelog data in a format that can be processed by the changelog generator. |
| purestorage.flasharray                   | 1.22.0        | 1.27.0           |                                                                                                                              |
| purestorage.flashblade                   | 1.14.0        | 1.17.0           |                                                                                                                              |
| splunk.es                                | 2.1.0         | 3.0.0            |                                                                                                                              |
| telekom_mms.icinga_director              | 1.34.1        | 2.1.0            |                                                                                                                              |
| theforeman.foreman                       | 3.14.0        | 4.0.0            |                                                                                                                              |
| vmware.vmware_rest                       | 2.3.1         | 3.0.1            |                                                                                                                              |
| vultr.cloud                              | 1.10.0        | 1.12.1           |                                                                                                                              |

<a id="major-changes"></a>
### Major Changes

<a id="ansible-core-1"></a>
#### Ansible\-core

* urls\.py \- Removed support for Python 2

<a id="ansible-netcommon"></a>
#### ansible\.netcommon

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.

<a id="ansible-utils"></a>
#### ansible\.utils

* Bumping <em class="title-reference">netaddr</em> to <em class="title-reference">\>\=0\.10\.1</em>\, means that starting from this release\, the minimum <em class="title-reference">netaddr</em> version this collection requires is <em class="title-reference">\>\=0\.10\.1</em>\.
* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.
* This release mainly addresses the breaking changes in the <em class="title-reference">netaddr</em> library\.
* With the new release of <em class="title-reference">netaddr</em> 1\.0\.0\, the <em class="title-reference">IPAddress\.is\_private\(\)</em> method has been removed and instead\, the <em class="title-reference">IPAddress\.is\_global\(\)</em> method has been extended to support the same functionality\. This change has been reflected in the <em class="title-reference">ipaddr</em> filter plugin\.

<a id="arista-eos"></a>
#### arista\.eos

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.
* This release removes previously deprecated modules and attributes from this collection\. Please refer to the <strong>Removed Features</strong> section for details\.

<a id="cisco-asa"></a>
#### cisco\.asa

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.

<a id="cisco-ios"></a>
#### cisco\.ios

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.
* ios\_ntp \- Remove deprecated ntp legacy module

<a id="cisco-iosxr"></a>
#### cisco\.iosxr

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.
* This release removes previously deprecated module and attributes from this collection\. Please refer to the <strong>Removed Features</strong> section for details\.

<a id="cisco-nxos"></a>
#### cisco\.nxos

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.
* This release removes four previously deprecated modules from this collection\. Please refer to the <strong>Removed Features</strong> section for details\.

<a id="community-docker"></a>
#### community\.docker

* The <code>community\.docker</code> collection now depends on the <code>community\.library\_inventory\_filtering\_v1</code> collection\. This utility collection provides host filtering functionality for inventory plugins\. If you use the Ansible community package\, both collections are included and you do not have to do anything special\. If you install the collection with <code>ansible\-galaxy collection install</code>\, it will be installed automatically\. If you install the collection by copying the files of the collection to a place where ansible\-core can find it\, for example by cloning the git repository\, you need to make sure that you also have to install the dependency if you are using the inventory plugins \([https\://github\.com/ansible\-collections/community\.docker/pull/698](https\://github\.com/ansible\-collections/community\.docker/pull/698)\)\.

<a id="community-hashi-vault"></a>
#### community\.hashi\_vault

* requirements \- the <code>requests</code> package which is required by <code>hvac</code> now has a more restrictive range for this collection in certain use cases due to breaking security changes in <code>ansible\-core</code> that were backported \([https\://github\.com/ansible\-collections/community\.hashi\_vault/pull/416](https\://github\.com/ansible\-collections/community\.hashi\_vault/pull/416)\)\.

<a id="community-mysql"></a>
#### community\.mysql

* Collection version 2\.\*\.\* is EOL\, no more bugfixes will be backported\. Please consider upgrading to the latest version\.

<a id="dellemc-openmanage"></a>
#### dellemc\.openmanage

* All OME modules are enhanced to support the environment variables <em class="title-reference">OME\_USERNAME</em> and <em class="title-reference">OME\_PASSWORD</em> as fallback for credentials\.
* All iDRAC and Redfish modules are enhanced to support the environment variables <em class="title-reference">IDRAC\_USERNAME</em> and <em class="title-reference">IDRAC\_PASSWORD</em> as fallback for credentials\.
* idrac\_certificates \- The module is enhanced to support the import and export of <em class="title-reference">CUSTOMCERTIFICATE</em>\.
* idrac\_diagnostics \- The module is introduced to run and export diagnostics on iDRAC\.
* idrac\_gather\_facts \- This role is enhanced to support secure boot\.
* idrac\_license \- The module is introduced to configure iDRAC licenses\.
* idrac\_user \- This role is introduced to manage local users of iDRAC\.

<a id="dellemc-unity"></a>
#### dellemc\.unity

* Adding support for Unity Puffin v5\.4\.

<a id="fortinet-fortios"></a>
#### fortinet\.fortios

* Add notes for backup modules in the documentation in both monitor and monitor\_fact modules\.
* Supported new FOS versions 7\.4\.2 and 7\.4\.3\, and support data type mac\_address in the collection\.
* Update all the boolean values to true/false in the documents and examples\.
* Update the document of log\_fact\.
* Update the documentation for the supported versions from latest to a fix version number\.
* Update the mismatched version message with version ranges\.
* Update the required ansible version to 2\.14\.
* Update the required ansible version to 2\.15\.
* Update the supported version ranges instead of concrete version numbers to reduce the collection size\.

<a id="grafana-grafana"></a>
#### grafana\.grafana

* Add an Ansible role for OpenTelemetry Collector by \@ishanjainn in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/138](https\://github\.com/grafana/grafana\-ansible\-collection/pull/138)

<a id="ibm-qradar"></a>
#### ibm\.qradar

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.

<a id="infoblox-nios-modules"></a>
#### infoblox\.nios\_modules

* Upgrade Ansible version support from 2\.13 to 2\.16\.
* Upgrade Python version support from 3\.8 to 3\.10\.

<a id="junipernetworks-junos"></a>
#### junipernetworks\.junos

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.
* This release removes previously deprecated modules from this collection\. Please refer to the <strong>Removed Features</strong> section for details\.

<a id="splunk-es"></a>
#### splunk\.es

* Bumping <em class="title-reference">requires\_ansible</em> to <em class="title-reference">\>\=2\.14\.0</em>\, since previous ansible\-core versions are EoL now\.

<a id="minor-changes"></a>
### Minor Changes

<a id="ansible-core-2"></a>
#### Ansible\-core

* Add <code>dump</code> and <code>passno</code> mount information to facts component \([https\://github\.com/ansible/ansible/issues/80478](https\://github\.com/ansible/ansible/issues/80478)\)
* Added MIRACLE LINUX 9\.2 in RedHat OS Family\.
* Interpreter Discovery \- Remove hardcoded references to specific python interpreters to use for certain distro versions\, and modify logic for python3 to become the default\.
* Use Python\'s built\-in <code>functools\.update\_wrapper</code> instead an inline copy from Python 3\.7\.
* User can now set ansible\.log to record higher verbosity than what is specified for display via new configuration item LOG\_VERBOSITY\.
* <code>DEFAULT\_PRIVATE\_ROLE\_VARS</code> is now overridden by explicit setting of <code>public</code> for <code>include\_roles</code> and <code>import\_roles</code>\.
* <code>ansible\-galaxy role\|collection init</code> \- accept <code>\-\-extra\-vars</code> to supplement/override the variables <code>ansible\-galaxy</code> injects for templating <code>\.j2</code> files in the skeleton\.
* <code>import\_role</code> action now also gets a <code>public</code> option that controls variable exports\,  default depending on <code>DEFAULT\_PRIVATE\_ROLE\_VARS</code> \(if using defaults equates to <code>public\=True</code>\)\.
* added configuration item <code>TARGET\_LOG\_INFO</code> that allows the user/author to add an information string to the log output on targets\.
* ansible\-doc \- treat double newlines in documentation strings as paragraph breaks\. This is useful to create multi\-paragraph notes in module/plugin documentation \([https\://github\.com/ansible/ansible/pull/82465](https\://github\.com/ansible/ansible/pull/82465)\)\.
* ansible\-doc output has been revamped to make it more visually pleasing when going to a terminal\, also more concise\, use \-v to show extra information\.
* ansible\-galaxy \- Started normalizing build directory with a trailing separator when building collections\, internally\. \([https\://github\.com/ansible/ansible/pull/81619](https\://github\.com/ansible/ansible/pull/81619)\)\.
* ansible\-galaxy dependency resolution messages have changed the unexplained \'virtual\' collection for the specific type \(\'scm\'\, \'dir\'\, etc\) that is more user friendly
* ansible\-test \- Add Alpine 3\.19 container\.
* ansible\-test \- Add Alpine 3\.19 to remotes\.
* ansible\-test \- Add Fedora 39 container\.
* ansible\-test \- Add Fedora 39 remote\.
* ansible\-test \- Add a work\-around for permission denied errors when using <code>pytest \>\= 8</code> on multi\-user systems with an installed version of <code>ansible\-test</code>\.
* ansible\-test \- Add support for RHEL 9\.3 remotes\.
* ansible\-test \- Added a macOS 14\.3 remote VM\.
* ansible\-test \- Bump the <code>nios\-test\-container</code> from version 2\.0\.0 to version 3\.0\.0\.
* ansible\-test \- Containers and remotes managed by ansible\-test will have their Python <code>EXTERNALLY\-MANAGED</code> marker \(PEP668\) removed\. This provides backwards compatibility for existing tests running in newer environments which mark their Python as externally managed\. A future version of ansible\-test may change this behavior\, requiring tests to be adapted to such environments\.
* ansible\-test \- Make Python 3\.12 the default version used in the <code>base</code> and <code>default</code> containers\.
* ansible\-test \- Remove Alpine 3\(\.18\) container\.
* ansible\-test \- Remove Alpine 3\.18 from remotes\.
* ansible\-test \- Remove Fedora 38 remote support\.
* ansible\-test \- Remove Fedora 38 test container\.
* ansible\-test \- Remove rhel/9\.2 test remote
* ansible\-test \- Remove the FreeBSD 13\.2 remote\.
* ansible\-test \- Removed fallback to <code>virtualenv</code> when <code>\-m venv</code> is non\-functional\.
* ansible\-test \- Removed test remotes\: macos/13\.2
* ansible\-test \- Removed the <code>no\-basestring</code> sanity test\. The test is no longer necessary now that Python 3 is required\.
* ansible\-test \- Removed the <code>no\-dict\-iteritems</code>\, <code>no\-dict\-iterkeys</code> and <code>no\-dict\-itervalues</code> sanity tests\. The tests are no longer necessary since Python 3 is required\.
* ansible\-test \- Removed the <code>no\-main\-display</code> sanity test\. The unwanted pattern is unlikely to occur\, since the test has existed since Ansible 2\.8\.
* ansible\-test \- Removed the <code>no\-unicode\-literals</code> sanity test\. The test is unnecessary now that Python 3 is required and the <code>unicode\_literals</code> feature has no effect\.
* ansible\-test \- Special handling for installation of <code>cryptography</code> has been removed\, as it is no longer necessary\.
* ansible\-test \- The <code>shellcheck</code> sanity test no longer disables the <code>SC2164</code> check\. In most cases\, seeing this error means the script is missing <code>set \-e</code>\.
* ansible\-test \- The <code>unidiomatic\-typecheck</code> rule has been enabled in the <code>pylint</code> sanity test\.
* ansible\-test \- The <code>unidiomatic\-typecheck</code> rule has been removed from the <code>validate\-modules</code> sanity test\.
* ansible\-test \- Update the base and default containers to use Ubuntu 22\.04 for the base image\. This also updates PowerShell to version 7\.4\.0 with \.NET 8\.0\.0 and ShellCheck to version 0\.8\.0\.
* ansible\-test \- Updated the CloudStack test container to version 1\.7\.0\.
* ansible\-test \- Updated the distro test containers to version 6\.3\.0 to include coverage 7\.3\.2 for Python 3\.8\+\. The alpine3 container is now based on 3\.18 instead of 3\.17 and includes Python 3\.11 instead of Python 3\.10\.
* ansible\-test \- Updated the distro test containers to version 7\.1\.0\.
* ansible\-test \- When ansible\-test installs requirements\, it now instructs pip to allow installs on externally managed environments as defined by PEP 668\. This only occurs in ephemeral environments managed by ansible\-test\, such as containers\, or when the <em class="title-reference">\-\-requirements</em> option is used\.
* ansible\-test \- When invoking <code>sleep</code> in containers during container setup\, the <code>env</code> command is used to avoid invoking the shell builtin\, if present\.
* ansible\-test \- document block name now included in error message for YAML parsing errors \([https\://github\.com/ansible/ansible/issues/82353](https\://github\.com/ansible/ansible/issues/82353)\)\.
* ansible\-test \- sanity test allows <code>EXAMPLES</code> to be multi\-document YAML \([https\://github\.com/ansible/ansible/issues/82353](https\://github\.com/ansible/ansible/issues/82353)\)\.
* ansible\-test now has FreeBSD 13\.3 and 14\.0 support
* ansible\.builtin\.user \- Remove user not found warning \([https\://github\.com/ansible/ansible/issues/80267](https\://github\.com/ansible/ansible/issues/80267)\)
* apt\_repository\.py \- use api\.launchpad\.net endpoint instead of launchpad\.net/api
* async tasks can now also support check mode at the same time\.
* async\_status now supports check mode\.
* constructed inventory plugin \- Adding a note that only group\_vars of explicit groups are loaded \([https\://github\.com/ansible/ansible/pull/82580](https\://github\.com/ansible/ansible/pull/82580)\)\.
* csvfile \- add a keycol parameter to specify in which column to search\.
* dnf \- add the <code>best</code> option
* dnf5 \- add the <code>best</code> option
* filter plugin \- Add the count and mandatory\_count parameters in the regex\_replace filter
* find \- add a encoding parameter to specify which encoding of the files to be searched\.
* git module \- gpg\_allowlist name was added in 2\.17 and we will eventually deprecate the gpg\_whitelist alias\.
* import\_role \- allow subdirectories with <code>\_from</code> options for parity with <code>include\_role</code> \([https\://github\.com/ansible/ansible/issues/82584](https\://github\.com/ansible/ansible/issues/82584)\)\.
* module argument spec \- Allow module authors to include arbitrary additional context in the argument spec\, by making use of a new top level key called <code>context</code>\. This key should be a dict type\. This allows for users to customize what they place in the argument spec\, without having to ignore sanity tests that validate the schema\.
* modules \- Add the ability for an action plugin to call <code>self\.\_execute\_module\(\*\, ignore\_unknown\_opts\=True\)</code> to execute a module with options that may not be supported for the version being called\. This tells the module basic wrapper to ignore validating the options provided match the arg spec\.
* package action now has a configuration that overrides the detected package manager\, it is still overridden itself by the use option\.
* py3compat \- Remove <code>ansible\.utils\.py3compat</code> as it is no longer necessary
* removed the unused argument <code>create\_new\_password</code> from <code>CLI\.build\_vault\_ids</code> \([https\://github\.com/ansible/ansible/pull/82066](https\://github\.com/ansible/ansible/pull/82066)\)\.
* urls \- Add support for TLS 1\.3 post handshake certificate authentication \- [https\://github\.com/ansible/ansible/issues/81782](https\://github\.com/ansible/ansible/issues/81782)
* urls \- reduce complexity of <code>Request\.open</code>
* user \- accept yescrypt hash as user password
* validate\-modules tests now correctly handles <code>choices</code> in dictionary format\.

<a id="amazon-aws"></a>
#### amazon\.aws

* AnsibeAWSModule \- added <code>fail\_json\_aws\_error\(\)</code> as a wrapper for <code>fail\_json\(\)</code> and <code>fail\_json\_aws\(\)</code> when passed an <code>AnsibleAWSError</code> exception \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1997](https\://github\.com/ansible\-collections/amazon\.aws/pull/1997)\)\.
* autoscaling\_group \- minor PEP8 whitespace sanity fixes \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1846](https\://github\.com/ansible\-collections/amazon\.aws/pull/1846)\)\.
* backup\_plan \- Let user to set <code>schedule\_expression\_timezone</code> for backup plan rules when when using botocore \>\= 1\.31\.36 \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1952](https\://github\.com/ansible\-collections/amazon\.aws/issues/1952)\)\.
* ec2\_ami\_info \- simplify parameters to <code>get\_image\_attribute</code> to only pass ID of image \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1846](https\://github\.com/ansible\-collections/amazon\.aws/pull/1846)\)\.
* ec2\_eip \- use <code>ResourceTags</code> to set initial tags upon creation \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1843](https\://github\.com/ansible\-collections/amazon\.aws/issues/1843)\)
* ec2\_instance \- Add support for modifying metadata options of an existing instance \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1918](https\://github\.com/ansible\-collections/amazon\.aws/pull/1918)\)\.
* ec2\_instance \- add support for AdditionalInfo option when creating an instance \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1828](https\://github\.com/ansible\-collections/amazon\.aws/pull/1828)\)\.
* ec2\_security\_group \- use <code>ResourceTags</code> to set initial tags upon creation \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1844](https\://github\.com/ansible\-collections/amazon\.aws/pull/1844)\)
* ec2\_vpc\_igw \- use <code>ResourceTags</code> to set initial tags upon creation \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1843](https\://github\.com/ansible\-collections/amazon\.aws/issues/1843)\)
* ec2\_vpc\_route\_table \- use <code>ResourceTags</code> to set initial tags upon creation \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1843](https\://github\.com/ansible\-collections/amazon\.aws/issues/1843)\)
* ec2\_vpc\_subnet \- the default value for <code>tags</code> has been changed from <code>\{\}</code> to <code>None</code>\, to remove tags from a subnet an empty map must be explicitly passed to the module \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1876](https\://github\.com/ansible\-collections/amazon\.aws/pull/1876)\)\.
* ec2\_vpc\_subnet \- use <code>ResourceTags</code> to set initial tags upon creation \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1843](https\://github\.com/ansible\-collections/amazon\.aws/issues/1843)\)
* ec2\_vpc\_subnet \- use <code>wait\_timeout</code> to also control maximum time to wait for initial creation of subnets \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1848](https\://github\.com/ansible\-collections/amazon\.aws/pull/1848)\)\.
* iam\_access\_key \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_access\_key\_info \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_group \- Basic testing of <code>name</code> and <code>path</code> has been added to improve error messages \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_group \- <code>group\_name</code> has been added as an alias to <code>name</code> for consistency with other IAM modules \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_group \- add support for setting group path \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1892](https\://github\.com/ansible\-collections/amazon\.aws/pull/1892)\)\.
* iam\_group \- adds attached\_policies return value \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1892](https\://github\.com/ansible\-collections/amazon\.aws/pull/1892)\)\.
* iam\_group \- code refactored to avoid single long function \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1892](https\://github\.com/ansible\-collections/amazon\.aws/pull/1892)\)\.
* iam\_group \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_instance\_profile \- Basic testing of <code>name</code> and <code>path</code> has been added to improve error messages \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_instance\_profile \- attempting to change the <code>path</code> for an existing profile will now generate a warning\, previously this was silently ignored \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_instance\_profile \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_instance\_profile \- the <code>prefix</code> parameter has been renamed <code>path</code> for consistency with other IAM modules\, <code>prefix</code> remains as an alias\. No change to playbooks is required \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_instance\_profile \- the default value for <code>path</code> has been removed\.  New instances will still be created with a default path of <code>/</code>\. No change to playbooks is required \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_instance\_profile\_info \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_managed\_policy \- Basic testing of <code>name</code> and <code>path</code> has been added to improve error messages \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_managed\_policy \- <code>description</code> attempting to update the description now results in a warning\, previously it was simply ignored \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1936](https\://github\.com/ansible\-collections/amazon\.aws/pull/1936)\)\.
* iam\_managed\_policy \- <code>policy</code> is no longer a required parameter \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1936](https\://github\.com/ansible\-collections/amazon\.aws/pull/1936)\)\.
* iam\_managed\_policy \- added support for tagging managed policies \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1936](https\://github\.com/ansible\-collections/amazon\.aws/pull/1936)\)\.
* iam\_managed\_policy \- more consistently perform retries on rate limiting errors \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1936](https\://github\.com/ansible\-collections/amazon\.aws/pull/1936)\)\.
* iam\_managed\_policy \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_managed\_policy \- support for setting <code>path</code> \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1936](https\://github\.com/ansible\-collections/amazon\.aws/pull/1936)\)\.
* iam\_managed\_policy \- the <code>policy\_description</code> parameter has been renamed <code>description</code> for consistency with other IAM modules\, <code>policy\_description</code> remains as an alias\. No change to playbooks is required \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_managed\_policy \- the <code>policy\_name</code> parameter has been renamed <code>name</code> for consistency with other IAM modules\, <code>policy\_name</code> remains as an alias\. No change to playbooks is required \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_mfa\_device\_info \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_role \- Basic testing of <code>name</code> and <code>path</code> has been added to improve error messages \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_role \- <code>prefix</code> and <code>path\_prefix</code> have been added as aliases to <code>path</code> for consistency with other IAM modules \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_role \- <code>role\_name</code> has been added as an alias to <code>name</code> for consistency with other IAM modules \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_role \- attempting to change the <code>path</code> for an existing profile will now generate a warning\, previously this was silently ignored \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_role \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_role \- the default value for <code>path</code> has been removed\.  New roles will still be created with a default path of <code>/</code>\. No change to playbooks is required \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_role\_info \- <code>path</code> and <code>prefix</code> have been added as aliases to <code>path\_prefix</code> for consistency with other IAM modules \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_role\_info \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_user \- Basic testing of <code>name</code> and <code>path</code> has been added to improve error messages \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_user \- <code>user\_name</code> has been added as an alias to <code>name</code> for consistency with other IAM modules \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_user \- add <code>boundary</code> parameter to support managing boundary policy on users \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1912](https\://github\.com/ansible\-collections/amazon\.aws/pull/1912)\)\.
* iam\_user \- add <code>path</code> parameter to support managing user path \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1912](https\://github\.com/ansible\-collections/amazon\.aws/pull/1912)\)\.
* iam\_user \- added <code>attached\_policies</code> to return value \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1912](https\://github\.com/ansible\-collections/amazon\.aws/pull/1912)\)\.
* iam\_user \- refactored code to reduce complexity \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1912](https\://github\.com/ansible\-collections/amazon\.aws/pull/1912)\)\.
* iam\_user \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_user \- refactored error handling to use a decorator \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1951](https\://github\.com/ansible\-collections/amazon\.aws/pull/1951)\)\.
* iam\_user\_info \- Add <code>login\_profile</code> to return info that is get from a user\, to know if they can login from AWS console \([https\://github\.com/ansible\-collections/amazon\.aws/pull/2012](https\://github\.com/ansible\-collections/amazon\.aws/pull/2012)\)\.
* iam\_user\_info \- <code>prefix</code> has been added as an alias to <code>path\_prefix</code> for consistency with other IAM modules \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* iam\_user\_info \- refactored code to use <code>AnsibleIAMError</code> and <code>IAMErrorHandler</code> as well as moving shared code into module\_utils\.iam \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.
* iam\_user\_info \- the <code>path</code> parameter has been renamed <code>path\_prefix</code> for consistency with other IAM modules\, <code>path</code> remains as an alias\. No change to playbooks is required \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1933](https\://github\.com/ansible\-collections/amazon\.aws/pull/1933)\)\.
* lambda \- added support for using ECR images for the function \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1939](https\://github\.com/ansible\-collections/amazon\.aws/pull/1939)\)\.
* module\_utils\.errors \- added a basic error handler decorator \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1951](https\://github\.com/ansible\-collections/amazon\.aws/pull/1951)\)\.
* module\_utils\.iam \- refactored normalization functions to use <code>boto3\_resource\_to\_ansible\_dict\(\)</code> and <code>boto3\_resource\_list\_to\_ansible\_dict\(\)</code> \([https\://github\.com/ansible\-collections/amazon\.aws/pull/2006](https\://github\.com/ansible\-collections/amazon\.aws/pull/2006)\)\.
* module\_utils\.transformations \- add <code>boto3\_resource\_to\_ansible\_dict\(\)</code> and <code>boto3\_resource\_list\_to\_ansible\_dict\(\)</code> helpers \([https\://github\.com/ansible\-collections/amazon\.aws/pull/2006](https\://github\.com/ansible\-collections/amazon\.aws/pull/2006)\)\.
* rds\_cluster \- Add support for ServerlessV2ScalingConfiguration to create and modify cluster operations \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1839](https\://github\.com/ansible\-collections/amazon\.aws/pull/1839)\)\.
* rds\_instance\_snapshot \- minor PEP8 whitespace sanity fixes \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1846](https\://github\.com/ansible\-collections/amazon\.aws/pull/1846)\)\.
* s3\_bucket\_info \- add parameter <code>bucket\_versioning</code> to return the versioning state of a bucket \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1919](https\://github\.com/ansible\-collections/amazon\.aws/pull/1919)\)\.
* s3\_object\_info \- fix exception raised when listing objects from empty bucket \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1919](https\://github\.com/ansible\-collections/amazon\.aws/pull/1919)\)\.

<a id="ansible-utils-1"></a>
#### ansible\.utils

* Add support in fact\_diff filter plugin to show common lines\.\([https\://github\.com/ansible\-collections/ansible\.utils/issues/311](https\://github\.com/ansible\-collections/ansible\.utils/issues/311)\)
* Fact\_diff filter plugin \- Add fact\_diff filter plugin\. \([https\://github\.com/ansible\-collections/ansible\.utils/issues/78](https\://github\.com/ansible\-collections/ansible\.utils/issues/78)\)\.

<a id="ansible-windows"></a>
#### ansible\.windows

* Set minimum supported Ansible version to 2\.14 to align with the versions still supported by Ansible\.
* win\_share \- Added a new param called <code>scope\_name</code> that allows file shares to be scoped for Windows Server failover cluster roles\.
* win\_uri \- Max depth for json object conversion used to be 2\. Can now send json objects with up to 20 levels of nesting

<a id="check-point-mgmt"></a>
#### check\_point\.mgmt

* New resource modules for R81\.20 JHF Take 43
* meta/runtime\.yml \- update minimum Ansible version required to 2\.14\.0\.

<a id="cisco-aci"></a>
#### cisco\.aci

* Add Authentification option for EIGRP interface profile\.
* Add L3out Floating SVI modules \(aci\_l3out\_floating\_svi\, aci\_l3out\_floating\_svi\_path\, aci\_l3out\_floating\_svi\_path\_secondary\_ip and aci\_l3out\_floating\_svi\_secondary\_ip\) \(\#478\)
* Add No\-verification flag option to reduce the number of API calls\. If true\, a verifying GET will not be sent after a POST update to APIC
* Add access spine interface selector and port block binding in aci\_access\_port\_block\_to\_access\_port
* Add aci\_access\_spine\_interface\_selector module
* Add aci\_action\_rule\_additional\_communities module
* Add aci\_action\_rule\_set\_as\_path and aci\_action\_rule\_set\_as\_path\_asn modules
* Add aci\_bgp\_peer\_prefix\_policy\, aci\_bgp\_route\_summarization\_policy and aci\_bgp\_address\_family\_context\_policy modules
* Add aci\_fabric\_pod\, aci\_fabric\_pod\_external\_tep\, aci\_fabric\_pod\_profile\, aci\_fabric\_pod\_remote\_pool modules \(\#558\)
* Add aci\_hsrp\_interface\_policy\, aci\_l3out\_hsrp\_group\, aci\_l3out\_hsrp\_interface\_profile and aci\_l3out\_hsrp\_secondary\_vip modules \(\#505\)
* Add aci\_interface\_policy\_eigrp \(class\:eigrpIfPol\) module
* Add aci\_interface\_policy\_pim module
* Add aci\_interface\_policy\_storm\_control module
* Add aci\_keychain\_policy and aci\_key\_policy modules
* Add aci\_l3out\_bfd\_multihop\_interface\_profile\, aci\_l3out\_bfd\_interface\_profile\, aci\_interface\_policy\_bfd\_multihop\, aci\_interface\_policy\_bfd and aci\_bfd\_multihop\_node\_policy modules \(\#492\)
* Add aci\_l3out\_dhcp\_relay\_label\, aci\_dhcp\_option\_policy and aci\_dhcp\_option modules
* Add aci\_l3out\_eigrp\_interface\_profile module
* Add aci\_listify filter plugin to flattens nested dictionaries
* Add aci\_netflow\_exporter\_policy module
* Add aci\_netflow\_monitor\_policy and aci\_netflow\_record\_policy modules
* Add aci\_netflow\_monitor\_to\_exporter module
* Add aci\_node\_block module
* Add aci\_pim\_route\_map\_policy and aci\_pim\_route\_map\_entry modules
* Add aci\_qos\_custom\_policy and aci\_qos\_dscp\_class modules
* Add aci\_qos\_dot1p\_class module
* Add action rules attributes to aci\_tenant\_action\_rule\_profile\.
* Add auto to speed attribute options in aci\_interface\_policy\_link\_level module \(\#577\)
* Add missing options to aci\_bd module
* Add modules aci\_bd\_to\_netflow\_monitor\_policy and aci\_bd\_rogue\_exception\_mac \(\#600\)
* Add modules for Fabric External Connection Policies and its childs
* Add option to set delimiter to  \_  in aci\_epg\_to\_domain module
* Add qos\_custom\_policy\, pim\_interface\_policy and igmp\_interface\_policy as new child\_classes for aci\_l3out\_logical\_interface\_profile\.
* Add support for annotation in aci\_rest module \(\#437\)
* Add support for block statements in useg attributes with the aci\_epg\_useg\_attribute\_block\_statement module
* Add support for configuration of access switch policy groups with aci\_access\_switch\_policy\_group module
* Add support for configuration of certificate authorities in aci\_aaa\_certificate\_authority
* Add support for configuration of fabric management access policies in aci\_fabric\_management\_access
* Add support for configuration of vrf multicast with aci\_vrf\_multicast module
* Add support for configuring Azure cloud subnets using the aci\_cloud\_subnet module
* Add support for encap scope in aci\_l3out\_interface
* Add support for https ssl cipher configuration in aci\_fabric\_management\_access\_https\_cipher
* Add support for infra l3out nodes bgp\-evpn loopback\, mpls transport loopback and segment id in aci\_l3out\_logical\_node
* Add support for infra sr mpls micro bfd in aci\_l3out\_interface
* Add support for intra epg\, taboo\, and contract interface in aci\_epg\_to\_contract
* Add support for key ring configuration in aci\_aaa\_key\_ring
* Add support for mac and description in aci\_l3out\_interface
* Add support for mpls custom qos policy for infra sr mpls l3outs node profiles in aci\_l3out\_logical\_node\_profile
* Add support for security default settings configuration in aci\_aaa\_security\_default\_settings
* Add support for simple statements in useg attributes with the aci\_epg\_useg\_attribute\_simple\_statement module
* Add support for sr\-mpls bgpInfraPeerP and bgp\_password in aci\_l3out\_bgp\_peer module \(\#543\)
* Add support for sr\-mpls in aci\_l3out module
* Add support for sr\-mpls l3out to infra l3out in aci\_l3out\_to\_sr\_mpls\_infra\_l3out
* Add support for subject labels for EPG\, EPG Contract\, ESG\, Contract Subject\, L2Out External EPG\, L3out External EPG\, and L3out External EPG Contract with the aci\_subject\_label module
* Add support for taboo contract\, contract interface and intra\_epg contract in aci\_l3out\_extepg\_to\_contract
* Add support for useg default block statement configuration for useg epg in aci\_epg
* Modify child class node block conditions to be optional in aci\_switch\_leaf\_selector

<a id="cisco-dnac"></a>
#### cisco\.dnac

* Added a method to validate IP addresses\.
* Added attributes \'dnac\_api\_task\_timeout\' and \'dnac\_task\_poll\_interval\' in intent and workflow\_manager modules\.
* Added the op\_modifies\=True when calling SDK APIs in the workflow manager modules\.
* Addressed image un\-tagging issues in inherited site settings\.
* Changes the minimum supported version from Ansible v2\.9\.10 to v2\.14\.0
* Corrected site creation issues in the site module when optional parameters are missing\.
* Fixed a minor issue in the site workflow manager module\.
* Fixed management IP updates for devices on SNMP version v2\.
* Introduced sample playbooks for the discovery module\.
* Provided documentation for EWLC templates in Cisco Catalyst Center version 2\.3\.7\.x\.
* Resolved a \'NoneType\' error in discovery module credentials\.
* Updating galaxy\.yml ansible\.utils dependencies\.
* inventory\_workflow\_manager \- Added attributes \'add\_user\_defined\_field\'\, \'update\_interface\_details\'\, \'export\_device\_list\' and \'admin\_status\'
* inventory\_workflow\_manager \- Removed attributes \'provision\_wireless\_device\'\, \'reprovision\_wired\_device\'

<a id="cisco-ios-1"></a>
#### cisco\.ios

* Added ios\_evpn\_evi resource module\.
* Added ios\_evpn\_global resource module\.
* Added ios\_vxlan\_vtep resource module\.
* Fixed ios\_evpn\_evi resource module integration test failure \- code to remove VLAN config\.
* ios\_bgp\_address\_family \- Fixed an issue with inherit peer\-policy CLI
* ios\_bgp\_address\_family \- added \'advertise\' key
* ios\_bgp\_global \- added \'bgp\.default\.ipv4\_unicast\' and \'bgp\.default\.route\_target\.filter\' key
* ios\_l3\_interfaces \- added \'autostate\'\, \'mac\_address\'\, \'ipv4\.source\_interface\'\, and \'ipv6\.enable\' key
* ios\_vlans \- Add purged state to deal with toplevel vlan and vlan configuration config\.
* ios\_vlans \- added vlan config CLI feature\.
* ios\_vrf \- added MDT related keys

<a id="cisco-iosxr-1"></a>
#### cisco\.iosxr

* Add missing options in afi and safi in address\-family of bgp\_templates RM\.
* iosxr\_facts \- Add cdp neighbors in ansible\_net\_neighbors dictionary \([https\://github\.com/ansible\-collections/cisco\.iosxr/pull/457](https\://github\.com/ansible\-collections/cisco\.iosxr/pull/457)\)\.

<a id="cisco-ise"></a>
#### cisco\.ise

* Changes the minimum supported version from Ansible v2\.9\.10 to v2\.14\.0
* Services included configuration\, edda\, dataconnect\_services\, subscriber\.
* cisco\.ise collection now supports ansible\.utils v3

<a id="cisco-meraki"></a>
#### cisco\.meraki

* Adding support to ansible\.utils \"\>\=2\.0\.0\, \<4\.00\"\.
* Ansible collection now support v1\.44\.1 of Dashboard Api\.
* administered\_licensing\_subscription\_entitlements\_info \- new plugin\.
* administered\_licensing\_subscription\_subscriptions\_bind \- new plugin\.
* administered\_licensing\_subscription\_subscriptions\_claim \- new plugin\.
* administered\_licensing\_subscription\_subscriptions\_claim\_key\_validate \- new plugin\.
* administered\_licensing\_subscription\_subscriptions\_compliance\_statuses\_info \- new plugin\.
* administered\_licensing\_subscription\_subscriptions\_info \- new plugin\.
* devices\_appliance\_radio\_settings \- new plugin\.
* devices\_appliance\_radio\_settings\_info \- new plugin\.
* devices\_live\_tools\_arp\_table \- new plugin\.
* devices\_live\_tools\_arp\_table\_info \- new plugin\.
* devices\_live\_tools\_cable\_test \- new plugin\.
* devices\_live\_tools\_cable\_test\_info \- new plugin\.
* devices\_live\_tools\_throughput\_test \- new plugin\.
* devices\_live\_tools\_throughput\_test\_info \- new plugin\.
* devices\_live\_tools\_wake\_on\_lan \- new plugin\.
* devices\_live\_tools\_wake\_on\_lan\_info \- new plugin\.
* devices\_wireless\_alternate\_management\_interface\_ipv6 \- new plugin\.
* networks\_appliance\_rf\_profiles \- new plugin\.
* networks\_appliance\_rf\_profiles\_info \- new plugin\.
* networks\_appliance\_traffic\_shaping\_vpn\_exclusions \- new plugin\.
* networks\_sm\_devices\_install\_apps \- new plugin\.
* networks\_sm\_devices\_reboot \- new plugin\.
* networks\_sm\_devices\_shutdown \- new plugin\.
* networks\_sm\_devices\_uninstall\_apps \- new plugin\.
* networks\_vlan\_profiles \- new plugin\.
* networks\_vlan\_profiles\_assignments\_by\_device\_info \- new plugin\.
* networks\_vlan\_profiles\_assignments\_reassign \- new plugin\.
* networks\_vlan\_profiles\_info \- new plugin\.
* networks\_wireless\_ethernet\_ports\_profiles \- new plugin\.
* networks\_wireless\_ethernet\_ports\_profiles\_assign \- new plugin\.
* networks\_wireless\_ethernet\_ports\_profiles\_info \- new plugin\.
* networks\_wireless\_ethernet\_ports\_profiles\_set\_default \- new plugin\.
* organizations\_appliance\_traffic\_shaping\_vpn\_exclusions\_by\_network\_info \- new plugin\.
* organizations\_appliance\_uplinks\_statuses\_overview\_info \- new plugin\.
* organizations\_appliance\_uplinks\_usage\_by\_network\_info \- new plugin\.
* organizations\_camera\_boundaries\_areas\_by\_device\_info \- new plugin\.
* organizations\_camera\_boundaries\_lines\_by\_device\_info \- new plugin\.
* organizations\_camera\_detections\_history\_by\_boundary\_by\_interval\_info \- new plugin\.
* organizations\_camera\_permissions\_info \- new plugin\.
* organizations\_camera\_roles \- new plugin\.
* organizations\_camera\_roles\_info \- new plugin\.
* organizations\_devices\_availabilities\_change\_history\_info \- new plugin\.
* organizations\_devices\_boots\_history\_info \- new plugin\.
* organizations\_sm\_admins\_roles \- new plugin\.
* organizations\_sm\_admins\_roles\_info \- new plugin\.
* organizations\_sm\_sentry\_policies\_assignments \- new plugin\.
* organizations\_sm\_sentry\_policies\_assignments\_by\_network\_info \- new plugin\.
* organizations\_summary\_top\_networks\_by\_status\_info \- new plugin\.
* organizations\_webhooks\_callbacks\_statuses\_info \- new plugin\.
* organizations\_wireless\_devices\_channel\_utilization\_by\_device\_info \- new plugin\.
* organizations\_wireless\_devices\_channel\_utilization\_by\_network\_info \- new plugin\.
* organizations\_wireless\_devices\_channel\_utilization\_history\_by\_device\_by\_interval\_info \- new plugin\.
* organizations\_wireless\_devices\_channel\_utilization\_history\_by\_network\_by\_interval\_info \- new plugin\.
* organizations\_wireless\_devices\_packet\_loss\_by\_client\_info \- new plugin\.
* organizations\_wireless\_devices\_packet\_loss\_by\_device\_info \- new plugin\.
* organizations\_wireless\_devices\_packet\_loss\_by\_network\_info \- new plugin\.

<a id="cisco-mso"></a>
#### cisco\.mso

* Add Azure Cloud site support to mso\_schema\_site\_contract\_service\_graph
* Add Azure Cloud site support to mso\_schema\_site\_service\_graph
* Add functionality to resolve same name in remote and local user\.
* Add l3out\_template and l3out\_schema arguments to mso\_schema\_site\_external\_epg \(\#394\)
* Add mso\_schema\_site\_contract\_service\_graph module to manage site contract service graph
* Add mso\_schema\_site\_contract\_service\_graph\_listener module to manage Azure site contract service graph listeners and update other modules
* Add new parameter remote\_user to add multiple remote users associated with multiple login domains
* Add support for replacing all existing contracts with new provided contracts in a single operation with one request and adding/removing multiple contracts in multiple operations with a single request in mso\_schema\_template\_anp\_epg\_contract module
* Add support for replacing all existing static ports with new provided static ports in a single operation with one request and adding/removing multiple static ports in multiple operations with a single request in mso\_schema\_template\_anp\_epg\_staticport module
* Add support for required attributes introduced in NDO 4\.2 for mso\_schema\_site\_anp\_epg\_domain
* Support for creation of schemas without templates with the mso\_schema module

<a id="cisco-nxos-1"></a>
#### cisco\.nxos

* nxos\_config \- Relax restrictions on I\(src\) parameter so it can be used more like I\(lines\)\. \([https\://github\.com/ansible\-collections/cisco\.nxos/issues/89](https\://github\.com/ansible\-collections/cisco\.nxos/issues/89)\)\.

<a id="community-aws"></a>
#### community\.aws

* aws\_ssm \- Updated the documentation to explicitly state that an S3 bucket is required\, the behavior of the files in that bucket\, and requirements around that\. \([https\://github\.com/ansible\-collections/community\.aws/issues/1775](https\://github\.com/ansible\-collections/community\.aws/issues/1775)\)\.
* cloudfront\_distribution \- added support for <code>cache\_policy\_id</code> and <code>origin\_request\_policy\_id</code> for behaviors \([https\://github\.com/ansible\-collections/community\.aws/pull/1589](https\://github\.com/ansible\-collections/community\.aws/pull/1589)\)
* glue\_job \- add support for 2 new instance types which are G\.4X and G\.8X \([https\://github\.com/ansible\-collections/community\.aws/pull/2048](https\://github\.com/ansible\-collections/community\.aws/pull/2048)\)\.
* mq\_broker \- add support to wait for broker state via <code>wait</code> and <code>wait\_timeout</code> parameter values \([https\://github\.com/ansible\-collections/community\.aws/pull/1879](https\://github\.com/ansible\-collections/community\.aws/pull/1879)\)\.
* msk\_cluster \- Support for additional <code>m5</code> and <code>m7g</code> types of MSK clusters \([https\://github\.com/ansible\-collections/community\.aws/pull/1947](https\://github\.com/ansible\-collections/community\.aws/pull/1947)\)\.

<a id="community-ciscosmb"></a>
#### community\.ciscosmb

* docs \- addeed info about SG\-250 support and testing

<a id="community-crypto"></a>
#### community\.crypto

* luks\_device \- add allow discards option \([https\://github\.com/ansible\-collections/community\.crypto/pull/693](https\://github\.com/ansible\-collections/community\.crypto/pull/693)\)\.
* x509\_crl \- the new option <code>serial\_numbers</code> allow to configure in which format serial numbers can be provided to <code>revoked\_certificates\[\]\.serial\_number</code>\. The default is as integers \(<code>serial\_numbers\=integer</code>\) for backwards compatibility\; setting <code>serial\_numbers\=hex\-octets</code> allows to specify colon\-separated hex octet strings like <code>00\:11\:22\:FF</code> \([https\://github\.com/ansible\-collections/community\.crypto/issues/687](https\://github\.com/ansible\-collections/community\.crypto/issues/687)\, [https\://github\.com/ansible\-collections/community\.crypto/pull/715](https\://github\.com/ansible\-collections/community\.crypto/pull/715)\)\.

<a id="community-digitalocean"></a>
#### community\.digitalocean

* digital\_ocean\_kubernetes \- add project\_name parameter \([https\://github\.com/ansible\-collections/community\.digitalocean/issues/264](https\://github\.com/ansible\-collections/community\.digitalocean/issues/264)\)\.
* fix sanity tests \([https\://github\.com/ansible\-collections/community\.digitalocean/issues/323](https\://github\.com/ansible\-collections/community\.digitalocean/issues/323)\)\.

<a id="community-dns"></a>
#### community\.dns

* hetzner\_dns\_records and hosttech\_dns\_records inventory plugins \- the <code>filters</code> option has been renamed to <code>simple\_filters</code>\. The old name still works until community\.hrobot 2\.0\.0\. Then it will change to allow more complex filtering with the <code>community\.library\_inventory\_filtering\_v1</code> collection\'s functionality \([https\://github\.com/ansible\-collections/community\.dns/pull/181](https\://github\.com/ansible\-collections/community\.dns/pull/181)\)\.
* nameserver\_info and nameserver\_record\_info \- add <code>server</code> parameter to specify custom DNS servers \([https\://github\.com/ansible\-collections/community\.dns/pull/168](https\://github\.com/ansible\-collections/community\.dns/pull/168)\, [https\://github\.com/ansible\-collections/community\.dns/pull/178](https\://github\.com/ansible\-collections/community\.dns/pull/178)\)\.
* wait\_for\_txt \- add <code>server</code> parameter to specify custom DNS servers \([https\://github\.com/ansible\-collections/community\.dns/pull/178](https\://github\.com/ansible\-collections/community\.dns/pull/178)\)\.

<a id="community-docker-1"></a>
#### community\.docker

* The <code>ca\_cert</code> option available to almost all modules and plugins has been renamed to <code>ca\_path</code>\. The name <code>ca\_path</code> is also used for similar options in ansible\-core and other collections\. The old name has been added as an alias and can still be used \([https\://github\.com/ansible\-collections/community\.docker/pull/744](https\://github\.com/ansible\-collections/community\.docker/pull/744)\)\.
* The <code>docker\_stack\*</code> modules now use the common CLI\-based module code added for the <code>docker\_image\_build</code> and <code>docker\_compose\_v2</code> modules\. This means that the modules now have various more configuration options with respect to talking to the Docker Daemon\, and now also are part of the <code>community\.docker\.docker</code> and <code>docker</code> module default groups \([https\://github\.com/ansible\-collections/community\.docker/pull/745](https\://github\.com/ansible\-collections/community\.docker/pull/745)\)\.
* docker\_compose\_v2 \- add <code>scale</code> option to allow to explicitly scale services \([https\://github\.com/ansible\-collections/community\.docker/pull/776](https\://github\.com/ansible\-collections/community\.docker/pull/776)\)\.
* docker\_compose\_v2 \- allow to wait until containers are running/health when running <code>docker compose up</code> with the new <code>wait</code> option \([https\://github\.com/ansible\-collections/community\.docker/issues/794](https\://github\.com/ansible\-collections/community\.docker/issues/794)\, [https\://github\.com/ansible\-collections/community\.docker/pull/796](https\://github\.com/ansible\-collections/community\.docker/pull/796)\)\.
* docker\_compose\_v2\, docker\_compose\_v2\_pull \- support <code>files</code> parameter to specify multiple Compose files \([https\://github\.com/ansible\-collections/community\.docker/issues/772](https\://github\.com/ansible\-collections/community\.docker/issues/772)\, [https\://github\.com/ansible\-collections/community\.docker/pull/775](https\://github\.com/ansible\-collections/community\.docker/pull/775)\)\.
* docker\_container \- add <code>networks\[\]\.mac\_address</code> option for Docker API 1\.44\+\. Note that Docker API 1\.44 no longer uses the global <code>mac\_address</code> option\, this new option is the only way to set the MAC address for a container \([https\://github\.com/ansible\-collections/community\.docker/pull/763](https\://github\.com/ansible\-collections/community\.docker/pull/763)\)\.
* docker\_container \- implement better <code>platform</code> string comparisons to improve idempotency \([https\://github\.com/ansible\-collections/community\.docker/issues/654](https\://github\.com/ansible\-collections/community\.docker/issues/654)\, [https\://github\.com/ansible\-collections/community\.docker/pull/705](https\://github\.com/ansible\-collections/community\.docker/pull/705)\)\.
* docker\_container \- internal refactorings which allow comparisons to use more information like details of the current image or the Docker host config \([https\://github\.com/ansible\-collections/community\.docker/pull/713](https\://github\.com/ansible\-collections/community\.docker/pull/713)\)\.
* docker\_container \- the <code>pull\_check\_mode\_behavior</code> option now allows to control the module\'s behavior in check mode when <code>pull\=always</code> \([https\://github\.com/ansible\-collections/community\.docker/issues/792](https\://github\.com/ansible\-collections/community\.docker/issues/792)\, [https\://github\.com/ansible\-collections/community\.docker/pull/797](https\://github\.com/ansible\-collections/community\.docker/pull/797)\)\.
* docker\_container \- the <code>pull</code> option now accepts the three values <code>never</code>\, <code>missing\_image</code> \(default\)\, and <code>never</code>\, next to the previously valid values <code>true</code> \(equivalent to <code>always</code>\) and <code>false</code> \(equivalent to <code>missing\_image</code>\)\. This allows the equivalent to <code>\-\-pull\=never</code> from the Docker command line \([https\://github\.com/ansible\-collections/community\.docker/issues/783](https\://github\.com/ansible\-collections/community\.docker/issues/783)\, [https\://github\.com/ansible\-collections/community\.docker/pull/797](https\://github\.com/ansible\-collections/community\.docker/pull/797)\)\.
* docker\_image \- allow to specify labels and <code>/dev/shm</code> size when building images \([https\://github\.com/ansible\-collections/community\.docker/issues/726](https\://github\.com/ansible\-collections/community\.docker/issues/726)\, [https\://github\.com/ansible\-collections/community\.docker/pull/727](https\://github\.com/ansible\-collections/community\.docker/pull/727)\)\.
* docker\_image \- allow to specify memory size and swap memory size in other units than bytes \([https\://github\.com/ansible\-collections/community\.docker/pull/727](https\://github\.com/ansible\-collections/community\.docker/pull/727)\)\.
* inventory plugins \- add <code>filter</code> option which allows to include and exclude hosts based on Jinja2 conditions \([https\://github\.com/ansible\-collections/community\.docker/pull/698](https\://github\.com/ansible\-collections/community\.docker/pull/698)\, [https\://github\.com/ansible\-collections/community\.docker/issues/610](https\://github\.com/ansible\-collections/community\.docker/issues/610)\)\.

<a id="community-general"></a>
#### community\.general

* bitwarden lookup plugin \- add <code>bw\_session</code> option\, to pass session key instead of reading from env \([https\://github\.com/ansible\-collections/community\.general/pull/7994](https\://github\.com/ansible\-collections/community\.general/pull/7994)\)\.
* bitwarden lookup plugin \- allows to fetch all records of a given collection ID\, by allowing to pass an empty value for <code>search\_value</code> when <code>collection\_id</code> is provided \([https\://github\.com/ansible\-collections/community\.general/pull/8013](https\://github\.com/ansible\-collections/community\.general/pull/8013)\)\.
* bitwarden lookup plugin \- when looking for items using an item ID\, the item is now accessed directly with <code>bw get item</code> instead of searching through all items\. This doubles the lookup speed \([https\://github\.com/ansible\-collections/community\.general/pull/7468](https\://github\.com/ansible\-collections/community\.general/pull/7468)\)\.
* consul\_auth\_method\, consul\_binding\_rule\, consul\_policy\, consul\_role\, consul\_session\, consul\_token \- added action group <code>community\.general\.consul</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7897](https\://github\.com/ansible\-collections/community\.general/pull/7897)\)\.
* consul\_policy \- added support for diff and check mode \([https\://github\.com/ansible\-collections/community\.general/pull/7878](https\://github\.com/ansible\-collections/community\.general/pull/7878)\)\.
* consul\_policy\, consul\_role\, consul\_session \- removed dependency on <code>requests</code> and factored out common parts \([https\://github\.com/ansible\-collections/community\.general/pull/7826](https\://github\.com/ansible\-collections/community\.general/pull/7826)\, [https\://github\.com/ansible\-collections/community\.general/pull/7878](https\://github\.com/ansible\-collections/community\.general/pull/7878)\)\.
* consul\_role \- <code>node\_identities</code> now expects a <code>node\_name</code> option to match the Consul API\, the old <code>name</code> is still supported as alias \([https\://github\.com/ansible\-collections/community\.general/pull/7878](https\://github\.com/ansible\-collections/community\.general/pull/7878)\)\.
* consul\_role \- <code>service\_identities</code> now expects a <code>service\_name</code> option to match the Consul API\, the old <code>name</code> is still supported as alias \([https\://github\.com/ansible\-collections/community\.general/pull/7878](https\://github\.com/ansible\-collections/community\.general/pull/7878)\)\.
* consul\_role \- added support for diff mode \([https\://github\.com/ansible\-collections/community\.general/pull/7878](https\://github\.com/ansible\-collections/community\.general/pull/7878)\)\.
* consul\_role \- added support for templated policies \([https\://github\.com/ansible\-collections/community\.general/pull/7878](https\://github\.com/ansible\-collections/community\.general/pull/7878)\)\.
* elastic callback plugin \- close elastic client to not leak resources \([https\://github\.com/ansible\-collections/community\.general/pull/7517](https\://github\.com/ansible\-collections/community\.general/pull/7517)\)\.
* git\_config \- allow multiple git configs for the same name with the new <code>add\_mode</code> option \([https\://github\.com/ansible\-collections/community\.general/pull/7260](https\://github\.com/ansible\-collections/community\.general/pull/7260)\)\.
* git\_config \- the <code>after</code> and <code>before</code> fields in the <code>diff</code> of the return value can be a list instead of a string in case more configs with the same key are affected \([https\://github\.com/ansible\-collections/community\.general/pull/7260](https\://github\.com/ansible\-collections/community\.general/pull/7260)\)\.
* git\_config \- when a value is unset\, all configs with the same key are unset \([https\://github\.com/ansible\-collections/community\.general/pull/7260](https\://github\.com/ansible\-collections/community\.general/pull/7260)\)\.
* gitlab modules \- add <code>ca\_path</code> option \([https\://github\.com/ansible\-collections/community\.general/pull/7472](https\://github\.com/ansible\-collections/community\.general/pull/7472)\)\.
* gitlab modules \- remove duplicate <code>gitlab</code> package check \([https\://github\.com/ansible\-collections/community\.general/pull/7486](https\://github\.com/ansible\-collections/community\.general/pull/7486)\)\.
* gitlab\_deploy\_key\, gitlab\_group\_members\, gitlab\_group\_variable\, gitlab\_hook\, gitlab\_instance\_variable\, gitlab\_project\_badge\, gitlab\_project\_variable\, gitlab\_user \- improve API pagination and compatibility with different versions of <code>python\-gitlab</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7790](https\://github\.com/ansible\-collections/community\.general/pull/7790)\)\.
* gitlab\_hook \- adds <code>releases\_events</code> parameter for supporting Releases events triggers on GitLab hooks \([https\://github\.com/ansible\-collections/community\.general/pull/7956](https\://github\.com/ansible\-collections/community\.general/pull/7956)\)\.
* gitlab\_runner \- add support for new runner creation workflow \([https\://github\.com/ansible\-collections/community\.general/pull/7199](https\://github\.com/ansible\-collections/community\.general/pull/7199)\)\.
* icinga2 inventory plugin \- add Jinja2 templating support to <code>url</code>\, <code>user</code>\, and <code>password</code> paramenters \([https\://github\.com/ansible\-collections/community\.general/issues/7074](https\://github\.com/ansible\-collections/community\.general/issues/7074)\, [https\://github\.com/ansible\-collections/community\.general/pull/7996](https\://github\.com/ansible\-collections/community\.general/pull/7996)\)\.
* icinga2 inventory plugin \- adds new parameter <code>group\_by\_hostgroups</code> in order to make grouping by Icinga2 hostgroups optional \([https\://github\.com/ansible\-collections/community\.general/pull/7998](https\://github\.com/ansible\-collections/community\.general/pull/7998)\)\.
* ini\_file \- support optional spaces between section names and their surrounding brackets \([https\://github\.com/ansible\-collections/community\.general/pull/8075](https\://github\.com/ansible\-collections/community\.general/pull/8075)\)\.
* ipa\_config \- adds <code>passkey</code> choice to <code>ipauserauthtype</code> parameter\'s choices \([https\://github\.com/ansible\-collections/community\.general/pull/7588](https\://github\.com/ansible\-collections/community\.general/pull/7588)\)\.
* ipa\_dnsrecord \- adds ability to manage NS record types \([https\://github\.com/ansible\-collections/community\.general/pull/7737](https\://github\.com/ansible\-collections/community\.general/pull/7737)\)\.
* ipa\_pwpolicy \- refactor module and exchange a sequence <code>if</code> statements with a <code>for</code> loop \([https\://github\.com/ansible\-collections/community\.general/pull/7723](https\://github\.com/ansible\-collections/community\.general/pull/7723)\)\.
* ipa\_pwpolicy \- update module to support <code>maxrepeat</code>\, <code>maxsequence</code>\, <code>dictcheck</code>\, <code>usercheck</code>\, <code>gracelimit</code> parameters in FreeIPA password policies \([https\://github\.com/ansible\-collections/community\.general/pull/7723](https\://github\.com/ansible\-collections/community\.general/pull/7723)\)\.
* ipa\_sudorule \- adds options to include denied commands or command groups \([https\://github\.com/ansible\-collections/community\.general/pull/7415](https\://github\.com/ansible\-collections/community\.general/pull/7415)\)\.
* ipa\_user \- adds <code>idp</code> and <code>passkey</code> choice to <code>ipauserauthtype</code> parameter\'s choices \([https\://github\.com/ansible\-collections/community\.general/pull/7589](https\://github\.com/ansible\-collections/community\.general/pull/7589)\)\.
* irc \- add <code>validate\_certs</code> option\, and rename <code>use\_ssl</code> to <code>use\_tls</code>\, while keeping <code>use\_ssl</code> as an alias\. The default value for <code>validate\_certs</code> is <code>false</code> for backwards compatibility\. We recommend to every user of this module to explicitly set <code>use\_tls\=true</code> and <em class="title-reference">validate\_certs\=true\`</em> whenever possible\, especially when communicating to IRC servers over the internet \([https\://github\.com/ansible\-collections/community\.general/pull/7550](https\://github\.com/ansible\-collections/community\.general/pull/7550)\)\.
* java\_cert \- enable <code>owner</code>\, <code>group</code>\, <code>mode</code>\, and other generic file arguments \([https\://github\.com/ansible\-collections/community\.general/pull/8116](https\://github\.com/ansible\-collections/community\.general/pull/8116)\)\.
* keycloak module utils \- expose error message from Keycloak server for HTTP errors in some specific situations \([https\://github\.com/ansible\-collections/community\.general/pull/7645](https\://github\.com/ansible\-collections/community\.general/pull/7645)\)\.
* keycloak\_realm\_key \- the <code>config\.algorithm</code> option now supports 8 additional key algorithms \([https\://github\.com/ansible\-collections/community\.general/pull/7698](https\://github\.com/ansible\-collections/community\.general/pull/7698)\)\.
* keycloak\_realm\_key \- the <code>config\.certificate</code> option value is no longer defined with <code>no\_log\=True</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7698](https\://github\.com/ansible\-collections/community\.general/pull/7698)\)\.
* keycloak\_realm\_key \- the <code>provider\_id</code> option now supports RSA encryption key usage \(value <code>rsa\-enc</code>\) \([https\://github\.com/ansible\-collections/community\.general/pull/7698](https\://github\.com/ansible\-collections/community\.general/pull/7698)\)\.
* keycloak\_user\_federation \- add option for <code>krbPrincipalAttribute</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7538](https\://github\.com/ansible\-collections/community\.general/pull/7538)\)\.
* keycloak\_user\_federation \- allow custom user storage providers to be set through <code>provider\_id</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7789](https\://github\.com/ansible\-collections/community\.general/pull/7789)\)\.
* ldap\_attrs \- module now supports diff mode\, showing which attributes are changed within an operation \([https\://github\.com/ansible\-collections/community\.general/pull/8073](https\://github\.com/ansible\-collections/community\.general/pull/8073)\)\.
* lvol \- change <code>pvs</code> argument type to list of strings \([https\://github\.com/ansible\-collections/community\.general/pull/7676](https\://github\.com/ansible\-collections/community\.general/pull/7676)\, [https\://github\.com/ansible\-collections/community\.general/issues/7504](https\://github\.com/ansible\-collections/community\.general/issues/7504)\)\.
* lxd connection plugin \- tighten the detection logic for lxd <code>Instance not found</code> errors\, to avoid false detection on unrelated errors such as <code>/usr/bin/python3\: not found</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7521](https\://github\.com/ansible\-collections/community\.general/pull/7521)\)\.
* lxd\_container \- uses <code>/1\.0/instances</code> API endpoint\, if available\. Falls back to <code>/1\.0/containers</code> or <code>/1\.0/virtual\-machines</code>\. Fixes issue when using Incus or LXD 5\.19 due to migrating to <code>/1\.0/instances</code> endpoint \([https\://github\.com/ansible\-collections/community\.general/pull/7980](https\://github\.com/ansible\-collections/community\.general/pull/7980)\)\.
* mail \- add <code>Message\-ID</code> header\; which is required by some mail servers \([https\://github\.com/ansible\-collections/community\.general/pull/7740](https\://github\.com/ansible\-collections/community\.general/pull/7740)\)\.
* mail module\, mail callback plugin \- allow to configure the domain name of the Message\-ID header with a new <code>message\_id\_domain</code> option \([https\://github\.com/ansible\-collections/community\.general/pull/7765](https\://github\.com/ansible\-collections/community\.general/pull/7765)\)\.
* mssql\_script \- adds transactional \(rollback/commit\) support via optional boolean param <code>transaction</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7976](https\://github\.com/ansible\-collections/community\.general/pull/7976)\)\.
* netcup\_dns \- adds support for record types <code>OPENPGPKEY</code>\, <code>SMIMEA</code>\, and <code>SSHFP</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7489](https\://github\.com/ansible\-collections/community\.general/pull/7489)\)\.
* nmcli \- add support for new connection type <code>loopback</code> \([https\://github\.com/ansible\-collections/community\.general/issues/6572](https\://github\.com/ansible\-collections/community\.general/issues/6572)\)\.
* nmcli \- allow for <code>infiniband</code> slaves of <code>bond</code> interface types \([https\://github\.com/ansible\-collections/community\.general/pull/7569](https\://github\.com/ansible\-collections/community\.general/pull/7569)\)\.
* nmcli \- allow for the setting of <code>MTU</code> for <code>infiniband</code> and <code>bond</code> interface types \([https\://github\.com/ansible\-collections/community\.general/pull/7499](https\://github\.com/ansible\-collections/community\.general/pull/7499)\)\.
* nmcli \- allow setting <code>MTU</code> for <code>bond\-slave</code> interface types \([https\://github\.com/ansible\-collections/community\.general/pull/8118](https\://github\.com/ansible\-collections/community\.general/pull/8118)\)\.
* onepassword lookup plugin \- support 1Password Connect with the opv2 client by setting the connect\_host and connect\_token parameters \([https\://github\.com/ansible\-collections/community\.general/pull/7116](https\://github\.com/ansible\-collections/community\.general/pull/7116)\)\.
* onepassword\_raw lookup plugin \- support 1Password Connect with the opv2 client by setting the connect\_host and connect\_token parameters \([https\://github\.com/ansible\-collections/community\.general/pull/7116](https\://github\.com/ansible\-collections/community\.general/pull/7116)\)
* passwordstore \- adds <code>timestamp</code> and <code>preserve</code> parameters to modify the stored password format \([https\://github\.com/ansible\-collections/community\.general/pull/7426](https\://github\.com/ansible\-collections/community\.general/pull/7426)\)\.
* proxmox \- adds <code>startup</code> parameters to configure startup order\, startup delay and shutdown delay \([https\://github\.com/ansible\-collections/community\.general/pull/8038](https\://github\.com/ansible\-collections/community\.general/pull/8038)\)\.
* proxmox \- adds <code>template</code> value to the <code>state</code> parameter\, allowing conversion of container to a template \([https\://github\.com/ansible\-collections/community\.general/pull/7143](https\://github\.com/ansible\-collections/community\.general/pull/7143)\)\.
* proxmox \- adds <code>update</code> parameter\, allowing update of an already existing containers configuration \([https\://github\.com/ansible\-collections/community\.general/pull/7540](https\://github\.com/ansible\-collections/community\.general/pull/7540)\)\.
* proxmox inventory plugin \- adds an option to exclude nodes from the dynamic inventory generation\. The new setting is optional\, not using this option will behave as usual \([https\://github\.com/ansible\-collections/community\.general/issues/6714](https\://github\.com/ansible\-collections/community\.general/issues/6714)\, [https\://github\.com/ansible\-collections/community\.general/pull/7461](https\://github\.com/ansible\-collections/community\.general/pull/7461)\)\.
* proxmox\_disk \- add ability to manipulate CD\-ROM drive \([https\://github\.com/ansible\-collections/community\.general/pull/7495](https\://github\.com/ansible\-collections/community\.general/pull/7495)\)\.
* proxmox\_kvm \- add parameter <code>update\_unsafe</code> to avoid limitations when updating dangerous values \([https\://github\.com/ansible\-collections/community\.general/pull/7843](https\://github\.com/ansible\-collections/community\.general/pull/7843)\)\.
* proxmox\_kvm \- adds <code>template</code> value to the <code>state</code> parameter\, allowing conversion of a VM to a template \([https\://github\.com/ansible\-collections/community\.general/pull/7143](https\://github\.com/ansible\-collections/community\.general/pull/7143)\)\.
* proxmox\_kvm \- support the <code>hookscript</code> parameter \([https\://github\.com/ansible\-collections/community\.general/issues/7600](https\://github\.com/ansible\-collections/community\.general/issues/7600)\)\.
* proxmox\_ostype \- it is now possible to specify the <code>ostype</code> when creating an LXC container \([https\://github\.com/ansible\-collections/community\.general/pull/7462](https\://github\.com/ansible\-collections/community\.general/pull/7462)\)\.
* proxmox\_vm\_info \- add ability to retrieve configuration info \([https\://github\.com/ansible\-collections/community\.general/pull/7485](https\://github\.com/ansible\-collections/community\.general/pull/7485)\)\.
* redfish\_config \- add command <code>SetServiceIdentification</code> to set service identification \([https\://github\.com/ansible\-collections/community\.general/issues/7916](https\://github\.com/ansible\-collections/community\.general/issues/7916)\)\.
* redfish\_info \- add command <code>GetServiceIdentification</code> to get service identification \([https\://github\.com/ansible\-collections/community\.general/issues/7882](https\://github\.com/ansible\-collections/community\.general/issues/7882)\)\.
* redfish\_info \- adding the <code>BootProgress</code> property when getting <code>Systems</code> info \([https\://github\.com/ansible\-collections/community\.general/pull/7626](https\://github\.com/ansible\-collections/community\.general/pull/7626)\)\.
* revbitspss lookup plugin \- removed a redundant unicode prefix\. The prefix was not necessary for Python 3 and has been cleaned up to streamline the code \([https\://github\.com/ansible\-collections/community\.general/pull/8087](https\://github\.com/ansible\-collections/community\.general/pull/8087)\)\.
* ssh\_config \- adds <code>controlmaster</code>\, <code>controlpath</code> and <code>controlpersist</code> parameters \([https\://github\.com/ansible\-collections/community\.general/pull/7456](https\://github\.com/ansible\-collections/community\.general/pull/7456)\)\.
* ssh\_config \- new feature to set <code>AddKeysToAgent</code> option to <code>yes</code> or <code>no</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7703](https\://github\.com/ansible\-collections/community\.general/pull/7703)\)\.
* ssh\_config \- new feature to set <code>IdentitiesOnly</code> option to <code>yes</code> or <code>no</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7704](https\://github\.com/ansible\-collections/community\.general/pull/7704)\)\.
* sudoers \- add support for the <code>NOEXEC</code> tag in sudoers rules \([https\://github\.com/ansible\-collections/community\.general/pull/7983](https\://github\.com/ansible\-collections/community\.general/pull/7983)\)\.
* terraform \- add support for <code>diff\_mode</code> for terraform resource\_changes \([https\://github\.com/ansible\-collections/community\.general/pull/7896](https\://github\.com/ansible\-collections/community\.general/pull/7896)\)\.
* terraform \- fix <code>diff\_mode</code> in state <code>absent</code> and when terraform <code>resource\_changes</code> does not exist \([https\://github\.com/ansible\-collections/community\.general/pull/7963](https\://github\.com/ansible\-collections/community\.general/pull/7963)\)\.
* xcc\_redfish\_command \- added support for raw POSTs \(<code>command\=PostResource</code> in <code>category\=Raw</code>\) without a specific action info \([https\://github\.com/ansible\-collections/community\.general/pull/7746](https\://github\.com/ansible\-collections/community\.general/pull/7746)\)\.

<a id="community-grafana"></a>
#### community\.grafana

* Add Quickwit search engine datasource \([https\://quickwit\.io](https\://quickwit\.io)\)\.
* Add parameter <em class="title-reference">org\_name</em> to <em class="title-reference">grafana\_dashboard</em>
* Add parameter <em class="title-reference">org\_name</em> to <em class="title-reference">grafana\_datasource</em>
* Add parameter <em class="title-reference">org\_name</em> to <em class="title-reference">grafana\_organization\_user</em>
* Add support for Grafana Tempo datasource type \([https\://grafana\.com/docs/grafana/latest/datasources/tempo/](https\://grafana\.com/docs/grafana/latest/datasources/tempo/)\)
* Manage <em class="title-reference">grafana\_folder</em> for organizations
* Merged ansible role telekom\-mms/ansible\-role\-grafana into ansible\-collections/community\.grafana
* added <em class="title-reference">community\.grafana\.notification\_channel</em> to role
* default to true/false in docs and code
* grafana\_dashboard \- add check\_mode support

<a id="community-hashi-vault-1"></a>
#### community\.hashi\_vault

* cert auth \- add option to set the <code>cert\_auth\_public\_key</code> and <code>cert\_auth\_private\_key</code> parameters using the variables <code>ansible\_hashi\_vault\_cert\_auth\_public\_key</code> and <code>ansible\_hashi\_vault\_cert\_auth\_private\_key</code> \([https\://github\.com/ansible\-collections/community\.hashi\_vault/issues/428](https\://github\.com/ansible\-collections/community\.hashi\_vault/issues/428)\)\.

<a id="community-hrobot"></a>
#### community\.hrobot

* robot inventory plugin \- the <code>filters</code> option has been renamed to <code>simple\_filters</code>\. The old name still works until community\.hrobot 2\.0\.0\. Then it will change to allow more complex filtering with the <code>community\.library\_inventory\_filtering\_v1</code> collection\'s functionality \([https\://github\.com/ansible\-collections/community\.hrobot/pull/94](https\://github\.com/ansible\-collections/community\.hrobot/pull/94)\)\.

<a id="community-mysql-1"></a>
#### community\.mysql

* mysql\_user \- add the <code>password\_expire</code> and <code>password\_expire\_interval</code> arguments to implement the password expiration management for mysql user \([https\://github\.com/ansible\-collections/community\.mysql/pull/598](https\://github\.com/ansible\-collections/community\.mysql/pull/598)\)\.
* mysql\_user \- add user attribute support via the <code>attributes</code> parameter and return value \([https\://github\.com/ansible\-collections/community\.mysql/pull/604](https\://github\.com/ansible\-collections/community\.mysql/pull/604)\)\.

<a id="community-postgresql"></a>
#### community\.postgresql

* postgresql\_db \- add the <code>comment</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/614](https\://github\.com/ansible\-collections/community\.postgresql/issues/614)\)\.
* postgresql\_db \- add the <code>icu\_locale</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/666](https\://github\.com/ansible\-collections/community\.postgresql/issues/666)\)\.
* postgresql\_db \- add the <code>locale\_provider</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/666](https\://github\.com/ansible\-collections/community\.postgresql/issues/666)\)\.
* postgresql\_ext \- add the <code>comment</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/354](https\://github\.com/ansible\-collections/community\.postgresql/issues/354)\)\.
* postgresql\_publication \- add the <code>comment</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/354](https\://github\.com/ansible\-collections/community\.postgresql/issues/354)\)\.
* postgresql\_schema \- add the <code>comment</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/354](https\://github\.com/ansible\-collections/community\.postgresql/issues/354)\)\.
* postgresql\_subscription \- add the <code>comment</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/354](https\://github\.com/ansible\-collections/community\.postgresql/issues/354)\)\.
* postgresql\_tablespace \- add the <code>comment</code> argument \([https\://github\.com/ansible\-collections/community\.postgresql/issues/354](https\://github\.com/ansible\-collections/community\.postgresql/issues/354)\)\.

<a id="community-rabbitmq"></a>
#### community\.rabbitmq

* rabbitmq\_user \- add support to user manipulation through RabbitMQ API \([https\://github\.com/ansible\-collections/community\.rabbitmq/issues/76](https\://github\.com/ansible\-collections/community\.rabbitmq/issues/76)\)

<a id="community-routeros"></a>
#### community\.routeros

* api\_info\, api\_modify \- add <code>interface ovpn\-client</code> path \([https\://github\.com/ansible\-collections/community\.routeros/issues/242](https\://github\.com/ansible\-collections/community\.routeros/issues/242)\, [https\://github\.com/ansible\-collections/community\.routeros/pull/244](https\://github\.com/ansible\-collections/community\.routeros/pull/244)\)\.
* api\_info\, api\_modify \- add <code>radius</code> path \([https\://github\.com/ansible\-collections/community\.routeros/issues/241](https\://github\.com/ansible\-collections/community\.routeros/issues/241)\, [https\://github\.com/ansible\-collections/community\.routeros/pull/245](https\://github\.com/ansible\-collections/community\.routeros/pull/245)\)\.
* api\_info\, api\_modify \- add <code>routing rule</code> path \([https\://github\.com/ansible\-collections/community\.routeros/issues/162](https\://github\.com/ansible\-collections/community\.routeros/issues/162)\, [https\://github\.com/ansible\-collections/community\.routeros/pull/246](https\://github\.com/ansible\-collections/community\.routeros/pull/246)\)\.
* api\_info\, api\_modify \- add missing DoH parameters <code>doh\-max\-concurrent\-queries</code>\, <code>doh\-max\-server\-connections</code>\, and <code>doh\-timeout</code> to the <code>ip dns</code> path \([https\://github\.com/ansible\-collections/community\.routeros/issues/230](https\://github\.com/ansible\-collections/community\.routeros/issues/230)\, [https\://github\.com/ansible\-collections/community\.routeros/pull/235](https\://github\.com/ansible\-collections/community\.routeros/pull/235)\)
* api\_info\, api\_modify \- add missing parameters <code>address\-list</code>\, <code>address\-list\-timeout</code>\, <code>randomise\-ports</code>\, and <code>realm</code> to subpaths of the <code>ip firewall</code> path \([https\://github\.com/ansible\-collections/community\.routeros/issues/236](https\://github\.com/ansible\-collections/community\.routeros/issues/236)\, [https\://github\.com/ansible\-collections/community\.routeros/pull/237](https\://github\.com/ansible\-collections/community\.routeros/pull/237)\)\.
* api\_info\, api\_modify \- add missing path <code>routing bgp template</code> \([https\://github\.com/ansible\-collections/community\.routeros/pull/243](https\://github\.com/ansible\-collections/community\.routeros/pull/243)\)\.
* api\_info\, api\_modify \- add read\-only fields <code>installed\-version</code>\, <code>latest\-version</code> and <code>status</code> in <code>system package update</code> \([https\://github\.com/ansible\-collections/community\.routeros/pull/263](https\://github\.com/ansible\-collections/community\.routeros/pull/263)\)\.
* api\_info\, api\_modify \- add support for the <code>tx\-power</code> attribute in <code>interface wireless</code> \([https\://github\.com/ansible\-collections/community\.routeros/pull/239](https\://github\.com/ansible\-collections/community\.routeros/pull/239)\)\.
* api\_info\, api\_modify \- added support for <code>interface wifi</code> and its sub\-paths \([https\://github\.com/ansible\-collections/community\.routeros/pull/266](https\://github\.com/ansible\-collections/community\.routeros/pull/266)\)\.
* api\_info\, api\_modify \- make path <code>user group</code> modifiable and add <code>comment</code> attribute \([https\://github\.com/ansible\-collections/community\.routeros/issues/256](https\://github\.com/ansible\-collections/community\.routeros/issues/256)\, [https\://github\.com/ansible\-collections/community\.routeros/pull/257](https\://github\.com/ansible\-collections/community\.routeros/pull/257)\)\.
* api\_info\, api\_modify \- mark the <code>interface wireless</code> parameter <code>running</code> as read\-only \([https\://github\.com/ansible\-collections/community\.routeros/pull/233](https\://github\.com/ansible\-collections/community\.routeros/pull/233)\)\.
* api\_info\, api\_modify \- remove default value for read\-only <code>running</code> field in <code>interface wireless</code> \([https\://github\.com/ansible\-collections/community\.routeros/pull/264](https\://github\.com/ansible\-collections/community\.routeros/pull/264)\)\.
* api\_info\, api\_modify \- removed <code>host</code> primary key in <code>tool netwatch</code> path \([https\://github\.com/ansible\-collections/community\.routeros/pull/248](https\://github\.com/ansible\-collections/community\.routeros/pull/248)\)\.
* api\_info\, api\_modify \- set the default value to <code>false</code> for the  <code>disabled</code> parameter in some more paths where it can be seen in the documentation \([https\://github\.com/ansible\-collections/community\.routeros/pull/237](https\://github\.com/ansible\-collections/community\.routeros/pull/237)\)\.
* api\_modify \- add missing <code>comment</code> attribute to <code>/routing id</code> \([https\://github\.com/ansible\-collections/community\.routeros/pull/234](https\://github\.com/ansible\-collections/community\.routeros/pull/234)\)\.
* api\_modify \- add missing attributes to the <code>routing bgp connection</code> path \([https\://github\.com/ansible\-collections/community\.routeros/pull/234](https\://github\.com/ansible\-collections/community\.routeros/pull/234)\)\.
* api\_modify \- add versioning to the <code>/tool e\-mail</code> path \(RouterOS 7\.12 release\) \([https\://github\.com/ansible\-collections/community\.routeros/pull/234](https\://github\.com/ansible\-collections/community\.routeros/pull/234)\)\.
* api\_modify \- make <code>/ip traffic\-flow target</code> a multiple value attribute \([https\://github\.com/ansible\-collections/community\.routeros/pull/234](https\://github\.com/ansible\-collections/community\.routeros/pull/234)\)\.
* api\_modify\, api\_info \- add support for the <code>ip vrf</code> path in RouterOS 7  \([https\://github\.com/ansible\-collections/community\.routeros/pull/259](https\://github\.com/ansible\-collections/community\.routeros/pull/259)\)
* api\_modify\, api\_info \- added support for <code>interface wifiwave2</code> \([https\://github\.com/ansible\-collections/community\.routeros/pull/226](https\://github\.com/ansible\-collections/community\.routeros/pull/226)\)\.

<a id="community-vmware"></a>
#### community\.vmware

* Add standard function vmware\_argument\_spec\(\) from module\_utils for using default env fallback function\. [https\://github\.com/ansible\-collections/community\.vmware/issues/1977](https\://github\.com/ansible\-collections/community\.vmware/issues/1977)
* vmware\_first\_class\_disk\_info \- Add a module to gather informations about first class disks\. \([https\://github\.com/ansible\-collections/community\.vmware/pull/1996](https\://github\.com/ansible\-collections/community\.vmware/pull/1996)\)\. \([https\://github\.com/ansible\-collections/community\.vmware/issues/1988](https\://github\.com/ansible\-collections/community\.vmware/issues/1988)\)\.
* vmware\_guest \- Add IPv6 support for VM network interfaces \([https\://github\.com/ansible\-collections/community\.vmware/pull/1937](https\://github\.com/ansible\-collections/community\.vmware/pull/1937)\)\.
* vmware\_guest\_sendkey \- Add Windows key \([https\://github\.com/ansible\-collections/community\.vmware/issues/1959](https\://github\.com/ansible\-collections/community\.vmware/issues/1959)\)\.
* vmware\_guest\_tools\_upgrade \- Add parameter <em class="title-reference">installer\_options</em> to pass command line options to the installer to modify the installation procedure for tools \([https\://github\.com/ansible\-collections/community\.vmware/pull/1059](https\://github\.com/ansible\-collections/community\.vmware/pull/1059)\)\.
* vmware\_host\_facts \- Add the possibility to get the related datacenter\. \([https\://github\.com/ansible\-collections/community\.vmware/pull/1994](https\://github\.com/ansible\-collections/community\.vmware/pull/1994)\)\.
* vmware\_vm\_inventory \- Add parameter <em class="title-reference">subproperties</em> \([https\://github\.com/ansible\-collections/community\.vmware/pull/1972](https\://github\.com/ansible\-collections/community\.vmware/pull/1972)\)\.
* vmware\_vmkernel \- Add the function to set the enable\_backup\_nfc setting \([https\://github\.com/ansible\-collections/community\.vmware/pull/1978](https\://github\.com/ansible\-collections/community\.vmware/pull/1978)\)
* vsphere\_copy \- Add parameter to tell vsphere\_copy which diskformat is being uploaded \([https\://github\.com/ansible\-collections/community\.vmware/pull/1995](https\://github\.com/ansible\-collections/community\.vmware/pull/1995)\)\.

<a id="community-windows"></a>
#### community\.windows

* Set minimum supported Ansible version to 2\.14 to align with the versions still supported by Ansible\.
* win\_regmerge \- Add content \'content\' parameter for specifying registry file contents directly

<a id="community-zabbix"></a>
#### community\.zabbix

* Added zabbix\_group\_events\_info module
* action module \- Added notify\_if\_canceled property
* agent and proxy roles \- Set default <em class="title-reference">zabbix\_api\_server\_port</em> to 80 or 443 based on <em class="title-reference">zabbix\_api\_use\_ssl</em>
* agent role \- Removed duplicative Windows agent task
* agent role \- Standardized default yum priority to 99
* all roles \- Re\-added ability to override Debian repo source
* all roles \- Updated Debian repository format to 822 standard
* api\_requests \- Handled error from depricated CertificateError class
* multiple roles \- Removed unneeded Apt Clean commands\.
* proxy role \- Updated MariaDB version for Centos 7 to 10\.11
* various \- updated testing modules
* various \- updated to fully qualified module names
* zabbix agent \- Added capability to add additional configuration includes
* zabbix web \- Allowed the independent configuration of php\-fpm without creating vhost\.
* zabbix\_api\_info module added
* zabbix\_host\_info \- added ability to get all the hosts configured in Zabbix
* zabbix\_proxy role \- Add variable zabbix\_proxy\_dbpassword\_hash\_method to control whether you want postgresql user password to be hashed with md5 or want to use db default\. When zabbix\_proxy\_dbpassword\_hash\_method is set to anything other than md5 then do not hash the password with md5 so you could use postgresql scram\-sha\-256 hashing method\.
* zabbix\_server role \- Add variable zabbix\_server\_dbpassword\_hash\_method to control whether you want postgresql user password to be hashed with md5 or want to use db default\. When zabbix\_server\_dbpassword\_hash\_method is set to anything other than md5 then do not hash the password with md5 so you could use postgresql scram\-sha\-256 hashing method\.
* zabbix\_templategroup module added
* zabbix\_user module \- add current\_passwd optional parameter to enable password updating of the currently logged in user \([https\://www\.zabbix\.com/documentation/6\.4/en/manual/api/reference/user/update](https\://www\.zabbix\.com/documentation/6\.4/en/manual/api/reference/user/update)\)

<a id="containers-podman"></a>
#### containers\.podman

* Add log\_opt and annotaion options to podman\_play module
* Add option to parse CreateCommand easily for diff calc
* Add support for setting underlying interface in podman\_network
* Alias generate systemd options stop\_timeout and time
* CI \- Fix rootfs test in CI
* CI \- add custom podman path to tasks
* CI \- add parametrized executables to tests
* Fix CI rootfs for podman\_container
* Fix broken conmon version in CI install
* Improve security\_opt comparison between existing container
* podman\_container \- Add new arguments to podman status commands
* podman\_container \- Add pasta as default network mode after v5
* podman\_container \- Update env\_file to accept a list of files instead of a single file
* podman\_container\_exec \- Return data for podman exec module
* podman\_generate\_systemd \- Fix broken example for podman\_generate\_systemd \(\#708\)
* podman\_login \- Update podman\_login\.py
* podman\_play \- Add support for kube yaml files with multi\-documents \(\#724\)
* podman\_play \- Update the logic for deleting pods/containers in podman\_play
* podman\_pod\_info \- handle return being list in Podman 5 \(\#713\)
* podman\_secret\_info \- Add secrets info module

<a id="dellemc-enterprise-sonic"></a>
#### dellemc\.enterprise\_sonic

* sonic\_aaa \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/304](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/304)\)\.
* sonic\_aaa \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_acl\_interfaces \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/306](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/306)\)\.
* sonic\_acl\_interfaces \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_bgp\_as\_paths \- Add support for replaced and overridden states \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/290](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/290)\)\.
* sonic\_bgp\_communities \- Add support for replaced and overridden states \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/251](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/251)\)\.
* sonic\_bgp\_ext\_communities \- Add support for replaced and overridden states \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/252](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/252)\)\.
* sonic\_interfaces \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/301](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/301)\)\.
* sonic\_interfaces \- Add support for replaced and overridden states \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314)\)\.
* sonic\_interfaces \- Change deleted design for interfaces module \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/310](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/310)\)\.
* sonic\_interfaces \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_ip\_neighbor \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/285](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/285)\)\.
* sonic\_ip\_neighbor \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_l2\_acls \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/306](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/306)\)\.
* sonic\_l2\_acls \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_l2\_interfaces \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/303](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/303)\)\.
* sonic\_l2\_interfaces \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_l3\_acls \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/306](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/306)\)\.
* sonic\_l3\_acls \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_l3\_interfaces \- Add support for replaced and overridden states \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/241](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/241)\)\.
* sonic\_lag\_interfaces \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/303](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/303)\)\.
* sonic\_lag\_interfaces \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_logging \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/285](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/285)\)\.
* sonic\_logging \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_mclag \- Add VLAN range support for \'unique\_ip\' and \'peer\_gateway\' options \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/288](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/288)\)\.
* sonic\_mclag \- Add support for replaced and overridden states \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/288](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/288)\)\.
* sonic\_ntp \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/281](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/281)\)\.
* sonic\_ntp \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_port\_breakout \- Add Ansible support for all port breakout modes now allowed in Enterprise SONiC \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/276](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/276)\)\.
* sonic\_port\_breakout \- Add support for replaced and overridden states \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/291](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/291)\)\.
* sonic\_port\_group \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/284](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/284)\)\.
* sonic\_port\_group \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_radius\_server \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/279](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/279)\)\.
* sonic\_radius\_server \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_static\_routes \- Add playbook check and diff modes support for static routes resource module \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/313](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/313)\)\.
* sonic\_static\_routes \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_system \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/284](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/284)\)\.
* sonic\_system \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_tacacs\_server \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/281](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/281)\)\.
* sonic\_tacacs\_server \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_users \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/304](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/304)\)\.
* sonic\_users \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_vlans \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/301](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/301)\)\.
* sonic\_vlans \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* sonic\_vrfs \- Add mgmt VRF replaced state handling to sonic\_vrfs module \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/298](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/298)\)\.
* sonic\_vrfs \- Add mgmt VRF support to sonic\_vrfs module \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/293](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/293)\)\.
* sonic\_vrfs \- Add support for playbook check and diff modes \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/285](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/285)\)\.
* sonic\_vrfs \- Enhance config diff generation function \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/318)\)\.
* tests \- Add UTs for BFD\, COPP\, and MAC modules \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/287](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/287)\)\.
* tests \- Enable contiguous execution of all regression integration tests on an S5296f \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/277](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/277)\)\.
* tests \- Fix the bgp CLI test base\_cfg\_path derivation of the bgp role\_path by avoiding relative pathing from the possibly external playbook\_dir \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/283](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/283)\)\.

<a id="dellemc-openmanage-1"></a>
#### dellemc\.openmanage

* Ansible lint issues are fixed for the collections\.
* For idrac\_certificate role\, added support for import operation of <em class="title-reference">HTTPS</em> certificate with the SSL key\.
* For idrac\_certificates module\, below enhancements are made\: Added support for import operation of <em class="title-reference">HTTPS</em> certificate with the SSL key\. The <em class="title-reference">email\_address</em> has been made as an optional parameter\.
* For idrac\_gather\_facts role\, added storage controller details in the role output\.
* Module <code>redfish\_storage\_volume</code> is enhanced to support reboot options and job tracking operation\.
* redfish\_storage\_volume \- This module is enhanced to support iDRAC8\.

<a id="dellemc-powerflex"></a>
#### dellemc\.powerflex

* Added support for PowerFlex Denver version\(4\.5\.x\) to TB and Config role\.
* Added support for PowerFlex ansible modules and roles on Azure\.
* Added support for resource group provisioning to validate\, deploy\, edit\, add nodes and delete a resource group\.
* The Info module is enhanced to list the firmware repositories\.
* The Info module is enhanced to retrieve lists related to fault sets\, service templates\, deployments\, and managed devices\.
* The SDS module has been enhanced to facilitate SDS creation within a fault set\.

<a id="f5networks-f5-modules"></a>
#### f5networks\.f5\_modules

* bigiq\_device\_discovery \- Changes in documentation related to Provider block

<a id="fortinet-fortimanager"></a>
#### fortinet\.fortimanager

* Added deprecated warning to invalid argument name\, please change the invalid argument name such as \"var\-name\"\, \"var name\" to \"var\_name\"\.
* Supported fortimanager 7\.4\.2\, 21 new modules\.

<a id="google-cloud"></a>
#### google\.cloud

* anisble\-test \- integration tests are now run against 2\.14\.0 and 2\.15\.0
* ansible \- 2\.14\.0 is now the minimum version supported
* ansible\-lint \- fixed over a thousand reported errors
* ansible\-lint \- upgraded to 6\.22
* ansible\-test \- add support for GCP application default credentials \([https\://github\.com/ansible\-collections/google\.cloud/issues/359](https\://github\.com/ansible\-collections/google\.cloud/issues/359)\)\.
* gcp\_serviceusage\_service \- added backoff when checking for operation completion\.
* gcp\_serviceusage\_service \- use alloyb API for the integration test as spanner conflicts with other tests
* gcp\_sql\_ssl\_cert \- made sha1\_fingerprint optional\, which enables resource creation
* gcp\_storage\_default\_object\_acl \- removed non\-existent fields\; the resource is not usable\.

<a id="grafana-grafana-1"></a>
#### grafana\.grafana

* Add \'run\_once\' to download\&unzip tasks by \@v\-zhuravlev in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/136](https\://github\.com/grafana/grafana\-ansible\-collection/pull/136)
* Adding <em class="title-reference">oauth\_allow\_insecure\_email\_lookup</em> to fix oauth user sync error by \@hypery2k in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/132](https\://github\.com/grafana/grafana\-ansible\-collection/pull/132)
* Bump ansible\-core from 2\.15\.4 to 2\.15\.8 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/137](https\://github\.com/grafana/grafana\-ansible\-collection/pull/137)
* Bump ansible\-lint from 6\.13\.1 to 6\.14\.3 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/139](https\://github\.com/grafana/grafana\-ansible\-collection/pull/139)
* Bump ansible\-lint from 6\.14\.3 to 6\.22\.2 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/142](https\://github\.com/grafana/grafana\-ansible\-collection/pull/142)
* Bump ansible\-lint from 6\.22\.2 to 24\.2\.0 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/150](https\://github\.com/grafana/grafana\-ansible\-collection/pull/150)
* Bump cryptography from 41\.0\.4 to 41\.0\.6 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/126](https\://github\.com/grafana/grafana\-ansible\-collection/pull/126)
* Bump jinja2 from 3\.1\.2 to 3\.1\.3 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/129](https\://github\.com/grafana/grafana\-ansible\-collection/pull/129)
* Bump pylint from 2\.16\.2 to 3\.0\.3 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/141](https\://github\.com/grafana/grafana\-ansible\-collection/pull/141)
* Bump pylint from 3\.0\.3 to 3\.1\.0 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/158](https\://github\.com/grafana/grafana\-ansible\-collection/pull/158)
* Bump pylint from 3\.0\.3 to 3\.1\.0 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/161](https\://github\.com/grafana/grafana\-ansible\-collection/pull/161)
* Bump the pip group across 1 directories with 1 update by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/156](https\://github\.com/grafana/grafana\-ansible\-collection/pull/156)
* Bump yamllint from 1\.29\.0 to 1\.33\.0 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/140](https\://github\.com/grafana/grafana\-ansible\-collection/pull/140)
* Bump yamllint from 1\.29\.0 to 1\.33\.0 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/143](https\://github\.com/grafana/grafana\-ansible\-collection/pull/143)
* Bump yamllint from 1\.33\.0 to 1\.34\.0 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/151](https\://github\.com/grafana/grafana\-ansible\-collection/pull/151)
* Bump yamllint from 1\.33\.0 to 1\.35\.1 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/155](https\://github\.com/grafana/grafana\-ansible\-collection/pull/155)
* Bump yamllint from 1\.33\.0 to 1\.35\.1 by \@dependabot in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/159](https\://github\.com/grafana/grafana\-ansible\-collection/pull/159)
* Change handler to systemd by \@v\-zhuravlev in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/135](https\://github\.com/grafana/grafana\-ansible\-collection/pull/135)
* Drop curl check by \@v\-zhuravlev in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/120](https\://github\.com/grafana/grafana\-ansible\-collection/pull/120)
* ExecStartPre and EnvironmentFile settings to system unit file by \@fabiiw05 in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/157](https\://github\.com/grafana/grafana\-ansible\-collection/pull/157)
* Fix check mode for grafana role by \@Boschung\-Mecatronic\-AG\-Infrastructure in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/125](https\://github\.com/grafana/grafana\-ansible\-collection/pull/125)
* Fix check mode in Grafana Agent by \@AmandaCameron in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/124](https\://github\.com/grafana/grafana\-ansible\-collection/pull/124)
* Fix links in grafana\_agent/defaults/main\.yaml by \@PabloCastellano in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/134](https\://github\.com/grafana/grafana\-ansible\-collection/pull/134)
* Topic/grafana agent idempotency by \@ohdearaugustin in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/147](https\://github\.com/grafana/grafana\-ansible\-collection/pull/147)
* Update tags in README by \@ishanjainn in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/121](https\://github\.com/grafana/grafana\-ansible\-collection/pull/121)
* datasources url parameter fix by \@dergudzon in [https\://github\.com/grafana/grafana\-ansible\-collection/pull/162](https\://github\.com/grafana/grafana\-ansible\-collection/pull/162)

<a id="hetzner-hcloud"></a>
#### hetzner\.hcloud

* Add the <em class="title-reference">hetzner\.hcloud\.all</em> group to configure all the modules using <em class="title-reference">module\_defaults</em>\.
* Allow to set the <em class="title-reference">api\_endpoint</em> module argument using the <em class="title-reference">HCLOUD\_ENDPOINT</em> environment variable\.
* Removed the <em class="title-reference">hcloud\_</em> prefix from all modules names\, e\.g\. <em class="title-reference">hetzner\.hcloud\.hcloud\_firewall</em> was renamed to <em class="title-reference">hetzner\.hcloud\.firewall</em>\. Old module names will continue working\.
* Renamed the <em class="title-reference">endpoint</em> module argument to <em class="title-reference">api\_endpoint</em>\, backward compatibility is maintained using an alias\.
* Replace deprecated <em class="title-reference">ansible\.netcommon</em> ip utils with python <em class="title-reference">ipaddress</em> module\. The <em class="title-reference">ansible\.netcommon</em> collection is no longer required by the collections\.
* firewall \- Allow forcing the deletion of firewalls that are still in use\.
* firewall \- Do not silence \'firewall still in use\' delete failures\.
* firewall \- Return resources the firewall is <em class="title-reference">applied\_to</em>\.
* firewall\_info \- Add new <em class="title-reference">firewall\_info</em> module to gather firewalls info\.
* firewall\_resource \- Add new <em class="title-reference">firewall\_resource</em> module to manage firewalls resources\.
* hcloud inventory \- Add the <em class="title-reference">api\_endpoint</em> option\.
* hcloud inventory \- Deprecate the <em class="title-reference">api\_token\_env</em> option\, suggest using a lookup plugin \(<em class="title-reference">\{\{ lookup\(\'ansible\.builtin\.env\'\, \'YOUR\_ENV\_VAR\'\) \}\}</em>\) or use the well\-known <em class="title-reference">HCLOUD\_TOKEN</em> environment variable name\.
* hcloud inventory \- Rename the <em class="title-reference">token\_env</em> option to <em class="title-reference">api\_token\_env</em>\, use aliases for backward compatibility\.
* hcloud inventory \- Rename the <em class="title-reference">token</em> option to <em class="title-reference">api\_token</em>\, use aliases for backward compatibility\.
* inventory \- Add <em class="title-reference">hostname</em> option used to template the hostname of the instances\.
* inventory \- Add <em class="title-reference">hostvars\_prefix</em> and hostvars\_suffix\` options to customize the inventory host variables keys\.
* network \- Allow renaming networks\.

<a id="ibm-storage-virtualize"></a>
#### ibm\.storage\_virtualize

* ibm\_sv\_manage\_replication\_policy \- Added support to configure a 2\-site\-ha policy\.
* ibm\_sv\_manage\_snapshot \- Added support to restore entire volumegroup from a snapshot of that volumegroup\.
* ibm\_sv\_manage\_snapshot \- Added support to restore subset of volumes of a volumegroup from a snapshot
* ibm\_svc\_host \- Added support to create nvmetcp host\.
* ibm\_svc\_info \- Added support to display information about partition\, quorum\, IO group\, VG replication and enclosure\, snmp server and ldap server
* ibm\_svc\_info \- Added support to display information about thinclone/clone volumes and volumegroups\.
* ibm\_svc\_manage\_volume \- Added support to create clone or thinclone from snapshot
* ibm\_svc\_manage\_volumgroup \- Added support to create clone or thinkclone volumegroup from snapshot from a subset of volumes
* ibm\_svc\_manage\_volumgroup \- Added support to delete volumegroups keeping volumes via \'evictvolumes\'\.

<a id="inspur-ispim"></a>
#### inspur\.ispim

* Modify edit\_smtp\_com and add description information\.

<a id="kubernetes-core"></a>
#### kubernetes\.core

* helm \- add <code>reuse\_values</code> and <code>reset\_values</code> support to helm module \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/394](https\://github\.com/ansible\-collections/kubernetes\.core/issues/394)\)\.
* k8s \- add new option <code>delete\_all</code> to support deletion of all resources when state is set to <code>absent</code>\. \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/504](https\://github\.com/ansible\-collections/kubernetes\.core/issues/504)\)
* k8s\, k8s\_info \- add a hidden\_fields option to allow fields to be hidden in the results of k8s and k8s\_info
* k8s\_drain \- add ability to filter the list of pods to be drained by a pod label selector \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/474](https\://github\.com/ansible\-collections/kubernetes\.core/issues/474)\)\.

<a id="lowlydba-sqlserver"></a>
#### lowlydba\.sqlserver

* Add ability to prevent changing login\'s password\, even if password supplied\.
* Add new input strings to be compatible with dbops v0\.9\.x \([https\://github\.com/lowlydba/lowlydba\.sqlserver/pull/231](https\://github\.com/lowlydba/lowlydba\.sqlserver/pull/231)\)

<a id="microsoft-ad"></a>
#### microsoft\.ad

* Added <code>group/microsoft\.ad\.domain</code> module defaults group for the <code>computer</code>\, <code>group</code>\, <code>object\_info</code>\, <code>object</code>\, <code>ou</code>\, and <code>user</code> module\. Users can use this defaults group to set common connection options for these modules such as the <code>domain\_server</code>\, <code>domain\_username</code>\, and <code>domain\_password</code> options\.
* Added support for Jinja2 templating in ldap inventory\.
* Make <code>name</code> an optional parameter for the AD modules\. Either <code>name</code> or <code>identity</code> needs to be set with their respective behaviours\. If creating a new AD user and only <code>identity</code> is set\, that will be the value used for the name of the object\.
* Set minimum supported Ansible version to 2\.14 to align with the versions still supported by Ansible\.
* object\_info \- Add ActiveDirectory module import

<a id="netapp-ontap"></a>
#### netapp\.ontap

* na\_ontap\_cifs\_server \- new option <em class="title-reference">is\_multichannel\_enabled</em> added in REST\, requires ONTAP 9\.10 or later\.
* na\_ontap\_cifs\_server \- new option <em class="title-reference">lm\_compatibility\_level</em> added in REST\, requires ONTAP 9\.8 or later\.
* na\_ontap\_cluster \- new option <em class="title-reference">certificate\.uuid</em> added in REST\, requires ONTAP 9\.10 or later\.
* na\_ontap\_cluster\_peer \- added REST only support for modifying remote intercluster addresses in cluster peer relation\.
* na\_ontap\_ems\_destination \- new options <em class="title-reference">syslog</em>\, <em class="title-reference">port</em>\, <em class="title-reference">transport</em>\, <em class="title-reference">message\_format</em>\, <em class="title-reference">timestamp\_format\_override</em> and <em class="title-reference">hostname\_format\_override</em> added in REST\, requires ONTAP 9\.12\.1 or later\.
* na\_ontap\_export\_policy\_rule \- added <em class="title-reference">actions</em> and <em class="title-reference">modify</em> in module output\.
* na\_ontap\_file\_security\_permissions\_acl \- added <em class="title-reference">actions</em> and <em class="title-reference">modify</em> in module output\.
* na\_ontap\_igroup\_initiator \- added <em class="title-reference">actions</em> in module output\.
* na\_ontap\_lun\_map \- added <em class="title-reference">actions</em> in module output\.
* na\_ontap\_lun\_map\_reporting\_nodes \- added <em class="title-reference">actions</em> in module output\.
* na\_ontap\_name\_mappings \- added <em class="title-reference">actions</em> and <em class="title-reference">modify</em> in module output\.
* na\_ontap\_node \- added <em class="title-reference">modify</em> in module output\.
* na\_ontap\_rest\_info \- added warning message if given subset doesn\'t support option <em class="title-reference">owning\_resource</em>\.
* na\_ontap\_s3\_services \- create\, modify S3 service returns <em class="title-reference">s3\_service\_info</em> in module output\.
* na\_ontap\_snapmirror \- updated resync and resume operation for synchronous snapmirror relationship in REST\.
* na\_ontap\_storage\_auto\_giveback \- added information on modified attributes in module output\.
* na\_ontap\_vscan\_scanner\_pool \- added REST support to Vscan Scanner Pools Configuration module\, requires ONTAP 9\.6 or later\.

<a id="netapp-storagegrid"></a>
#### netapp\.storagegrid

* na\_sg\_grid\_account \- New option <code>allow\_select\_object\_content</code> for enabling use of the S3 SelectObjectContent API\.
* na\_sg\_grid\_account \- New option <code>description</code> for setting additional identifying information for the tenant account\.

<a id="netbox-netbox"></a>
#### netbox\.netbox

* CI \- CI adjustments \[\#1154\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1154](https\://github\.com/netbox\-community/ansible\_modules/pull/1154)\) \[\#1155\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1155](https\://github\.com/netbox\-community/ansible\_modules/pull/1155)\) \[\#1157\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1157](https\://github\.com/netbox\-community/ansible\_modules/pull/1157)\)
* nb\_inventory \- Add facility group\_by option \[\#1059\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1059](https\://github\.com/netbox\-community/ansible\_modules/pull/1059)\)
* nb\_inventory \- Enable ansible\-vault strings in config\-context data \[\#1114\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1114](https\://github\.com/netbox\-community/ansible\_modules/pull/1114)\)
* nb\_lookup \- Add new VPN endpoints for NetBox 3\.7 support \[\#1162\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1162](https\://github\.com/netbox\-community/ansible\_modules/pull/1162)\)
* netbox\_platform \- Add config\_template option to netbox\_platform \[\#1119\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1119](https\://github\.com/netbox\-community/ansible\_modules/pull/1119)\)
* netbox\_power\_port\_template \- Add option module\_type to netbox\_power\_port\_template \[\#1105\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1105](https\://github\.com/netbox\-community/ansible\_modules/pull/1105)\)
* netbox\_rack\_role \- Add description option \[\#1143\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1143](https\://github\.com/netbox\-community/ansible\_modules/pull/1143)\)
* netbox\_virtual\_disk \- New module \[\#1153\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1153](https\://github\.com/netbox\-community/ansible\_modules/pull/1153)\)
* netbox\_virtual\_machine and netbox\_device \- Add option config\_template \[\#1171\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1171](https\://github\.com/netbox\-community/ansible\_modules/pull/1171)\)

<a id="purestorage-flasharray"></a>
#### purestorage\.flasharray

* all \- <code>distro</code> package added as a pre\-requisite
* multiple \- Remove packaging pre\-requisite\.
* multiple \- Where only REST 2\.x endpoints are used\, convert to REST 2\.x methodology\.
* purefa\_arrayname \- Convert to REST v2
* purefa\_dns \- Added facility to add a CA certifcate to management DNS and check peer\.
* purefa\_eula \- Only sign if not previously signed\. From REST 2\.30 name\, title and company are no longer required
* purefa\_info \- Add NSID value for NVMe namespace in <em class="title-reference">hosts</em> response
* purefa\_info \- Add support for controller uptime from Purity//FA 6\.6\.3
* purefa\_info \- Expose NFS security flavor for policies
* purefa\_info \- Expose cloud capacity details if array is a Cloud Block Store\.
* purefa\_info \- Subset <em class="title-reference">pgroups</em> now also provides a new dict called <em class="title-reference">deleted\_pgroups</em>
* purefa\_inventory \- Convert to REST v2
* purefa\_ntp \- Convert to REST v2
* purefa\_offload \- Convert to REST v2
* purefa\_offload \- Remove <em class="title-reference">nfs</em> as an option when Purity//FA 6\.6\.0 or higher is detected
* purefa\_pgsnap \- Module now requires minimum FlashArray Purity//FA 6\.1\.0
* purefa\_policy \- Add SMB user based enumeration parameter
* purefa\_policy \- Added NFS security flavors for accessing files in the mount point\.
* purefa\_policy \- Remove default setting for nfs\_version to allow for change of version at policy level
* purefa\_ra \- Add <code>present</code> and <code>absent</code> as valid <code>state</code> options
* purefa\_ra \- Add connecting as valid status of RA to perform operations on
* purefa\_ra \- Convert to REST v2
* purefa\_snap \- Add support for suffix on remote offload snapshots
* purefa\_syslog \- <code>name</code> becomes a required parameter as module converts to full REST 2 support
* purefa\_vnc \- Convert to REST v2

<a id="purestorage-flashblade"></a>
#### purestorage\.flashblade

* purefb\_bucket \- Add support for public buckets
* purefb\_bucket \- Add support for strict 17a\-4 WORM compliance\.
* purefb\_bucket \- From REST 2\.12 the <em class="title-reference">mode</em> parameter default changes to <em class="title-reference">multi\-site\-writable</em>\.
* purefb\_connect \- Increase Fan\-In and Fan\-Out maximums
* purefb\_ds \- Add <em class="title-reference">force\_bind\_password</em> parameter to allow module to be idempotent\.
* purefb\_fs \- Add <code>group\_ownership</code> parameter from Purity//FB 4\.4\.0\.
* purefb\_fs \- Added SMB Continuous Availability parameter\. Requires REST 2\.12 or higher\.
* purefb\_info \- Added enhanced information for buckets\, filesystems and snapshots\, based on new features in REST 2\.12
* purefb\_info \- Show array network access policy from Purity//FB 4\.4\.0
* purefb\_policy \- Add support for network access policies from Purity//FB 4\.4\.0
* purefb\_s3acc \- Add support for public buckets
* purefb\_s3acc \- Remove default requirements for <code>hard\_limit</code> and <code>default\_hard\_limit</code>

<a id="telekom-mms-icinga-director"></a>
#### telekom\_mms\.icinga\_director

* Extended docs and examples for multiple assign\_filter conditions \([https\://github\.com/telekom\-mms/ansible\-collection\-icinga\-director/pull/227](https\://github\.com/telekom\-mms/ansible\-collection\-icinga\-director/pull/227)\)
* Increase sleep to 5 seconds \([https\://github\.com/telekom\-mms/ansible\-collection\-icinga\-director/pull/245](https\://github\.com/telekom\-mms/ansible\-collection\-icinga\-director/pull/245)\)

<a id="theforeman-foreman"></a>
#### theforeman\.foreman

* content\_view\_publish role \- allow passing <code>async</code> and <code>poll</code> to the module \([https\://github\.com/theforeman/foreman\-ansible\-modules/pull/1676](https\://github\.com/theforeman/foreman\-ansible\-modules/pull/1676)\)
* convert2rhel role \- install <code>convert2rhel</code> from <code>cdn\-public\.redhat\.com</code>\, dropping the requirement of a custom CA cert

<a id="vmware-vmware-rest"></a>
#### vmware\.vmware\_rest

* Add requires\_ansible to manifest \([https\://github\.com/ansible\-community/ansible\.content\_builder/pull/76](https\://github\.com/ansible\-community/ansible\.content\_builder/pull/76)\)\.
* Generate action\_groups for the vmware\.vmware\_rest collection \([https\://github\.com/ansible\-community/ansible\.content\_builder/issues/75](https\://github\.com/ansible\-community/ansible\.content\_builder/issues/75)\)\.
* Use 7\.0 U3 API spec to build the modules \([https\://github\.com/ansible\-collections/vmware\.vmware\_rest/pull/449](https\://github\.com/ansible\-collections/vmware\.vmware\_rest/pull/449)\)\.
* Use folder attribute for host and dc module only \([https\://github\.com/ansible\-community/ansible\.content\_builder/pull/79](https\://github\.com/ansible\-community/ansible\.content\_builder/pull/79)\)\.

<a id="vultr-cloud"></a>
#### vultr\.cloud

* Added retry on HTTP 504 returned by the API \([https\://github\.com/vultr/ansible\-collection\-vultr/pull/104](https\://github\.com/vultr/ansible\-collection\-vultr/pull/104)\)\.
* Implemented a feature to distinguish resources by region if available\. This allows to have identical name per region e\.g\. a VPC named <code>default</code> in each region\. \([https\://github\.com/vultr/ansible\-collection\-vultr/pull/98](https\://github\.com/vultr/ansible\-collection\-vultr/pull/98)\)\.
* instance \- Added a new param <code>user\_scheme</code> to change user scheme to non\-root on Linux while creating the instance \([https\://github\.com/vultr/ansible\-collection\-vultr/issues/96](https\://github\.com/vultr/ansible\-collection\-vultr/issues/96)\)\.

<a id="breaking-changes--porting-guide"></a>
### Breaking Changes / Porting Guide

<a id="ansible-core-3"></a>
#### Ansible\-core

* assert \- Nested templating may result in an inability for the conditional to be evaluated\. See the porting guide for more information\.

<a id="cloud-common"></a>
#### cloud\.common

* Bump minimum Python supported version to 3\.9\.
* Remove support for ansible\-core \< 2\.14\.

<a id="community-ciscosmb-1"></a>
#### community\.ciscosmb

* in facts of interface \'bandwith\' changed to \'bandwidth\'

<a id="community-okd"></a>
#### community\.okd

* Bump minimum Python suupported version to 3\.9 \([https\://github\.com/openshift/community\.okd/pull/202](https\://github\.com/openshift/community\.okd/pull/202)\)\.
* Remove support for ansible\-core \< 2\.14 \([https\://github\.com/openshift/community\.okd/pull/202](https\://github\.com/openshift/community\.okd/pull/202)\)\.

<a id="hetzner-hcloud-1"></a>
#### hetzner\.hcloud

* Drop support for ansible\-core 2\.13\.
* certificate \- The <em class="title-reference">not\_valid\_before</em> and <em class="title-reference">not\_valid\_after</em> values are now returned as ISO\-8601 formatted strings\.
* certificate\_info \- The <em class="title-reference">not\_valid\_before</em> and <em class="title-reference">not\_valid\_after</em> values are now returned as ISO\-8601 formatted strings\.
* inventory \- Remove the deprecated <em class="title-reference">api\_token\_env</em> option\, you may use the <em class="title-reference">ansible\.builtin\.env</em> lookup as alternative\.
* iso\_info \- The <em class="title-reference">deprecated</em> value is now returned as ISO\-8601 formatted strings\.

<a id="kubernetes-core-1"></a>
#### kubernetes\.core

* Remove support for ansible\-core \< 2\.14
* Update python kubernetes library to 24\.2\.0\, helm/kind\-action to 1\.8\.0\, kubernetes \>\= 1\.24\.

<a id="theforeman-foreman-1"></a>
#### theforeman\.foreman

* content\_view\_filter \- stop managing rules from this module\, <code>content\_view\_filter\_rule</code> should be used for that
* inventory plugin \- do not default to <code>http\://localhost\:3000</code> as the Foreman URL\, providing a URL is now mandatory

<a id="vmware-vmware-rest-1"></a>
#### vmware\.vmware\_rest

* Remove support for ansible\-core \< 2\.14

<a id="deprecated-features"></a>
### Deprecated Features

* The <code>inspur\.sm</code> collection is considered unmaintained and will be removed from Ansible 11 if no one starts maintaining it again before Ansible 11\. See [the removal process for details on how this works](https\://github\.com/ansible\-collections/overview/blob/main/removal\_from\_ansible\.rst\#cancelling\-removal\-of\-an\-unmaintained\-collection) \([https\://forum\.ansible\.com/t/2854](https\://forum\.ansible\.com/t/2854)\)\.
* The <code>netapp\.storagegrid</code> collection is considered unmaintained and will be removed from Ansible 11 if no one starts maintaining it again before Ansible 11\. See [the removal process for details on how this works](https\://github\.com/ansible\-collections/overview/blob/main/removal\_from\_ansible\.rst\#cancelling\-removal\-of\-an\-unmaintained\-collection) \([https\://forum\.ansible\.com/t/2811](https\://forum\.ansible\.com/t/2811)\)\.

<a id="ansible-core-4"></a>
#### Ansible\-core

* Old style vars plugins which use the entrypoints <em class="title-reference">get\_host\_vars</em> or <em class="title-reference">get\_group\_vars</em> are deprecated\. The plugin should be updated to inherit from <em class="title-reference">BaseVarsPlugin</em> and define a <em class="title-reference">get\_vars</em> method as the entrypoint\.
* The \'required\' parameter in \'ansible\.module\_utils\.common\.process\.get\_bin\_path\' API is deprecated \([https\://github\.com/ansible/ansible/issues/82464](https\://github\.com/ansible/ansible/issues/82464)\)\.
* <code>module\_utils</code> \- importing the following convenience helpers from <code>ansible\.module\_utils\.basic</code> has been deprecated\: <code>get\_exception</code>\, <code>literal\_eval</code>\, <code>\_literal\_eval</code>\, <code>datetime</code>\, <code>signal</code>\, <code>types</code>\, <code>chain</code>\, <code>repeat</code>\, <code>PY2</code>\, <code>PY3</code>\, <code>b</code>\, <code>binary\_type</code>\, <code>integer\_types</code>\, <code>iteritems</code>\, <code>string\_types</code>\, <code>test\_type</code>\, <code>map</code> and <code>shlex\_quote</code>\.
* ansible\-doc \- role entrypoint attributes are deprecated and eventually will no longer be shown in ansible\-doc from ansible\-core 2\.20 on \([https\://github\.com/ansible/ansible/issues/82639](https\://github\.com/ansible/ansible/issues/82639)\, [https\://github\.com/ansible/ansible/pull/82678](https\://github\.com/ansible/ansible/pull/82678)\)\.
* paramiko connection plugin\, configuration items in the global scope are being deprecated and will be removed in favor or the existing same options in the plugin itself\. Users should not need to change anything \(how to configure them are the same\) but plugin authors using the global constants should move to using the plugin\'s get\_option\(\)\.

<a id="amazon-aws-1"></a>
#### amazon\.aws

* iam\_role\_info \- in a release after 2026\-05\-01 paths must begin and end with <code>/</code> \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1998](https\://github\.com/ansible\-collections/amazon\.aws/pull/1998)\)\.

<a id="community-crypto-1"></a>
#### community\.crypto

* openssl\_csr\_pipe\, openssl\_privatekey\_pipe\, x509\_certificate\_pipe \- the current behavior of check mode is deprecated and will change in community\.crypto 3\.0\.0\. The current behavior is similar to the modules without <code>\_pipe</code>\: if the object needs to be \(re\-\)generated\, only the <code>changed</code> status is set\, but the object is not updated\. From community\.crypto 3\.0\.0 on\, the modules will ignore check mode and always act as if check mode is not active\. This behavior can already achieved now by adding <code>check\_mode\: false</code> to the task\. If you think this breaks your use\-case of this module\, please [create an issue in the community\.crypto repository](https\://github\.com/ansible\-collections/community\.crypto/issues/new/choose) \([https\://github\.com/ansible\-collections/community\.crypto/issues/712](https\://github\.com/ansible\-collections/community\.crypto/issues/712)\, [https\://github\.com/ansible\-collections/community\.crypto/pull/714](https\://github\.com/ansible\-collections/community\.crypto/pull/714)\)\.

<a id="community-dns-1"></a>
#### community\.dns

* hetzner\_dns\_records and hosttech\_dns\_records inventory plugins \- the <code>filters</code> option has been renamed to <code>simple\_filters</code>\. The old name will stop working in community\.hrobot 2\.0\.0 \([https\://github\.com/ansible\-collections/community\.dns/pull/181](https\://github\.com/ansible\-collections/community\.dns/pull/181)\)\.

<a id="community-docker-2"></a>
#### community\.docker

* docker\_container \- the default <code>ignore</code> for the <code>image\_name\_mismatch</code> parameter has been deprecated and will switch to <code>recreate</code> in community\.docker 4\.0\.0\. A deprecation warning will be printed in situations where the default value is used and where a behavior would change once the default changes \([https\://github\.com/ansible\-collections/community\.docker/pull/703](https\://github\.com/ansible\-collections/community\.docker/pull/703)\)\.

<a id="community-general-1"></a>
#### community\.general

* consul\_acl \- the module has been deprecated and will be removed in community\.general 10\.0\.0\. <code>consul\_token</code> and <code>consul\_policy</code> can be used instead \([https\://github\.com/ansible\-collections/community\.general/pull/7901](https\://github\.com/ansible\-collections/community\.general/pull/7901)\)\.

<a id="community-hrobot-1"></a>
#### community\.hrobot

* robot inventory plugin \- the <code>filters</code> option has been renamed to <code>simple\_filters</code>\. The old name will stop working in community\.hrobot 2\.0\.0 \([https\://github\.com/ansible\-collections/community\.hrobot/pull/94](https\://github\.com/ansible\-collections/community\.hrobot/pull/94)\)\.

<a id="community-okd-1"></a>
#### community\.okd

* openshift \- the <code>openshift</code> inventory plugin has been deprecated and will be removed in release 4\.0\.0 \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/31](https\://github\.com/ansible\-collections/kubernetes\.core/issues/31)\)\.

<a id="dellemc-openmanage-2"></a>
#### dellemc\.openmanage

* The <code>dellemc\_idrac\_storage\_volume</code> module is deprecated and replaced with <code>idrac\_storage\_volume</code>\.

<a id="kubernetes-core-2"></a>
#### kubernetes\.core

* k8s \- the <code>k8s</code> inventory plugin has been deprecated and will be removed in release 4\.0\.0 \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/31](https\://github\.com/ansible\-collections/kubernetes\.core/issues/31)\)\.

<a id="removed-features-previously-deprecated"></a>
### Removed Features \(previously deprecated\)

* The <code>gluster\.gluster</code> collection was considered unmaintained and removed from Ansible 10 \([https\://github\.com/ansible\-community/community\-topics/issues/225](https\://github\.com/ansible\-community/community\-topics/issues/225)\)\. Users can still install this collection with <code>ansible\-galaxy collection install gluster\.gluster</code>\.
* The <code>hpe\.nimble</code> collection was considered unmaintained and removed from Ansible 10 \([https\://github\.com/ansible\-community/community\-topics/issues/254](https\://github\.com/ansible\-community/community\-topics/issues/254)\)\. Users can still install this collection with <code>ansible\-galaxy collection install hpe\.nimble</code>\.
* The <code>netapp\.aws</code> collection was considered unmaintained and removed from Ansible 10 \([https\://github\.com/ansible\-community/community\-topics/issues/223](https\://github\.com/ansible\-community/community\-topics/issues/223)\)\. Users can still install this collection with <code>ansible\-galaxy collection install netapp\.aws</code>\.
* The <code>netapp\.azure</code> collection was considered unmaintained and removed from Ansible 10 \([https\://github\.com/ansible\-community/community\-topics/issues/234](https\://github\.com/ansible\-community/community\-topics/issues/234)\)\. Users can still install this collection with <code>ansible\-galaxy collection install netapp\.azure</code>\.
* The <code>netapp\.elementsw</code> collection was considered unmaintained and removed from Ansible 10 \([https\://github\.com/ansible\-community/community\-topics/issues/235](https\://github\.com/ansible\-community/community\-topics/issues/235)\)\. Users can still install this collection with <code>ansible\-galaxy collection install netapp\.elementsw</code>\.
* The <code>netapp\.um\_info</code> collection was considered unmaintained and removed from Ansible 10 \([https\://github\.com/ansible\-community/community\-topics/issues/244](https\://github\.com/ansible\-community/community\-topics/issues/244)\)\. Users can still install this collection with <code>ansible\-galaxy collection install netapp\.um\_info</code>\.
* The deprecated <code>community\.azure</code> collection has been removed\. There is a successor collection <code>azure\.azcollection</code> in the community package which should cover the same functionality\.
* The deprecated <code>community\.sap</code> collection has been removed from Ansible 10 \([https\://github\.com/ansible\-community/community\-topics/issues/247](https\://github\.com/ansible\-community/community\-topics/issues/247)\)\. There is a successor collection <code>community\.sap\_libs</code> in the community package which should cover the same functionality\.
* The deprecated <code>purestorage\.fusion</code> collection has been removed \([https\://forum\.ansible\.com/t/3712](https\://forum\.ansible\.com/t/3712)\)\.

<a id="ansible-core-5"></a>
#### Ansible\-core

* Remove deprecated APIs from ansible\-docs \([https\://github\.com/ansible/ansible/issues/81716](https\://github\.com/ansible/ansible/issues/81716)\)\.
* Remove deprecated JINJA2\_NATIVE\_WARNING environment variable \([https\://github\.com/ansible/ansible/issues/81714](https\://github\.com/ansible/ansible/issues/81714)\)
* Remove deprecated <code>scp\_if\_ssh</code> from ssh connection plugin \([https\://github\.com/ansible/ansible/issues/81715](https\://github\.com/ansible/ansible/issues/81715)\)\.
* Remove deprecated crypt support from ansible\.utils\.encrypt \([https\://github\.com/ansible/ansible/issues/81717](https\://github\.com/ansible/ansible/issues/81717)\)
* With the removal of Python 2 support\, the yum module and yum action plugin are removed and redirected to <code>dnf</code>\.

<a id="arista-eos-1"></a>
#### arista\.eos

* Remove depreacted eos\_bgp module which is replaced with eos\_bgp\_global and eos\_bgp\_address\_family\.
* Remove deprecated eos\_logging module which is replaced with eos\_logging\_global resource module\.
* Remove deprecated timers\.throttle attribute\.

<a id="cisco-ios-2"></a>
#### cisco\.ios

* Deprecated ios\_ntp module in favor of ios\_ntp\_global\.
* Removed previously deprecated ios\_bgp module in favor of ios\_bgp\_global and ios\_bgp\_address\_family\.

<a id="cisco-iosxr-2"></a>
#### cisco\.iosxr

* Remove deprecated iosxr\_logging module which is replaced with iosxr\_logging\_global resource module\.

<a id="cisco-nxos-2"></a>
#### cisco\.nxos

* The nxos\_logging module has been removed with this release\.
* The nxos\_ntp module has been removed with this release\.
* The nxos\_ntp\_auth module has been removed with this release\.
* The nxos\_ntp\_options module has been removed with this release\.

<a id="junipernetworks-junos-1"></a>
#### junipernetworks\.junos

* Remove deprected junos\_logging module which is replaced by junos\_logging\_global resource module\.

<a id="security-fixes"></a>
### Security Fixes

<a id="ansible-core-6"></a>
#### Ansible\-core

* ANSIBLE\_NO\_LOG \- Address issue where ANSIBLE\_NO\_LOG was ignored \(CVE\-2024\-0690\)
* ansible\-galaxy \- Prevent roles from using symlinks to overwrite files outside of the installation directory \(CVE\-2023\-5115\)
* templating \- Address issues where internal templating can cause unsafe variables to lose their unsafe designation \(CVE\-2023\-5764\)

<a id="community-dns-2"></a>
#### community\.dns

* hosttech\_dns\_records and hetzner\_dns\_records inventory plugins \- make sure all data received from the remote servers is marked as unsafe\, so remote code execution by obtaining texts that can be evaluated as templates is not possible \([https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/](https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/)\, [https\://github\.com/ansible\-collections/community\.dns/pull/189](https\://github\.com/ansible\-collections/community\.dns/pull/189)\)\.

<a id="community-docker-3"></a>
#### community\.docker

* docker\_containers\, docker\_machine\, and docker\_swarm inventory plugins \- make sure all data received from the Docker daemon / Docker machine is marked as unsafe\, so remote code execution by obtaining texts that can be evaluated as templates is not possible \([https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/](https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/)\, [https\://github\.com/ansible\-collections/community\.docker/pull/815](https\://github\.com/ansible\-collections/community\.docker/pull/815)\)\.

<a id="community-general-2"></a>
#### community\.general

* cobbler\, gitlab\_runners\, icinga2\, linode\, lxd\, nmap\, online\, opennebula\, proxmox\, scaleway\, stackpath\_compute\, virtualbox\, and xen\_orchestra inventory plugin \- make sure all data received from the remote servers is marked as unsafe\, so remote code execution by obtaining texts that can be evaluated as templates is not possible \([https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/](https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/)\, [https\://github\.com/ansible\-collections/community\.general/pull/8098](https\://github\.com/ansible\-collections/community\.general/pull/8098)\)\.

<a id="community-hrobot-2"></a>
#### community\.hrobot

* robot inventory plugin \- make sure all data received from the Hetzner robot service server is marked as unsafe\, so remote code execution by obtaining texts that can be evaluated as templates is not possible \([https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/](https\://www\.die\-welt\.net/2024/03/remote\-code\-execution\-in\-ansible\-dynamic\-inventory\-plugins/)\, [https\://github\.com/ansible\-collections/community\.hrobot/pull/99](https\://github\.com/ansible\-collections/community\.hrobot/pull/99)\)\.

<a id="bugfixes"></a>
### Bugfixes

<a id="ansible-core-7"></a>
#### Ansible\-core

* All core lookups now use set\_option\(s\) even when doing their own custom parsing\. This ensures that the options are always the proper type\.
* Allow for searching handler subdir for included task via include\_role \([https\://github\.com/ansible/ansible/issues/81722](https\://github\.com/ansible/ansible/issues/81722)\)
* AnsibleModule\.atomic\_move \- fix preserving extended ACLs of the destination when it exists \([https\://github\.com/ansible/ansible/issues/72929](https\://github\.com/ansible/ansible/issues/72929)\)\.
* Cache host\_group\_vars after instantiating it once and limit the amount of repetitive work it needs to do every time it runs\.
* Call PluginLoader\.all\(\) once for vars plugins\, and load vars plugins that run automatically or are enabled specifically by name subsequently\.
* Consolidate systemd detection logic into one place \([https\://github\.com/ansible/ansible/issues/80975](https\://github\.com/ansible/ansible/issues/80975)\)\.
* Consolidated the list of internal static vars\, centralized them as constant and completed from some missing entries\.
* Do not print undefined error message twice \([https\://github\.com/ansible/ansible/issues/78703](https\://github\.com/ansible/ansible/issues/78703)\)\.
* Enable file cache for vaulted files during vars lookup to fix a strong performance penalty in huge and complex playbboks\.
* Fix NEVRA parsing of package names that include digit\(s\) in them \([https\://github\.com/ansible/ansible/issues/76463](https\://github\.com/ansible/ansible/issues/76463)\, [https\://github\.com/ansible/ansible/issues/81018](https\://github\.com/ansible/ansible/issues/81018)\)
* Fix <code>force\_handlers</code> not working with <code>any\_errors\_fatal</code> \([https\://github\.com/ansible/ansible/issues/36308](https\://github\.com/ansible/ansible/issues/36308)\)
* Fix <code>run\_once</code> being incorrectly interpreted on handlers \([https\://github\.com/ansible/ansible/issues/81666](https\://github\.com/ansible/ansible/issues/81666)\)
* Fix an issue when setting a plugin name from an unsafe source resulted in <code>ValueError\: unmarshallable object</code> \([https\://github\.com/ansible/ansible/issues/82708](https\://github\.com/ansible/ansible/issues/82708)\)
* Fix check for missing \_sub\_plugin attribute in older connection plugins \([https\://github\.com/ansible/ansible/pull/82954](https\://github\.com/ansible/ansible/pull/82954)\)
* Fix condition for unquoting configuration strings from ini files \([https\://github\.com/ansible/ansible/issues/82387](https\://github\.com/ansible/ansible/issues/82387)\)\.
* Fix for when <code>any\_errors\_fatal</code> was ignored if error occurred in a block with always \([https\://github\.com/ansible/ansible/issues/31543](https\://github\.com/ansible/ansible/issues/31543)\)
* Fix handling missing urls in ansible\.module\_utils\.urls\.fetch\_file for Python 3\.
* Fix issue where an <code>include\_tasks</code> handler in a role was not able to locate a file in <code>tasks/</code> when <code>tasks\_from</code> was used as a role entry point and <code>main\.yml</code> was not present \([https\://github\.com/ansible/ansible/issues/82241](https\://github\.com/ansible/ansible/issues/82241)\)
* Fix issues when tasks withing nested blocks wouldn\'t run when <code>force\_handlers</code> is set \([https\://github\.com/ansible/ansible/issues/81533](https\://github\.com/ansible/ansible/issues/81533)\)
* Fix loading vars\_plugins in roles \([https\://github\.com/ansible/ansible/issues/82239](https\://github\.com/ansible/ansible/issues/82239)\)\.
* Fix notifying role handlers by listen keyword topics with the \"role\_name \: \" prefix \([https\://github\.com/ansible/ansible/issues/82849](https\://github\.com/ansible/ansible/issues/82849)\)\.
* Fix setting proper locale for git executable when running on non english systems\, ensuring git output can always be parsed\.
* Fix tasks in always section not being executed for nested blocks with <code>any\_errors\_fatal</code> \([https\://github\.com/ansible/ansible/issues/73246](https\://github\.com/ansible/ansible/issues/73246)\)
* Fixes permission for cache json file from 600 to 644 \([https\://github\.com/ansible/ansible/issues/82683](https\://github\.com/ansible/ansible/issues/82683)\)\.
* Give the tombstone error for <code>include</code> pre\-fork like other tombstoned action/module plugins\.
* Harden python templates for respawn and ansiballz around str literal quoting
* Include the task location when a module or action plugin is deprecated \([https\://github\.com/ansible/ansible/issues/82450](https\://github\.com/ansible/ansible/issues/82450)\)\.
* Interpreter discovery \- Add <code>Amzn</code> to <code>OS\_FAMILY\_MAP</code> for correct family fallback for interpreter discovery \([https\://github\.com/ansible/ansible/issues/80882](https\://github\.com/ansible/ansible/issues/80882)\)\.
* Mirror the behavior of dnf on the command line when handling NEVRAs with omitted epoch \([https\://github\.com/ansible/ansible/issues/71808](https\://github\.com/ansible/ansible/issues/71808)\)
* Plugin loader does not dedupe nor cache filter/test plugins by file basename\, but full path name\.
* Properly template tags in parent blocks \([https\://github\.com/ansible/ansible/issues/81053](https\://github\.com/ansible/ansible/issues/81053)\)
* Provide additional information about the alternative plugin in the deprecation message \([https\://github\.com/ansible/ansible/issues/80561](https\://github\.com/ansible/ansible/issues/80561)\)\.
* Remove the galaxy\_info field <code>platforms</code> from the role templates \([https\://github\.com/ansible/ansible/issues/82453](https\://github\.com/ansible/ansible/issues/82453)\)\.
* Restoring the ability of filters/tests can have same file base name but different tests/filters defined inside\.
* Reword the error message when the module fails to parse parameters in JSON format \([https\://github\.com/ansible/ansible/issues/81188](https\://github\.com/ansible/ansible/issues/81188)\)\.
* Reword warning if the reserved keyword \_ansible\_ used as a module parameter \([https\://github\.com/ansible/ansible/issues/82514](https\://github\.com/ansible/ansible/issues/82514)\)\.
* Run all handlers with the same <code>listen</code> topic\, even when notified from another handler \([https\://github\.com/ansible/ansible/issues/82363](https\://github\.com/ansible/ansible/issues/82363)\)\.
* Slight optimization to hostvars \(instantiate template only once per host\, vs per call to var\)\.
* Stopped misleadingly advertising <code>async</code> mode support in the <code>reboot</code> module \([https\://github\.com/ansible/ansible/issues/71517](https\://github\.com/ansible/ansible/issues/71517)\)\.
* <code>ansible\-galaxy role import</code> \- fix using the <code>role\_name</code> in a standalone role\'s <code>galaxy\_info</code> metadata by disabling automatic removal of the <code>ansible\-role\-</code> prefix\. This matches the behavior of the Galaxy UI which also no longer implicitly removes the <code>ansible\-role\-</code> prefix\. Use the <code>\-\-role\-name</code> option or add a <code>role\_name</code> to the <code>galaxy\_info</code> dictionary in the role\'s <code>meta/main\.yml</code> to use an alternate role name\.
* <code>ansible\-test sanity \-\-test runtime\-metadata</code> \- add <code>action\_plugin</code> as a valid field for modules in the schema \([https\://github\.com/ansible/ansible/pull/82562](https\://github\.com/ansible/ansible/pull/82562)\)\.
* <code>ansible\.module\_utils\.service</code> \- ensure binary data transmission in <code>daemonize\(\)</code>
* <code>any\_errors\_fatal</code> should fail all hosts and rescue all of them when a <code>rescue</code> section is specified \([https\://github\.com/ansible/ansible/issues/80981](https\://github\.com/ansible/ansible/issues/80981)\)
* <code>include\_role</code> \- properly execute <code>v2\_playbook\_on\_include</code> and <code>v2\_runner\_on\_failed</code> callbacks as well as increase <code>ok</code> and <code>failed</code> stats in the play recap\, when appropriate \([https\://github\.com/ansible/ansible/issues/77336](https\://github\.com/ansible/ansible/issues/77336)\)
* allow\_duplicates \- fix evaluating if the current role allows duplicates instead of using the initial value from the duplicate\'s cached role\.
* ansible\-config init will now dedupe ini entries from plugins\.
* ansible\-galaxy \- Deprecate use of the Galaxy v2 API \([https\://github\.com/ansible/ansible/issues/81781](https\://github\.com/ansible/ansible/issues/81781)\)
* ansible\-galaxy \- Provide a better error message when using a requirements file with an invalid format \- [https\://github\.com/ansible/ansible/issues/81901](https\://github\.com/ansible/ansible/issues/81901)
* ansible\-galaxy \- Resolve issue with the dataclass used for galaxy\.yml manifest caused by using future annotations
* ansible\-galaxy \- ensure path to ansible collection when installing or downloading doesn\'t have a backslash \([https\://github\.com/ansible/ansible/pull/79705](https\://github\.com/ansible/ansible/pull/79705)\)\.
* ansible\-galaxy \- started allowing the use of pre\-releases for collections that do not have any stable versions published\. \([https\://github\.com/ansible/ansible/pull/81606](https\://github\.com/ansible/ansible/pull/81606)\)
* ansible\-galaxy \- started allowing the use of pre\-releases for dependencies on any level of the dependency tree that specifically demand exact pre\-release versions of collections and not version ranges\. \([https\://github\.com/ansible/ansible/pull/81606](https\://github\.com/ansible/ansible/pull/81606)\)
* ansible\-galaxy error on dependency resolution will not error itself due to \'virtual\' collections not having a name/namespace\.
* ansible\-galaxy info \- fix reporting no role found when lookup\_role\_by\_name returns None\.
* ansible\-galaxy role import \- exit with 1 when the import fails \([https\://github\.com/ansible/ansible/issues/82175](https\://github\.com/ansible/ansible/issues/82175)\)\.
* ansible\-galaxy role install \- fix installing roles from Galaxy that have version <code>None</code> \([https\://github\.com/ansible/ansible/issues/81832](https\://github\.com/ansible/ansible/issues/81832)\)\.
* ansible\-galaxy role install \- normalize tarfile paths and symlinks using <code>ansible\.utils\.path\.unfrackpath</code> and consider them valid as long as the realpath is in the tarfile\'s role directory \([https\://github\.com/ansible/ansible/issues/81965](https\://github\.com/ansible/ansible/issues/81965)\)\.
* ansible\-inventory \- index available\_hosts for major performance boost when dumping large inventories
* ansible\-pull now will expand relative paths for the <code>\-d\|\-\-directory</code> option is now expanded before use\.
* ansible\-pull will now correctly handle become and connection password file options for ansible\-playbook\.
* ansible\-test \- Add a <code>pylint</code> plugin to work around a known issue on Python 3\.12\.
* ansible\-test \- Explicitly supply <code>ControlPath\=none</code> when setting up port forwarding over SSH to address the scenario where the local ssh configuration uses <code>ControlPath</code> for all hosts\, and would prevent ports to be forwarded after the initial connection to the host\.
* ansible\-test \- Fix parsing of cgroup entries which contain a <code>\:</code> in the path \([https\://github\.com/ansible/ansible/issues/81977](https\://github\.com/ansible/ansible/issues/81977)\)\.
* ansible\-test \- Include missing <code>pylint</code> requirements for Python 3\.10\.
* ansible\-test \- Properly detect docker host when using <code>ssh\://</code> protocol for connecting to the docker daemon\.
* ansible\-test \- The <code>libexpat</code> package is automatically upgraded during remote bootstrapping to maintain compatibility with newer Python packages\.
* ansible\-test \- The <code>validate\-modules</code> sanity test no longer attempts to process files with unrecognized extensions as Python \(resolves [https\://github\.com/ansible/ansible/issues/82604](https\://github\.com/ansible/ansible/issues/82604)\)\.
* ansible\-test \- Update <code>pylint</code> to version 3\.0\.1\.
* ansible\-test ansible\-doc sanity test \- do not remove underscores from plugin names in collections before calling <code>ansible\-doc</code> \([https\://github\.com/ansible/ansible/pull/82574](https\://github\.com/ansible/ansible/pull/82574)\)\.
* ansible\-test validate\-modules sanity test \- do not treat leading underscores for plugin names in collections as an attempted deprecation \([https\://github\.com/ansible/ansible/pull/82575](https\://github\.com/ansible/ansible/pull/82575)\)\.
* ansible\-test — Python 3\.8–3\.12 will use <code>coverage</code> v7\.3\.2\.
* ansible\.builtin\.apt \- calling clean \= true does not properly clean certain cache files such as /var/cache/apt/pkgcache\.bin and /var/cache/apt/pkgcache\.bin \([https\://github\.com/ansible/ansible/issues/82611](https\://github\.com/ansible/ansible/issues/82611)\)
* ansible\.builtin\.uri \- the module was ignoring the <code>force</code> parameter and always requesting a cached copy \(via the <code>If\-Modified\-Since</code> header\) when downloading to an existing local file\. Disable caching when <code>force</code> is <code>true</code>\, as documented \([https\://github\.com/ansible/ansible/issues/82166](https\://github\.com/ansible/ansible/issues/82166)\)\.
* apt \- honor install\_recommends and dpkg\_options while installing python3\-apt library \([https\://github\.com/ansible/ansible/issues/40608](https\://github\.com/ansible/ansible/issues/40608)\)\.
* apt \- install recommended packages when installing package via deb file \([https\://github\.com/ansible/ansible/issues/29726](https\://github\.com/ansible/ansible/issues/29726)\)\.
* apt\_repository \- do not modify repo files if the file is a symlink \([https\://github\.com/ansible/ansible/issues/49809](https\://github\.com/ansible/ansible/issues/49809)\)\.
* apt\_repository \- update PPA URL to point to https URL \([https\://github\.com/ansible/ansible/issues/82463](https\://github\.com/ansible/ansible/issues/82463)\)\.
* assemble \- fixed missing parameter \'content\' in \_get\_diff\_data API \([https\://github\.com/ansible/ansible/issues/82359](https\://github\.com/ansible/ansible/issues/82359)\)\.
* async \- Fix bug that stopped running async task in <code>\-\-check</code> when <code>check\_mode\: False</code> was set as a task attribute \- [https\://github\.com/ansible/ansible/issues/82811](https\://github\.com/ansible/ansible/issues/82811)
* blockinfile \- when <code>create\=true</code> is used with a filename without path\, the module crashed \([https\://github\.com/ansible/ansible/pull/81638](https\://github\.com/ansible/ansible/pull/81638)\)\.
* check if there are attributes to set before attempting to set them \([https\://github\.com/ansible/ansible/issues/76727](https\://github\.com/ansible/ansible/issues/76727)\)
* copy action now also generates temprary files as hidden \(\'\.\' prefixed\) to avoid accidental pickup by running services that glob by extension\.
* copy action now ensures that tempfiles use the same suffix as destination\, to allow for <code>validate</code> to work with utilities that check extensions\.
* deb822\_repository \- handle idempotency if the order of parameters is changed \([https\://github\.com/ansible/ansible/issues/82454](https\://github\.com/ansible/ansible/issues/82454)\)\.
* debconf \- allow user to specify a list for value when vtype is multiselect \([https\://github\.com/ansible/ansible/issues/81345](https\://github\.com/ansible/ansible/issues/81345)\)\.
* delegate\_to when set to an empty or undefined variable will now give a proper error\.
* distribution\.py \- Recognize ALP\-Dolomite as part of the SUSE OS family in Ansible\, fixing its previous misidentification \([https\://github\.com/ansible/ansible/pull/82496](https\://github\.com/ansible/ansible/pull/82496)\)\.
* distro \- bump bundled distro version from 1\.6\.0 to 1\.8\.0 \([https\://github\.com/ansible/ansible/issues/81713](https\://github\.com/ansible/ansible/issues/81713)\)\.
* dnf \- fix an issue when cached RPMs were left in the cache directory even when the keepcache setting was unset \([https\://github\.com/ansible/ansible/issues/81954](https\://github\.com/ansible/ansible/issues/81954)\)
* dnf \- fix an issue when installing a package by specifying a file it provides could result in installing a different package providing the same file than the package already installed resulting in resolution failure \([https\://github\.com/ansible/ansible/issues/82461](https\://github\.com/ansible/ansible/issues/82461)\)
* dnf \- properly set gpg check options on enabled repositories according to the <code>disable\_gpg\_check</code> option \([https\://github\.com/ansible/ansible/issues/80110](https\://github\.com/ansible/ansible/issues/80110)\)
* dnf \- properly skip unavailable packages when <code>skip\_broken</code> is enabled \([https\://github\.com/ansible/ansible/issues/80590](https\://github\.com/ansible/ansible/issues/80590)\)
* dnf \- the <code>nobest</code> option only overrides the distribution default when explicitly used\, and is used for all supported operations \([https\://github\.com/ansible/ansible/issues/82616](https\://github\.com/ansible/ansible/issues/82616)\)
* dnf5 \- respect <code>allow\_downgrade</code> when installing packages directly from rpm files
* dnf5 \- the <code>nobest</code> option only overrides the distribution default when used
* dwim functions for lookups should be better at detectging role context even in abscense of tasks/main\.
* expect \- fix argument spec error using timeout\=null \([https\://github\.com/ansible/ansible/issues/80982](https\://github\.com/ansible/ansible/issues/80982)\)\.
* fact gathering on linux now handles thread count by using rounding vs dropping decimals\, it should give slightly more accurate numbers\.
* facts \- detect VMware ESXi 8\.0 virtualization by product name VMware20\,1
* fetch \- Do not calculate the file size for Windows fetch targets to improve performance\.
* fetch \- add error message when using <code>dest</code> with a trailing slash that becomes a local directory \- [https\://github\.com/ansible/ansible/issues/82878](https\://github\.com/ansible/ansible/issues/82878)
* find \- do not fail on Permission errors \([https\://github\.com/ansible/ansible/issues/82027](https\://github\.com/ansible/ansible/issues/82027)\)\.
* first\_found lookup now always returns a full \(absolute\) and normalized path
* first\_found lookup now always takes into account k\=v options
* flush\_handlers \- properly handle a handler failure in a nested block when <code>force\_handlers</code> is set \([http\://github\.com/ansible/ansible/issues/81532](http\://github\.com/ansible/ansible/issues/81532)\)
* galaxy \- skip verification for unwanted Python compiled bytecode files \([https\://github\.com/ansible/ansible/issues/81628](https\://github\.com/ansible/ansible/issues/81628)\)\.
* handle exception raised while validating with elements\=\'int\' and value is not within choices \([https\://github\.com/ansible/ansible/issues/82776](https\://github\.com/ansible/ansible/issues/82776)\)\.
* include\_tasks \- include <em class="title-reference">ansible\_loop\_var</em> and <em class="title-reference">ansible\_index\_var</em> in a loop \([https\://github\.com/ansible/ansible/issues/82655](https\://github\.com/ansible/ansible/issues/82655)\)\.
* include\_vars \- fix calculating <code>depth</code> relative to the root and ensure all files are included \([https\://github\.com/ansible/ansible/issues/80987](https\://github\.com/ansible/ansible/issues/80987)\)\.
* interpreter\_discovery \- handle AnsibleError exception raised while interpreter discovery \([https\://github\.com/ansible/ansible/issues/78264](https\://github\.com/ansible/ansible/issues/78264)\)\.
* iptables \- add option choices \'src\,src\' and \'dst\,dst\' in match\_set\_flags \([https\://github\.com/ansible/ansible/issues/81281](https\://github\.com/ansible/ansible/issues/81281)\)\.
* iptables \- set jump to DSCP when set\_dscp\_mark or set\_dscp\_mark\_class is set \([https\://github\.com/ansible/ansible/issues/77077](https\://github\.com/ansible/ansible/issues/77077)\)\.
* known\_hosts \- Fix issue with <em class="title-reference">\@cert\-authority</em> entries in known\_hosts incorrectly being removed\.
* module no\_log will no longer affect top level booleans\, for example <code>no\_log\_module\_parameter\=\'a\'</code> will no longer hide <code>changed\=False</code> as a \'no log value\' \(matches \'a\'\)\.
* moved assemble\, raw\, copy\, fetch\, reboot\, script and wait\_for\_connection to query task instead of play\_context ensuring they get the lastest and most correct data\.
* reboot action now handles connections with \'timeout\' vs only \'connection\_timeout\' settings\.
* role params now have higher precedence than host facts again\, matching documentation\, this had unintentionally changed in 2\.15\.
* roles\, code cleanup and performance optimization of dependencies\, now cached\,  and <code>public</code> setting is now determined once\, at role instantiation\.
* roles\, the <code>static</code> property is now correctly set\, this will fix issues with <code>public</code> and <code>DEFAULT\_PRIVATE\_ROLE\_VARS</code> controls on exporting vars\.
* set\_option method for plugins to update config now properly passes through type casting and validation\.
* ssh \- add tests for the SSH connection plugin\.
* support url\-encoded credentials in URLs like [http\://x\%40\:\%40\@example\.com](http\://x\%40\:\%40\@example\.com) \([https\://github\.com/ansible/ansible/pull/82552](https\://github\.com/ansible/ansible/pull/82552)\)
* syslog \- Handle ValueError exception raised when sending Null Characters to syslog with Python 3\.12\.
* systemd\_services \- update documentation regarding required\_one\_of and required\_by parameters \([https\://github\.com/ansible/ansible/issues/82914](https\://github\.com/ansible/ansible/issues/82914)\)\.
* template \- Fix error when templating an unsafe string which corresponds to an invalid type in Python \([https\://github\.com/ansible/ansible/issues/82600](https\://github\.com/ansible/ansible/issues/82600)\)\.
* template action will also inherit the behavior from copy \(as it uses it internally\)\.
* templating \- ensure syntax errors originating from a template being compiled into Python code object result in a failure \([https\://github\.com/ansible/ansible/issues/82606](https\://github\.com/ansible/ansible/issues/82606)\)
* unarchive \- add support for 8 character permission strings for zip archives \([https\://github\.com/ansible/ansible/pull/81705](https\://github\.com/ansible/ansible/pull/81705)\)\.
* unarchive \- force unarchive if symlink target changes \([https\://github\.com/ansible/ansible/issues/30420](https\://github\.com/ansible/ansible/issues/30420)\)\.
* unarchive modules now uses zipinfo options without relying on implementation defaults\, making it more compatible with all OS/distributions\.
* unsafe data \- Address an incompatibility when iterating or getting a single index from <code>AnsibleUnsafeBytes</code>
* unsafe data \- Address an incompatibility with <code>AnsibleUnsafeText</code> and <code>AnsibleUnsafeBytes</code> when pickling with <code>protocol\=0</code>
* unsafe data \- Enable directly using <code>AnsibleUnsafeText</code> with Python <code>pathlib</code> \([https\://github\.com/ansible/ansible/issues/82414](https\://github\.com/ansible/ansible/issues/82414)\)
* uri action plugin now skipped during check mode \(not supported\) instead of even trying to execute the module\, which already skipped\, this does not really change the result\, but returns much faster\.
* vars \- handle exception while combining VarsWithSources and dict \([https\://github\.com/ansible/ansible/issues/81659](https\://github\.com/ansible/ansible/issues/81659)\)\.
* wait\_for should not handle \'non mmapable files\' again\.
* winrm \- Better handle send input failures when communicating with hosts under load
* winrm \- Do not raise another exception during cleanup when a task is timed out \- [https\://github\.com/ansible/ansible/issues/81095](https\://github\.com/ansible/ansible/issues/81095)
* winrm \- does not hang when attempting to get process output when stdin write failed

<a id="amazon-aws-2"></a>
#### amazon\.aws

* backup\_plan \- Fix idempotency issue when using botocore \>\= 1\.31\.36 \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1952](https\://github\.com/ansible\-collections/amazon\.aws/issues/1952)\)\.
* cloudwatchevent\_rule \- Fix to avoid adding quotes to JSON input for provided input\_template \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1883](https\://github\.com/ansible\-collections/amazon\.aws/pull/1883)\)\.
* cloudwatchlogs\_log\_group\_info \- Implement exponential backoff when making API calls to prevent throttling exceptions \([https\://github\.com/ansible\-collections/amazon\.aws/issues/2011](https\://github\.com/ansible\-collections/amazon\.aws/issues/2011)\)\.
* ec2\_vpc\_subnet \- cleanly handle failure when subnet isn\'t created in time \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1848](https\://github\.com/ansible\-collections/amazon\.aws/pull/1848)\)\.
* iam\_managed\_policy \- fixed an issue where only partial results were returned \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1936](https\://github\.com/ansible\-collections/amazon\.aws/pull/1936)\)\.
* lookup/secretsmanager\_secret \- fix the issue when the nested secret is missing and on\_missing is set to warn\, the lookup was raising an error instead of a warning message \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1781](https\://github\.com/ansible\-collections/amazon\.aws/issues/1781)\)\.
* module\_utils/elbv2 \- Fix issue when creating or modifying Load balancer rule type authenticate\-oidc using <code>ClientSecret</code> parameter and <code>UseExistingClientSecret\=true</code> \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1877](https\://github\.com/ansible\-collections/amazon\.aws/issues/1877)\)\.
* plugin\_utils\.inventory \- Ensure templated options in lookup plugins are converted \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1955](https\://github\.com/ansible\-collections/amazon\.aws/issues/1955)\)\.
* plugins/inventory/aws\_ec2 \- Fix failure when retrieving information for more than 40 instances with use\_ssm\_inventory \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1713](https\://github\.com/ansible\-collections/amazon\.aws/issues/1713)\)\.
* s3\_object \- Fix the issue when copying an object with overriding metadata\. \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1991](https\://github\.com/ansible\-collections/amazon\.aws/issues/1991)\)\.
* s3\_object \- Fix typo that caused false deprecation warning when setting <code>overwrite\=latest</code> \([https\://github\.com/ansible\-collections/amazon\.aws/pull/1847](https\://github\.com/ansible\-collections/amazon\.aws/pull/1847)\)\.
* s3\_object \- when doing a put and specifying <code>Content\-Type</code> in metadata\, this module \(since 6\.0\.0\) erroneously set the <code>Content\-Type</code> to <code>None</code> causing the put to fail\. Fix now correctly honours the specified <code>Content\-Type</code> \([https\://github\.com/ansible\-collections/amazon\.aws/issues/1881](https\://github\.com/ansible\-collections/amazon\.aws/issues/1881)\)\.

<a id="ansible-utils-2"></a>
#### ansible\.utils

* Avoid unnecessary use of persistent connection in <em class="title-reference">cli\_parse</em>\, <em class="title-reference">fact\_diff</em>\, <em class="title-reference">update\_fact</em> and <em class="title-reference">validate</em> as this action does not require a connection\.

<a id="ansible-windows-1"></a>
#### ansible\.windows

* Process\.cs \- Fix up the <code>ProcessCreationFlags\.CreateProtectedProcess</code> typo in the enum name
* setup \- Fix up typo <code>collection \-\> collect</code> when a timeout occurred during a fact subset
* win\_acl \- Fix broken path in case of volume junction
* win\_get\_url \- Fix Tls1\.3 getting removed from the list of security protocols
* win\_powershell \- Remove unecessary using in code causing stray error records in output \- [https\://github\.com/ansible\-collections/ansible\.windows/issues/571](https\://github\.com/ansible\-collections/ansible\.windows/issues/571)
* win\_service\_info \- Warn and not fail if ERROR\_FILE\_NOT\_FOUND when trying to query a service \- [https\://github\.com/ansible\-collections/ansible\.windows/issues/556](https\://github\.com/ansible\-collections/ansible\.windows/issues/556)
* win\_updates \- Fix up typo for Download progress event messages \- [https\://github\.com/ansible\-collections/ansible\.windows/issues/554](https\://github\.com/ansible\-collections/ansible\.windows/issues/554)

<a id="arista-eos-2"></a>
#### arista\.eos

* This fix is needed because static\_routes and vlans are not returning anything when resources are not configured\.
* This got noticed in this issue \([https\://github\.com/network\-automation/toolkit/issues/47](https\://github\.com/network\-automation/toolkit/issues/47)\)
* correct a missing whitespace and add \'auth\' string\.
* correct the parsing of the elements in \'name\_servers\' in \'eos\_system\' module\.
* correct the reference of string attribute \'reference\_bandwith\'\.
* when static\_routes and vlans are not confirgured then return empty list\.

<a id="check-point-mgmt-1"></a>
#### check\_point\.mgmt

* httpapi/checkpoint\.py \- Raise a fatal error if login wasn\'t successful\.

<a id="cisco-aci-1"></a>
#### cisco\.aci

* Fix auto logout issue in aci connection plugin to keep connection active between tasks
* Fix idempotency for l3out configuration when l3protocol is used in aci\_l3out
* Fix issues with new attributes in aci\_interface\_policy\_leaf\_policy\_group module by adding conditions to include attributes in the payload only when they are specified by the user \(\#578\)
* Fix query in aci\_vmm\_controller

<a id="cisco-asa-1"></a>
#### cisco\.asa

* Prevents module\_defaults from were being incorrectly applied to the platform action\, instead of the concerned module\.

<a id="cisco-ios-3"></a>
#### cisco\.ios

* Prevents module\_defaults from were being incorrectly applied to the platform action\, instead of the concerned module\.
* Updated the ios\_ping ping module to support size param\.
* ios\_acls \- Adds back existing remarks for an ace entry when updated with replaced or overridden state\, as all remarks for a specific sequence gets removed when ace entry is updated\.
* ios\_acls \- Fix replaced state to consider remarks and ace entries while comparing configuration\.
* ios\_acls \- correctly match the different line for ACL without sequence number
* ios\_acls \- make sequence optional for rendering of standard acls\.
* ios\_acls \- take correctly in case where we want to push an ACL from a different type
* ios\_acls \- update module to apply remarks entry with sequence numbers\.
* ios\_bgp\_address\_family \- description attribute\, evalutated as complex object casted to string\.
* ios\_bgp\_global \- Explicitly add neighbor address to every parser\.
* ios\_bgp\_global \- Shutdown attributes generates negate command on set as false\.
* ios\_bgp\_global \- description attribute\, evalutated as complex object casted to string\.
* ios\_bgp\_global \- fix template attribute to generate configuration commands\.
* ios\_bgp\_global \- remote\_as not mendatory for neighbors\.
* ios\_interfaces \- description attribute\, evalutated as complex object casted to string\.
* ios\_l3\_interfaces \- remove validation from ipv6 address parameter\.
* ios\_ospfv2 \- Fix improper rendering of admin\_distance attribute\.
* ios\_prefix\_lists \- description attribute\, evalutated as complex object casted to string\.
* ios\_route\_maps \- description attribute\, evalutated as complex object casted to string\.
* ios\_snmp\_server \- fix group and user IPv6 ACL commands\.
* ios\_snmp\_server \- fixed config issue with snmp user password update being idempotent on consecutive runs\.
* ios\_user \- Fix configuration of hashed passwords and secrets\.
* ios\_user \- fix configuration of user with hashed password\.
* ios\_user \- fixed configuration removal of ssh users using purge\.
* ios\_vlans \- Make behaviour of the action states consistent\.
* ios\_vlans \- Top level configuration attribute is not required\, the module works with vlan and vlan configuration both\.
* ios\_vlans \- fixes behaviour of shutdown attribute with action states\.
* ios\_vrf \- Update and add missing argspec keys that define the attributes\.
* ios\_vrf \- added MDT related keys

<a id="cisco-iosxr-3"></a>
#### cisco\.iosxr

* Fix \'afi\' value in bgp\_templates RM to valid values\.
* Fix issue in gathered state of interfaces and l3\_interfaces RMs\([https\://github\.com/ansible\-collections/cisco\.iosxr/issues/452](https\://github\.com/ansible\-collections/cisco\.iosxr/issues/452)\, [https\://github\.com/ansible\-collections/cisco\.iosxr/issues/451](https\://github\.com/ansible\-collections/cisco\.iosxr/issues/451)\)

<a id="cisco-ise-1"></a>
#### cisco\.ise

* Added missing import re in endpoint module
* Updated to use ciscoisesdk v2\.1\.1 or newer fixing ciscoisesdk problem\.
* ansible\.utils changes to <em class="title-reference">\"\>\=2\.0\.0\,\<5\.0\"</em> in galaxy\.yml dependencies\.

<a id="cisco-meraki-1"></a>
#### cisco\.meraki

* Adding <em class="title-reference">network\_clients\_info</em> and <em class="title-reference">network\_client\_info</em>\.
* Adding <em class="title-reference">platform\_meraki\.rst</em> to docs\.
* Adding <em class="title-reference">product\_types</em> for update request on networks\.
* Adding <em class="title-reference">smartquotes \= False</em> to <em class="title-reference">conf\.py</em> and romoving <em class="title-reference">\'</em> from rst files\.
* Adding build\_ignore property to galaxy file\.
* Adding support to ansible\.utils \>\=3\.0
* Idempotency bugs fixed in devices\_switch\_ports\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_claim\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_clone\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_inventory\_claim\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_inventory\_onboarding\_cloud\_monitoring\_export\_events\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_inventory\_onboarding\_cloud\_monitoring\_prepare\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_inventory\_release\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_licenses\_assign\_seats\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_licenses\_move\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_licenses\_move\_seats\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_licenses\_renew\_seats\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_licensing\_coterm\_licenses\_move\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_networks\_combine\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_switch\_devices\_clone\.
* Parameter\`organization\_id\` change to <em class="title-reference">organizationId</em> organizations\_users\.
* Removing logs in meraki\.py\.
* networks\_syslog\_servers is now just an Update action to API\.

<a id="cisco-mso-1"></a>
#### cisco\.mso

* Fix TypeError for iteration on NoneType in mso\_schema\_template
* Fixed the useg\_subnet logic in mso\_schema\_template\_anp\_epg\_useg\_attribute

<a id="cisco-nxos-3"></a>
#### cisco\.nxos

* Prevents module\_defaults from were being incorrectly applied to the platform action\, instead of the concerned module\.
* nxos\_acls \- Fix parsing of ace entries with range in it\. \([https\://github\.com/ansible\-collections/cisco\.nxos/issues/788](https\://github\.com/ansible\-collections/cisco\.nxos/issues/788)\)
* nxos\_file\_copy \- correctly set file\_pull\_timeout/persistent\_command\_timeout value\.
* nxos\_interfaces \- Correctly enable L3 interfaces on supported N3K platforms \([https\://github\.com/ansible\-collections/cisco\.nxos/issues/749](https\://github\.com/ansible\-collections/cisco\.nxos/issues/749)\)\.

<a id="community-aws-1"></a>
#### community\.aws

* aws\_ssm \- disable <code>enable\-bracketed\-paste</code> to fix issue with amazon linux 2023 and other OSes \([https\://github\.com/ansible\-collections/community\.aws/issues/1756](https\://github\.com/ansible\-collections/community\.aws/issues/1756)\)
* ssm\(connection\) \- fix bucket region logic when region is <code>us\-east\-1</code> \([https\://github\.com/ansible\-collections/community\.aws/pull/1908](https\://github\.com/ansible\-collections/community\.aws/pull/1908)\)\.

<a id="community-ciscosmb-2"></a>
#### community\.ciscosmb

* issue
* solved issue

<a id="community-crypto-2"></a>
#### community\.crypto

* acme\_\* modules \- also retry requests in case of socket errors\, bad status lines\, and unknown connection errors\; improve error messages in these cases \([https\://github\.com/ansible\-collections/community\.crypto/issues/680](https\://github\.com/ansible\-collections/community\.crypto/issues/680)\)\.
* acme\_\* modules \- directly react on bad return data for account creation/retrieval/updating requests \([https\://github\.com/ansible\-collections/community\.crypto/pull/682](https\://github\.com/ansible\-collections/community\.crypto/pull/682)\)\.
* acme\_\* modules \- fix improved error reporting in case of socket errors\, bad status lines\, and unknown connection errors \([https\://github\.com/ansible\-collections/community\.crypto/pull/684](https\://github\.com/ansible\-collections/community\.crypto/pull/684)\)\.
* acme\_\* modules \- increase number of retries from 5 to 10 to increase stability with unstable ACME endpoints \([https\://github\.com/ansible\-collections/community\.crypto/pull/685](https\://github\.com/ansible\-collections/community\.crypto/pull/685)\)\.
* acme\_\* modules \- make account registration handling more flexible to accept 404 instead of 400 send by DigiCert\'s ACME endpoint when an account does not exist \([https\://github\.com/ansible\-collections/community\.crypto/pull/681](https\://github\.com/ansible\-collections/community\.crypto/pull/681)\)\.
* luks\_device \- fixed module a bug that prevented using <code>remove\_keyslot</code> with the value <code>0</code> \([https\://github\.com/ansible\-collections/community\.crypto/pull/710](https\://github\.com/ansible\-collections/community\.crypto/pull/710)\)\.
* luks\_device \- fixed module falsely outputting <code>changed\=false</code> when trying to add a new slot with a key that is already present in another slot\. The module now rejects adding keys that are already present in another slot \([https\://github\.com/ansible\-collections/community\.crypto/pull/710](https\://github\.com/ansible\-collections/community\.crypto/pull/710)\)\.
* luks\_device \- fixed testing of LUKS passphrases in when specifying a keyslot for cryptsetup version 2\.0\.3\. The output of this cryptsetup version slightly differs from later versions \([https\://github\.com/ansible\-collections/community\.crypto/pull/710](https\://github\.com/ansible\-collections/community\.crypto/pull/710)\)\.
* openssl\_dhparam \- was using an internal function instead of the public API to load DH param files when using the <code>cryptography</code> backend\. The internal function was removed in cryptography 42\.0\.0\. The module now uses the public API\, which has been available since support for DH params was added to cryptography \([https\://github\.com/ansible\-collections/community\.crypto/pull/698](https\://github\.com/ansible\-collections/community\.crypto/pull/698)\)\.
* openssl\_privatekey\_info \- <code>check\_consistency\=true</code> no longer works for RSA keys with cryptography 42\.0\.0\+ \([https\://github\.com/ansible\-collections/community\.crypto/pull/701](https\://github\.com/ansible\-collections/community\.crypto/pull/701)\)\.
* openssl\_privatekey\_info \- <code>check\_consistency\=true</code> now reports a warning if it cannot determine consistency \([https\://github\.com/ansible\-collections/community\.crypto/pull/705](https\://github\.com/ansible\-collections/community\.crypto/pull/705)\)\.

<a id="community-digitalocean-1"></a>
#### community\.digitalocean

* The C\(project\_name\) parameter for many modules was used by alias C\(project\) internally in the codebase\, but to work properly C\(project\_name\) must be used in the code\. Replace self\.module\.params\.get\(\"project\"\) with self\.module\.params\.get\(\"project\_name\"\) \([https\://github\.com/ansible\-collections/community\.digitalocean/issues/326](https\://github\.com/ansible\-collections/community\.digitalocean/issues/326)\)\.
* digital\_ocean\_kubernetes \- module didn\'t return kubeconfig properly\, return documentation was invalid\. Fixed version returns data with the same structure all the time\, also it is aligned with M\(community\.digitalocean\.digital\_ocean\_kubernetes\_info\) documentation return data now\. \([https\://github\.com/ansible\-collections/community\.digitalocean/issues/322](https\://github\.com/ansible\-collections/community\.digitalocean/issues/322)\)\.
* inventory plugin \- restore reading auth token from env variables \([https\://github\.com/ansible\-collections/community\.digitalocean/pull/315](https\://github\.com/ansible\-collections/community\.digitalocean/pull/315)\)\.

<a id="community-dns-3"></a>
#### community\.dns

* DNS record modules\, inventory plugins \- fix the TXT entry encoder to avoid splitting up escape sequences for quotes and backslashes over multiple TXT strings \([https\://github\.com/ansible\-collections/community\.dns/issues/190](https\://github\.com/ansible\-collections/community\.dns/issues/190)\, [https\://github\.com/ansible\-collections/community\.dns/pull/191](https\://github\.com/ansible\-collections/community\.dns/pull/191)\)\.
* Update Public Suffix List\.
* nameserver\_record\_info \- fix crash when more than one record is retrieved \([https\://github\.com/ansible\-collections/community\.dns/pull/172](https\://github\.com/ansible\-collections/community\.dns/pull/172)\)\.
* wait\_for\_txt\, nameserver\_info\, nameserver\_record\_info \- when looking up nameservers for a domain\, do not treat <code>NXDOMAIN</code> as a fatal error \([https\://github\.com/ansible\-collections/community\.dns/pull/177](https\://github\.com/ansible\-collections/community\.dns/pull/177)\)\.

<a id="community-docker-4"></a>
#### community\.docker

* Use <code>unix\:///var/run/docker\.sock</code> instead of the legacy <code>unix\://var/run/docker\.sock</code> as default for <code>docker\_host</code> \([https\://github\.com/ansible\-collections/community\.docker/pull/736](https\://github\.com/ansible\-collections/community\.docker/pull/736)\)\.
* docker\_compose\_v2 \- do not consider a <code>Waiting</code> event as an action/change \([https\://github\.com/ansible\-collections/community\.docker/pull/804](https\://github\.com/ansible\-collections/community\.docker/pull/804)\)\.
* docker\_compose\_v2 \- do not fail when non\-fatal errors occur\. This can happen when pulling an image fails\, but then the image can be built for another service\. Docker Compose emits an error in that case\, but <code>docker compose up</code> still completes successfully \([https\://github\.com/ansible\-collections/community\.docker/issues/807](https\://github\.com/ansible\-collections/community\.docker/issues/807)\, [https\://github\.com/ansible\-collections/community\.docker/pull/810](https\://github\.com/ansible\-collections/community\.docker/pull/810)\, [https\://github\.com/ansible\-collections/community\.docker/pull/811](https\://github\.com/ansible\-collections/community\.docker/pull/811)\)\.
* docker\_compose\_v2 \- do not treat service\-level pull events as changes to avoid incorrect <code>changed\=true</code> return value of <code>pull\=always</code> \([https\://github\.com/ansible\-collections/community\.docker/issues/802](https\://github\.com/ansible\-collections/community\.docker/issues/802)\, [https\://github\.com/ansible\-collections/community\.docker/pull/803](https\://github\.com/ansible\-collections/community\.docker/pull/803)\)\.
* docker\_compose\_v2 \- properly parse dry\-run build events from <code>stderr</code> \([https\://github\.com/ansible\-collections/community\.docker/issues/778](https\://github\.com/ansible\-collections/community\.docker/issues/778)\, [https\://github\.com/ansible\-collections/community\.docker/pull/779](https\://github\.com/ansible\-collections/community\.docker/pull/779)\)\.
* docker\_compose\_v2\* modules \- correctly parse <code>Warning</code> events emitted by Docker Compose \([https\://github\.com/ansible\-collections/community\.docker/issues/807](https\://github\.com/ansible\-collections/community\.docker/issues/807)\, [https\://github\.com/ansible\-collections/community\.docker/pull/811](https\://github\.com/ansible\-collections/community\.docker/pull/811)\)\.
* docker\_compose\_v2\* modules \- parse <code>logfmt</code> warnings emitted by Docker Compose \([https\://github\.com/ansible\-collections/community\.docker/issues/787](https\://github\.com/ansible\-collections/community\.docker/issues/787)\, [https\://github\.com/ansible\-collections/community\.docker/pull/811](https\://github\.com/ansible\-collections/community\.docker/pull/811)\)\.
* docker\_compose\_v2\, docker\_compose\_v2\_pull \- fix parsing of pull messages for Docker Compose 2\.20\.0 \([https\://github\.com/ansible\-collections/community\.docker/issues/785](https\://github\.com/ansible\-collections/community\.docker/issues/785)\, [https\://github\.com/ansible\-collections/community\.docker/pull/786](https\://github\.com/ansible\-collections/community\.docker/pull/786)\)\.
* docker\_compose\_v2\_pull \- fixing idempotence by checking actual pull progress events instead of service\-level pull request when <code>policy\=always</code>\. This stops the module from reporting <code>changed\=true</code> if no actual change happened when pulling\. In check mode\, it has to assume that a change happens though \([https\://github\.com/ansible\-collections/community\.docker/issues/813](https\://github\.com/ansible\-collections/community\.docker/issues/813)\, [https\://github\.com/ansible\-collections/community\.docker/pull/814](https\://github\.com/ansible\-collections/community\.docker/pull/814)\)\.
* docker\_compose\_v2\_pull \- the module was documented as part of the <code>community\.docker\.docker</code> action group\, but was not actually part of it\. That has now been fixed \([https\://github\.com/ansible\-collections/community\.docker/pull/773](https\://github\.com/ansible\-collections/community\.docker/pull/773)\)\.
* docker\_image \- fix archiving idempotency with Docker API 1\.44 or later \([https\://github\.com/ansible\-collections/community\.docker/pull/765](https\://github\.com/ansible\-collections/community\.docker/pull/765)\)\.
* modules and plugins using the Docker SDK for Python \- remove <code>ssl\_version</code> from the parameters passed to Docker SDK for Python 7\.0\.0\+\. Explicitly fail with a nicer error message if it was explicitly set in this case \([https\://github\.com/ansible\-collections/community\.docker/pull/715](https\://github\.com/ansible\-collections/community\.docker/pull/715)\)\.
* modules and plugins using the Docker SDK for Python \- remove <code>tls\_hostname</code> from the parameters passed to Docker SDK for Python 7\.0\.0\+\. Explicitly fail with a nicer error message if it was explicitly set in this case \([https\://github\.com/ansible\-collections/community\.docker/pull/721](https\://github\.com/ansible\-collections/community\.docker/pull/721)\)\.
* vendored Docker SDK for Python \- avoid passing on <code>ssl\_version</code> and <code>tls\_hostname</code> if they were not provided by the user\. Remove dead code\. \([https\://github\.com/ansible\-collections/community\.docker/pull/722](https\://github\.com/ansible\-collections/community\.docker/pull/722)\)\.

<a id="community-general-3"></a>
#### community\.general

* aix\_filesystem \- fix issue with empty list items in crfs logic and option order \([https\://github\.com/ansible\-collections/community\.general/pull/8052](https\://github\.com/ansible\-collections/community\.general/pull/8052)\)\.
* apt\-rpm \- the module did not upgrade packages if a newer version exists\. Now the package will be reinstalled if the candidate is newer than the installed version \([https\://github\.com/ansible\-collections/community\.general/issues/7414](https\://github\.com/ansible\-collections/community\.general/issues/7414)\)\.
* cargo \- fix idempotency issues when using a custom installation path for packages \(using the <code>\-\-path</code> parameter\)\. The initial installation runs fine\, but subsequent runs use the <code>get\_installed\(\)</code> function which did not check the given installation location\, before running <code>cargo install</code>\. This resulted in a false <code>changed</code> state\. Also the removal of packeges using <code>state\: absent</code> failed\, as the installation check did not use the given parameter \([https\://github\.com/ansible\-collections/community\.general/pull/7970](https\://github\.com/ansible\-collections/community\.general/pull/7970)\)\.
* cloudflare\_dns \- fix Cloudflare lookup of SHFP records \([https\://github\.com/ansible\-collections/community\.general/issues/7652](https\://github\.com/ansible\-collections/community\.general/issues/7652)\)\.
* consul\_token \- fix token creation without <code>accessor\_id</code> \([https\://github\.com/ansible\-collections/community\.general/pull/8091](https\://github\.com/ansible\-collections/community\.general/pull/8091)\)\.
* gitlab\_issue \- fix behavior to search GitLab issue\, using <code>search</code> keyword instead of <code>title</code> \([https\://github\.com/ansible\-collections/community\.general/issues/7846](https\://github\.com/ansible\-collections/community\.general/issues/7846)\)\.
* gitlab\_runner \- fix pagination when checking for existing runners \([https\://github\.com/ansible\-collections/community\.general/pull/7790](https\://github\.com/ansible\-collections/community\.general/pull/7790)\)\.
* homebrew \- detect already installed formulae and casks using JSON output from <code>brew info</code> \([https\://github\.com/ansible\-collections/community\.general/issues/864](https\://github\.com/ansible\-collections/community\.general/issues/864)\)\.
* homebrew \- error returned from brew command was ignored and tried to parse empty JSON\. Fix now checks for an error and raises it to give accurate error message to users \([https\://github\.com/ansible\-collections/community\.general/issues/8047](https\://github\.com/ansible\-collections/community\.general/issues/8047)\)\.
* incus connection plugin \- treats <code>inventory\_hostname</code> as a variable instead of a literal in remote connections \([https\://github\.com/ansible\-collections/community\.general/issues/7874](https\://github\.com/ansible\-collections/community\.general/issues/7874)\)\.
* interface\_files \- also consider <code>address\_family</code> when changing <code>option\=method</code> \([https\://github\.com/ansible\-collections/community\.general/issues/7610](https\://github\.com/ansible\-collections/community\.general/issues/7610)\, [https\://github\.com/ansible\-collections/community\.general/pull/7612](https\://github\.com/ansible\-collections/community\.general/pull/7612)\)\.
* ipa\_hbacrule \- the module uses a string for <code>ipaenabledflag</code> for new FreeIPA versions while the returned value is a boolean \([https\://github\.com/ansible\-collections/community\.general/pull/7880](https\://github\.com/ansible\-collections/community\.general/pull/7880)\)\.
* ipa\_otptoken \- the module expect <code>ipatokendisabled</code> as string but the <code>ipatokendisabled</code> value is returned as a boolean \([https\://github\.com/ansible\-collections/community\.general/pull/7795](https\://github\.com/ansible\-collections/community\.general/pull/7795)\)\.
* ipa\_sudorule \- the module uses a string for <code>ipaenabledflag</code> for new FreeIPA versions while the returned value is a boolean \([https\://github\.com/ansible\-collections/community\.general/pull/7880](https\://github\.com/ansible\-collections/community\.general/pull/7880)\)\.
* iptables\_state \- fix idempotency issues when restoring incomplete iptables dumps \([https\://github\.com/ansible\-collections/community\.general/issues/8029](https\://github\.com/ansible\-collections/community\.general/issues/8029)\)\.
* irc \- replace <code>ssl\.wrap\_socket</code> that was removed from Python 3\.12 with code for creating a proper SSL context \([https\://github\.com/ansible\-collections/community\.general/pull/7542](https\://github\.com/ansible\-collections/community\.general/pull/7542)\)\.
* keycloak\_\* \- fix Keycloak API client to quote <code>/</code> properly \([https\://github\.com/ansible\-collections/community\.general/pull/7641](https\://github\.com/ansible\-collections/community\.general/pull/7641)\)\.
* keycloak\_authz\_permission \- resource payload variable for scope\-based permission was constructed as a string\, when it needs to be a list\, even for a single item \([https\://github\.com/ansible\-collections/community\.general/issues/7151](https\://github\.com/ansible\-collections/community\.general/issues/7151)\)\.
* keycloak\_client \- fixes issue when metadata is provided in desired state when task is in check mode \([https\://github\.com/ansible\-collections/community\.general/issues/1226](https\://github\.com/ansible\-collections/community\.general/issues/1226)\, [https\://github\.com/ansible\-collections/community\.general/pull/7881](https\://github\.com/ansible\-collections/community\.general/pull/7881)\)\.
* keycloak\_identity\_provider \- <code>mappers</code> processing was not idempotent if the mappers configuration list had not been sorted by name \(in ascending order\)\. Fix resolves the issue by sorting mappers in the desired state using the same key which is used for obtaining existing state \([https\://github\.com/ansible\-collections/community\.general/pull/7418](https\://github\.com/ansible\-collections/community\.general/pull/7418)\)\.
* keycloak\_identity\_provider \- it was not possible to reconfigure \(add\, remove\) <code>mappers</code> once they were created initially\. Removal was ignored\, adding new ones resulted in dropping the pre\-existing unmodified mappers\. Fix resolves the issue by supplying correct input to the internal update call \([https\://github\.com/ansible\-collections/community\.general/pull/7418](https\://github\.com/ansible\-collections/community\.general/pull/7418)\)\.
* keycloak\_user \- when <code>force</code> is set\, but user does not exist\, do not try to delete it \([https\://github\.com/ansible\-collections/community\.general/pull/7696](https\://github\.com/ansible\-collections/community\.general/pull/7696)\)\.
* ldap \- previously the order number \(if present\) was expected to follow an equals sign in the DN\. This makes it so the order number string is identified correctly anywhere within the DN \([https\://github\.com/ansible\-collections/community\.general/issues/7646](https\://github\.com/ansible\-collections/community\.general/issues/7646)\)\.
* linode inventory plugin \- add descriptive error message for linode inventory plugin \([https\://github\.com/ansible\-collections/community\.general/pull/8133](https\://github\.com/ansible\-collections/community\.general/pull/8133)\)\.
* log\_entries callback plugin \- replace <code>ssl\.wrap\_socket</code> that was removed from Python 3\.12 with code for creating a proper SSL context \([https\://github\.com/ansible\-collections/community\.general/pull/7542](https\://github\.com/ansible\-collections/community\.general/pull/7542)\)\.
* lvol \- test for output messages in both <code>stdout</code> and <code>stderr</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7601](https\://github\.com/ansible\-collections/community\.general/pull/7601)\, [https\://github\.com/ansible\-collections/community\.general/issues/7182](https\://github\.com/ansible\-collections/community\.general/issues/7182)\)\.
* modprobe \- listing modules files or modprobe files could trigger a FileNotFoundError if <code>/etc/modprobe\.d</code> or <code>/etc/modules\-load\.d</code> did not exist\. Relevant functions now return empty lists if the directories do not exist to avoid crashing the module \([https\://github\.com/ansible\-collections/community\.general/issues/7717](https\://github\.com/ansible\-collections/community\.general/issues/7717)\)\.
* mssql\_script \- make the module work with Python 2 \([https\://github\.com/ansible\-collections/community\.general/issues/7818](https\://github\.com/ansible\-collections/community\.general/issues/7818)\, [https\://github\.com/ansible\-collections/community\.general/pull/7821](https\://github\.com/ansible\-collections/community\.general/pull/7821)\)\.
* nmcli \- fix <code>connection\.slave\-type</code> wired to <code>bond</code> and not with parameter <code>slave\_type</code> in case of connection type <code>wifi</code> \([https\://github\.com/ansible\-collections/community\.general/issues/7389](https\://github\.com/ansible\-collections/community\.general/issues/7389)\)\.
* onepassword lookup plugin \- failed for fields that were in sections and had uppercase letters in the label/ID\. Field lookups are now case insensitive in all cases \([https\://github\.com/ansible\-collections/community\.general/pull/7919](https\://github\.com/ansible\-collections/community\.general/pull/7919)\)\.
* onepassword lookup plugin \- field and section titles are now case insensitive when using op CLI version two or later\. This matches the behavior of version one \([https\://github\.com/ansible\-collections/community\.general/pull/7564](https\://github\.com/ansible\-collections/community\.general/pull/7564)\)\.
* pacemaker\_cluster \- actually implement check mode\, which the module claims to support\. This means that until now the module also did changes in check mode \([https\://github\.com/ansible\-collections/community\.general/pull/8081](https\://github\.com/ansible\-collections/community\.general/pull/8081)\)\.
* pam\_limits \- when the file does not exist\, do not create it in check mode \([https\://github\.com/ansible\-collections/community\.general/issues/8050](https\://github\.com/ansible\-collections/community\.general/issues/8050)\, [https\://github\.com/ansible\-collections/community\.general/pull/8057](https\://github\.com/ansible\-collections/community\.general/pull/8057)\)\.
* pkgin \- pkgin \(pkgsrc package manager used by SmartOS\) raises erratic exceptions and spurious <code>changed\=true</code> \([https\://github\.com/ansible\-collections/community\.general/pull/7971](https\://github\.com/ansible\-collections/community\.general/pull/7971)\)\.
* proxmox \- fix updating a container config if the setting does not already exist \([https\://github\.com/ansible\-collections/community\.general/pull/7872](https\://github\.com/ansible\-collections/community\.general/pull/7872)\)\.
* proxmox\_kvm \- fixed status check getting from node\-specific API endpoint \([https\://github\.com/ansible\-collections/community\.general/issues/7817](https\://github\.com/ansible\-collections/community\.general/issues/7817)\)\.
* proxmox\_kvm \- running <code>state\=template</code> will first check whether VM is already a template \([https\://github\.com/ansible\-collections/community\.general/pull/7792](https\://github\.com/ansible\-collections/community\.general/pull/7792)\)\.
* redfish\_info \- allow for a GET operation invoked by <code>GetUpdateStatus</code> to allow for an empty response body for cases where a service returns 204 No Content \([https\://github\.com/ansible\-collections/community\.general/issues/8003](https\://github\.com/ansible\-collections/community\.general/issues/8003)\)\.
* redfish\_info \- correct uncaught exception when attempting to retrieve <code>Chassis</code> information \([https\://github\.com/ansible\-collections/community\.general/pull/7952](https\://github\.com/ansible\-collections/community\.general/pull/7952)\)\.
* redhat\_subscription \- use the D\-Bus registration on RHEL 7 only on 7\.4 and
  greater\; older versions of RHEL 7 do not have it
  \([https\://github\.com/ansible\-collections/community\.general/issues/7622](https\://github\.com/ansible\-collections/community\.general/issues/7622)\,
  [https\://github\.com/ansible\-collections/community\.general/pull/7624](https\://github\.com/ansible\-collections/community\.general/pull/7624)\)\.
* statusio\_maintenance \- fix error caused by incorrectly formed API data payload\. Was raising \"Failed to create maintenance HTTP Error 400 Bad Request\" caused by bad data type for date/time and deprecated dict keys \([https\://github\.com/ansible\-collections/community\.general/pull/7754](https\://github\.com/ansible\-collections/community\.general/pull/7754)\)\.
* terraform \- fix multiline string handling in complex variables \([https\://github\.com/ansible\-collections/community\.general/pull/7535](https\://github\.com/ansible\-collections/community\.general/pull/7535)\)\.

<a id="community-grafana-1"></a>
#### community\.grafana

* Add <em class="title-reference">grafana\_organiazion\_user</em> to <em class="title-reference">action\_groups\.grafana</em>
* Fixed orgId handling in diff comparison for <em class="title-reference">grafana\_datasource</em> if using org\_name
* test\: replace deprecated <em class="title-reference">TestCase\.assertEquals</em> to support Python 3\.12

<a id="community-mysql-2"></a>
#### community\.mysql

* mysql\_info \- the <code>slave\_status</code> filter was returning an empty list on MariaDB with multiple replication channels\. It now returns all channels by running <code>SHOW ALL SLAVES STATUS</code> for MariaDB servers \([https\://github\.com/ansible\-collections/community\.mysql/issues/603](https\://github\.com/ansible\-collections/community\.mysql/issues/603)\)\.

<a id="community-postgresql-1"></a>
#### community\.postgresql

* postgresql\_privs \- fix a failure when altering privileges with <code>grant\_option\: true</code> \([https\://github\.com/ansible\-collections/community\.postgresql/issues/668](https\://github\.com/ansible\-collections/community\.postgresql/issues/668)\)\.
* postgresql\_query \- now reports not changed for queries starting with \"SHOW\" \([https\://github\.com/ansible\-collections/community\.postgresql/pull/592](https\://github\.com/ansible\-collections/community\.postgresql/pull/592)\)\.
* postgresql\_user \- module failed when running against an SQL\_ASCII encoded database as the user\'s current password was returned as bytes as opposed to a str\. Fix now checks for this case and decodes the bytes as an ascii encoded string\. \([https\://github\.com/ansible\-collections/community\.postgresql/issues/584](https\://github\.com/ansible\-collections/community\.postgresql/issues/584)\)\.

<a id="community-routeros-1"></a>
#### community\.routeros

* facts \- fix date not getting removed for idempotent config export \([https\://github\.com/ansible\-collections/community\.routeros/pull/262](https\://github\.com/ansible\-collections/community\.routeros/pull/262)\)\.

<a id="community-sap-libs"></a>
#### community\.sap\_libs

* fixes failures in sanity test for all modules

<a id="community-vmware-1"></a>
#### community\.vmware

* Fix InsecureRequestWarning for modules based on the VmwareRestClient module util when setting <code>validate\_certs</code> to <code>False</code> \([https\://github\.com/ansible\-collections/community\.vmware/pull/1969](https\://github\.com/ansible\-collections/community\.vmware/pull/1969)\)\.
* module\_utils/vmware\.py \- remove ssl\.wrap\_socet\(\) function\. Replaced for code based on ssl\.get\_server\_certificate \([https\://github\.com/ansible\-collections/community\.vmware/issues/1930](https\://github\.com/ansible\-collections/community\.vmware/issues/1930)\)\.
* vmware\_guest \- Fix failure of vm reconfiguration with enabled virt\_based\_security \([https\://github\.com/ansible\-collections/community\.vmware/pull/1848](https\://github\.com/ansible\-collections/community\.vmware/pull/1848)\)\.
* vmware\_vm\_info \- Fix an AttributeError when gathering network information \([https\://github\.com/ansible\-collections/community\.vmware/pull/1919](https\://github\.com/ansible\-collections/community\.vmware/pull/1919)\)\.

<a id="community-windows-1"></a>
#### community\.windows

* Remove some code which is no longer valid for dotnet 5\+
* community\.windows\.win\_psmodule\_info \- exception thrown when host has no Installed Module\. Fix now checks that variable \$installedModules is not null before calling the \.Contains\(\.\.\) function on it\.
* win\_format\, win\_partition \- Add support for Windows failover cluster disks
* win\_psmodule \- Fix up error message with <code>state\=latest</code>
* win\_rabbitmq\_plugin \- Avoid using <code>Invoke\-Expression</code> when running external commands
* win\_rds\_rap \- The module crashed when creating a RAP with Gateway Managed Computer Group \([https\://github\.com/ansible\-collections/community\.windows/issues/184](https\://github\.com/ansible\-collections/community\.windows/issues/184)\)\.
* win\_robocopy \- Fix up <code>cmd</code> return value to include the executable <code>robocopy</code>

<a id="community-zabbix-1"></a>
#### community\.zabbix

* Avoid to update user\-directory configuration in dry run\.
* api module \- Fixed certificiate errors
* proxy and server roles \- Defaulted location of fping and fping6 based on OS\.
* proxy role \- Removed requirement for mysql group definition\.
* server role \- typo in configuration var StasAllowedIP to StatsAllowedIP
* zabbix\-\{agent\, javagateway\, proxy\, server\, web\} \- support raspberry pi without repository url specification
* zabbix\_inventory \- fixed handeling of add\_zabbix\_groups option
* zabbix\_template \- fix template export when template\'s content has \"error\" word
* zabbix\_web role \- fix variable naming issues \(undefined\) to zabbix\_web\_version and zabbix\_web\_apt\_repository

<a id="containers-podman-1"></a>
#### containers\.podman

* Add idempotency for podman\_secret module
* Catch exceptions when no JSON output in podman\_image
* Fail if systemd generation failed and it\'s explicitly set
* Fix example name
* Fix idempotency for podman\_network
* Fix idempotency when using 0\.0\.0\.0 in ports
* Fix multi\-image support for podman\_save
* Fix volume inspection by name in podman\_volume
* Recreate stopped containers if recreate flag is enabled
* podman\_container \- Add check and fixed for v5 network diff
* podman\_container \- Fix pasta networking idempotency for v5 \(\#728\)
* podman\_container\_exec \- Remove unnecessary quotes in podman\_container\_exec module
* podman\_image\_info \- Fix wrong return data type in podman\_image\_info
* podman\_play \- Fix kube play annotations
* podman\_pod \- Fix broken info of pods in Podman v5
* podman\_pod \- Fix pod for Podman v5
* podman\_pod \- Fix podman pod v5 broken info issue

<a id="dellemc-enterprise-sonic-1"></a>
#### dellemc\.enterprise\_sonic

* requirements \- Update requires\_ansible version in meta/runtime\.yml to the oldest supported version \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/321](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/321)\)\.
* sonic\_bgp\_communities \- Fix incorrect \"facts\" handling for parsing of a BGP community list configured with an empty \"members\" list \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/319](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/319)\)\.
* sonic\_bgp\_neighbors \- Fix prefix\-limit issue \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/289](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/289)\)\.
* sonic\_interfaces \- Add warnings when speed and auto\_negotiate is configured at same time \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314)\)\.
* sonic\_interfaces \- Fix support for standard naming interfaces \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314)\)\.
* sonic\_interfaces \- Prevent configuring speed in port group interfaces \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/314)\)\.
* sonic\_stp \- Correct the commands list for STP delete state \([https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/302](https\://github\.com/ansible\-collections/dellemc\.enterprise\_sonic/pull/302)\)\.

<a id="dellemc-openmanage-3"></a>
#### dellemc\.openmanage

* Added support for RAID creation using NVMe disks\.\([https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/635](https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/635)\)
* Fixed the issue for ignoring the environment variable <em class="title-reference">NO\_PROXY</em> earlier\. \([https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/554](https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/554)\)
* For idrac\_certificates module\, the <em class="title-reference">email\_address</em> has been made as an optional parameter\. \([https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/582](https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/582)\)\.
* Issue is fixed for deploying a new configuration on quick deploy slot when IPv6 is disabled\.\([https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/533](https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/533)\)
* idrac\_network\_attributes \- Issue\(279049\) \-  If unsupported values are provided for the parameter <code>ome\_network\_attributes</code>\, then this module does not provide a correct error message\.
* ome\_device\_network\_services \- Issue\(212681\) \- The module does not provide a proper error message if unsupported values are provided for the following parameters\- port\_number\, community\_name\, max\_sessions\, max\_auth\_retries\, and idle\_timeout\.
* ome\_device\_power\_settings \- Issue\(212679\) \- The module displays the following message if the value provided for the parameter <code>power\_cap</code> is not within the supported range of 0 to 32767\, <code>Unable to complete the request because PowerCap does not exist or is not applicable for the resource URI\.</code>
* ome\_inventory \- The plugin returns 50 results when a group is specified\. No results are shown when a group is not specified\. \([https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/575](https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/575)\)\.
* redfish\_storage\_volume is enhanced to support iDRAC8\.\([https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/625](https\://github\.com/dell/dellemc\-openmanage\-ansible\-modules/issues/625)\)

<a id="f5networks-f5-modules-1"></a>
#### f5networks\.f5\_modules

* bigip\_gtm\_monitor\_bigip \- fixed an issue where IP and port were not applied correctly when creating new monitor\.
* bigip\_gtm\_monitor\_firepass \- fixed an issue where IP and port were not applied correctly when creating new monitor\.
* bigip\_gtm\_monitor\_http \- fixed an issue where IP and port were not applied correctly when creating new monitor\.
* bigip\_gtm\_monitor\_https\- fixed an issue where IP and port were not applied correctly when creating new monitor\.
* bigip\_gtm\_monitor\_tcp \- fixed an issue where IP and port were not applied correctly when creating new monitor\.
* bigip\_gtm\_monitor\_tcp\_half\_open \- fixed an issue where IP and port were not applied correctly when creating new monitor\.
* bigip\_gtm\_topology\_region \- fixed an issue where if multiple states with spaces in values were defined\, module would throw invalid command error
* bigip\_gtm\_topology\_region \- fixed an issue where states names that contained spaces caused the idempotency to break\.
* bigip\_ssl\_key\_cert \- fixed an issue where the passphrase was not being properly send to the BIG\-IP\.

<a id="fortinet-fortimanager-1"></a>
#### fortinet\.fortimanager

* Added missing enum values for some arguments\.
* Change minimum required ansible\-core version to 2\.14\.0
* Changed revision to v\_range to reduce the size of the code\.
* Fixed a bug where ansible may skip update incorrectly\.
* Fixed the behavior of module fmgr\_firewall\_internetservicecustom\.
* Fixed the behavior of some modules that contain the argument policyid\.
* Improved example ansible playbooks\.
* Improved the logic of fmgr\_fact\, fmgr\_clone\, fmgr\_rename\, fmgr\_move\. Usage remains unchanged\.
* Reduced the size of module\_arg\_spec in each module\.
* Removed most of the sanity test ignores\.
* Support FortiManager 7\.0\.10

<a id="fortinet-fortios-1"></a>
#### fortinet\.fortios

* Fix the issue that ssl\-certificate cannot be set in <em class="title-reference">fortios\_firewall\_vip</em> and <em class="title-reference">fortios\_firewall\_vip6</em>\.
* Github issue
* mantis issue

<a id="hetzner-hcloud-2"></a>
#### hetzner\.hcloud

* hcloud inventory \- Ensure the API client use a new cache for every <em>cached session</em>\.
* load\_balancer\_info \- Correctly return the <em class="title-reference">cookie\_lifetime</em> value\.
* load\_balancer\_service \- Correctly return the <em class="title-reference">cookie\_lifetime</em> value\.

<a id="ibm-qradar-1"></a>
#### ibm\.qradar

* A bunch of ansible\-lint and ansible\-test sanity issues have been fixed\.

<a id="ibm-storage-virtualize-1"></a>
#### ibm\.storage\_virtualize

* ibm\_svc\_info \- Command and release mapping to remove errors in gather\_subset\=all
* ibm\_svc\_info \- Return error in listing entities that require object name

<a id="infoblox-nios-modules-1"></a>
#### infoblox\.nios\_modules

* Fixes environment variable max\_results using INFOBLOX\_MAX\_RESULTS [\#209](https\://github\.com/infobloxopen/infoblox\-ansible/pull/209)
* Fixes index error for transform fields in DTC LBDN \(auth\_zone and Pool\) and DTC POOL \(servers and monitors\) [\#209](https\://github\.com/infobloxopen/infoblox\-ansible/pull/209)
* Fixes typo for environment variable INFOBLOX\_WAPI\_VERSION [\#209](https\://github\.com/infobloxopen/infoblox\-ansible/pull/209)

<a id="junipernetworks-junos-2"></a>
#### junipernetworks\.junos

* Fix the empty facts list placement
* Prevents module\_defaults from were being incorrectly applied to the platform action\, instead of the concerned module\.
* acls
* fix to gather l2\_interfaces facts with default port\-mode access\.
* initialize facts dictionary with empty containers for respective resources mentioned below
* lldp\_global
* lldp\_interfaces
* logging\_global
* ntp\_global
* ospf\_interfaces
* ospfv2
* ospfv3
* prefix\_lists
* routing\_instances
* routing\_options
* security\_policies
* security\_policies\_global
* security\_zones
* snmp\_server
* static\_routes
* vlans

<a id="kubernetes-core-3"></a>
#### kubernetes\.core

* Resolve Collections util resource discovery fails when complex subresources present \([https\://github\.com/ansible\-collections/kubernetes\.core/pull/676](https\://github\.com/ansible\-collections/kubernetes\.core/pull/676)\)\.
* align <em class="title-reference">helmdiff\_check\(\)</em> function commandline rendering with the <em class="title-reference">deploy\(\)</em> function \([https\://github\.com/ansible\-collections/kubernetes\.core/pull/670](https\://github\.com/ansible\-collections/kubernetes\.core/pull/670)\)\.
* helm \- Put the chart\_ref into quotes when running <code>helm show chart</code>\, <code>helm upgrade</code> and <code>helm dependency update</code> commands \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/653](https\://github\.com/ansible\-collections/kubernetes\.core/issues/653)\)\.
* helm \- delete temporary file created when deploying chart with option <code>release\_values</code> set \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/530](https\://github\.com/ansible\-collections/kubernetes\.core/issues/530)\)\.
* helm \- fix issue occurring when uninstalling chart with statues others than <code>deployed</code> \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/319](https\://github\.com/ansible\-collections/kubernetes\.core/issues/319)\)\.
* helm \- fix post\_renderer argument breaking the helm deploy\_command \([https\://github\.com/ansible\-collections/kubernetes\.core/pull/586](https\://github\.com/ansible\-collections/kubernetes\.core/pull/586)\)\.
* helm \- use <code>reuse\-values</code> when running <code>helm diff</code> command \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/680](https\://github\.com/ansible\-collections/kubernetes\.core/issues/680)\)\.
* helm \- use post\_renderer when checking <code>changed</code> status for a helm release \([https\://github\.com/ansible\-collections/kubernetes\.core/pull/588](https\://github\.com/ansible\-collections/kubernetes\.core/pull/588)\)\.
* integrations test helm\_kubeconfig \- set helm version to v3\.10\.3 to avoid incompatability with new bitnami charts \([https\://github\.com/ansible\-collections/kubernetes\.core/pull/670](https\://github\.com/ansible\-collections/kubernetes\.core/pull/670)\)\.
* k8s\_scale \- clean handling of ResourceTimeout exception \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/583](https\://github\.com/ansible\-collections/kubernetes\.core/issues/583)\)\.
* k8s\_scale \- fix issue when scaling StatefulSets with <code>updateStrategy\=OnDelete</code> \([https\://github\.com/ansible\-collections/kubernetes\.core/issues/579](https\://github\.com/ansible\-collections/kubernetes\.core/issues/579)\)\.

<a id="lowlydba-sqlserver-1"></a>
#### lowlydba\.sqlserver

* Add ActiveStartDate to the compare properties so this item is marked accurately as changed\.
* Fixed the formatting of the SPN by updating the backslash to a forward\-slash for the \$spn var \(lowlydba\.sqlserver\.spn\)
* Update documentation for agent\_job\_schedule to reflect proper input formatting\. \([https\://github\.com/lowlydba/lowlydba\.sqlserver/pull/229](https\://github\.com/lowlydba/lowlydba\.sqlserver/pull/229)\)

<a id="microsoft-ad-1"></a>
#### microsoft\.ad

* debug\_ldap\_client \- handle failures when attempting to get the krb5 context and default CCache rather than fail with a traceback
* microsoft\.ad\.group \- Support membership lookup of groups that are longer than 20 characters long
* microsoft\.ad\.membership \- Add helpful hint when the failure was due to a missing/invalid <code>domain\_ou\_path</code> \- [https\://github\.com/ansible\-collections/microsoft\.ad/issues/88](https\://github\.com/ansible\-collections/microsoft\.ad/issues/88)

<a id="netapp-ontap-1"></a>
#### netapp\.ontap

* na\_ontap\_ems\_destination \- fix field error with <em class="title-reference">certificate\.name</em> for ONTAP 9\.11\.1 or later in REST\.
* na\_ontap\_igroup\_initiator \- fixed issue with idempotency\.
* na\_ontap\_nfs \- fix error with <em class="title-reference">windows</em> in REST for ONTAP 9\.10 or earlier\.
* na\_ontap\_security\_certificates \- fix error with ontap\_info returned in module output in REST\.
* na\_ontap\_snapshot\_policy \- fix issue with modifying snapshot policy in REST\.
* na\_ontap\_volume \- modified <em class="title-reference">type</em> to be case insensitive in REST\.
* na\_ontap\_vserver\_peer \- fix issue with peering multiple clusters with same vserver name in REST\.

<a id="netapp-storagegrid-1"></a>
#### netapp\.storagegrid

* Removed fetch limit in API request and implemented pagination\.

<a id="netbox-netbox-1"></a>
#### netbox\.netbox

* Improve error reporting for missing module \[\#1126\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1126](https\://github\.com/netbox\-community/ansible\_modules/pull/1126)\)
* nb\_inventory \- Fix API cache failure \[\#1111\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1111](https\://github\.com/netbox\-community/ansible\_modules/pull/1111)\)
* nb\_lookup \- Allow multiple IDs in nb\_lookup \[\#1042\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1042](https\://github\.com/netbox\-community/ansible\_modules/pull/1042)\)
* netbox\_vlan \- Fix documentation of vlan\_group \[\#1138\]\([https\://github\.com/netbox\-community/ansible\_modules/pull/1138](https\://github\.com/netbox\-community/ansible\_modules/pull/1138)\)

<a id="purestorage-flasharray-1"></a>
#### purestorage\.flasharray

* purefa\_cert \- Fixed issue where parts of the subject where not included in the CSR if they did not exist in the currently used cert\.
* purefa\_certs \- Allow certificates of over 3000 characters to be imported\.
* purefa\_dns \- Fixed attribute error on deletion of management DNS
* purefa\_ds \- Fix issue with SDK returning empty data for data directory services even when it does exist
* purefa\_info \- Resolved issue with KeyError when LACP bonds are in use
* purefa\_inventory \- Fix issue with iSCSI\-only FlashArrays
* purefa\_pg \- Allows a protection group to be correctly created when <em class="title-reference">target</em> is specified as well as other objects\, such as <em class="title-reference">volumes</em> or <em class="title-reference">hosts</em>
* purefa\_pgsched \- Fixed issue with disabling schedules
* purefa\_pgsnap \- Add support for restoring volumes connected to hosts in a host\-based protection group and hosts in a hostgroup\-based protection group\.
* purefa\_pgsnap \- Fixed incorrect parameter name
* purefa\_policy \- Fix incorrect call of psot instead of patch for NFS policies

<a id="purestorage-flashblade-1"></a>
#### purestorage\.flashblade

* purefb\_bucket \- Changed logic to allow complex buckets to be created in a single call\, rather than having to split into two tasks\.
* purefb\_info \- Added missing object lock retention details if enabledd
* purefb\_lag \- Enable LAG port configuration with multi\-chassis
* purefb\_timeout \- Fixed arithmetic error that resulted in module incorrectly reporting changed when no change was required\.

<a id="splunk-es-1"></a>
#### splunk\.es

* Fixed argspec validation for plugins with empty task attributes when run with Ansible 2\.9\.

<a id="telekom-mms-icinga-director-1"></a>
#### telekom\_mms\.icinga\_director

* Fixes \#190 \- Workaround for service apply bug \([https\://github\.com/telekom\-mms/ansible\-collection\-icinga\-director/pull/239](https\://github\.com/telekom\-mms/ansible\-collection\-icinga\-director/pull/239)\)

<a id="theforeman-foreman-2"></a>
#### theforeman\.foreman

* compute\_profile\, host \- refer to VMware storage pods by name\, not id \([https\://github\.com/theforeman/foreman\-ansible\-modules/issues/1247](https\://github\.com/theforeman/foreman\-ansible\-modules/issues/1247)\)
* content\_view\_filter\_rule \- handle multiple rules for the same package but different architectures and versions correctly \([https\://bugzilla\.redhat\.com/show\_bug\.cgi\?id\=2189687](https\://bugzilla\.redhat\.com/show\_bug\.cgi\?id\=2189687)\)

<a id="vmware-vmware-rest-2"></a>
#### vmware\.vmware\_rest

* content\_library\_item\_info \- fixed error with unsupported property
* lookup plugins \- Refactor to use native options configuration via doc\_fragment\, which ensures that vcenter\_validate\_certs\=false is honored \([https\://github\.com/ansible\-collections/vmware\.vmware\_rest/issues/425](https\://github\.com/ansible\-collections/vmware\.vmware\_rest/issues/425)\)\.

<a id="vultr-cloud-1"></a>
#### vultr\.cloud

* Fixed an error while waiting for a specific state and the API returns an empty response\. \([https\://github\.com/vultr/ansible\-collection\-vultr/issues/108](https\://github\.com/vultr/ansible\-collection\-vultr/issues/108)\)\.
* Fixed an issue with waiting for state \([https\://github\.com/vultr/ansible\-collection\-vultr/pull/102](https\://github\.com/vultr/ansible\-collection\-vultr/pull/102)\)\.
* instance \- Fixed an issue detecting the instance state returned by the API \([https\://github\.com/vultr/ansible\-collection\-vultr/pull/89](https\://github\.com/vultr/ansible\-collection\-vultr/pull/89)\)\.
* instance\_info \- Fixed the alias <code>name</code> being was used on the wrong argument\. \([https\://github\.com/vultr/ansible\-collection\-vultr/issues/105](https\://github\.com/vultr/ansible\-collection\-vultr/issues/105)\)\.
* reserved\_ip \- Fixed an issue which caused the module to fail\, also enabled integration tests \([https\://github\.com/vultr/ansible\-collection\-vultr/issues/92](https\://github\.com/vultr/ansible\-collection\-vultr/issues/92)\)\.

<a id="known-issues"></a>
### Known Issues

<a id="dellemc-openmanage-4"></a>
#### dellemc\.openmanage

* idrac\_diagnostics \- Issue\(285322\) \- This module doesn\'t support export of diagnostics file to HTTP and HTTPS share via SOCKS proxy\.
* idrac\_firmware \- Issue\(279282\) \- This module does not support firmware update using HTTP\, HTTPS\, and FTP shares with authentication on iDRAC8\.
* idrac\_network\_attributes \- Issue\(279049\) \-  If unsupported values are provided for the parameter <code>ome\_network\_attributes</code>\, then this module does not provide a correct error message\.
* idrac\_storage\_volume \- Issue\(290766\) \- The module will report success instead of showing failure for new virtual creation on the BOSS\-N1 controller if a virtual disk is already present on the same controller\.
* ome\_device\_network\_services \- Issue\(212681\) \- The module does not provide a proper error message if unsupported values are provided for the following parameters\- port\_number\, community\_name\, max\_sessions\, max\_auth\_retries\, and idle\_timeout\.
* ome\_device\_power\_settings \- Issue\(212679\) \- The module displays the following message if the value provided for the parameter <code>power\_cap</code> is not within the supported range of 0 to 32767\, <code>Unable to complete the request because PowerCap does not exist or is not applicable for the resource URI\.</code>
* ome\_device\_quick\_deploy \- Issue\(275231\) \- This module does not deploy a new configuration to a slot that has disabled IPv6\.
* ome\_diagnostics \- Issue\(279193\) \- Export of SupportAssist collection logs to the share location fails on OME version 4\.0\.0\.
* ome\_smart\_fabric\_uplink \- Issue\(186024\) \- The module supported by OpenManage Enterprise Modular\, however it does not allow the creation of multiple uplinks of the same name\. If an uplink is created using the same name as an existing uplink\, then the existing uplink is modified\.

<a id="new-plugins"></a>
### New Plugins

<a id="callback"></a>
#### Callback

* community\.general\.default\_without\_diff \- The default ansible callback without diff output

<a id="connection"></a>
#### Connection

* community\.general\.incus \- Run tasks in Incus instances via the Incus CLI\.

<a id="filter"></a>
#### Filter

* ansible\.utils\.fact\_diff \- Find the difference between currently set facts
* community\.crypto\.parse\_serial \- Convert a serial number as a colon\-separated list of hex numbers to an integer
* community\.crypto\.to\_serial \- Convert an integer to a colon\-separated list of hex numbers
* community\.general\.from\_ini \- Converts INI text input into a dictionary
* community\.general\.lists\_difference \- Difference of lists with a predictive order
* community\.general\.lists\_intersect \- Intersection of lists with a predictive order
* community\.general\.lists\_symmetric\_difference \- Symmetric Difference of lists with a predictive order
* community\.general\.lists\_union \- Union of lists with a predictive order
* community\.general\.to\_ini \- Converts a dictionary to the INI file format
* microsoft\.ad\.dn\_escape \- Escape an LDAP DistinguishedName value string\.
* microsoft\.ad\.parse\_dn \- Parses an LDAP DistinguishedName string into an object\.

<a id="lookup"></a>
#### Lookup

* community\.general\.github\_app\_access\_token \- Obtain short\-lived Github App Access tokens
* community\.general\.onepassword\_doc \- Fetch documents stored in 1Password

<a id="test"></a>
#### Test

* community\.general\.fqdn\_valid \- Validates fully\-qualified domain names against RFC 1123

<a id="new-modules"></a>
### New Modules

<a id="check-point-mgmt-2"></a>
#### check\_point\.mgmt

* check\_point\.mgmt\.cp\_mgmt\_add\_central\_license \- Add central license\.
* check\_point\.mgmt\.cp\_mgmt\_central\_license\_facts \- Get central\-license objects facts on Checkpoint over Web Services API\.
* check\_point\.mgmt\.cp\_mgmt\_delete\_central\_license \- Delete central license\.
* check\_point\.mgmt\.cp\_mgmt\_distribute\_cloud\_licenses \- Distribute licenses to target CloudGuard gateways\.
* check\_point\.mgmt\.cp\_mgmt\_show\_cloud\_licenses\_usage \- Show attached licenses usage\.
* check\_point\.mgmt\.cp\_mgmt\_show\_ha\_status \- Retrieve domain high availability status\.

<a id="cisco-ios-4"></a>
#### cisco\.ios

* cisco\.ios\.ios\_evpn\_evi \- Resource module to configure L2VPN EVPN EVI\.
* cisco\.ios\.ios\_evpn\_global \- Resource module to configure L2VPN EVPN\.
* cisco\.ios\.ios\_vxlan\_vtep \- Resource module to configure VXLAN VTEP interface\.

<a id="community-aws-2"></a>
#### community\.aws

* community\.aws\.dynamodb\_table\_info \- Returns information about a Dynamo DB table

<a id="community-digitalocean-2"></a>
#### community\.digitalocean

* community\.digitalocean\.digital\_ocean\_project\_resource\_info \- Gather information about DigitalOcean Project Resources

<a id="community-docker-5"></a>
#### community\.docker

* community\.docker\.docker\_compose\_v2 \- Manage multi\-container Docker applications with Docker Compose CLI plugin
* community\.docker\.docker\_compose\_v2\_pull \- Pull a Docker compose project
* community\.docker\.docker\_image\_build \- Build Docker images using Docker buildx
* community\.docker\.docker\_image\_export \- Export \(archive\) Docker images
* community\.docker\.docker\_image\_pull \- Pull Docker images from registries
* community\.docker\.docker\_image\_push \- Push Docker images to registries
* community\.docker\.docker\_image\_remove \- Remove Docker images
* community\.docker\.docker\_image\_tag \- Tag Docker images with new names and/or tags

<a id="community-general-4"></a>
#### community\.general

* community\.general\.consul\_acl\_bootstrap \- Bootstrap ACLs in Consul
* community\.general\.consul\_auth\_method \- Manipulate Consul auth methods
* community\.general\.consul\_binding\_rule \- Manipulate Consul binding rules
* community\.general\.consul\_token \- Manipulate Consul tokens
* community\.general\.dnf\_config\_manager \- Enable or disable dnf repositories using config\-manager
* community\.general\.git\_config\_info \- Read git configuration
* community\.general\.gitlab\_group\_access\_token \- Manages GitLab group access tokens
* community\.general\.gitlab\_issue \- Create\, update\, or delete GitLab issues
* community\.general\.gitlab\_label \- Creates/updates/deletes GitLab Labels belonging to project or group\.
* community\.general\.gitlab\_milestone \- Creates/updates/deletes GitLab Milestones belonging to project or group
* community\.general\.gitlab\_project\_access\_token \- Manages GitLab project access tokens
* community\.general\.keycloak\_component\_info \- Retrive component info in Keycloak
* community\.general\.keycloak\_realm\_rolemapping \- Allows administration of Keycloak realm role mappings into groups with the Keycloak API
* community\.general\.nomad\_token \- Manage Nomad ACL tokens
* community\.general\.proxmox\_node\_info \- Retrieve information about one or more Proxmox VE nodes
* community\.general\.proxmox\_storage\_contents\_info \- List content from a Proxmox VE storage
* community\.general\.usb\_facts \- Allows listing information about USB devices

<a id="community-hashi-vault-2"></a>
#### community\.hashi\_vault

* community\.hashi\_vault\.vault\_database\_connection\_configure \- Configures the database engine
* community\.hashi\_vault\.vault\_database\_connection\_delete \- Delete a Database Connection
* community\.hashi\_vault\.vault\_database\_connection\_read \- Returns the configuration settings for a O\(connection\_name\)
* community\.hashi\_vault\.vault\_database\_connection\_reset \- Closes a O\(connection\_name\) and its underlying plugin and restarts it with the configuration stored
* community\.hashi\_vault\.vault\_database\_connections\_list \- Returns a list of available connections
* community\.hashi\_vault\.vault\_database\_role\_create \- Creates or updates a \(dynamic\) role definition
* community\.hashi\_vault\.vault\_database\_role\_delete \- Delete a role definition
* community\.hashi\_vault\.vault\_database\_role\_read \- Queries a dynamic role definition
* community\.hashi\_vault\.vault\_database\_roles\_list \- Returns a list of available \(dynamic\) roles
* community\.hashi\_vault\.vault\_database\_rotate\_root\_credentials \- Rotates the root credentials stored for the database connection\. This user must have permissions to update its own password\.
* community\.hashi\_vault\.vault\_database\_static\_role\_create \- Create or update a static role
* community\.hashi\_vault\.vault\_database\_static\_role\_get\_credentials \- Returns the current credentials based on the named static role
* community\.hashi\_vault\.vault\_database\_static\_role\_read \- Queries a static role definition
* community\.hashi\_vault\.vault\_database\_static\_role\_rotate\_credentials \- Trigger the credential rotation for a static role
* community\.hashi\_vault\.vault\_database\_static\_roles\_list \- Returns a list of available static roles

<a id="containers-podman-2"></a>
#### containers\.podman

* containers\.podman\.podman\_secret\_info \- Secrets info module

<a id="dellemc-enterprise-sonic-2"></a>
#### dellemc\.enterprise\_sonic

* dellemc\.enterprise\_sonic\.sonic\_dhcp\_snooping \- Manage DHCP Snooping on SONiC
* dellemc\.enterprise\_sonic\.sonic\_pki \- Manages PKI attributes of Enterprise Sonic
* dellemc\.enterprise\_sonic\.sonic\_stp \- Manage STP configuration on SONiC

<a id="dellemc-openmanage-5"></a>
#### dellemc\.openmanage

* dellemc\.openmanage\.idrac\_diagnostics \- This module allows to run and export diagnostics on iDRAC\.
* dellemc\.openmanage\.idrac\_license \- This module allows to import\, export\, and delete licenses on iDRAC\.
* dellemc\.openmanage\.idrac\_storage\_volume \- Configures the RAID configuration attributes\.

<a id="dellemc-powerflex-1"></a>
#### dellemc\.powerflex

* dellemc\.powerflex\.fault\_set \- Manage Fault Sets on Dell PowerFlex
* dellemc\.powerflex\.resource\_group \- Manage resource group deployments on Dell PowerFlex

<a id="fortinet-fortimanager-2"></a>
#### fortinet\.fortimanager

* fortinet\.fortimanager\.fmgr\_diameterfilter\_profile \- Configure Diameter filter profiles\.
* fortinet\.fortimanager\.fmgr\_firewall\_accessproxysshclientcert \- Configure Access Proxy SSH client certificate\.
* fortinet\.fortimanager\.fmgr\_firewall\_accessproxysshclientcert\_certextension \- Configure certificate extension for user certificate\.
* fortinet\.fortimanager\.fmgr\_firewall\_vip6\_quic \- QUIC setting\.
* fortinet\.fortimanager\.fmgr\_firewall\_vip\_gslbpublicips \- Publicly accessible IP addresses for the FortiGSLB service\.
* fortinet\.fortimanager\.fmgr\_sctpfilter\_profile \- Configure SCTP filter profiles\.
* fortinet\.fortimanager\.fmgr\_sctpfilter\_profile\_ppidfilters \- PPID filters list\.
* fortinet\.fortimanager\.fmgr\_switchcontroller\_managedswitch\_vlan \- Configure VLAN assignment priority\.
* fortinet\.fortimanager\.fmgr\_system\_admin\_profile\_writepasswdprofiles \- Profile list\.
* fortinet\.fortimanager\.fmgr\_system\_admin\_profile\_writepasswduserlist \- User list\.
* fortinet\.fortimanager\.fmgr\_system\_npu\_nputcam \- Configure NPU TCAM policies\.
* fortinet\.fortimanager\.fmgr\_system\_npu\_nputcam\_data \- Data fields of TCAM\.
* fortinet\.fortimanager\.fmgr\_system\_npu\_nputcam\_mask \- Mask fields of TCAM\.
* fortinet\.fortimanager\.fmgr\_system\_npu\_nputcam\_miract \- Mirror action of TCAM\.
* fortinet\.fortimanager\.fmgr\_system\_npu\_nputcam\_priact \- Priority action of TCAM\.
* fortinet\.fortimanager\.fmgr\_system\_npu\_nputcam\_sact \- Source action of TCAM\.
* fortinet\.fortimanager\.fmgr\_system\_npu\_nputcam\_tact \- Target action of TCAM\.
* fortinet\.fortimanager\.fmgr\_videofilter\_keyword \- Configure video filter keywords\.
* fortinet\.fortimanager\.fmgr\_videofilter\_keyword\_word \- List of keywords\.
* fortinet\.fortimanager\.fmgr\_videofilter\_profile\_filters \- YouTube filter entries\.
* fortinet\.fortimanager\.fmgr\_videofilter\_youtubekey \- Configure YouTube API keys\.

<a id="hetzner-hcloud-3"></a>
#### hetzner\.hcloud

* hetzner\.hcloud\.firewall\_resource \- Manage Resources a Hetzner Cloud Firewall is applied to\.

<a id="infoblox-nios-modules-2"></a>
#### infoblox\.nios\_modules

* infoblox\.nios\_modules\.nios\_dtc\_monitor\_http \- Configures the Infoblox NIOS DTC HTTP monitor\.
* infoblox\.nios\_modules\.nios\_dtc\_monitor\_icmp \- Configures the Infoblox NIOS DTC ICMP monitor
* infoblox\.nios\_modules\.nios\_dtc\_monitor\_pdp \- Configures the Infoblox NIOS DTC PDP monitor
* infoblox\.nios\_modules\.nios\_dtc\_monitor\_sip \- Configures the Infoblox NIOS DTC SIP monitor
* infoblox\.nios\_modules\.nios\_dtc\_monitor\_snmp \- Configures the Infoblox NIOS DTC SNMP monitor
* infoblox\.nios\_modules\.nios\_dtc\_monitor\_tcp \- Configures the Infoblox NIOS DTC TCP monitor
* infoblox\.nios\_modules\.nios\_dtc\_topology \- Configures the Infoblox NIOS DTC Topology

<a id="netapp-ontap-2"></a>
#### netapp\.ontap

* netapp\.ontap\.na\_ontap\_cifs\_unix\_symlink\_mapping \- NetApp ONTAP module to manage UNIX symbolic link mapping for CIFS clients\.
* netapp\.ontap\.na\_ontap\_cli\_timeout \- NetApp ONTAP module to set the CLI inactivity timeout value\.
* netapp\.ontap\.na\_ontap\_snmp\_config \- NetApp ONTAP module to modify SNMP configuration\.

<a id="netbox-netbox-2"></a>
#### netbox\.netbox

* netbox\.netbox\.netbox\_virtual\_disk \- Create\, updates\, or removes a disk from a Virtual Machine

<a id="purestorage-flasharray-2"></a>
#### purestorage\.flasharray

* purestorage\.flasharray\.purefa\_hardware \- Manage FlashArray Hardware Identification

<a id="purestorage-flashblade-2"></a>
#### purestorage\.flashblade

* purestorage\.flashblade\.purefb\_hardware \- Manage FlashBlade Hardware

<a id="theforeman-foreman-3"></a>
#### theforeman\.foreman

* theforeman\.foreman\.registration\_command \- Manage Registration Command
* theforeman\.foreman\.webhook \- Manage Webhooks

<a id="vultr-cloud-2"></a>
#### vultr\.cloud

* vultr\.cloud\.object\_storage \- Manages object storages on Vultr

<a id="new-roles"></a>
### New Roles

* dellemc\.openmanage\.idrac\_user \- Role to manage local users of iDRAC\.

<a id="unchanged-collections"></a>
### Unchanged Collections

* ansible\.posix \(still version 1\.5\.4\)
* chocolatey\.chocolatey \(still version 1\.5\.1\)
* cisco\.ucs \(still version 1\.10\.0\)
* cloudscale\_ch\.cloud \(still version 2\.3\.1\)
* community\.libvirt \(still version 1\.3\.0\)
* community\.network \(still version 5\.0\.2\)
* community\.proxysql \(still version 1\.5\.1\)
* community\.sops \(still version 1\.6\.7\)
* cyberark\.conjur \(still version 1\.2\.2\)
* frr\.frr \(still version 2\.0\.2\)
* ibm\.spectrum\_virtualize \(still version 2\.0\.0\)
* inspur\.sm \(still version 2\.3\.0\)
* netapp\.cloudmanager \(still version 21\.22\.1\)
* netapp\_eseries\.santricity \(still version 1\.4\.0\)
* ngine\_io\.cloudstack \(still version 2\.3\.0\)
* ngine\_io\.exoscale \(still version 1\.1\.0\)
* openvswitch\.openvswitch \(still version 2\.1\.1\)
* ovirt\.ovirt \(still version 3\.2\.0\)
* sensu\.sensu\_go \(still version 1\.14\.0\)
* t\_systems\_mms\.icinga\_director \(still version 2\.0\.1\)
* vyos\.vyos \(still version 4\.1\.0\)
* wti\.remote \(still version 1\.0\.5\)

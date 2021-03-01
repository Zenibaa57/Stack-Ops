![Imgur](https://i.imgur.com/30HoYoj.png)

# OpenStack

#### Module used in this project:


* [`Nova`](https://opendev.org/openstack/puppet-nova/) -  (Compute)
* [`Neutron`](https://opendev.org/openstack/puppet-neutron/) - (Networking)
* [`Keystone`](https://opendev.org/openstack/puppet-keystone/) - (Identity)
* [`Glance`](https://opendev.org/openstack/puppet-glance/) - (Image Service)
* [`Heat`](https://opendev.org/openstack/puppet-heat/) - (Orchestration)
* [`Horizon`](https://opendev.org/openstack/puppet-horizon/) - (Dashboard)

# Client tenant infrastructure

<div align="center"><img src="https://imgur.com/wpuuXzH.png" width="700" height="730"></div><br />

For additional information about instances network configuration:

|                           |       *ssh_jumphost*       |                    *internet_gw*                     |        *ntp_server*        |       *ldap_server*        |      *dns_server*       |
| :------------------------ | :------------------------: | :--------------------------------------------------: | :------------------------: | :------------------------: | :---------------------: |
| **Floating IP**           |            yes             |                         yes                          |            yes             |             no             |           no            |
| **Routes**                |            yes*            |                         yes*                         |            yes*            |             no             |           no            |
| **DNS servers**           | ip_dns_server<br />8.8.8.8 |              ip_dns_server<br />8.8.8.8              | ip_dns_server<br />8.8.8.8 | ip_dns_server<br />8.8.8.8 | 127.0.0.1<br />8.8.8.8  |
| **Security group**        |           sg_ssh           | sg_all_from_svc_network<br />sg_all_from_adm_network |           sg_ntp           |  sg_ssh_from_adm_network   | sg_ssh_from_adm_network |
| **Availability zone**     |            az2             |                         az2                          |            az2             |            az1             |           az1           |
| **Allowed address pairs** |             no             |                        yes**                         |             no             |             no             |           no            |

`(*) destination: 172.16.2.0/23 172.16.4.0/23, nexthop: 192.168.0.142`

`(**) ip_address: 0.0.0.0, mac_address: not_defined (by default - its own)`
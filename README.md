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

<div align="center"><img src="https://imgur.com/wpuuXzH.png" width="700" height="730"></div>



|                           | *ssh_jumphost* | *internet_gw* | *ntp_server* | *ldap_server* | *dns_server* |
| :------------------------ | -------------- | ------------- | ------------ | ------------- | ------------ |
| **Floating IP**           |                |               |              |               |              |
| **Routes**                |                |               |              |               |              |
| **DNS servers**           |                |               |              |               |              |
| **Security group**        |                |               |              |               |              |
| **Availability zone**     |                |               |              |               |              |
| **Allowed address pairs** |                |               |              |               |              |

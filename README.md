# cloud-init-public
cloud-init text and iso files for use with ubuntu cloud-init enabled images 

The ubuntu image has a `network-config` file which sets up `ens6` as a dhcp NIC which does not happen by default.

The CentOS image does not use `network-config` since its ehternet interface is created as `eth0` and the default cloud-init configures it as dhcp out of the box.

#### CLI
* Ubuntu `cloud-localds user-data-default-ubuntu.iso user-data-default-ubuntu.txt -N network-config`
* CentOS `cloud-localds user-data-default-centos.iso user-data-default-centos.txt`

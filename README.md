# Vagrant based Kubernetes Cluster

This is intended to be a homelab testbed for Kubernetes

This is not intended to be a production environment, and may be vulernable.

## Setup
- Install Vagrant and Virtualbox (*nix or OSX/MacOS based system)
- Clone and `cd` into this repo
- Configure Vagrantfile to meet your needs and to fit your network setup
- Run `vagrant up`, then get a coffee while the VMs are provisioned

## Cleanup
Run `vagrant destroy -f` to forcibly remove VMs and related resources

## Configuration
The VMs provisioned by this vagrant file are configured to run in **bridged** mode, so they will be assigned IP Addresses by your local DHCP server. It's recommended that you set a static IP in your network configuration to ensure each node is able to reliable communicate with the Master. Each node has a defined MAC address in the server configuration block. It is not required to set static IPs for nodes.

Each node can be configured independently by modifying the object defined in the servers array.

---

# Disclaimer

This has only been tested on a Ubuntu Xenial based system. There is no warranty or guarentee supplied with anything code or configuration in this repository.
# VMware and Chef

**Author**: JJ Asghar

 * Two different paradigms in Chef:
   1. Treat different providers as different clouds.
   2. Integrates directly into VRA.
 * Chef doesn't care _how_ the node is created: it just cares about bootstrapping it and managing it.
 * All of Chef's integrations are free.
 * Chef is working with VMware to implement a holistic approach to provisioning from PXE bootstrapping to converging w/ chef.
 
## VMware Photon
 * Based on PhotonOS.
   - Their containerization solution (Dockerish).
   - Runs on OVA.
   - Have a Kubinetes-like solution too.
 * Habitat integrates w/ Photon and works inside of Photon too.
 * Can use the kitchen docker driver to talk to Photon directly.

## Knife integration w/ VMware
 * chef-provisioning-vsphere integrates w/ vSphere.
   - Demo cookbook: `vsphere_testing`.
   - Illustrates how to integrate knife w/ vSphere.

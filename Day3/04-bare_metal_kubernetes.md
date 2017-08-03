# Bare Metal Kubernetes -- More Containers, Less Overhead
**Author:** Dustin Kirkland

## The Yin-Yang tension
 * There's a tension between keeping infra on-premises and in the cloud. It is important to be able to have both.

## Toolchain
 * [Conjure-up](https://github.com/conjure-up/conjure-up) can help spin up hybrid Kubernetes clusters.
   - It's a CUI (Command-line User Interface) that enables the selection of a deployment recipe and mechanism in a wizard fashion.
 * Kubernetes is demonstrating cloud native methodologies, has the potential to define the programming paradigm for the next 20 years.

## Kubernetes on Baremetal
 * `conjure-up`: Kubernetes cluster provisioning.
 * Juju: Software moddler
   - Manages interactions between software installation, dependencies.
   - Helps model complex software.
 * LXD: Machine container
   - Like a Process container (example: Docker), except you can have multiple processes running in a LXD container. Essentially a lightweight Linux machine.
   - LXD still shares the host's kernel, modules, etc.
 * MAAS (Metal As A Service): Baremetal provisioning.
   - Manages the provisioning of baremetal systems (aka. _NOT VMs_).
   - A collections of sysadmin toolchains.
   - Manages physical infrastructure.
   - Node:
     + Discovery: PXE  TFTP
     + HW inventory: lshw
     + BMC: freeipmi
     + BIOS & firmware: fwupd
     + Boot process: BIOS & UEFI
     + OS Deployment: curtain
   - Can deploy:
     + Ubuntu, RHEL, SUSE
     + Windows
     + Custom images
   - Includes a full-featured management UI.
   - Is intelligent enough to detect when a node under management is broken and stop assigning workloads to it.
   - Performs health checks (can add more at-will) against nodes.
     + Happens upon initial bootstrapping (called "commissioning").
     + Can also happen on-demand
   - Has lots of baremetal cluster management tooling, such as BIOS patching.
   - Supports the construction of new physical machines using pools of CPU, Disk, and RAM using Intel's Rack Scale technology.



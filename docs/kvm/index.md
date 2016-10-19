<h1>KVM Basics</h1>

This section contains basic requirements, knowledge and tools.


## Packages

* `qemu-kvm` - KVM
* `libvirt` - libvirtd service, manages hypervisors
* `libvirt-client` - virsh command
* `virt-install` - Creating VMs
* `virt-manager` - GUI administration tool
* `virt-top` - virtualization statistics
* `virt-viewer` - Connect to VMs

## Kernel Module

`lsmod | grep kvm`

if the module is missing:

`modprobe kvm_intel` or `modprobe kvm_amd`

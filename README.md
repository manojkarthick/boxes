# Boxes

Collection of Vagrant boxes I use regularly.

## Instructions

```
git clone https://github.com/manojkarthick/boxes
cd <box_path>
vagrant up
vagrant ssh
```

## Using the VMware provider

To install vagrant with the vmware plugin, follow these steps:

1. Download [VMware Fusion 12 Player][1] for macOS
2. Use license key from your myVMware account and install the application
3. Allow VMware Fusion to control system events within the app when prompted
4. Enable the accessibility preference at System Preferences > Security & Privacy > Accessibility > VMware Fusion
5. Install [vagrant][2]: `brew tap hashicorp/tap && brew install vagrant`
6. Find the box you want to install from Vagrant [Cloud][3] or my boxes on [Github][4]
7. Install the [vagrant-vmware-desktop plugin][5]: `vagrant plugin install vagrant-vmware-desktop`
8. Install the [VMware utility][6] for vagrant: `brew install --cask vagrant-vmware-utility`
9. Navigate to the folder containing the Vagrantfile and run `vagrant up`. The command might fail on the first run, so try running the same command again.
10. Run `vagrant ssh` to login to the vagrant box. Profit! 

Note: On macOS 11.x, using custom network settings does not work! Take a look at the [Known Issues][7] section for more info.

[1]: https://my.vmware.com/group/vmware/evalcenter?p=fusion-player-personal
[2]: https://www.vagrantup.com/downloads
[3]: https://app.vagrantup.com/boxes/search?provider=vmware
[4]: https://github.com/manojkarthick/boxes
[5]: https://www.vagrantup.com/vmware/downloads
[6]: https://www.vagrantup.com/docs/providers/vmware/vagrant-vmware-utility
[7]: https://www.vagrantup.com/docs/providers/vmware/known-issues 

## List of Boxes

| Box     | Version          | Image                             |  Provider   | Path                   | Notes                                                         |
|---------|------------------|-----------------------------------|-------------|------------------------|---------------------------------------------------------------|
| Ubuntu  | 18.04            | hashicorp/bionic64                | VMware      | ubuntu1804/Vagrantfile |                                                               |
| Ubuntu  | 20.04            | bento/ubuntu-20.04                | VMware      | ubuntu2004/Vagrantfile |                                                               |
| Ubuntu  | 20.10            | bento/ubuntu-20.10                | VMware      | ubuntu2010/Vagrantfile |                                                               |
| Arch    | Rolling release  | generic/arch                      | VMware      | archlinux/Vagrantfile  |                                                               |
| NixOS   | 20.09            | griff/nixos-stable-x86_64         | VMware      | nixos2009/Vagrantfile  |                                                               |
| KubeAdm | N/A              | bento/ubuntu-20.04                | Virtualbox  | kubeadm/Vagrantfile    | Master/Worker setup for Kubeadm cluster                       |

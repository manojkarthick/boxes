# Boxes

Collection of Vagrant boxes I use regularly.

## Instructions

```
git clone https://github.com/manojkarthick/boxes
cd <box_path>
vagrant up
vagrant ssh
```

## List of Boxes

| Box     | Version | Image                             | Path                     | Notes                                                         |
|---------|---------|-----------------------------------|--------------------------|---------------------------------------------------------------|
| Ubuntu  | 18.04   | geerlingguy/ubuntu1804            | ubuntu-18_04/Vagrantfile |                                                               |
| Ubuntu  | 20.04   | bento/ubuntu-20.04                | ubuntu-20_04/Vagrantfile |                                                               |
| Ubuntu  | 20.10   | bento/ubuntu-20.10                | ubuntu-20_10/Vagrantfile |                                                               |
| NixOS   | 20.09   | nixos-20.09-virtualbox-x86_64.box | nixos-20_09/Vagrantfile  | See https://github.com/nix-community/nixbox/ for instructions |
| KubeAdm | N/A     | bento/ubuntu-20.04                | kubeadm/Vagrantfile      | Master/Worker setup for Kubeadm cluster                       |

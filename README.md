# home_pxelinux

This repo contains :

- "Skeltion" with all files and binairies for netboot (SYSLINUX)
- a custom Menu for pxelinux
- Extracts of Ubuntu Xenial & Bionic minimal iso(s)
- Custom kickstart files (.ks)

### Prerequisites

* Git
* Apache2
* Tftp Server (TFTPBoot)
* Ubuntu local mirror (optional)

### Download & configure

1 - Clone directly in your TFTPBoot folder.

```
git clone git@github.com:picardflo/home_pxelinux.git
```
2 - Create folling folder in your TFTPBoot folder.
```
mkdir iso
```
3 - Download in iso/

- Download last version of clonezilla-live-*.iso (from official Website) - https://gparted.org/download.php
- Download last version of gparted-live-*.iso (from official Website)  - https://clonezilla.org/
- Download last version of netboot.xyz.iso (from official Website) - https://netboot.xyz/
- Download last version of super_grub2_disk_hybrid_*.iso (from official Website) - https://www.supergrubdisk.org/super-grub2-disk/
- Download last version of  ontpre.iso (Offline NT Password & Registry Editor)- http://www.octetmalin.net/windows/tutoriels/offline-nt-password-registry-editor.php

- Download last version of Acronis-*.iso (from official Website) - https://www.acronis.com/ (optional)

Correct the following files and adapt them to your environment :
- pxelinux.cfg/default (isoname and URs)
- /linux/ubuntu/xenial/ks/bionic_desktop_ks.cfg (URLs)
- /linux/ubuntu/xenial/ks/bionic_server_ks.cfg (URLs)
- /linux/ubuntu/xenial/ks/xenial_desktop_ks.cfg (URLs)
- /linux/ubuntu/xenial/ks/xenial_server_ks.cfg (URLs)


4 - Create symlinks (get *.ks files over http) in /var/www/html/

```
ln -s /var/www/html/ks <PATH_OF_YOUR_TFTPBoot_folder>
```

## Topics & How-To (FR)

- PXE - Netboot : https://wiki.dinfadom.com/index.php/PXE_-_Netboot
- Ubuntu Local mirror : https://wiki.dinfadom.com/index.php/Apt-mirror
- Kickstart Ubuntu :
  - https://wiki.dinfadom.com/index.php/Kickstart_-_Ubuntu_16.04_LTS
  - https://wiki.dinfadom.com/index.php/Kickstart_-_Ubuntu_18.04_LTS

## License

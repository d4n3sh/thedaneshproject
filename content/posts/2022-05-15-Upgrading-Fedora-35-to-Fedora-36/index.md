---
author: "Danesh Manoharan"
title: "Upgrading Fedora 35 to Fedora 36"
date: 2022-05-15T13:25:48-05:00
description: "Steps to upgrade Fedora 35 to Fedora 36." # Post description, shows up below title
cover:
    image: "2022-05-15-fedora36-upgrade.png" # image path/url
    alt: "Fedora 36 Upgrade Screen" # alt text
    caption: "Fedora 36 Upgrade Screen" # display caption under cover
    relative: true # when using page bundles set this to true
    hidden: false # only hide on current single page
images:
- 
tags:
- howto
- fedora
- linux
lastmod: 2022-05-15T13:25:48-05:00
draft: false
---

Successfully upgraded my Fedora 35 work station to Fedora 36 today.

```bash
❯ cat /etc/redhat-release
Fedora release 35 (Thirty Five)

❯ sudo dnf makecache

❯ sudo dnf upgrade --refresh

❯ sudo dnf install dnf-plugin-system-upgrade

❯ sudo dnf system-upgrade download --releasever=36

Before you continue ensure that your system is fully upgraded by running "dnf --refresh upgrade". Do you want to continue [y/N]:y

Transaction Summary
=============================================================================================================================================
Install     114 Packages
Upgrade    1859 Packages
Remove        4 Packages
Downgrade     1 Package

Total download size: 2.1 G
DNF will only download packages, install gpg keys, and check the transaction.
Is this ok [y/N]:y

Total                                                                                                        6.3 MB/s | 2.1 GB     05:34
Fedora 36 - x86_64 - Updates                                                                                 1.6 MB/s | 1.6 kB     00:00
Importing GPG key 0x38AB71F4:
 Userid     : "Fedora (36) <fedora-36-primary@fedoraproject.org>"
 Fingerprint: 53DE D2CB 922D 8B8D 9E63 FD18 999F 7CBF 38AB 71F4
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-fedora-36-x86_64
Is this ok [y/N]:y
Key imported successfully
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Complete!
Transaction saved to /var/lib/dnf/system-upgrade/system-upgrade-transaction.json.
Download complete! Use 'dnf system-upgrade reboot' to start the upgrade.
To remove cached metadata and transaction use 'dnf system-upgrade clean'
The downloaded packages were saved in cache until the next successful transaction.
You can remove cached packages by executing 'dnf clean packages'.

❯ sudo dnf system-upgrade reboot

❯ cat /etc/redhat-release
Fedora release 36 (Thirty Six)

❯ sudo dnf upgrade
Last metadata expiration check: 0:00:43 ago on Sun 15 May 2022 01:54:21 PM CDT.
Dependencies resolved.
Nothing to do.
Complete!
```

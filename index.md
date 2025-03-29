---
layout: default
---

Over the years I have developed a number of tools and scripts that have been useful to me. I have published them here in apt repositories, on github so that others can use them.

## Install the repository

To install the repository, you need to add the repository to your apt sources. This can be done by adding the following line to your `/etc/apt/sources.list.d/howtonebie.list` file:

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/HowToNebie.gpg] https://michaelschaecher.github.io/apt-repo stable main" |
sudo tee /etc/apt/sources.list.d/howtonebie.list
```

After adding the repository, you need to add the repository key to your keyring. This can be done by running the following command:

```bash
wget -qO - https://raw.githubusercontent.com/MichaelSchaecher/apt-repo/refs/heads/main/key/HowToNebie.gpg |
gpg --dearmor | sudo dd of=/usr/share/keyrings/HowToNebie.gpg
```

Once that is done update your package list and install the package simple-zram:

```bash
sudo apt update
sudo apt install -y simple-zram
```

## Available packages

The following packages are available in the repository:

- [simple-zram](https://github.com/MichaelSchaecher/simple-zram): Create a ZRAM device and use it as swap space.
- [ddns](https://github.com/MichaelSchaecher/ddns): A simple script used to update the IP address of a domain name on Cloudflare or DuckDNS.
- [btrfs-snapshots-manager](https://github.com/MichaelSchaecher/btrfs-snapshots-manager): A tool to manage btrfs snapshots.
- [grub-theme-minimal](https://github.com/MichaelSchaecher/grub-theme-minimal): A minimalistic yet stylish grub theme.
- [dpkg-changelog](https://github.com/MichaelSchaecher/dpkg-changelog): Generate a changelog for a debian package.

---
layout: default
---

[dist](https://github.com/MichaelSchaecher/repository.howtonebie.com/tree/main/dists)
[pool](https://github.com/MichaelSchaecher/repository.howtonebie.com/tree/main/pool)

The HowToNebie repository is a collection of packages designed to help users that have installed and setup their Debian/Ubuntu systems in a way that is not the most common. For example, it includes packages to assist maintaining **BTRFS Snapshots**, **DDNS** services with [DuckDNS](https://duckdns.org)/[cloudflare](https://cloudflare.com), and other useful tools that are not available in the default repositories.

It is designed to be used with Debian/Ubuntu and systems based on them, such as Linux Mint, Pop!_OS, and others. The repository is maintained by the [HowToNebie](https://HowToNebie.com) team and is open for contributions from the community.

## Install the repository

To install the repository, you need to add the repository to your apt sources. This can be done by adding the following line to your `/etc/apt/sources.list.d/howtonebie.list` file:

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/HowToNebie.gpg] https://repository.howtonebie.com/ stable main" |
sudo tee /etc/apt/sources.list.d/howtonebie.list
```

After adding the repository, you need to add the repository key to your keyring. This can be done by running the following command:

```bash
wget -qO - https://repository.howtonebie.com/key/HowToNebie.gpg |
gpg --dearmor | sudo dd of=/usr/share/keyrings/HowToNebie.gpg
```

Once that is done update your package list you can install packages from the repository using the following command:

```bash
sudo apt update
sudo apt install -y <package-name>
```

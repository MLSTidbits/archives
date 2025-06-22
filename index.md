---
layout: default
---

Over the years I have developed a number of tools and scripts that have been useful to me. I have published them here in apt repositories, on github so that others can use them.

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

Once that is done update your package list and install the package simple-zram:

```bash
sudo apt update
sudo apt install -y <package-name>

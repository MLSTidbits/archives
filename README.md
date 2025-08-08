<div align="right">
  <img
    src="images/logo.png"
    alt="Repository Logo"
    width="auto"
    height="360"
  />
</div>

## About

The MLSTidbits repository is a collection of packages designed to help users that have installed and setup their Debian/Ubuntu systems in a way that is not the most common. For example, it includes packages to assist maintaining **BTRFS Snapshots**, **DDNS** services with **DuckDNS**/**Cloudflare**, and more.

It is designed to be used with Debian/Ubuntu and systems based on them, such as Linux Mint, Pop!_OS, and others. The repository is maintained by the [MLSTidbits](https://MLSTidbits.com) team and is open for contributions from the community.

## Install the repository

To install the repository, you need to add the repository to your apt sources. This can be done by adding the following line to your `/etc/apt/sources.list.d/MLSTidbits.list` file:

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/MLSTidbits.gpg] https://archive.MLSTidbits.com/ stable main" |
sudo tee /etc/apt/sources.list.d/MLSTidbits.list
```

After adding the repository, you need to add the repository key to your keyring. This can be done by running the following command:

```bash
wget -qO - https://archive.MLSTidbits.com/key/MLSTidbits.gpg |
gpg --dearmor | sudo dd of=/usr/share/keyrings/MLSTidbits.gpg
```

Once that is done update your package list you can install packages from the repository using the following command:

```bash
sudo apt update
sudo apt install -y <package-name>
```

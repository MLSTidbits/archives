<div align="center">
    <span><img src="images/logo.svg" alt="MLSTidbits Logo" width="200"/>
    <h1>MLSTidbits Repository</h1>
    </span>
</div>

## About

The MLSTidbits repository is a collection of packages designed to help users that have installed and setup their Debian/Ubuntu systems in a way that is not the most common. For example, it includes packages to assist maintaining **BTRFS Snapshots**, **DDNS** services with **DuckDNS**/**Cloudflare**, and more.

It is designed to be used with Debian/Ubuntu and systems based on them, such as Linux Mint, Pop!_OS, and others. The repository is maintained by the [MLSTidbits](https://MLSTidbits.com) team which is just [me](https://github.com/MichaelSchaecher) at the moment.

## Install the repository

To install the repository, you need to add the repository to your apt sources. This can be done by adding the following line to your `/etc/apt/sources.list.d/MLSTidbits.list` file:

```bash
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/MLSTidbits.gpg] https://archive.mlstidbits.com/ stable main" |
sudo tee /etc/apt/sources.list.d/MLSTidbits.list
```

After adding the repository, you need to add the repository key to your keyring. This can be done by running the following command:

```bash
wget -qO - https://archive.mlstidbits.com/key/MLSTidbits.gpg |
gpg --dearmor | sudo dd of=/usr/share/keyrings/MLSTidbits.gpg
```

Once that is done update your package list you can install packages from the repository using the following command:

```bash
sudo apt update
sudo apt install -y <package-name>
```

## Contributing

If you want to contribute to the [MLSTidbits](https://mlstidbits.com) repository, or any of the applications, you can do so by submitting an [email](mailto:contact@mlstidbits.com). Include a brief description of yourself and a link to your GitHub profile. If you have a specific package in mind, please include that as well.

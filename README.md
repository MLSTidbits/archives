<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MLSTidbits Repository</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      line-height: 1.6;
      margin: 20px;
    }
    h1, h2, h3 {
      color: #d8d6d1ff;
    }
    h1 {
      font-size: 3em;
      margin-bottom: 10px;
      text-align: center;
      color: #eed89dff;
    }
    h2 {
      font-size: 2em;
      margin-top: 20px;
      color: #eed89dff;
    }
    code {
      padding: 2px 4px;
      border-radius: 4px;
    }
    pre {
      padding: 10px;
      overflow-x: auto;
    }
    img {
      width: 240px;
      height: auto;
      display: block;
      margin: 0 auto 20px;
    }
  </style>
</head>

# ![Logo](images/logo.svg) MLSTidbits Repository

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

```md
# Script for easy installation and configuration of X-ray core without a graphical interface

You are all familiar with control panels like 3x-ui, Marzban, and others. All these panels are just graphical interfaces over the X-ray core and serve for convenient management, as well as for creating connections and settings. The core itself can work without any panels and be fully managed via the terminal. The main advantage of using a "bare" core is that you don't need to bother with domains and TLS certificates. The core itself can be installed and administered manually using the official documentation. This script is designed to simplify this task: it will automatically install the core on the server, create configuration files, and several executable files for convenient user management.

## VPS for the panel

To install the panel, we will need a VPS server.
The service offers more than 36 locations. If you don't need a specific country, choose the one closest to you.

## System Requirements

- 1 CPU
- 1 GB RAM
- 10 GB Disk
- OS Ubuntu 22 x64 or Ubuntu 24 x64

## How to use the script
The script was created and tested under OS Ubuntu 22 x64 and Ubuntu 24 x64. It may not work correctly on other OS. To download and run the script, use this command:

```sh
wget -qO- https://raw.githubusercontent.com/kcelsi/simple-xray-core/refs/heads/main/xray-install | bash
```

## Commands for user management

**List all clients:**

```sh
userlist
```

**Display the link and QR code for connecting the main user:**

```sh
mainuser
```

**Create a new user:**

```sh
newuser
```

**Delete a user:**

```sh
rmuser
```

**Create a connection link:**

```sh
sharelink
```

A `help` file will be created in the user's home folder — it contains tips with command descriptions. You can view it using the command (you need to be in the user's home folder):

```sh
cat help
```

## Useful links

- [X-ray Core GitHub project](https://github.com/XTLS/Xray-core)
- [Official documentation in Russian](https://xtls.github.io/ru/)

## Clients for connection

**Windows**

- [v2rayN](https://github.com/2dust/v2rayN)
- [Furious](https://github.com/LorenEteval/Furious)
- [Invisible Man - Xray](https://github.com/InvisibleManVPN/InvisibleMan-XRayClient)

**Android**

- [v2rayNG](https://github.com/2dust/v2rayNG)
- [X-flutter](https://github.com/XTLS/X-flutter)
- [SaeedDev94/Xray](https://github.com/SaeedDev94/Xray)

**iOS & macOS arm64**

- [Shadowrocker](https://apps.apple.com/us/app/shadowrocket/id932747118) **Recommended** 💰 Paid
- [Streisand](https://apps.apple.com/app/streisand/id6450534064)
- [Happ](https://apps.apple.com/app/happ-proxy-utility/id6504287215)
- [OneXray](https://github.com/OneXray/OneXray)

**macOS arm64 & x64**

- [V2rayU](https://github.com/yanue/V2rayU)
- [V2RayXS](https://github.com/tzmax/V2RayXS)
- [Furious](https://github.com/LorenEteval/Furious)
- [OneXray](https://github.com/OneXray/OneXray)

**Linux**

- [Nekoray](https://github.com/MatsuriDayo/nekoray)
- [v2rayA](https://github.com/v2rayA/v2rayA)
- [Furious](https://github.com/LorenEteval/Furious)

## If you suddenly need to uninstall, use these commands:
```sh
bash -c "$(curl -L https://github.com/XTLS/Xray-install/raw/main/install-release.sh)" @ remove
rm /usr/local/etc/xray/config.json
rm /usr/local/etc/xray/.keys
rm /usr/local/bin/userlist
rm /usr/local/bin/mainuser
rm /usr/local/bin/newuser
rm /usr/local/bin/rmuser
rm /usr/local/bin/sharelink
```
